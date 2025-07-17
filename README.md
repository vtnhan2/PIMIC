
# PIMIC (High-Performance Audio Processing System)

This repository contains firmware for an STM32-based high-fidelity audio system utilizing I2S (Inter-IC Sound) and various audio processing components. It includes code to configure the I2S interface, manage audio data flow, and perform real-time audio recording and playback.

## Features

* **I2S Audio Transmission & Reception**: Configures I2S for real-time audio data processing with support for both transmit and receive modes.
* **Audio Mode Control**: Includes audio modes such as Live Mode and ENC (Environmental Noise Cancellation).
* **Multi-Channel Support**: Supports multi-channel audio transmission and reception, with the option for stereo or mono audio modes.
* **Touchscreen Interface**: Utilizes a touchscreen interface for controlling audio playback, volume, and settings.
* **Volume Control**: Adjust audio output levels with a configurable gain setting.
* **Real-time Audio Processing**: Processes live audio streams in real-time, with capabilities to mute, unmute, and adjust the audio volume.

## Hardware Requirements

* **Microcontroller**: STM32F4 series (Cortex-M4)
* **External Audio Codec**: Supports external audio components like the NC100 chip for high-quality audio capture and playback.
* **Touchscreen**: Uses a resistive touchscreen for user interaction (set up via the `TouchScreen_kbv` library).
* **External SRAM/SDRAM**: Option to configure external memory for data storage.

## File Structure

* **main.c**: The main entry point, which configures peripherals and handles audio data flow.
* **HiFi.h/cpp**: High-fidelity audio driver, including configurations for I2S transmission and reception, and interrupt handling.
* **TouchScreen\_kbv.h/cpp**: Touchscreen interface code with oversampling and debouncing for stable touch inputs.
* **Soloma.h**: Header file for configuring and interacting with the NC100 audio processing chip.
* **ssc.h/c**: Synchronous Serial Controller (SSC) driver for audio data transmission.

## Setup & Installation

1. **Clone the Repository**:

   ```bash
   git clone https://github.com/yourusername/PIMIC.git
   ```

2. **Dependencies**:

   * STM32 HAL library
   * FreeRTOS (if applicable)
   * I2C and I2S peripheral drivers configured for STM32

3. **Hardware Setup**:

   * Connect the touchscreen and audio codec (e.g., NC100) as specified in the hardware configuration section.
   * Ensure that the I2S bus is properly wired for audio data transmission.

4. **Building the Firmware**:

   * Use STM32CubeIDE or another compatible toolchain to build the project.
   * Upload the firmware to your STM32 device via ST-Link or another programming/debugging interface.

## How to Use

* **Touchscreen**: Interact with the touchscreen to control playback, stop, or record audio.
* **Volume Control**: Use the touchscreen to adjust the gain and manage the audio output level.
* **Audio Modes**: Switch between live audio and other processing modes as per the requirements.


