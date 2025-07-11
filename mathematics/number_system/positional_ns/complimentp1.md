# 1's and 2's Complement in Binary [Computer Science, Part 1]

In computer science, 1's and 2's complements are techniques used to represent numbers in binary, enabling subtraction to be performed as addition. This simplifies computer arithmetic, as hardware can use a single addition circuit for both operations. In this part, we focus on the mechanics of 1's and 2's complements without discussing signed or unsigned numbers (to be covered in Part 2). We’ll explain why these methods work, starting with a clock analogy, then moving to decimal examples, and finally applying the concept to binary. A key requirement is using the same number of digits or bits for both numbers, padding with zeros if necessary.

## Why: Subtraction Using Addition

The core idea of 1's and 2's complements is to perform subtraction by adding a special number called the complement. This complement, when added to the number being subtracted, completes a cycle to produce the correct result, similar to modular arithmetic.

### Clock Analogy
Imagine a 12-hour clock to perform subtraction, such as 3 - 2 = 1. Instead of subtracting 2 directly, we add a number that “completes the cycle” around the clock. The cycle is 12 hours, so the complement of 2 is the number that, when added to 2, equals 12:

- **Complement of 2**: 12 - 2 = 10.
- **Operation**: 3 + 10 = 13. On a 12-hour clock, 13 is equivalent to 1 (since 13 - 12 = 1).

Thus, 3 - 2 becomes 3 + 10 = 13 ≡ 1 (mod 12). The complement (10) allows subtraction to be performed as addition.

### Decimal Example with Single Digit
Let’s apply this idea to decimal numbers using a single digit (base-10), where the cycle is 10, similar to the clock’s cycle of 12. The maximum single-digit value is 9, so we calculate the complement relative to 9 (not 10, as we’re working within one digit). For example, to subtract 7 from 8 (8 - 7 = 1):

1. **Find the 1's complement of 7**:
   - Maximum single-digit value: 9.
   - Complement of 7: 9 - 7 = 2.
2. **Add the complement**:
   - 8 + 2 = 10.
   - In a single-digit system, take the last digit: 10 ≡ 0 (since 10 - 10 = 0).
3. **Observation**: The result (0) is one less than the correct answer (1, since 8 - 7 = 1).

This “one less” behavior is consistent in 1's complement. To correct it, we define the **2's complement** by adding 1 to the 1's complement:
- 2's complement of 7: 2 + 1 = 3.
- Add: 8 + 3 = 11. Last digit: 1 (correct, since 8 - 7 = 1).

The gap is always 1 in the ones place, so adding 1 to the 1's complement gives the 2's complement, which produces the correct result.

### More Decimal Examples
Let’s try additional single-digit decimal examples to reinforce the pattern:

- **5 - 3**:
  - 1's complement of 3: 9 - 3 = 6.
  - 5 + 6 = 11. Last digit: 1.
  - Result: 1 (one less than 2, since 5 - 3 = 2).
  - 2's complement: 6 + 1 = 7.
  - 5 + 7 = 12. Last digit: 2 (correct).

- **9 - 4**:
  - 1's complement of 4: 9 - 4 = 5.
  - 9 + 5 = 14. Last digit: 4.
  - Result: 4 (one less than 5, since 9 - 4 = 5).
  - 2's complement: 5 + 1 = 6.
  - 9 + 6 = 15. Last digit: 5 (correct).

- **6 - 2**:
  - 1's complement of 2: 9 - 2 = 7.
  - 6 + 7 = 13. Last digit: 3.
  - Result: 3 (one less than 4, since 6 - 2 = 4).
  - 2's complement: 7 + 1 = 8.
  - 6 + 8 = 14. Last digit: 4 (correct).

**Key Observation**: The 1's complement result is always one less than the desired result in the ones place. In a single-digit decimal system, after reaching 9, adding 1 cycles to 0 (as in 10, ones place 0). To correct the “one less” issue, we add 1 to the 1's complement to form the 2's complement, which gives the correct result when added.

### Key to Consistent Behavior
To achieve this behavior, both numbers must use the same number of digits. In these decimal examples, we used single digits. If numbers have different digit lengths, pad the shorter number with leading zeros (e.g., treat 3 as 03 if working with two digits). This ensures the arithmetic aligns with the cycle (e.g., 9 for one digit, 99 for two digits).

### Binary Application: 1's and 2's Complement
Now, let’s apply this to binary (base-2), where we work with bits. For consistency, both numbers must use the same number of bits (e.g., 4 bits). The maximum value in n bits is 2ⁿ - 1 (e.g., for 4 bits, max value is 15, or 1111 in binary). If numbers have different bit lengths, pad the shorter one with leading zeros.

#### 1's Complement in Binary
To find the 1's complement of a binary number, flip each bit (0 becomes 1, 1 becomes 0). This is analogous to subtracting from the maximum value (9 in decimal, 2ⁿ - 1 in binary).

Example: Subtract 3 from 5 in 4-bit binary (5 - 3 = 2):
- 5 in binary: 0101
- 3 in binary: 0011
- Maximum value (4 bits): 1111 (15 in decimal).
- 1's complement of 0011: Flip bits → 1100 (equivalent to 15 - 3 = 12 in decimal).
- Add: 0101 + 1100 = 10001 (5 bits, discard overflow bit): 0001.
- Result: 0001 = 1 (decimal), one less than 2.

The 1's complement gives a result one less than the correct answer, just like in decimal.

#### 2's Complement in Binary
To get the 2's complement, take the 1's complement and add 1. This corrects the “one less” issue.

Example: Revisit 5 - 3 in 4-bit binary:
- 1's complement of 0011: 1100.
- 2's complement: 1100 + 0001 = 1101.
- Add: 0101 + 1101 = 10010 (discard overflow): 0010.
- Result: 0010 = 2 (decimal), correct (5 - 3 = 2).

#### Another Binary Example: 7 - 4
- 7 in binary (4 bits): 0111
- 4 in binary (4 bits): 0100
- 1's complement of 0100: Flip bits → 1011 (equivalent to 15 - 4 = 11).
- 2's complement: 1011 + 0001 = 1100.
- Add: 0111 + 1100 = 10011 (discard overflow): 0011.
- Result: 0011 = 3 (decimal), correct (7 - 4 = 3).

**Why It Works in Binary**: Flipping the bits (1's complement) is equivalent to subtracting the number from the maximum value (2ⁿ - 1, e.g., 15 for 4 bits). This produces a result one less than desired, so adding 1 (2's complement) corrects it, aligning with the cycle of 2ⁿ (e.g., 16 for 4 bits, where 1111 + 0001 = 10000 ≡ 0000).

### Key to Consistent Behavior in Binary
Always use the same number of bits for both numbers. If one number has fewer bits, pad with leading zeros (e.g., 3 as 0011 in 4 bits). This ensures the arithmetic respects the cycle (2ⁿ), just like using the same number of digits in decimal.

### Summary
- **1's Complement**: In decimal, subtract from 9 (single digit) to get a result one less than the correct answer. In binary, flip the bits (subtract from 2ⁿ - 1) for the same effect.
- **2's Complement**: Add 1 to the 1's complement to correct the “one less” issue, giving the correct subtraction result.
- **Why It Works**: Subtraction is transformed into addition, simplifying computer arithmetic.
- **Bit/Digit Consistency**: Use the same number of bits or digits, padding with zeros if needed.

In Part 2, we’ll explore how 1's and 2's complements relate to signed numbers and how to handle digits without the sign bit. For now, practice these steps with fixed bit lengths to master the process!