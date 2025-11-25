## RAM
#### Memory organisation
Data going into cell:
	**Select -** Enable a particular memory cell
	**R/W -** Indicate read or write
	**Data -** Input when writing or output when reading
### SRAM
	Stores data using configurations of flip flops & logic gates
- Requires constant power to maintain data
### DRAM
	Stores data as charge on capacitors
- Requires periodic charge to maintain data
- Cheaper than SRAM

## Cache
Average memory access time = Hit time + (Miss rate $\times$ Miss penalty)

#### Caches on Disks
- **READ:** Reads whole track "as you're already there", then loads in memory
- **WRITE:** write to RAM then write to disk in nice order
