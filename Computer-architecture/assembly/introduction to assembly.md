# Introduction to assembly

## Program format
- .DATA is a section where variables are defined
- .BSS is a section where space is reserved for not defined variables
- .TEXT is a section where actual code is written

### GPRs

We have r (64 bit), e (32 bits), and 16 bits registers:
- ax - accumulator
- bx - base
- cx - counter
- dx - data
- si - source index
- di - destination index
- bp - base pointer
- sp - stack pointer

### Comments

Comments are written after ";"

### Defining constants

> {name} equ {value}

### Data section
1. Byte - db - 8 bit
2. Word - dw - 16 bit
3. Double word - dd - 32 bit
4. Quadword - dq - 64 bit
5. Ten bytes - dt - 128 bit -> float

### BSS section 
1. resb - 8 bit
2. resw - 16 bit
3. resd - 32 bit
4. resq - 64 bit
5. resdq - 128 bit

### TEXT section

Text section needs to have label start
> global _start <br>
> _start:

## Assembly syntax

### Mnemonics
1. ADD
2. SUB
3. MOV
4. LDA
5. STA
6. PUSH

### Example program
```
  .data
  hello   db    "Hello World!", 10

  .text
  global _start
  _start:
      mov rax, 1
      mov rdi, 1
      mov rsi, hello
      mov rdx, 13
      syscall
      
      mov rax, 60
      syscall
```

### Compiling with yasm
```
yasm -f elf64 {name}.asm
ld -o {Name_of_executable} {name}.o
```
