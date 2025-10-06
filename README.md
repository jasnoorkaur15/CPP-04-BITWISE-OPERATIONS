# 🧠 C++ Experiment 4: Bitwise Operators 

## 🎯 Aim

- Understand how **bitwise operators** work in C++
- Learn how to **set (turn ON)** and **reset (turn OFF)** specific bits in a number

## 🎓 Objectives

- 🔹 Use bitwise operators: `&`, `|`, `^`, `~`, `<<`, `>>`  
- 🔹 Change a **single bit** in a number without affecting the rest  
- 🔹 Understand how **shifting bits** changes the entire value  

## 📖 Theory

### 📌 What Are Bitwise Operators?

- Every number is represented as **bits** (`0s` and `1s`)
- Bitwise operators are useful in low-level programming, **hardware control**, and **flag management**

### 🔢 Common Bitwise Operators in C++

| Operator | Symbol | Description                               |
|----------|--------|-------------------------------------------|
| AND      | `&`    | Sets bit to 1 **only if both** bits are 1 |
| OR       | `|`    | Sets bit to 1 if **at least one** bit is 1|
| XOR      | `^`    | Sets bit to 1 if **only one** bit is 1    |
| NOT      | `~`    | Inverts all bits (1↔0)                    |
| Left Shift  | `<<` | Shifts bits **left**, multiplies by 2    |
| Right Shift | `>>` | Shifts bits **right**, divides by 2      |

### 🔧 Set and Reset a Bit

Sometimes, we only want to change **one bit** in a number (e.g., controlling one LED).

#### ✅ To **Set** a Bit (make it `1`):
```cpp
num | (1 << 3); // Sets bit at position 3
```

#### ❌ To **Reset** a Bit (make it `0`):
```cpp
num & (~(1 << 4)); // Resets bit at position 4
```
## 🛠️ Program Description

### 🟢 Bitwise Operations

Given two numbers:
```cpp
int a = 12;  // Binary: 00001100
int b = 14;  // Binary: 00001110
```

Operations performed:
```cpp
a & b   // AND
a | b   // OR
a ^ b   // XOR
~a      // NOT
a << 2  // Left shift by 2 (multiply by 4)
a >> 3  // Right shift by 3 (divide by 8)
```

### 🔵 Set & Reset Specific Bits

```cpp
a | (1 << 2);     // Set bit 2 of 'a'
a & (~(1 << 1));  // Reset bit 1 of 'a'
```

Only the specified bits are changed — the rest of the number remains the same.

## 🧠 Concepts Used

- Bitwise Operators: `&`, `|`, `^`, `~`, `<<`, `>>`  
- Set a bit: `num | (1 << position)`  
- Reset a bit: `num & (~(1 << position))`  

## 🖥️ Sample Output

### 🔹 Bitwise Operators
```
AND: 0  
OR: 14  
XOR: 14  
NOT: -13  
LEFT_SHIFT: 48  
RIGHT_SHIFT: 1  
```

### 🔹 Set-Reset Operation
```
Enter bit to set: 3  
Enter bit to reset: 4  
SET OUTPUT: 88  
RESET OUTPUT: 64  
```
