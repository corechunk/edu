# Why Changing Higher Hex Digits Leaves Lower Bits Unchanged

#### Hex Example: B5  
B = 11 (in decimal)  
5 = 5  
Binary: 1011 0101  

Changing the 'B' (16¹ place) → 'C':  
C5  
Adds 16¹ = 16  

## Reason it resets neatly:  
- Right 4 bits can represent values 0–15.  
- Adding 16 (which is 1 higher than 15) “wraps over” that 4-bit block, keeping it exactly in the same position.  

## General Pattern:  
- The rightmost 4 bits have 16 combinations (0–15), which is 2⁴.  
- When you add 16¹ = 16, it’s like “resetting” the counter of lower 4 bits.  

Similarly for 16² place:  
- Imagine hex 1F5 (1 in 16² place):  
      1F5 in decimal = (1×256) + (15×16) + 5  
- Adding 16² = 256  
- Now you have 2F5  

Why do the right 8 bits stay the same?  
- The right 8 bits can hold values 0–255 (max), which is 2⁸.  
- Adding 256 (one more than 255) resets that 8-bit range neatly.  

In other words:  
- 4 bits → max value 15 → adding 16 resets this “slot” cleanly.  
- 8 bits → max value 255 → adding 256 resets this “slot” cleanly.  

## Quick Reference
Hex digit positions and their impact:  

Position      Multiplier          Max Value in bits covered  
-------------------------------------------------------------  
16⁰ place     +1                  affects only right 4 bits (0–15)  
16¹ place     +16                 resets right 4 bits  
16² place     +256                resets right 8 bits  
16³ place     +4096               resets right 12 bits  

So:  
- Changing the 16¹ digit adds 16, which is 1 higher than 15 (max 4-bit).  
- Changing the 16² digit adds 256, which is 1 higher than 255 (max 8-bit).  
- This causes the lower bits to “stay aligned,” just shifted by a clean step.