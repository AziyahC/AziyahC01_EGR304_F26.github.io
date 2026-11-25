# Microcontroller Code — Acoustic Subsystem Verification

## Overview
This page contains the verification firmware developed for the **PIC18F57Q43 Curiosity Nano** on the noise sensing subsystem board. The firmware samples the conditioned analog output of the **MCP6004** microphone stage via ADC channel **ANB2 (RB2)**, detects acoustic noise events, drives the local debug LED (**D1 on RA0**), and transmits formatted serial packets (**`T,00`**, **`T,10`**, **`T,11`**) over UART1 to Christopher Plumley's main board across the inter-board ribbon cable (`J2`).

---

## Packaged Project Download
**[Download Complete MPLAB X Verification Firmware (.zip)](Microphone_Subsystem.zip)**

---

## Source Code (`main.c`)


#include <xc.h>
#include "mcc_generated_files/system/system.h"
#include <stdio.h>
#include <stdlib.h>
#include <stdint.h>
#include <stdbool.h>

#define QUIET_BASELINE          2048    // 2.50V DC midpoint on 12-bit ADC
#define THRESHOLD_MODERATE      150     // Threshold for talking / ambient noise
#define THRESHOLD_LOUD          500     // Threshold for clapping / loud whistling
#define TRANSMIT_INTERVAL_MS    500     // Required inter-board packet interval
#define SAMPLE_INTERVAL_MS      25      // 40 Hz ADC sampling cadence

#define MIC_ADC_CHANNEL         0x0A    // RB2 / ANB2

// Direct Register Hardware Macros
#define LED_D1_ON()             (LATA |= (1 << 0))
#define LED_D1_OFF()            (LATA &= ~(1 << 0))
#define SW1_IS_PRESSED()        ((PORTA & (1 << 4)) == 0)   // RA4
#define SW2_IS_PRESSED()        ((PORTA & (1 << 3)) == 0)   // RA3

int main(void)
{
    SYSTEM_Initialize();

    // Configure RA0 (Debug LED D1) as Digital Output
    TRISA &= ~(1 << 0);
    ANSELA &= ~(1 << 0);
    LED_D1_OFF();

    // Configure RA3 (SW2) and RA4 (SW1) as Digital Inputs
    TRISA |= (1 << 3) | (1 << 4);
    ANSELA &= ~((1 << 3) | (1 << 4));

    // Configure RB2 (Audio Input from Header U5) as Analog Input
    TRISB |= (1 << 2);
    ANSELB |= (1 << 2);

    uint16_t adc_val = 0;
    int16_t deviation = 0;
    int16_t peak_deviation = 0;
    uint16_t elapsed_time_ms = 0;

    while (1)
    {
        // 1. Sample ADC Channel ANB2
        ADPCH = MIC_ADC_CHANNEL;
        ADC_ConversionStart();
        while(!ADC_IsConversionDone());
        adc_val = (uint16_t)ADC_ConversionResultGet();

        // Calculate deviation from 2.5V baseline
        deviation = abs((int16_t)adc_val - QUIET_BASELINE);
        if (deviation > peak_deviation)
        {
            peak_deviation = deviation;
        }

        // 2. Drive Local Debug LED D1
        if (peak_deviation > THRESHOLD_MODERATE || SW1_IS_PRESSED() || SW2_IS_PRESSED())
        {
            LED_D1_ON();
        }
        else
        {
            LED_D1_OFF();
        }

        // 3. Periodic 500 ms Packet Transmission to Main Board
        elapsed_time_ms += SAMPLE_INTERVAL_MS;
        if (elapsed_time_ms >= TRANSMIT_INTERVAL_MS)
        {
            elapsed_time_ms = 0;

            if (SW2_IS_PRESSED())
            {
                printf("T,11\r\n"); // Force Loud Sound
            }
            else if (SW1_IS_PRESSED())
            {
                printf("T,10\r\n"); // Force Moderate Sound
            }
            else if (peak_deviation >= THRESHOLD_LOUD)
            {
                printf("T,11\r\n"); // Detected Loud Sound
            }
            else if (peak_deviation >= THRESHOLD_MODERATE)
            {
                printf("T,10\r\n"); // Detected Moderate Sound
            }
            else
            {
                printf("T,00\r\n"); // Quiet
            }

            peak_deviation = 0;
        }

        __delay_ms(25);
    }
    return 0;
}

