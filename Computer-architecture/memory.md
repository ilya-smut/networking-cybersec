# Computer Memory

## Memory organisation

The organisation of memory in a computer system is called a **memory hierarchy**

When memory is at a higher level, it is faster, smaller, and more expensive

Registers operate at the highest level of memory

1. Register
2. Cache
3. Main memory ("RAM")
4. Magnetic Disc (Hard drive)
5. Magnetic tape / optical disc

### Registers VS main memory

- Registers are faster and smaller
- Registers store data temporarily during processing
- Each register performs its specific role (Unlike memory address, register serves only its particular role)
- Registers are assigned directly by the control unit

### Cache memory

- Cache memory may be seen as a bridge between main memory and CPU
- Cache holds data that is likely to be needed for next CPU operations (i.e. data which is used over and over)

[![memory.png](https://i.postimg.cc/267nKMW7/memory.png)](https://postimg.cc/HcjJJSBr)
(DMU, 2022)</br>

## Operation of memory

The main memory is composed of cells with a single value that can be stored in each cell, and a unique address for each cell

- MAR / MDR registers act as an interface between the CPU and Main memory
- MDR is also called as a memory buffer register
- MAR holds an address to be "opened"
- MAR is connected to a decoder which interpretes the address and activates a single address line into the memory

[![MAR-MDR.png](https://i.postimg.cc/mrhtWrnD/MAR-MDR.png)](https://postimg.cc/WDL2MsTL)


## Memory capacity

- Address size is a number of bits in address (K)
- Number of addressable memory locations (M), M = 2^k
- Each address size retains a number (B) of bytes
- Then **memory capacity** = (M * B) = (2^k * B)


## Types of memory
- Magnetic Core (Old and useless, consists of magnetic rings called "cores". Wires when passing through cores can change contents. Oldest type of RAM)
- Static RAM
- Dynamic RAM
- ROM (Read only)
- P-ROM (Programmable read only)
- E-PROM (Erasable programmable)
- EE-PROM (Electronically erasable)

## RAM

<table>
  <tr>
    <td>
      SRAM
    </td>
    <td>
      DRAM
    </td>
  </tr>
  <tr>
    <td>
      Faster
    </td>
    <td>
      Slower
    </td>
  </tr>
  <tr>
    <td>
      Complex
    </td>
    <td>
      Simpler to build
    </td>
  </tr> 
  <tr>
    <td>
      No refresh
    </td>
    <td>
      Needs refresh
    </td>
  </tr> 
  <tr>
    <td>
      More expensive
    </td>
    <td>
      Less expensive
    </td>
  </tr> 
  <tr>
    <td>
      Cache
    </td>
    <td>
      Main memory
    </td>
  </tr> 
  <tr>
    <td>
      Smaller
    </td>
    <td>
      Larger
    </td>
  </tr> 
  <tr>
    <td>
      Stores each bit using an electronical circuit
    </td>
    <td>
      Composed of a tine capacitor and transistor
    </td>
  </tr>
  <tr>
    <td>
      Volatile
    </td>
    <td>
      May be not volatile
    </td>
  </tr> 
</table>  


## ROM

Read-only memory
Not volatile
Cannot be changed. Is programmed when manufactured

### P-ROM

Content can be changed only once after the device is manufactured

### E-PROM

Can be erased with UV rays and reused

### EE-PROM 

Can be erased using electricity and reused



## Types of memory

- RAM (SRAM, DRAM)
- HYBRID (NVRAM, FLASH, EEPROM)
- ROM (EPROM, PROM, Masked)






















