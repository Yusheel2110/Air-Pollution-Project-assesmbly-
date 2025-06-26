Please refer to Assembly.txt for the code used in this project.
Please refer to the report for an in-depth reporting of the project.
This readme is a very simple breakdown of the project.

✅ Microcontroller Used
PIC16F690

8-bit microcontroller with built-in ADC (Analog-to-Digital Converter)

Used to read sensor values, drive the LCD, and control the buzzer

Operates at an internal oscillator frequency of 500 kHz (set in code)

📦 Required Hardware Components
PIC16F690 Microcontroller

MQ-135 Air Quality Sensor

Detects gases like CO₂, ammonia, benzene, and VOCs

16x2 LCD Display

Buzzer

Passive Components (resistors, capacitors)

Power Supply: 5V regulated

💻 Software Required
MPLAB X IDE

For writing and compiling Assembly code

MPASM Assembler (comes with MPLAB X)

Used to assemble the .asm file into a HEX file for the PIC16F690

Proteus (Optional but recommended)

For simulating the circuit (a Proteus schematic is shown in the report)

PIC Programmer (e.g., PICkit 3 or 4)

For flashing the compiled HEX code onto the PIC16F690

⚙️ Core Functionalities
Continuously reads air quality via ADC from MQ-135

Converts analog voltage to PPM (parts per million)

Displays value on LCD

If PPM > 250:

LCD shows “Polluted Air”

Buzzer sounds

If PPM ≤ 250:

LCD shows “Fresh Air”

Buzzer remains silent

🧠 Subroutines Overview
InitializeLCD: Prepares the LCD for output

ADC: Reads analog input from the sensor

ConvertADCtoPPM: Converts ADC value to PPM (via formula)

LCDWriteMain, LCDWriteGood, LCDWriteBad: Different display outputs

BuzzerOn / BuzzerOff: Controls the buzzer

🔁 Execution Flow
Initialization

Main Loop

ADC → PPM → Compare with Threshold

Update LCD

Sound buzzer if necessary
