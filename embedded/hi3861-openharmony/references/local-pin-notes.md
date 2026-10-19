# Local Hi3861 pin notes

These mappings came from the author's earlier draft. The exact development board, hardware revision, and schematic were not included. Treat this table only as a comparison checklist after the user identifies their board and supplies its schematic or pinout. Do not apply it automatically.

| Function | Draft GPIO | Note |
| --- | --- | --- |
| UART0 TX / RX | GPIO_06 / GPIO_05 | Debug UART in the draft |
| I2C0 SDA / SCL | GPIO_00 / GPIO_01 | Check alternate-function configuration |
| SPI0 CK / DI / DO | GPIO_02 / GPIO_03 / GPIO_04 | Check board routing |
| PWM0 / PWM1 | GPIO_07 / GPIO_08 | Check channel and package |
| ADC0 | GPIO_00 | Conflicts with the draft I2C0 SDA assignment |
| General GPIO | GPIO_09 through GPIO_14 | Confirm availability on the board |

The I2C/ADC overlap is a real design conflict if both are needed simultaneously. Resolve it against the target documentation before generating code.
