# Converting Decimal to Base-n Numbers

To convert a decimal (base-10) number to a target base-n number, repeatedly divide the decimal number by the target base, collecting the remainders in reverse order (from least significant to most significant). The remainders form the digits of the number in the target base.

## Division Terminology

In division, the terms are defined as follows:

- **Dividend (ভাজ্য)**: The number being divided (e.g., `a` in `a ÷ b = c`).
- **Divisor (ভাজক)**: The number by which the dividend is divided (e.g., `b`).
- **Quotient (ভাগফল)**: The integer result of the division (e.g., `c`).
- **Remainder (ভাগশেষ)**: The leftover value after division.

#### Example of this Terminology: 3 ÷ 2
3 ÷ 2 = 1.5  
- Dividend: 3  
- Divisor: 2  
- Quotient: 1  
- Remainder: 1 (since 2 × 1 = 2, and 3 - 2 = 1)  
Alternatively, in integer division:  
3 ÷ 2 = 1 with a remainder of 1.

## Example: Converting (375)₁₀ to Octal

Let's convert the decimal number (375)₁₀ to octal (base-8) step by step.

### Step-by-Step Calculation

To convert (375)₁₀ to octal, repeatedly divide by 8, record the quotient and remainder at each step, and collect the remainders from bottom to top (least significant to most significant).

#### Division Process
```text
Decimal to Octal: (375)₁₀
=====================
   8 │ 375
     ├──────── 46 , 7  <-- (quotient , remainder)
   8 │ 46
     ├────────  5 , 6  <-- (quotient , remainder)
   8 │ 5
     └────────  0 , 5  <-- (quotient , remainder)
=====================
Remainders (MSB to LSB): 5 6 7
Octal Result: 567
=====================
```


#### Collecting Remainders
- Remainders (from bottom to top): 5, 6, 7  
- These form the octal digits in order: 567

#### Result
(375)₁₀ = (567)₈

### Verification Table
To verify, convert (567)₈ back to decimal:  
| Calculation | Result |
|:-----------:|-------:|
| 5×8²       | 320   |
| 6×8¹       | 48    |
| 7×8⁰       | 7     |
| **Sum =**   | **375** |

This confirms (567)₈ = (375)₁₀.

## General Formula
For any decimal number d, to convert to base-n:  
1. Divide d by n, record the quotient and remainder.  
2. Repeat the division with the quotient until the quotient is 0.  
3. Collect the remainders in reverse order (bottom to top) to form the base-n number.

### Example General Formula
For a decimal number d, the base-n number is:  
rₖrₖ₋₁…r₁r₀ₙ  
Where rᵢ are the remainders from successive divisions by n, written from least significant (rₖ) to most significant (r₀).

This method applies to any target base, such as binary (base-2), octal (base-8), or hexadecimal (base-16).