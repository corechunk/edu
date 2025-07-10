# Binary to Decimal ( vise versa )

## Binary to Decimal Conversion

We have already learned how to convert any base-n number to decimal. Let’s apply this to binary (base-2) numbers and explore a faster method using a pattern.

## Example: Converting (110101)₂ to Decimal

We know the standard method:

(110101)₂  
= 1×2⁵ + 1×2⁴ + 0×2³ + 1×2² + 0×2¹ + 1×2⁰  
= 1×32 + 1×16 + 0×8 + 1×4 + 0×2 + 1×1  
= 32 + 16 + 0 + 4 + 0 + 1  
= 53  

So, (110101)₂ = (53)₁₀  

But we can solve it faster using a pattern!

### Step-by-Step (Faster Method)

1. **Write the pattern**: The powers of 2 from right to left, starting at 2⁰ = 1, for as many digits as the binary number (here, 6 digits):

   |…|32|16|8|4|2|1|
   |:-:|:-:|:-:|:-:|:-:|:-:|:-:|

2. **Write the binary number under the pattern**:

   |1|1|0|1|0|1|
   |:-:|:-:|:-:|:-:|:-:|:-:|

3. **It will look like this :**

   |32|16|8|4|2|1|
   |:-:|:-:|:-:|:-:|:-:|:-:|
   |1|1|0|1|0|1|

4. **Sum the numbers from the top row where there’s a 1 in the corresponding column**:  
32 + 16 + 4 + 1 = 53

**Result**: (110101)₂ = (53)₁₀

### Note
You just need to remember the pattern. Starting from 1, each number multiplies by 2, creating a sequence like:

|…|512|256|128|64|32|16|8|4|2|1|
|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|

## Decimal to Binary Conversion

We can use a similar pattern to convert from decimal to binary, working from left to right.

## Example: Converting (562)₁₀ to Binary

### Step-by-Step

1. **Prepare the pattern**: List powers of 2 from left to right, starting with the largest power of 2 less than or equal to the decimal number (562), up to 2⁰ = 1:

|…|512|256|128|64|32|16|8|4|2|1|
|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|

2. **Fill in 1s from left to right**:
   - Start with the largest number ≤ 562 (here, 512).
   - Place a 1 under 512, subtract 512 from 562 (562 − 512 = 50).
   - Continue with the largest number ≤ 50 (here, 32), place a 1, subtract 32 (50 − 32 = 18).
   - Continue with 18 (16), then 2 (2), until the sum of the selected numbers equals 562.
   - Finally, fill all the blank space with "0"

3. **Resulting table**:

|…|512|256|128|64|32|16|8|4|2|1|
|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|
||1|0|0|0|1|1|1|1|1|0|

4. **Read the binary digits**: The 1s and 0s form the binary number.

**Result**: (562)₁₀ = (1000111110)₂