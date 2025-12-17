# DSA-TwoPointer-Pattern

# Two Pointer Pattern (Beginner Notes)

I am learning DSA patterns step by step.  
This folder contains problems solved using the **Two Pointer technique**, with focus on
**understanding pointer movement through dry running**, not memorizing code.

---

## What is Two Pointer Pattern?

Instead of using nested loops, we use **two pointers** to traverse an array or string.
Each pointer has a **clear role**, and they move based on the problem condition.

Two pointers can move in:
1. Opposite directions
2. Same direction (slow / fast OR read / write)

---

## Type 1: Opposite Direction Pointers

### Idea
- One pointer starts from the **left**
- One pointer starts from the **right**
- Both pointers move **towards each other**
- Used when we need to compare or swap elements

---

### Problem 1: Reverse Array

#### Problem Statement
Reverse the given array **in place**.

#### Pointer Roles
- `left` pointer → starts at index `0`
- `right` pointer → starts at last index
- Both pointers move at the **same time**

#### Logic (Dry Run Thinking)
1. Swap values at `left` and `right`
2. Move `left` forward
3. Move `right` backward
4. Stop when `left` crosses `right`

#### Example
Input: [0, 1, 3, 2]

Steps:
- Swap `0` and `2`
- Swap `1` and `3`

Output:[2, 3, 1, 0]


#### Key Learning
- This pattern does **not** use slow/fast logic
- Both pointers move together
- Temporary variable is used to swap values safely

---

## Type 2: Same Direction Pointers (Read / Write)

### Idea
- Both pointers start from the **beginning**
- One pointer reads values
- One pointer writes values
- Used when we need to **filter or rearrange** elements

---

### Problem 2: Move Zeroes

#### Problem Statement
Move all zeroes to the **end** of the array while keeping
the order of non-zero elements the same.

#### Pointer Roles
- `i` → read pointer (iterates through array)
- `x` → write pointer (marks position for next non-zero)

#### Logic (Dry Run Thinking)
1. Start both pointers at index `0`
2. Read pointer (`i`) scans the array
3. When a non-zero is found:
   - Place it at index `x`
   - Increment `x`
4. After first pass:
   - All non-zero values are placed at the front
5. Fill remaining positions with `0`

#### Example
Input:[0, 1, 0, 3, 12]
After placing non-zero values: [1, 3, 12, _, _]

After filling zeroes:[1, 3, 12, 0, 0]


#### Key Learning
- Read pointer only **checks values**
- Write pointer **controls array modification**
- Understanding pointer roles is more important than code

---

---

### Problem 4: Remove Duplicates from Sorted Array

#### Pattern Used
Two Pointers (Slow / Fast)

#### Key Observation
- The array is sorted
- Duplicate elements always appear next to each other

#### Pointer Roles
- `i` → fast pointer (reads all elements)
- `x` → slow pointer (stores last unique element)

#### Core Logic
- Compare current element with last unique element
- If current value is greater, it is a new unique element
- Move `x` forward and store the new value

#### Why No Extra Loop Is Needed
- Unlike Move Zeroes, we are not adding new values
- We only keep unique elements at the front
- Duplicates are skipped naturally

#### Example
Input: [1, 1, 2, 2, 3]

Output (conceptually):[1, 2, 3, _, _]


#### Learning
Understanding pointer roles and dry running the condition
made this problem clear.


## Final Takeaway

- Two Pointer problems are about **movement and roles**
- Dry running helps build pointer intuition
- I focus on understanding patterns before optimizing

More problems will be added as I learn.

// Pattern: Two Pointers (Opposite Direction)
// Idea: Swap elements from both ends until pointers meet
// Pattern: Two Pointers (Read / Write)
// Idea: Read pointer scans, write pointer places non-zero values





