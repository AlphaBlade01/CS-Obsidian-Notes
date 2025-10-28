### Floating point
Represents numbers like scientific notation $m \times 2^e$  
- m represents the **mantissa**
- e represents the **exponent**

Order: ``Sign Bit`` | ``Exponent`` | ``Mantissa``
- Exponent stored after sign bit to make comparing numbers easier

**Offset/Bias:** Used to offset the binary representations so all negative numbers come before positive numbers. Calculated automatically based on the exponent.

**Special Bias**
	- Zero represented through all 0s
	- $+\infty$ represented using all 1s in exponent
	- $- \infty$ represented using all 1s in exponent in exponent and sign bit
	- NaN represented using all 1s in exponent and anything other than 0 for mantissa

