# Binary Arithmetic

Binary arithmetic is the foundation of all digital computing. In binary, only two digits are used: 0 and 1. The rules for arithmetic operations are similar to decimal, but much simpler.

---

## Binary Addition

Binary addition follows four simple rules:

```
A   ---->     0          0          1          1
B   ---->  (+)0      (+) 1      (+) 0      (+) 1
            ----       ----       ----       ----
sum ---->     0          1          1          0

              ↓          ↓          ↓          ↓

Carry         0          0          0          1
```

- If the sum is 2 (1+1), write 0 and carry over 1 to the next higher bit.

### Example: Add (1011)₂ and (1101)₂

**Note:** Calculate from right to left.

```
   1  (carry)
   1011
+  1101
-------
  11000
```

**Step-by-step:**

| **Bit Positional index (right to left)** | 3   | 2   | 1   | 0   |
|----------------|-----|-----|-----|-----|
| **1st Number :**   | 1   | 1   | 0   | 1   |
| **2nd Number :**   | 1   | 0   | 1   | 1   |
| **Carry In :**     | 0   | 1   | 1   | 1   |
| **Sum :**          | 0   | 0   | 0   | 1   |
| **Carry Out :**    | 1   | 1   | 1   | 1   |

*Carry-in means the carry from the previous column of addition. Carry-out means the carry being delivered to the next column.*

**Result:** (1011)₂ + (1101)₂ = (11000)₂

---

## Binary Subtraction

Binary subtraction uses these rules:

```
A   ---->     0          1          1          0
B   ---->     0          0          1          1
            ----       ----       ----       ----
A - B -->     0          1          0          1

              ↓          ↓          ↓          ↓

Borrow  --->  0          0          0          1
```

- If you subtract 1 from 0, you need to borrow 1 from the next higher bit.

### Example: Subtract (1010)₂ - (0111)₂

```
   1010
-  0111
-------
   0011
```

**Step-by-step:**

|                  | 0   | 1   | 2   | 3   |
|------------------|-----|-----|-----|-----|
| **Bit Position**   | 0   | 1   | 2   | 3   |
| **Minuend**        | 0   | 1   | 0   | 1   |
| **Subtrahend**     | 1   | 1   | 1   | 0   |
| **Borrow In**      | 0   | 1   | 1   | 1   |
| **Difference**     | 1   | 1   | 0   | 0   |
| **Borrow Out**     | 1   | 1   | 1   | 0   |

**Result:** (1010)₂ - (0111)₂ = (0011)₂

---

## Summary Table

|                | Addition         | Subtraction           |
|----------------|-----------------|-----------------------|
| **Rule Example**   | 1 + 1 = 10₂       | 10 - 1 = 1₂ (borrow)   |
| **Result Example** | 101 + 11 = 1000₂  | 1010 - 0111 = 0011₂    |

---

**Binary arithmetic is essential for understanding how computers perform calculations at the hardware level. Practice with more examples to master these concepts.**