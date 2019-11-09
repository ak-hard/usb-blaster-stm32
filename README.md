This is firmware for STM32F103C8T6 microcontrollers implementing the Altera USB blaster protocol.
It has been used with OpenOCD using stock USB Blaster configuration files.
Pay attention to JTAG voltage levels, e.g. a 3.3V STM32 board can only be used with 3.3V targets.

## PINOUT

	A7	TDI
	A6	TDO
	A5	TCK
	A4	TMS
	A3	nCE (pin6 in OpenOCD)
	A2	nCS (pin8 in OpenOCD)
	A1	LED

## SPEED

Standard TCK frequency is:

- 9 MHz for bit-shifted transfers
- 1.125 MHz for byte (bit-bang) transfers

The actual speed depends on USB speed (about 1 MB/s), USB turnaround times, software overhead, and other factors.

By pulling A0 to 3.3V, the TCK bit-shift data rate is reduced to 1.125 MHz.
This may be useful for slow targets or when signal integrity is an issue.

Use at your own risk, no warranties of any kind.
