This is firmware for STM32F103C8T6 microcontrollers implementing the Altera USB blaster protocol.
It has been used with OpenOCD using stock USB Blaster configuration files.

= PINOUT =

A7	TDI
A6	TDO
A5	TCK
A4	TMS
A3	NCE (pin6 in OpenOCD)
A2	NCS (pin8 in OpenOCD)
A1	LED

= SPEED =

Standard TCK frequency is:

-- 9 MHz for bit-shifted transfers
-- 1.125 MHz for byte transfers

By pulling A0 to 3.3V, the TCK bit-shift data rate is reduced to 1.125 MHz.
This may be useful for slow targets or when signal integrity is an issue.
