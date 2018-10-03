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
### Operators
* Bitwise: ~a (not), a&b (and), a|b (or), a^b (xor), a~^b (xnor) 
  * Compares each bit one-by-one
* Logical: !a, a&&b, a||b, ==, !=, ===, !==
  * Compares entities as a whole
* Logical shift: <<, >>
* Arithmetic shift: <<<, >>>
* Conditional: sel ? a : b
* Concatenation: {a, b}
* Replication: {n{m}} (represents m n times)
### Assignments
* Blocking assignments (=): assignment immediate, happens first
* Non-blocking assignment (<=): assignment deferred until all RHS has been evaluated, closer to hardware reg behavior
* Guidelines:
  1. For sequential logic, use nonblocking
  2. Pure combinational logic in "always" block: use blocking
  3. Do not mix blocking/nonblocking in same "always" block
  4. Both sequential and combinational logic in same "always" block: use nonblocking
  * Recommendation: in complex sequential circuit, use two always blocks: one for combinational circuit, one for state update
