# Lab 1: Oct 3, 2018
## Verilog
* Testbench: feeds inputs into and reads outputs from module
### Data Types
* Variables must be declared before used
  * Wire
    * Models basic wire that holds transient values
  * Reg
    * Anything that stores a value
### Data Values
* Values: 1, 0
* Radicies: d (decimal), h (hex), o (octal), b (binary)
* Format: `<size>'<radix><value>`
   ```
   123        // default decimal radix, unspecified width
   'd123      // decimal radix
   8'h7B      // hex radix
   'b111_1011 // binary radix, underscores allowed for readability
   ```
