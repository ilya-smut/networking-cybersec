# CPU Architecture

## What is CPU?
> A central processing unit (CPU), also called a central processor, main processor or just processor, is the electronic circuitry that executes instructions comprising a computer program. The CPU performs basic arithmetic, logic, controlling, and input/output (I/O) operations specified by the instructions in the program. This contrasts with external components such as main memory and I/O circuitry,[1] and specialized processors such as graphics processing units (GPUs). [Wikipedia]

## CPU Architecture 
<img src="https://imgs.search.brave.com/d9RXlQGLgHzVqFOnkJD--KkRpuTv1FY7Vp5w9HnR9U8/rs:fit:1200:831:1/g:ce/aHR0cDovL3N0YXJ0/ZXJ0dXRvcmlhbHMu/Y29tL2Jsb2cvd3At/Y29udGVudC91cGxv/YWRzLzIwMTYvMDQv/Y29tcHV0ZXItYXJj/aGl0ZWN0dXJlLnBu/Zw" height="250px" width="350px">

- **Control Unit** is used to fetch and decode instructions
- **ALU - Arithmetic and logical unit** is used to perform mathematical and logical operations, such as addition, subtraction, and, or, etc.
- **Secondary Memory** is represented by registers. Register is a permanent storage space within central processing unit used for a particular function

## Registers
- Register is a storage for different types of information CPU operates on
- Registers are operated directly by control unit
- Can hold data, address or instruction

### Register Functions:
1. Temporary Storage for CPU
2. Store info about CPU state and current running program:
It holds: data being processed, instructions, memory addresses, status codes.
3. Staring Values from other locatins, addition and subtraction, shifting or rotating data
4. Testing contents for conditions such as zero or positive

## General registers (User Visible Registers)

<table align=center>
  <tr>
    <th>
      Register name
    </th>
    <th>
      Register shortcut
    </th>
  </tr>
  <tr>
    <th>
      Accumulator
    </th>
    <th>
      AX
    </th>
  </tr>
  <tr>
    <th>
      Base
    </th>
    <th>
      BX
    </th>
  </tr>
  <tr>
    <th>
      Counter
    </th>
    <th>
      CX
    </th>
  </tr>
  <tr>
    <th>
      Data
    </th>
    <th>
      DX
    </th>
  </tr>
  <tr>
    <th>
      Base Pointer
    </th>
    <th>
      BP
    </th>
  </tr>
    <tr>
    <th>
      Stack Pointer
    </th>
    <th>
      SP
    </th>
  </tr>
  <tr>
    <th>
      Source Index
    </th>
    <th>
      SI
    </th>
  </tr>
  <tr>
    <th>
      Destination Index
    </th>
    <th>
      DI
    </th>
  </tr>
</table>

### User Invisible Registers (UIR)
<table align=center>
  <tr>
    <th>
      Register name
    </th>
    <th>
      Register shortcut
    </th>
  </tr>
  <tr>
    <th>
      Program Counter
    </th>
    <th>
      PC
    </th>
  </tr>
  <tr>
    <th>
      Instruction Register
    </th>
    <th>
      IR
    </th>
  </tr>
  <tr>
    <th>
      Memory address register
    </th>
    <th>
      MAR
    </th>
  </tr>
  <tr>
    <th>
      Memory Data Register
    </th>
    <th>
      MDR
    </th>
  </tr>
  <tr>
    <th>
      Status Flag register
    </th>
    <th>
      SFR
    </th>
  </tr>
  </table>
  
  #### PSW - Program Status Word (Status Flag register)
  1. Sign Flag (0 - positive, 1 -negative)
  2. Zero Flag (1 - is zero, 0 - not zero)
  3. Half-Carry Flag (HC)
  4. Carry Flag (C)
  5. Overflow (V)
  6. Partify Flag (P) (Checks whether number of ones is even)
