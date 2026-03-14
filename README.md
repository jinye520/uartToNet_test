# uartToNet_test

STM32F427VITx firmware project generated from STM32CubeMX with CMake support.

## Overview

- MCU: `STM32F427VITx`
- Build system: `CMake` + `Ninja`
- HAL: `STM32Cube FW_F4 V1.28.3`
- LED: `PB4`
- UART log: `USART2` on `PA2` (TX) / `PA3` (RX), `115200 8N1`

## Current Behavior

- Toggles the LED every 500 ms
- Sends `hello word` over `USART2` every 500 ms

## Project Structure

- `Core/`: application source and headers
- `Drivers/`: CMSIS and STM32 HAL drivers
- `cmake/`: STM32CubeMX generated CMake integration
- `uartToNet_test.ioc`: STM32CubeMX project configuration

## Build

This project is intended to be built with the STM32Cube toolchain bundle used by the VS Code STM32 extension.

Typical workflow in VS Code:

1. Open the folder in VS Code
2. Configure CMake for the `Debug` preset
3. Build the project

## Serial Output

Connect a USB-to-UART adapter to:

- `PA2` -> adapter RX
- `PA3` -> adapter TX
- `GND` -> adapter GND

Then open a serial terminal at `115200` baud to view the log output.
