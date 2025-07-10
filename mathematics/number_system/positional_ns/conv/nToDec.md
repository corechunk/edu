# Converting Base-n Numbers to Decimal

To convert a number from any base-n to its decimal (base-10) equivalent, calculate the **sum of each digit multiplied by its positional value**. 

`decimal_equivalent = sum ( each_digit * it's_positional_value )`

#### Positional Value
Positional Value is determined by the base raised to the power of the digit's Positional-Index, counting from right to left, starting at 0.

`positional-value = base to the power⁽ᴵᵗ'ˢ⁻ᵖᵒˢᶦᵗᶦᵒⁿᵃˡ⁻ᴵⁿᵈᵉˣ⁾ `

#### What is Position-Index
 
    7481  ( Any Number )
    ↓
    7   4   8   1   ( Separate Digits )
    ↓   ↓   ↓   ↓
    3   2   1   0   [ Their positional Index (Right to Left): ]

### Finally

`decimal_equivalent = sum ( each_digit * baseᵖᵒʷᵉʳ⁽ᴵᵗ'ˢ⁻ᵖᵒˢᶦᵗᶦᵒⁿᵃˡ⁻ᴵⁿᵈᵉˣ⁾ )`

## Example: Converting (13647)₈ to Decimal

Let's break down the conversion of the octal number **(13647)₈** to decimal step by step.

### Step-by-Step Calculation

The number **(13647)₈** can be expressed as:

    (13647)₈
    = 1×8⁴ + 3×8³ + 6×8² + 4×8¹ + 7×8⁰
    = 1×4096 + 3×512 + 6×64 + 4×8 + 7×1
    = 6055

#### Calculating Each Term
| Calculation | Result |
|:-----------:|-------:|
| 1×4096      | 4096   |
| 3×512       | 1536   |
| 6×64        | 384    |
| 4×8         | 32     |
| 7×1         | 7      |
| **Sum =**     | **6055** |
### Final Result
(13647)₈ = (6055)₁₀


# General Formula [ advance writing ]
For any base-n number dₘ dₘ₋₁ …d₁ d₀, the decimal value is:

dₘ×nᵐ + dₘ₋₁×nᵐ⁻¹ + … + d₁×n¹ + d₀×n⁰

Where:
- dᵢ is the digit at position i,
- n is the base,
- Position i is counted from right to left, starting at 0.

This method applies to any base-n number, such as binary (base-2), octal (base-8), or hexadecimal (base-16).