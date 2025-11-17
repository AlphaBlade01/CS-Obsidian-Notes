### 68008 Assembler instructions
Can be of the form:
> operation.datatype    source,    destination

- operation can be done in one of 3 data types:
	- **byte:** .b (8 bits)
	- **word:** .w (2 bytes)
	- **long word:** .l (4 bytes)
#### Movement instructions
- **move:** move between registers
- **exg:** exchange
- **swap:** swap lower and upper words
- **lea:** load effective address
	- lea $F20, A3 
#### Arithmetic instructions
- **add:** add two register contents
- **addx:** also add in x bit from CCR
- **sub:** subtract second register contents from first
- **subx:** also subtract x bit from CCR
- **mulu:** unsigned multiplication
- **muls:** signed multiplication
- **divu:** unsigned division
- **divs:** signed division
#### Logical instructions
- AND
- OR
- EOR
- NOT
#### Branch instructions
	Cause processor to branch to labelled address
- **BRA:** Branch always
- **BCC:** Branch on carry clear
- **BCS:** Branch on carry set
- **BEQ:** Branch on equal
- **BGE:** Branch if greater than or equal
- ...
- **BPL:** Branch on position
- **BVC:** Branch on overflow clear
- **BVS:** Branch on overflow set

### Subroutines
Uses a stack to save execution state
- **JSR \<label>:** Jump to subroutine
- **RTS:** Return from subroutine
### Addressing Modes
	Tells computer where to find data it needs
- **Data or Address Register Direct:** Address of operand specified by Data/Address register
- **Immediate Addressing:** Operand is a constant value used for the instruction
- **Absolute Addressing:** Operand specifies memory location of value
- **Address Register Indirect:**
	- Default `move (A0), D3` : content of memory A0 goes to register D3
	- Offset `move 7F(A1), D3` : adds 7F to content of memory A1 and moves to register D3
	- Post-Incrementing `move (A0)+, D3` : increments memory address after operation done

