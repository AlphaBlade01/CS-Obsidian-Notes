## Adders
#### Half Adders
- Consists of 1 XOR and 1 AND logic gate
#### Full Adders
- Consists of 2 half adders 
- OR applied to carry bits of both half adders to get total carry bit
#### Subtractors
- A control input $Z$ is introduced 
	- $Z=0 \implies S = A+B$
	- $Z=1 \implies S = A-B$
- Arithmetic is carried out in two's complement

## Control signals
#### Active High
- 0 = inactive
- 1 = active
#### Active Low
- 0 = active
- 1 = inactive

## Multiplexer
- Chooses which of the inputs are presented as outputs
- $Z=\bar{A}.I_{0} + A.I_{1}$  for two inputs
#### Demultiplexers
- Threads the input to one of outputs depending on control

## Encoders/Decoders
**Encoder:** Produces binary input code depending on which of the inputs are activated
**Decoder:** Circuit which maps an N-bit code to $2^N$ one-hot outputs

- An encoder has $2^N$ inputs and $N$ outputs

## Logic Circuits
### Combinatorial Logic Circuits
	output determined solely by inputs
### Sequential Logic Circuits
	output determined by inputs & previous outputs
#### Latches
- Contains a set and reset input