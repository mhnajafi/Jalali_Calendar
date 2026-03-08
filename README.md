# Jalali Calendar

This project implements a digital Persian (Jalali) calendar on an AVR microcontroller (ATmega16). It displays the date, time, and temperature on a 128x64 graphical LCD and allows user interaction to set the time and date.

## Features

- **Persian Calendar**: Accurately calculates and displays the Jalali date.
- **Real-Time Clock**: Uses a DS1307 RTC module for precise timekeeping.
- **Temperature Display**: Reads ambient temperature using an LM35 sensor.
- **Graphical Interface**: Displays information on a KS0108-based 128x64 GLCD.
- **User Settings**: Includes buttons to adjust the year, month, day, hour, and minute.

## Hardware Configuration

- **Microcontroller**: ATmega16
- **Display**: 128x64 Graphic LCD (KS0108 controller) connected to Port B.
- **RTC**: DS1307 connected via I2C (Software I2C implementation).
- **Sensor**: LM35 Temperature Sensor on ADC Channel 0.
- **Controls**:
    - **Menu/Set**: PIN D0
    - **Up**: PIN D1
    - **Down**: PIN D2

## Software Details

- **Language**: C
- **Compiler/IDE**: CodeVisionAVR (implied by file structure/headers) or Atmel Studio.
- **Libraries**:
    - `glcd.h`: For driving the graphical LCD.
    - `ds1307.h`: For communicating with the RTC.
    - `adad.h`: Likely contains bitmap font definitions for Persian/Arabic numbers.

## Usage

1. **Hardware Setup**: Assemble the circuit as per the pin definitions in the code (GLCD on Port B, Buttons on Port D, LM35 on PA0).
2. **Compile**: Open the project file and compile the source code (`c.c`) using an AVR-compatible C compiler.
3. **Flash**: Program the ATmega16 with the generated hex file.
4. **Operation**:
   - The default screen shows the current time, date, and temperature.
   - Press the **Menu** button to enter setting mode.
   - Use **Up/Down** to adjust values and **Menu** to confirm/move to the next field.
