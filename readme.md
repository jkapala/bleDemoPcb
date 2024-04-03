# Overview
The following PCB project has a few goals. Namely, it is a training board to expose the designer to working with various features. In this way, it serves as a development board first and foremost. The hardware and or firmware features that should be explored with the board are listed below.

## BLE and Inverted-F Antenna

## WiFi

## DMA

## Large Non-Volatile Memory

## Memory Encryption
Purely software implementations will be costly in terms of performance. Any algorithm used cannot require additional storage space. A plain-text media block should be encrypted in place, generating a ciphertext block of the same size.
NIST and FIPS-approved standards are desired.

## DMA

## STM32 Architecture and related toolchains
### STM32WB / STM32WBA / STM32WB0
The STM32WB line supports multiple wireless protocols. It does not support WiFi though. The B0 line is the simpler line of the three, the BA lime is the most robust.

The chips run for about $6 to $9 on Digikey. There are a few around $4-5 on Mouser. 

STM32WB30CEU5A is a decent option to start with.

## JTAG

## RTOS

## DC-DC Converter Design

## USB-C Power

## USB

## Multiple power sources

## Real-Time Clock

## LCD capable

## EMC Compliance and Testing-ready

## Programming interfaces
The STM32 devices typically have a few options that can be used to program the device. Primarily, these are the SWD and JTAG interfaces.

The Stlink V3 can be used to program devices.

## HAL