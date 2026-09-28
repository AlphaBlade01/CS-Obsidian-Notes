## Registers
#### Data registers:
- D0 - D7: Holds intermediate data values between calculations
#### Address registers:
- A0 - A6: Holds pointers in the calculation of operand addresses
- A7: Stack pointer to hold subroutine return addresses, etc.
	- Points to the next free location
#### Status register:
- 16 bit
- Contains various status bits which are set or reset upon certain conditions arising in ALU
#### Program counter:
- 32 bit (on 32-bit system)
- Points to the next instruction in memory

## Improving performance
### More cache
- Adding cache decouples processor from slower RAM
- cache hit rates are reaching their limits and SRAM is power hungry
### More complicated execution
