# Number System

## Topic Index
<details open>
<summary><strong>Collapsible Topic Index</strong></summary>

- [Definitions](#definitions)
  - [Number system](#number-system-1)
  - [Numeral](#numeral)
  - [Number](#number)
  - [Digit](#digit)
- [Types of Number Systems](#types-of-number-systems)
  - [Non-Positional number system](#1-non-positional-number-system)
  - [Positional number system](#2-positional-number-system)
    - [Base](#base)
    - [More Positional Number Systems](positional_ns/types.md)
      - [Counting to Base’s Value and Beyond [A good reasoning example]](positional_ns/count.md)
      - [Definitions:](positional_ns/types.md#definitions)
        - [Binary (Base-2)](positional_ns/types.md#1-binary-base-2-a-number-system-where-the-base-is-2)
        - [Octal (Base-8)](positional_ns/types.md#2-octal-base-8-a-number-system-where-the-base-is-8)
        - [Decimal (Base-10)](positional_ns/types.md#3-decimal-base-10-a-number-system-where-the-base-is-10)
        - [Hexadecimal (Base-16)](positional_ns/types.md#4-hexadecimal-base-16-a-number-system-where-the-base-is-16)
    - [Conversion of Positional Number Systems](conversion.md)
      - [Converting Base-n to Decimal](positional_ns/conv/nToDec.md)
      - [Converting Decimal to Base-n](positional_ns/conv/decToN.md)
      - [Special Conversion (Binary, Octal, Decimal, Hexadecimal)](positional_ns/conv/special/binOctDecHex.md)
        - [Binary to Decimal (vise versa)](positional_ns/conv/special/binToDecV.md)
        - [(Octal or Hexadecimal) to Binary](positional_ns/conv/special/octHexToBin.md)
        - [Binary to (Octal or Hexadecimal)](positional_ns/conv/special/binToOctHex.md)
        - [Why Hexadecimal and Octal Align with Binary](positional_ns/conv/special/why.md)

</details>

---
---
## Definitions:

### **Number system**: 
---
A number system is a set of rules for representing numbers using a specific set of digits.

### **Numeral**: 
---
A numeral is a group of digits that represents a number.

`For Example, “4”, “55” are numerals that represent the numbers four and fifty-five.`

### **Number**: 
---
A number is a mathematical concept used to represent quantity or value. It is not a symbol — it’s a concept of quantity.

`For example, four or fifty-five indicates two quantities, no matter how it is written.`

### **Digit**: 
---
A digit is a single symbol used to build numerals. 

`For example, in the decimal system (base 10), the digits are 0 to 9`


---
```
Here’s you might have a confusion: Can a single digit be a numeral?

Answer: Yes, a single digit can also be a numeral if it is used to represent a number.
```
---

## Types of Number Systems:

### 1. Non-Positional number system:
---
A number system where the value of a digit does not depend on its position in the number. Each symbol has a fixed value.
`
Example:
XX means (in roman number system)
=10 + 10
=20
Here “X” means 10 regardless of its position
`

### 2. Positional number system:
---
A system where the value of a digit depends on both the digit and its position (or place) in the number, with each position representing a power of the system’s base.

`
Example:
512 means (in decimal)
=(5x10²) + (1x10¹) + (2x10⁰)
=(500 + 10 + 2)
Here “1” in ten’s place means different than in one's place.
`

**Base**: The base of a number system is the sum of the total digits it uses, starting from 0. 
`For example: Decimal has base 10 (digits 0–9)`




- [More Positional Number Systems](positional_ns/types.md)
- [Conversion of Positional Number Systems](positional_ns/conversion.md)
- [Binary Arithmetic](positional_ns/arithmetic.md)
- [1's & 2's compliment in binary [ Computer Science ] part-1]()
- [signed & unsigned numbers [ Computer Science ]]()
- [1's & 2's compliment in binary [ Computer Science ] part-2]()