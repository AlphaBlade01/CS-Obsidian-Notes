**Noise:** unwanted information coming from various sources
## Parity
**Parity bit:** bit appended on which "summarises" a property of the message

**Even parity system:** Value of extra bit is chosen to make total number of logic 1s an even number
**Odd parity system:** The number of logic 1s is made odd

- Hardware implementations generally perform better than software

## Burst Errors
	Multiple errors occuring in bursts
- Checksums improve error detection capabilities
- Can extend to **Error Correcting Code** by calculating character & bit-column parity

## RAID
	Redundant Arrays of Inexpensive Disk
Disks are slow & unreliable.

**Raid 0:** Striping: Put successive blocks on successive disks, so that your reads and writes are spread evenly over the whole set.
	Faster, but just as reliable
**Raid 1:** Mirroring: Put entire data set on each disk, so each read can come from either and you can survive loss of n-1 disks.
	Faster, more reliable
**Raid 0+1 (10):** A striped volume, mirrored, or a set of mirrors, striped.
	Faster, more reliable, won't survive as many failures

