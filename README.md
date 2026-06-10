# I2C-Driver
This repository contains an I2C driver developed for the STM32 Nucleo-F411RE board and an I2C LCD interface. The LCD module is based on the PCF8574 I/O expander chip, which enables communication with the LCD through the I2C protocol using only two data lines (SDA and SCL).

Each byte is sent in two steps
1. High nibble (D7–D4)
2. Low nibble (D3–D0)

For each nibble, the Enable (EN) pin is toggled to latch the data.

Connected pins:
- SDA → PB9  
- SCL → PB8  

 Notes

- LCD operates in 4-bit mode
- PCF8574 is used as an I/O expander
- Backlight (BL) control is included in the data frame
