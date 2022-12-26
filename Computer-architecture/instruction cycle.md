# Instruction cycle

## Types of instructions
<p align="center"><big><big><strong>MIPS R2000 Instruction Types</strong></big></big></p>

All instructions in the MIPS R2000 Architecture are 32 bits in length; <br>
There are three different instruction formats: <br>
- R-Type instructions, 
- I-Type instructions, 
- and J-Type instructions. <br>
<br>
R-Type instructions, or Register instructions are used for register
based ALU operations. The two operands and the destination of the result are
specified by locations in the register file. <br>
<br>
I-Type instructions, or Immediate instructions, can be either Load/Store operations, Branch operations, or Immediate ALU operations; <br>
In these instructions, one two register file locations are specified as well as a 16bit immediate value which may be used as an operand or an address.<br>
<br>
J-Type instructions, or Jump instructions, devote all of the non-opcode space to a 26-bit jump destination field; <br>
<br>
The rs and rtr egister addresses, which are present in both R- and I-type instructions, specify the two addresses which the register file is to read; In R-Type instructions the destination (write) register for the register file is specifies by <em>rd</em> and in I-Type instructions the destination register is specified by <em>rt</em> (the second read from the register file is ignored)<br>
<br>

<p>An R-Type instruction contains 6 fields: a 6 bit function code (<em>funct</em>), a 5
bit shift amount (<em>shamt</em>), three 5 bit register addresses (<em>rd</em>, <em>rt</em>,
<em>rs</em>), and a 6 bit operation code (<em>opcode</em>) which is always zero.&nbsp; </p>

<p>An I-Type instruction contains 4 fields: a 16 bit immediate field (<em>immed</em>. or <em>address</em>),
two 5 bit register addresses (<em>rt</em>, <em>rs</em>) and a 6 bit operation code (<em>opcode</em>).</p>

<p>A J-Type instruction contains 2 fields: a 26 bit jump destination (<em>target</em>) and
a 6 bit operation code (<em>opcode).</em></p>

<p><strong>R-Type Instruction Format:</strong></p>

<table border="1" width="640">
  <tr>
    <td align="center" width="120">31-26</td>
    <td align="center" width="100">25-21</td>
    <td align="center" width="100">20-16</td>
    <td align="center" width="100">15-11</td>
    <td align="center" width="100">10-6</td>
    <td align="center" width="120">5-0</td>
  </tr>
  <tr>
    <td align="center" width="154"><em>opcode</em> (000000)</td>
    <td align="center" width="80"><em>rs</em></td>
    <td align="center" width="79"><em>rt</em></td>
    <td align="center" width="80"><em>rd</em></td>
    <td align="center" width="87"><em>shamt</em></td>
    <td align="center" width="76"><em>funct</em></td>
  </tr>
</table>

<p><small><small><em>rs</em> = operand A location in register file; <em>rt</em> = operand
B location in register file; rd = result destination location in register file; <em>shamt
= </em>shift amount; <em>funct</em> = function code</small></small></p>

<p><strong>I-Type Instruction Format (ALU immediate):</strong></p>

<table border="1" width="640">
  <tr>
    <td align="center" width="120">31-26</td>
    <td align="center" width="100">25-21</td>
    <td align="center" width="100">20-16</td>
    <td align="center" width="320">15-0</td>
  </tr>
  <tr>
    <td align="center" width="154"><em>opcode </em></td>
    <td align="center" width="80"><em>rs</em></td>
    <td align="center" width="79"><em>rt</em></td>
    <td align="center" width="76"><em>immed.</em></td>
  </tr>
</table>

<p><small><small><em>rs</em> = operand A location in register file; <em>rt</em> = result
destination location in register file; <em>immed.</em> = operand B location in register
file </small></small></p>

<p><strong>I-Type Instruction Format (Load or Store):</strong></p>

<table border="1" width="640">
  <tr>
    <td align="center" width="120">31-26</td>
    <td align="center" width="100">25-21</td>
    <td align="center" width="100">20-16</td>
    <td align="center" width="320">15-0</td>
  </tr>
  <tr>
    <td align="center" width="154"><em>opcode </em></td>
    <td align="center" width="80"><em>rs</em></td>
    <td align="center" width="79"><em>rt</em></td>
    <td align="center" width="76"><em>address</em></td>
  </tr>
</table>

<p><small><small><em>rs</em> = address base register; <em>rt</em> = source (store) or
destination(load)&nbsp; location in register file; <em>immed.</em> = offset address</small></small></p>

<p><strong>I-Type Instruction Format (Branch):</strong></p>

<table border="1" width="640">
  <tr>
    <td align="center" width="120">31-26</td>
    <td align="center" width="100">25-21</td>
    <td align="center" width="100">20-16</td>
    <td align="center" width="320">15-0</td>
  </tr>
  <tr>
    <td align="center" width="154"><em>opcode </em></td>
    <td align="center" width="80"><em>rs</em></td>
    <td align="center" width="79"><em>rt</em></td>
    <td align="center" width="76"><em>address</em></td>
  </tr>
</table>

<p><small><small><em>rs</em> = operand A for conditional branch; <em>rt</em> = operand B
for conditional branch; <em>immed.</em> = offset address for branch</small></small></p>

<p><strong>J-Type Instruction Format (Jump):</strong></p>

<table border="1" width="640">
  <tr>
    <td align="center" width="120">31-26</td>
    <td align="center" width="520">25-0</td>
  </tr>
  <tr>
    <td align="center" width="154"><em>opcode </em></td>
    <td align="center" width="76"><em>target</em></td>
  </tr>
</table>

<p><small><small><em>target </em>= destination location for jump operation</small></small></p>

## Instructon cycle

<table>
  <tr>
    <td> IF </td>
    <td> ID </td>
    <td> EX </td>
    <td> MEM </td>
    <td> WB </td>
  </tr>
  <tr>
    <td> Instruction fetch from memory </td>
    <td> Instruction decode, register read </td>
    <td> Execute operation or calculate address </td>
    <td> Access memory operand </td>
    <td> Write result back to memory </td>
  </tr>
</table>
