# ( Octal or Hexadecimal ) to Binary

To convert a number from base-8/16 (octal or hexadecimal) to its binary (base-2) equivalent, each digit in the base-8/16 number is represented by its corresponding binary value, using a fixed number of bits (3 bits for octal, 4 bits for hexadecimal). These binary groups are then concatenated in the same order, with or without leading zeros, to form the final binary number.

## Conversion Process

1. **Identify the base and digits**:
   - For octal (base-8), each digit (0–7) is represented by a 3-bit binary number.
   - For hexadecimal (base-16), each digit (0–9, A–F) is represented by a 4-bit binary number, where A=10, B=11, C=12, D=13, E=14, F=15.
2. **Convert each digit to binary**:
   - Use leading zeros to ensure 3 bits per octal digit or 4 bits per hexadecimal digit.
3. **Concatenate the binary groups**:
   - Write the binary groups in the same order as the original digits.
   - Concatenate them without gaps to form the binary number.
   - Optionally, omit leading zeros in the final binary number for a compact form.

## Example 1: Converting (127)₈ (Octal) to Binary

### Step-by-Step Conversion

The octal number (127)₈ is converted to binary by representing each digit (1, 2, 7) as a 3-bit binary number.

|         |     |     |     |
|:-------:|:---:|:---:|:---:|
| Digit   | 1   | 2   | 7   |
| Binary  | 001 | 010 | 111 |

#### Concatenation
- Binary groups: 001 ’ 010 ‘ 111
- Together without gaps: 001010111
- Compact (without leading zeros): 1010111

**Result**: (127)₈ = (001010111)₂ or (1010111)₂

## Example 2: Converting (127)₁₆ (Hexadecimal) to Binary

### Step-by-Step Conversion

The hexadecimal number (127)₁₆ is converted to binary by representing each digit (1, 2, 7) as a 4-bit binary number.

|         |     |     |     |
|:-------:|:---:|:---:|:---:|
| Digit   | 1   | 2   | 7   |
| Binary  | 0001 | 0010 | 0111 |

#### Concatenation
- Binary groups: 0001 ’ 0010 ‘ 0111
- Together without gaps: 000100100111
- Compact (without leading zeros): 100100111

**Result**: (127)₁₆ = (000100100111)₂ or (100100111)₂

## Example 3: Converting (2F7)₁₆ (Hexadecimal) to Binary

### Step-by-Step Conversion

The hexadecimal number (2F7)₁₆ is converted to binary by representing each digit (2, F, 7) as a 4-bit binary number. Note: F in hexadecimal equals 15 in decimal.

|         |     |         |     |
|:-------:|:---:|:-------:|:---:|
| Digit   | 2   | F --> (15)  | 7   |
| Binary  | 0010 | 1111   | 0111 |

#### Concatenation
- Binary groups: 0010 ’ 1111 ‘ 0111
- Together without gaps: 001011110111
- Compact (without leading zeros): 1011110111

**Result**: (2F7)₁₆ = (001011110111)₂ or (1011110111)₂

## General Formula

For any base-n number dₘdₘ₋₁…d₁d₀, convert to binary as follows:
1. Convert each digit dᵢ to its binary equivalent:
   - For octal (base-8), use 3 bits per digit.
   - For hexadecimal (base-16), use 4 bits per digit.
2. Concatenate the binary groups in the same order: dₘ → dₘ₋₁ → … → d₁ → d₀.
3. Optionally, remove leading zeros for the compact binary form.

This method applies to any base-n number, such as octal (base-8) or hexadecimal (base-16), when converting to binary (base-2).