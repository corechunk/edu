# Binary to ( Octal or Hexadecimal )

To convert a binary (base-2) number to a target base-8/16 ( octal or hexadecimal), group the bits appropriately (3 bits for octal, 4 bits for hexadecimal) ( from right to left ), convert each group to its corresponding digit in the target base, and read the digits from left to right. For hexadecimal

NOTE: pad the binary number with leading zeros if needed to make the total number of bits a multiple of 4.

## Conversion Process

1. **Group the bits**:
   - For octal (base-8), group bits from right to left in sets of 3.
   - For hexadecimal (base-16), group bits from right to left in sets of 4
   - NOTE: Padding with leading zeros if necessary.
2. **Convert each group**:
   - Each group of 3 bits (octal) or 4 bits (hexadecimal) represents a digit in the target base.
   - Use the binary-to-decimal formula for each group: b₃×2³ + b₂×2² + b₁×2¹ + b₀×2⁰.
   - For hexadecimal, digits 10–15 are represented as A–F.
3. **Read the digits**:
   - Concatenate the resulting digits from left to right to form the number in the target base.

## Example 1: Binary to Octal (110101)₂
```
┌─────────────────────────────────┐
│   Binary to Octal: (110101)₂    │
├─────────────────────────────────┤
│        110101                   │
│       110   101                 │
│        ↓     ↓                  │
│        6     5   (Each group converted to octal)
├─────────────────────────────────┤
│ Octal Result: 65                │
└─────────────────────────────────┘
```
### How to Convert
1. Group bits from right to left in sets of 3: 110 101
2. Convert each group to octal:
   - 110 = 1×2² + 1×2¹ + 0×2⁰ = 4+2+0 = 6
   - 101 = 1×2² + 0×2¹ + 1×2⁰ = 4+0+1 = 5
3. Read digits from left to right: 65

**Result**: (110101)₂ = (65)₈

## Example 2: Binary to Hexadecimal (110101)₂
```
┌───────────────────────────────┐
│   Binary to Hex: (110101)     │
├───────────────────────────────┤
│        110101                 │
│        (Pad left with zeros)  │
│      00110101                 │
│     0011  0101                │
│       ↓     ↓                 │
│       3     5   (Each group converted to hex)
├───────────────────────────────┤
│ Hexadecimal Result: 35        │
└───────────────────────────────┘
```
### How to Convert
1. Pad bits on the left with zeros to make a multiple of 4 bits: 110101 → 00110101
2. Group bits from right to left in sets of 4: 0011 0101
3. Convert each group to hexadecimal:
   - 0011 = 0×2³ + 0×2² + 1×2¹ + 1×2⁰ = 0+0+2+1 = 3
   - 0101 = 0×2³ + 1×2² + 0×2¹ + 1×2⁰ = 0+4+0+1 = 5
4. Read digits from left to right: 35

**Result**: (110101)₂ = (35)₁₆

## Example 3: Binary to Hexadecimal (11011011)₂
```
┌───────────────────────────────┐
│   Binary to Hex: (11011011)₂  │
├───────────────────────────────┤
│        11011011               │
│     1101   1011               │
│       ↓     ↓                 │
│       D     B   (Each group converted to hex) │
├───────────────────────────────┤
│ Hexadecimal Result: DB        │
└───────────────────────────────┘

### How to Convert
1. Length is 8 bits (already a multiple of 4). No padding needed.
2. Group bits from right to left in sets of 4: 1101 1011
3. Convert each group to hexadecimal:
   - 1101 = 1×2³ + 1×2² + 0×2¹ + 1×2⁰ = 8+4+0+1 = 13 (D)
   - 1011 = 1×2³ + 0×2² + 1×2¹ + 1×2⁰ = 8+0+2+1 = 11 (B)
4. Read digits from left to right: DB

**Result**: (11011011)₂ = (DB)₁₆

## General Formula

For any binary number bₖbₖ₋₁…b₁b₀, convert to base-n (octal or hexadecimal) as follows:
1. Group bits from right to left:
   - 3 bits per group for octal (base-8).
   - 4 bits per group for hexadecimal (base-16), padding with leading zeros if needed.
2. Convert each group to a digit in the target base using: b₃×2³ + b₂×2² + b₁×2¹ + b₀×2⁰.
3. Concatenate the digits from left to right to form the base-n number: dₘdₘ₋₁…d₁d₀ₙ.

This method applies to converting binary numbers to any target base, such as octal (base-8) or hexadecimal (base-16).