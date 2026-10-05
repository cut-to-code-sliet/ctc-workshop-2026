# CTC DSA Workshop 2026

*Click on the session name below to jump to that session.*

## Table of Contents
- [Session 1: C++ Basics, Memory, Operators & Conditionals (17 Sep 2026)](#session-1-c-basics-memory-operators--conditionals-17-sep-2026)
- [Session 2: Switch Case, Bitwise Operators, Loops & Pattern Printing (18 Sep 2026)](#session-2-switch-case-bitwise-operators-loops--pattern-printing-18-sep-2026)
- [Session 3: Arrays (1D & 2D), Break & Continue, STL Intro & Searching (19 Sep 2026)](#session-3-arrays-1d--2d-break--continue-stl-intro--searching-19-sep-2026)
- [Session 4: Time & Space Complexity, Linear & Binary Search (20 Sep 2026)](#session-4-time--space-complexity-linear--binary-search-20-sep-2026)
- [Session 5: Contest Review, Vectors & Selection Sort (23 Sep 2026)](#session-5-contest-review-vectors--selection-sort-23-sep-2026)
- [Session 6: Functions, Call Stack, Call by Value vs Reference (26 Sep 2026)](#session-6-functions-call-stack-call-by-value-vs-reference-26-sep-2026)
- [Session 7: Selection Sort & Bubble Sort (29 Sep 2026)](#session-7-selection-sort--bubble-sort-29-sep-2026)
---

## Session 1: C++ Basics, Memory, Operators & Conditionals (17 Sep 2026)

### Topics Covered
- **C++ basic syntax** — structure of a C++ program, semicolons, curly braces, `main()` function
- **Header files** — why they're used, `#include` directive, how it brings in pre-written code
- **Stack vs Heap** — brief intro to memory segments
- **Program execution flow** — how control enters `main()` first, and how function calls follow LIFO (Last In First Out) behavior on the stack
- **Data types** — `int`, `float`, `double`, `char`, `bool`, etc., and how much memory each occupies
- **ASCII table** — what it is and why it matters (how characters are stored as numbers)
- **Operators**
  - Binary: Arithmetic (`+`, `-`, `*`, `/`, `%`)
  - Unary: Increment/Decrement (`++`, `--`), pre-increment vs post-increment
  - Ternary: Conditional operator (`condition ? expr1 : expr2`)
  - Logical operators (`&&`, `||`, `!`)
  - Relational operators (`==`, `!=`, `<`, `>`, `<=`, `>=`)
- **Conditional statements** — `if`, `if-else`, `else-if` ladder

### Resources
- [C++ Basic Syntax – GeeksforGeeks](https://www.geeksforgeeks.org/cpp/cpp-programming-language/)
- [Data Types in C++](https://www.geeksforgeeks.org/cpp/cpp-data-types/)
- [Operators in C++](https://www.geeksforgeeks.org/cpp/operators-in-cpp/)
- [ASCII Table Reference](https://www.asciitable.com/)
- [Stack vs Heap Memory](https://www.geeksforgeeks.org/dsa/stack-vs-heap-memory-allocation/)

### Practice Questions
1. Write a program to swap two numbers without using a third variable.
2. Predict the output of a program using pre-increment and post-increment on the same variable in one expression.
3. Write a program using the ternary operator to find the largest of two numbers.
4. Write a program to check if a given year is a leap year using logical and relational operators.
5. Write a program using an `if-else if` ladder to categorize a number as positive, negative, or zero.

### Homework
- Learn about the **switch case** statement (syntax, when to use it over `if-else` ladder, `break` and `default`)
- Solve:
  1. Write a program using `switch-case` to build a simple calculator (+, -, *, /) based on user's operator input.
  2. Write a program using `switch-case` to print the name of the day (1–7 → Monday–Sunday).
  3. Convert one of your earlier `if-else if` ladder solutions into a `switch-case` version, and think about why switch case wouldn't work for some of them (e.g., relational conditions like `x > 10`).
  4. [C++ Switch Case Statement (GfG)](https://www.geeksforgeeks.org/problems/c-switch-case-statement5900/1) — given a number n, if it's between 1 and 10 (inclusive), return the number in words (lowercase), otherwise return "not in range".
  5. [Switch Statement (GfG)](https://www.geeksforgeeks.org/problems/switch-statement/1) — given a number n, use a switch statement to return "One" through "Nine" for n = 1 to 9, and "Unknown" for anything else.
- **Theory questions:**
  6. Why do we write `return 0;` at the end of `int main()`? What does the return value of `main()` signify?
  7. Explain the output of the following program (it outputs `20`):

```cpp
int main(){
    int y = 3;
    int z = (++y) + (y = 10);
    cout << z;
    return 0;
}
```

---

## Session 2: Switch Case, Bitwise Operators, Loops & Pattern Printing (18 Sep 2026)

### Topics Covered
- **Switch case statement** — syntax, `break`, `default`, when to prefer it over `if-else` ladders
- **Bitwise operators** — `&`, `|`, `^`, `~`, `<<`, `>>`
- **Loops**
  - `for` loop
  - `while` loop
  - `do-while` loop
- **Pattern printing** — approach:
  - For the outer loop, count the number of rows
  - For the inner loop, focus on the columns and connect them to the rows
  - Print inside the inner `for` loop
  - Observe symmetry in some special patterns (optional)

### Resources
- [Bitwise Operators in C++ – GeeksforGeeks](https://www.geeksforgeeks.org/cpp/bitwise-operators-in-c-cpp/)
- [Loops in C++ – GeeksforGeeks](https://www.geeksforgeeks.org/cpp/loops-in-c-and-cpp/)
- [Pattern Printing Sheet – takeUforward](https://takeuforward.org/strivers-a2z-dsa-course/must-do-pattern-problems-before-starting-dsa)

### Practice Questions
1. Rewrite one of the Session 1 `if-else if` programs using `switch-case`, and explain why switch wouldn't work for a relational-condition version.
2. Write a program to check if a number is even or odd using a bitwise operator instead of `%`.
3. Write a program to print a right-angled triangle pattern of `n` rows using stars (`*`).
4. Write a program using `do-while` to print numbers from 1 to 10, and explain how it differs in behavior from a `while` loop for the same task.

### Homework

**Pattern Sheet:**
- [Must-Do Pattern Problems – takeUforward](https://takeuforward.org/strivers-a2z-dsa-course/must-do-pattern-problems-before-starting-dsa) — solve **Q1 to Q10**

**Loop + Math Questions:**
1. Write a program to find the sum of digits of a given number.
2. Write a program to reverse a given integer. — [Reverse Integer (LeetCode)](https://leetcode.com/problems/reverse-integer/)
3. Write a program to check whether a given number is a palindrome. — [Palindrome Number (LeetCode)](https://leetcode.com/problems/palindrome-number/)
4. Write a program to check whether a number is prime, optimizing the loop to run only till `sqrt(n)`.
5. Write a program to find the GCD and LCM of two numbers using a loop.
6. Write a program to check whether a number is an Armstrong number.
7. Write a program to print all divisors of a number.
8. Write a program that repeatedly adds the digits of a number until a single digit remains. — [Add Digits (LeetCode)](https://leetcode.com/problems/add-digits/)

**Bitwise Questions:**
9. Write a program to count the number of set bits (1s) in the binary representation of a number, without using any built-in function. — [Number of 1 Bits (LeetCode)](https://leetcode.com/problems/number-of-1-bits/)
10. Write a program to check whether a given number is a power of 2 using bitwise operators. — [Power of Two (LeetCode)](https://leetcode.com/problems/power-of-two/)
11. Write a program to swap two numbers using the XOR bitwise operator, without a third variable.
12. Given an array where every element appears twice except one, find that one element using XOR. — [Single Number (LeetCode)](https://leetcode.com/problems/single-number/)	


---

## Session 3: Arrays (1D & 2D), Break & Continue, STL Intro & Searching (19 Sep 2026)

### Topics Covered
- **Arrays**
  - 1D arrays: declaration, initialization, indexing, traversal
  - 2D arrays: rows and columns, nested loops for traversal
- **`break` and `continue`** in loops — exiting a loop early vs. skipping the current iteration
- **STL (Standard Template Library)** — a brief idea of what it is and why it's useful
- **Searching**
  - Linear search
  - Binary search

### Resources
- **Arrays (1D)**
  - [Arrays in C++ – GeeksforGeeks](https://www.geeksforgeeks.org/cpp/cpp-arrays/)
- **Arrays (2D)**
  - [How to Create Array of Arrays (2D Arrays) in C++ – GeeksforGeeks](https://www.geeksforgeeks.org/cpp/how-to-create-array-of-arrays-in-cpp)
- **`break` and `continue`**
  - [Break vs Continue Statement – GeeksforGeeks](https://geeksforgeeks.org/break-vs-continue-statement-in-programming)
  - [continue Statement in C++ – GeeksforGeeks](https://www.geeksforgeeks.org/continue-statement-cpp)
- **STL (Standard Template Library)**
  - [C++ STL Tutorial – GeeksforGeeks](https://www.geeksforgeeks.org/cpp/cpp-stl-tutorial/)
  - [C++ STL Cheat Sheet – GeeksforGeeks](https://www.geeksforgeeks.org/cpp-stl-cheat-sheet/)
- **Linear search**
  - [Linear Search Algorithm – GeeksforGeeks](https://www.geeksforgeeks.org/linear-search/)
- **Binary search**
  - [std::binary_search() in C++ STL – GeeksforGeeks](https://www.geeksforgeeks.org/cpp/binary-search-algorithms-the-c-standard-template-library-stl)
- **Range-based `for` loop** (for the homework)
  - [Range-Based for Loop in C++ – GeeksforGeeks](https://www.geeksforgeeks.org/range-based-loop-c)
- **Pattern printing**
  - [Pattern Printing in Detail (YouTube)](https://youtu.be/tNm_NNSB3_w?si=XI-6pz2GJy1R0ICR) — for anyone who wants to learn pattern printing in more depth

  ### Practice Questions
Solved in class (Codeforces):
1. [Codeforces 2203A](https://codeforces.com/problemset/problem/2203/A)
2. [Codeforces 2193A](https://codeforces.com/problemset/problem/2193/A)
3. [Codeforces 2194A](https://codeforces.com/problemset/problem/2194/A)

### Homework
1. Learn about the **range-based `for` loop** in C++ (syntax and when to use it).
2. Take input from the user in a **2D array** and print each element.   
3. Homework pdf : [Homework](https://drive.google.com/file/d/1jdZFTCmcKE4_UeSs03lIkpY_05CBpViO/view?usp=sharing)

---

## Session 4: Time & Space Complexity, Linear & Binary Search (20 Sep 2026)

### Topics Covered
- **Time complexity**: how the running time of an algorithm grows with input size `n`, not the actual seconds it takes
- **Space complexity**: how much extra memory an algorithm uses as `n` grows
- **Big-O notation**: common complexities such as `O(1)`, `O(log n)`, `O(n)`, `O(n log n)`, `O(n^2)`
- **Linear search**: approach, pseudo code and implementation
- **Binary search**: approach, pseudo code and implementation (works only on a **sorted** array)

### Approach and Pseudo Code

**Linear search**
```
for i from 0 to n-1:
    if arr[i] == target:
        return i
return -1
```

**Binary search** (array must be sorted)
```
s = 0, e = n-1
while s <= e:
    mid = s + (e - s) / 2
    if arr[mid] == target:
        return mid
    else if arr[mid] < target:
        s = mid + 1        // target is in the right half
    else:
        e = mid - 1        // target is in the left half
return -1
```

### Code

**Linear search**
```cpp
#include <iostream>
using namespace std;

int linearSearch(int arr[], int n, int target) {
    for (int i = 0; i < n; i++) {
        if (arr[i] == target) {
            return i;      // index where the target was found
        }
    }
    return -1;             // target not present
}

int main() {
    int arr[] = {4, 8, 15, 16, 23, 42};
    int n = sizeof(arr) / sizeof(arr[0]);
    int target = 16;

    int idx = linearSearch(arr, n, target);
    if (idx != -1) cout << "Found at index " << idx << endl;
    else cout << "Not found" << endl;
    return 0;
}
```
Time complexity: `O(n)`. Space complexity: `O(1)`.

**Binary search (iterative)**
```cpp
#include <iostream>
using namespace std;

int binarySearch(int arr[], int n, int target) {
    int s = 0, e = n - 1;
    while (s <= e) {
        int mid = s + (e - s) / 2;   // safe way to find mid (avoids overflow)
        if (arr[mid] == target) {
            return mid;
        } else if (arr[mid] < target) {
            s = mid + 1;
        } else {
            e = mid - 1;
        }
    }
    return -1;
}

int main() {
    int arr[] = {4, 8, 15, 16, 23, 42};   // must be sorted
    int n = sizeof(arr) / sizeof(arr[0]);
    int target = 23;

    int idx = binarySearch(arr, n, target);
    if (idx != -1) cout << "Found at index " << idx << endl;
    else cout << "Not found" << endl;
    return 0;
}
```
Time complexity: `O(log n)`. Space complexity: `O(1)`.

### Resources
- **Time and space complexity**
  - [Analysis of Algorithms (Big-O) – GeeksforGeeks](https://www.geeksforgeeks.org/dsa/analysis-of-algorithms-big-o-analysis/)
  - [Time Complexity and Space Complexity – GeeksforGeeks](https://www.geeksforgeeks.org/dsa/time-complexity-and-space-complexity/)
- **Searching**
  - [Linear Search Algorithm – GeeksforGeeks](https://www.geeksforgeeks.org/linear-search/)
  - [Binary Search Algorithm – GeeksforGeeks](https://www.geeksforgeeks.org/dsa/binary-search/)
- **Sorting (for the homework)**
  - [Bubble Sort – GeeksforGeeks](https://www.geeksforgeeks.org/dsa/bubble-sort-algorithm/)
  - [Selection Sort – GeeksforGeeks](https://www.geeksforgeeks.org/dsa/selection-sort-algorithm-2/)
  - [Insertion Sort – GeeksforGeeks](https://www.geeksforgeeks.org/dsa/insertion-sort-algorithm/)
  - [Sorting Algorithms – takeUforward](https://takeuforward.org/strivers-a2z-dsa-course/strivers-a2z-dsa-course-sheet-2/) (Striver A2Z sheet, Sorting section)

### Homework
1. **Think and research:** In binary search, why do we calculate `mid` as `s + (e - s) / 2` instead of `(s + e) / 2`? (Hint: think about what happens when `s` and `e` are very large integers.)
2. **Learn all 3 basic sorting algorithms:**
   - Bubble sort
   - Selection sort
   - Insertion sort

   For each one, understand the idea, dry run it on a small array, write the code, and note its time complexity.
3. **Solve 5 binary search questions on LeetCode.** Suggested:
   1. [Binary Search (704)](https://leetcode.com/problems/binary-search/)
   2. [Search Insert Position (35)](https://leetcode.com/problems/search-insert-position/)
   3. [Sqrt(x) (69)](https://leetcode.com/problems/sqrtx/)
   4. [First Bad Version (278)](https://leetcode.com/problems/first-bad-version/)
   5. [Guess Number Higher or Lower (374)](https://leetcode.com/problems/guess-number-higher-or-lower/)
   
4. Homework pdf : [Homework](https://drive.google.com/file/d/1kd2nRXax1Cv2mKwWD780RlBiGyIapUQM/view?usp=sharing)

---

## Session 5: Contest Review, Vectors & Selection Sort (23 Sep 2026)

### Topics Covered

#### 1. Contest Problem Review
Solved and explained two problems from Codeforces:
- [Problem A](https://codeforces.com/contest/2266/problem/A)
- [Problem B](https://codeforces.com/contest/2266/problem/B)

#### 2. Vectors in C++
- **What is a vector?** A dynamic array from the STL — unlike a plain array, it can grow or shrink in size at runtime.
- **Declaring a vector**
```cpp
  vector<int> v;                  // empty vector of ints
  vector<int> v(5);               // vector of size 5, all elements 0
  vector<int> v(5, 10);           // vector of size 5, all elements 10
  vector<int> v = {1, 2, 3, 4};   // vector initialized with values
```
- **`push_back`** — adds an element to the end.
```cpp
  v.push_back(10);
```
- **`pop_back`** — removes the last element.
```cpp
  v.pop_back();
```
- **`size()` vs `capacity()`**
  - `size()` → number of elements currently stored in the vector.
  - `capacity()` → how many elements the vector *can* hold in its currently allocated memory before it needs to reallocate. Capacity is often larger than size (the vector over-allocates to avoid resizing on every single push, typically doubling when it runs out of room).
```cpp
  vector<int> v;
  v.push_back(1);
  v.push_back(2);
  cout << v.size();      // 2
  cout << v.capacity();  // could be 2, 4, etc. — implementation-defined
```
- **Range-based for loop with vectors**
```cpp
  for (int x : v) {
      cout << x << " ";
  }
```
  This works cleanly on vectors (unlike raw arrays passed into functions) because a `vector` always knows its own `begin()`/`end()` regardless of scope — it doesn't rely on compile-time size info the way a raw C-style array does.

#### 3. Selection Sort
**Idea:** Repeatedly find the minimum element from the unsorted part of the array and swap it into its correct position at the front.

```cpp
void selectionSort(vector<int>& arr) {
    int n = arr.size();
    for (int i = 0; i < n - 1; i++) {
        int minIdx = i;
        for (int j = i + 1; j < n; j++) {
            if (arr[j] < arr[minIdx]) {
                minIdx = j;
            }
        }
        swap(arr[i], arr[minIdx]);
    }
}
```
- **Time complexity:** O(n²) in all cases (best, average, worst) — it always scans the remaining unsorted portion fully to find the minimum, regardless of input order.
- **Space complexity:** O(1) — sorts in place, no extra array needed.

---

### Resources
- **Vectors**
  - [`std::vector` reference (cppreference)](https://en.cppreference.com/w/cpp/container/vector)
  - [Vector `push_back` (cppreference)](https://en.cppreference.com/w/cpp/container/vector/push_back)
  - [Vector `pop_back` (cppreference)](https://en.cppreference.com/w/cpp/container/vector/pop_back)
  - [Vector `size` (cppreference)](https://en.cppreference.com/w/cpp/container/vector/size)
  - [Vector `capacity` (cppreference)](https://en.cppreference.com/w/cpp/container/vector/capacity)
- **Iterators**
  - [Iterator library overview (cppreference)](https://en.cppreference.com/w/cpp/iterator)
  - [Vector `begin`/`end` (cppreference)](https://en.cppreference.com/w/cpp/container/vector/begin)
- **Sorting Algorithms**
  - [Selection Sort (GeeksforGeeks)](https://www.geeksforgeeks.org/dsa/selection-sort-algorithm-2/)
  - [Insertion Sort (GeeksforGeeks)](https://www.geeksforgeeks.org/dsa/insertion-sort-algorithm/)
  - [Bubble Sort (GeeksforGeeks)](https://www.geeksforgeeks.org/dsa/bubble-sort-algorithm/)

---

### Practice Questions
10 easy LeetCode questions on arrays and vectors:
1. [Two Sum](https://leetcode.com/problems/two-sum/)
2. [Best Time to Buy and Sell Stock](https://leetcode.com/problems/best-time-to-buy-and-sell-stock/)
3. [Contains Duplicate](https://leetcode.com/problems/contains-duplicate/)
4. [Maximum Subarray](https://leetcode.com/problems/maximum-subarray/)
5. [Merge Sorted Array](https://leetcode.com/problems/merge-sorted-array/)
6. [Remove Duplicates from Sorted Array](https://leetcode.com/problems/remove-duplicates-from-sorted-array/)
7. [Move Zeroes](https://leetcode.com/problems/move-zeroes/)
8. [Single Number](https://leetcode.com/problems/single-number/)
9. [Majority Element](https://leetcode.com/problems/majority-element/)
10. [Plus One](https://leetcode.com/problems/plus-one/)

---


### Homework
1. Learn about **iterators** in vectors — how `begin()`, `end()`, and iterator-based traversal work, as an alternative to index-based access.
2. Read the vector docs in detail — go through **every property and method** of `std::vector` (not just the ones covered today), using the cppreference link above.
3. Solve the 10 LeetCode array/vector questions given in class.
4. Study **insertion sort** and **bubble sort**, and practice writing their code from scratch.

---

- [Session 6: Functions, Call Stack, Call by Value vs Reference (26 Sep 2026)](#session-6-functions-call-stack-call-by-value-vs-reference-26-sep-2026)

---

## Session 6: Functions, Call Stack, Call by Value vs Reference (26 Sep 2026)

### Topics Covered

#### 1. Contest Review
Started the session by going over three Codeforces problems:
- [Problem 2263B](https://codeforces.com/contest/2263/problem/B)
- [Problem 2264A](https://codeforces.com/contest/2264/problem/A)
- [Problem 2259D](https://codeforces.com/contest/2259/problem/D)

#### 2. Introduction to Functions
- What a **function** is and why we break code into functions (reusability, readability).
- **How a function loads onto the call stack**: when a function is called, a new **stack frame** is pushed containing its local variables, parameters and the return address (where to go back to).
- Until a function **returns**, the function that called it is paused/blocked — it cannot move ahead until control comes back.
- **Return type** of a function decides what kind of value is sent back to the caller (`int`, `float`, `void`, etc.), and `return` is the keyword used to send that value back.

```
main() calls swap() ──▶  swap() pushed onto stack, runs
main() waits          ◀──  swap() returns, popped off stack, main() resumes
```

#### 3. Call by Value vs Call by Reference

**❌ Wrong: `swap()` using Call by Value (doesn't actually swap `a` and `b`)**
```cpp
#include <iostream>
using namespace std;

void swap(int a, int b) {
    int temp = a;
    a = b;
    b = temp;
}

int main() {
    int x = 5, y = 10;
    swap(x, y);
    cout << "x = " << x << ", y = " << y << endl; // Output: x = 5, y = 10 (unchanged!)
    return 0;
}
```
**Why it fails:** Call by value copies `x` and `y` into `a` and `b`. The function swaps its own local copies, but `x` and `y` in `main()` are never touched.

**✅ Fixed: `swap()` using Call by Reference**
```cpp
#include <iostream>
using namespace std;

void swap(int &a, int &b) {
    int temp = a;
    a = b;
    b = temp;
}

int main() {
    int x = 5, y = 10;
    swap(x, y);
    cout << "x = " << x << ", y = " << y << endl; // Output: x = 10, y = 5 (swapped!)
    return 0;
}
```
**Why it works:** The `&` makes `a` and `b` **aliases** for `x` and `y` themselves — no copies are made, so changes inside the function directly affect the caller's variables.

---

### Resources
- [Functions in C++ (GeeksforGeeks)](https://www.geeksforgeeks.org/cpp/functions-in-cpp/)
- [Call by Value vs Call by Reference (GeeksforGeeks)](https://www.geeksforgeeks.org/cpp/parameter-passing-techniques-in-cpp/)
- [Understanding the Call Stack (freeCodeCamp)](https://www.freecodecamp.org/news/how-recursion-works-explained-with-flowcharts-and-a-video-de61f40cb7f9/)

---

### Practice Questions — Classic Function-Based Problems
1. Write a function to find the **factorial** of a number.
2. Write a function to check if a number is **prime**.
3. Write a function to find the **GCD** of two numbers.
4. Write a function to find the **LCM** of two numbers.
5. Write a function to check if a number is a **palindrome**.
6. Write a function to check if a number is an **Armstrong number**.
7. Write a function to reverse a number using a function.
8. Write a function to find the **sum of digits** of a number.
9. Write a function to count the number of digits in a number.
10. Write a function to check if a number is a **perfect number**.
11. Write a function to compute **power(base, exponent)** without using `pow()`.
12. Write a function to check if a year is a **leap year**.
13. Write a function to find the **maximum of three numbers**.
14. Write a function to swap two numbers **without a temporary variable**.
15. Write a function that returns the **nth Fibonacci number**.
16. Write a function to check if a number is **even or odd**.
17. Write a function to find the **sum of an array** using a function.
18. Write a function to find the **maximum element in an array** using a function.
19. Write a recursive function to compute factorial (preview of next session's topic: recursion).
20. Write a function to check if a string is a palindrome (by passing the string as a parameter).

### Homework
1. Solve all 20 practice questions above and submit your `.cpp` file.
2. Try rewriting Q11 (power function) and Q19 (factorial) **recursively**, and note the difference in stack behavior compared to the loop-based version.
---
## Session 7: Selection Sort & Bubble Sort (29 Sep 2026)
---
### Topics Covered

#### 1. Why Sorting?
- **Sorting** means arranging elements in a particular order (ascending or descending).
- Sorted data makes other operations faster. For example, **binary search** only works on a sorted array.
- **In-place sorting:** sorts using only `O(1)` extra space. Both algorithms today are in-place.
- **Stable sorting:** equal elements keep their original relative order.

#### 2. Selection Sort
**Idea:** Repeatedly find the **minimum** element in the unsorted part and swap it into its correct position at the front.

**Dry run** on `[64, 25, 12, 22, 11]`:
```
Pass 1: min = 11  → swap with 64 → [11, 25, 12, 22, 64]
Pass 2: min = 12  → swap with 25 → [11, 12, 25, 22, 64]
Pass 3: min = 22  → swap with 25 → [11, 12, 22, 25, 64]
Pass 4: min = 25  → already in place → [11, 12, 22, 25, 64]
```

```cpp
void selectionSort(vector<int>& arr) {
    int n = arr.size();
    for (int i = 0; i < n - 1; i++) {
        int minIdx = i;
        for (int j = i + 1; j < n; j++) {
            if (arr[j] < arr[minIdx]) {
                minIdx = j;
            }
        }
        swap(arr[i], arr[minIdx]);
    }
}
```
- **Time complexity:** `O(n²)` in best, average and worst case, because it always scans the whole unsorted part.
- **Space complexity:** `O(1)`.
- **Stable?** No. The long-distance swap can change the order of equal elements.
- **Number of swaps:** at most `n - 1`, which is very few.

#### 3. Bubble Sort
**Idea:** Repeatedly compare **adjacent** elements and swap them if they are in the wrong order. After each pass, the largest remaining element "bubbles up" to its correct position at the end.

**Dry run** on `[5, 1, 4, 2, 8]`:
```
Pass 1: (5,1) swap → (5,4) swap → (5,2) swap → (5,8) no swap → [1, 4, 2, 5, 8]
Pass 2: (1,4) no    → (4,2) swap → (4,5) no                   → [1, 2, 4, 5, 8]
Pass 3: no swaps happened → array is sorted, stop early
```

```cpp
void bubbleSort(vector<int>& arr) {
    int n = arr.size();
    for (int i = 0; i < n - 1; i++) {
        bool swapped = false;
        for (int j = 0; j < n - i - 1; j++) {
            if (arr[j] > arr[j + 1]) {
                swap(arr[j], arr[j + 1]);
                swapped = true;
            }
        }
        if (!swapped) break;   // already sorted, no need to continue
    }
}
```
- **Time complexity:** `O(n²)` in the average and worst case, and `O(n)` in the best case (already sorted, thanks to the `swapped` flag).
- **Space complexity:** `O(1)`.
- **Stable?** Yes, because it only swaps when `arr[j] > arr[j + 1]` (strictly greater).

#### 4. Quick Comparison

| Feature | Selection Sort | Bubble Sort |
|---|---|---|
| Core idea | Pick the minimum, place it at the front | Swap adjacent out-of-order pairs |
| Best case | `O(n²)` | `O(n)` (with the `swapped` flag) |
| Average / Worst | `O(n²)` | `O(n²)` |
| Space | `O(1)` | `O(1)` |
| Stable | No | Yes |
| Swaps | At most `n - 1` | Up to `O(n²)` |

---

### Resources
- **Selection Sort**
  - [Selection Sort (GeeksforGeeks)](https://www.geeksforgeeks.org/dsa/selection-sort-algorithm-2/)
- **Bubble Sort**
  - [Bubble Sort (GeeksforGeeks)](https://www.geeksforgeeks.org/dsa/bubble-sort-algorithm/)
- **Sorting practice**
  - [Sorting Algorithms – takeUforward](https://takeuforward.org/strivers-a2z-dsa-course/strivers-a2z-dsa-course-sheet-2/) (Striver A2Z sheet, Sorting section)

---

### Practice Questions
1. Dry run selection sort on `[29, 10, 14, 37, 13]` and write the array after every pass.
2. Dry run bubble sort on `[6, 3, 8, 2, 9]` and write the array after every pass.
3. Write selection sort to sort an array in **descending** order.
4. Write bubble sort to sort an array in **descending** order.
5. How many comparisons does selection sort make for an array of size `n`? Does it change if the array is already sorted?
6. Why does the `swapped` flag make bubble sort `O(n)` on an already sorted array?
7. Count the total number of swaps bubble sort makes on a given array.

### Homework
1. Write **selection sort** and **bubble sort** from scratch (without looking at the notes) and submit your `.cpp` file.
2. Take input of `n` numbers from the user, sort them using bubble sort, and print the sorted array.
3. Modify selection sort to find the **k-th smallest element** of an array without fully sorting it.
4. Sort an array of strings (or characters) alphabetically using selection sort.
5. Print the array after **every pass** of both algorithms to see how they differ internally.
6. Solve these on LeetCode:
   1. [Sort Colors (75)](https://leetcode.com/problems/sort-colors/)
   2. [Squares of a Sorted Array (977)](https://leetcode.com/problems/squares-of-a-sorted-array/)
   3. [Height Checker (1051)](https://leetcode.com/problems/height-checker/)
7. **Theory:**
   1. Which of the two algorithms is stable, and why? Give a small example with duplicate values.
   2. When would you prefer selection sort over bubble sort (hint: think about the number of swaps)?
   3. Finish the pending homework from Session 5: **insertion sort**, and compare all three sorting algorithms in a table.


   ---
---

## Session 8: OOPs Basics, Procedural vs OOP, Class & Object, Constructors (05 Oct 2026)

### Topics Covered

#### 1. Introduction to OOPs
- **What is OOP?** Object-Oriented Programming is a way of writing programs by organizing code around **objects**, which bundle **data** (variables) and the **functions** that work on that data into a single unit.
- **Why OOP?**
  - **Real-world modelling** — a `Student`, `Car` or `BankAccount` in real life maps directly to a class in code.
  - **Reusability** — write a class once, create as many objects as needed (and reuse it through inheritance).
  - **Data security** — data can be hidden from outside code using access specifiers.
  - **Maintainability** — code is split into small independent units, so it is easier to read, debug and extend.
  - **Scalability** — large projects stay manageable.
- **Four pillars of OOP** (brief idea; each will be covered in detail later):

| Pillar | One-line idea |
|---|---|
| **Encapsulation** | Wrapping data and functions together in a class and restricting direct access to the data |
| **Abstraction** | Showing only the necessary details and hiding the internal working |
| **Inheritance** | A class acquiring the properties and behaviour of another class |
| **Polymorphism** | One name, many forms (same function name behaving differently) |

#### 2. Procedural vs Object-Oriented Programming
- **Procedural programming** (e.g. C) — the program is a **sequence of functions**. Data and functions are separate, and data is usually shared openly between functions.
- **Object-oriented programming** (e.g. C++, Java) — the program is a **collection of objects**. Data and functions live together inside the object.

**Same problem, both styles (bank account deposit):**
```cpp
// Procedural: data and function are separate
#include <iostream>
using namespace std;

void deposit(int &balance, int amount) {
    balance += amount;
}

int main() {
    int balance = 1000;
    deposit(balance, 500);
    balance = -99999;                 // anyone can modify the data directly!
    cout << balance << endl;
    return 0;
}
```
```cpp
// OOP: data and function are bundled, data is protected
#include <iostream>
using namespace std;

class BankAccount {
private:
    int balance;                      // hidden from outside
public:
    BankAccount(int b) { balance = b; }
    void deposit(int amount) {
        if (amount > 0) balance += amount;
    }
    int getBalance() { return balance; }
};

int main() {
    BankAccount acc(1000);
    acc.deposit(500);
    // acc.balance = -99999;          // ERROR: balance is private
    cout << acc.getBalance() << endl; // 1500
    return 0;
}
```

| Feature | Procedural | OOP |
|---|---|---|
| Focus | Functions / steps | Objects / data |
| Approach | Top-down | Bottom-up |
| Data security | Weak, data is mostly global or shared | Strong, via access specifiers |
| Code reuse | Limited (functions) | High (classes, inheritance) |
| Real-world mapping | Hard | Natural |
| Best for | Small, simple programs | Large, complex programs |
| Examples | C, Pascal | C++, Java, Python |

#### 3. Class and Object
- **Class** — a **blueprint / template** that defines what data (data members) and behaviour (member functions) something will have. A class itself does **not take memory** for its data until an object is created.
- **Object** — a **real instance** of a class. Each object has its own copy of the data members and occupies memory.
- **Access specifiers**
  - `public` — accessible from anywhere.
  - `private` — accessible only inside the class (**default** for a `class`).
  - `protected` — accessible inside the class and its derived classes (used with inheritance).
- **Dot operator (`.`)** accesses members through an object; the **arrow operator (`->`)** accesses them through a pointer to an object.
- **Getters and setters** — public functions used to safely read or change private data.

```cpp
#include <iostream>
#include <string>
using namespace std;

class Student {
private:
    int age;                          // private data member

public:
    string name;                      // public data member

    // setter
    void setAge(int a) {
        if (a > 0) age = a;
    }
    // getter
    int getAge() {
        return age;
    }
    // member function
    void display() {
        cout << "Name: " << name << ", Age: " << age << endl;
    }
};

int main() {
    Student s1;                       // object creation
    s1.name = "Aman";
    s1.setAge(20);
    s1.display();                     // Name: Aman, Age: 20

    Student s2;
    s2.name = "Riya";
    s2.setAge(21);
    s2.display();                     // Name: Riya, Age: 21

    Student* p = new Student();       // object created on the heap
    p->name = "Karan";
    p->setAge(19);
    p->display();                     // Name: Karan, Age: 19
    delete p;                         // free heap memory

    return 0;
}
```
- `s1` and `s2` are two separate objects of the same class, and each has its own `name` and `age`.
- A `struct` in C++ is almost the same as a `class`, but its members are **public by default**.

#### 4. Methods (Member Functions)
- A **method** (member function) is a function **defined inside a class** that works on the data of that class. It describes the **behaviour** of an object, just like data members describe its **state**.
- It is called through an object using the dot operator: `obj.method()`. Inside the method, the object's data members can be used directly.
- A method can take parameters and can return a value (or `void`), just like a normal function.

**Ways to define a method:**
1. **Inside the class** — written fully within the class body (the compiler treats it as `inline`, so this suits short functions).
2. **Outside the class** — only the **declaration** is inside the class, and the body is written outside using the **scope resolution operator (`::`)**. This keeps large classes clean and readable.

```cpp
#include <iostream>
using namespace std;

class Rectangle {
private:
    int length, breadth;

public:
    // 1. Defined inside the class
    void setValues(int l, int b) {
        length = l;
        breadth = b;
    }

    // 2. Declared here, defined outside the class
    int area();
    int perimeter() const;            // const method: promises not to modify the object
};

// Definition outside the class using ::
int Rectangle::area() {
    return length * breadth;
}

int Rectangle::perimeter() const {
    return 2 * (length + breadth);
}

int main() {
    Rectangle r;
    r.setValues(5, 3);
    cout << "Area: " << r.area() << endl;            // Area: 15
    cout << "Perimeter: " << r.perimeter() << endl;  // Perimeter: 16
    return 0;
}
```

**Types of methods (by purpose):**
- **Getter / accessor** — returns the value of a private data member (`getAge()`).
- **Setter / mutator** — changes a private data member safely, with validation (`setAge()`).
- **Utility / behaviour methods** — perform an action using the object's data (`area()`, `deposit()`, `display()`).

**Important points:**
- A method that does **not modify** the object should be marked **`const`** (`int perimeter() const`). A `const` object can call only `const` methods.
- Methods can be **overloaded**: the same name with different parameters (e.g. `add(int, int)` and `add(double, double)`).
- A method can call other methods of the same class directly.
- **Method vs function:** a normal function stands alone, while a method belongs to a class and needs an object to be called (except `static` methods, which belong to the class itself).

```cpp
class Calculator {
public:
    int add(int a, int b)             { return a + b; }
    double add(double a, double b)    { return a + b; }    // method overloading
    int add(int a, int b, int c)      { return a + b + c; }
};

int main() {
    Calculator c;
    cout << c.add(2, 3) << endl;          // 5
    cout << c.add(2.5, 3.5) << endl;      // 6
    cout << c.add(1, 2, 3) << endl;       // 6
    return 0;
}
```

#### 5. Constructor
- A **constructor** is a special member function that is **called automatically when an object is created**. It is used to **initialize** the data members.
- Rules:
  - Its name is the **same as the class name**.
  - It has **no return type** (not even `void`).
  - It is called automatically; you never call it manually.
  - It can be **overloaded** (multiple constructors with different parameters).
  - If you write no constructor, the compiler provides a **default constructor** (it does not initialize `int` or `float` members, so they hold garbage values).

**Types of constructors:**
1. **Default constructor** — takes no parameters.
2. **Parameterized constructor** — takes parameters to initialize the object with given values.
3. **Copy constructor** — creates a new object as a copy of an existing object.

```cpp
#include <iostream>
#include <string>
using namespace std;

class Student {
public:
    string name;
    int age;

    // 1. Default constructor
    Student() {
        name = "Unknown";
        age = 0;
        cout << "Default constructor called" << endl;
    }

    // 2. Parameterized constructor
    Student(string name, int age) {
        this->name = name;            // 'this' points to the current object
        this->age = age;
        cout << "Parameterized constructor called" << endl;
    }

    // 3. Copy constructor
    Student(const Student &other) {
        name = other.name;
        age = other.age;
        cout << "Copy constructor called" << endl;
    }

    // Destructor
    ~Student() {
        cout << "Destructor called for " << name << endl;
    }

    void display() {
        cout << name << " " << age << endl;
    }
};

int main() {
    Student s1;                       // Default constructor called
    Student s2("Aman", 20);           // Parameterized constructor called
    Student s3(s2);                   // Copy constructor called
    Student s4 = s2;                  // Copy constructor called

    s1.display();                     // Unknown 0
    s2.display();                     // Aman 20
    s3.display();                     // Aman 20
    s4.display();                     // Aman 20
    return 0;
}   // Destructors are called here, in reverse order: s4, s3, s2, s1
```

**Constructor initializer list** — a cleaner and more efficient way to initialize members (it is **required** for `const` members and reference members):
```cpp
class Point {
    int x, y;
public:
    Point(int a, int b) : x(a), y(b) { }   // initializer list
    void show() { cout << x << ", " << y << endl; }
};
```

**`this` pointer** — an implicit pointer available inside every non-static member function that points to the object that called the function. It is mainly used to separate member names from parameter names (`this->age = age;`).

**Destructor**
- A special member function that is **called automatically when an object is destroyed** (goes out of scope or is deleted).
- Name is `~ClassName()`, with no parameters and no return type, and a class can have **only one** destructor.
- Used to free resources, such as heap memory allocated with `new`.
- Objects are destroyed in the **reverse order** of their creation.

**Shallow copy vs deep copy (brief idea):** if a class holds a pointer, the default copy constructor copies only the **address** (shallow copy), so both objects point to the same memory. To give each object its own memory, write your own copy constructor that allocates new memory (**deep copy**).

---

### Resources
  - [OOPs Recource ](https://www.w3schools.com/cpp/cpp_oop.asp)
---

### Practice Questions
1. Write a class `Rectangle` with `length` and `breadth`, and member functions to calculate the **area** and **perimeter**.
2. Create a class `Student` with a default constructor and a parameterized constructor. Create one object using each and print both.
3. Predict the output (and explain): how many times is each constructor and the destructor called?
```cpp
Student a;
Student b("Aman", 20);
Student c = b;
```
4. Why does the following code give an error? How can you fix it?
```cpp
class Test {
    int x;
};
int main() {
    Test t;
    t.x = 10;
}
```
5. Write a class `Car` with private data (`brand`, `price`) and public getters and setters. Don't allow a negative price.
6. What is the difference between `class` and `struct` in C++?
7. Write a class with a parameterized constructor using an **initializer list**.
8. Write a program to show the use of the `this` pointer when the parameter name and the data member name are the same.
9. Write a class `Circle` with a method `area()` defined **outside the class** using the scope resolution operator `::`.
10. Write a class `Calculator` with an overloaded `add()` method for `int` and `double` arguments.
11. What is the difference between a normal function and a member function? What does a `const` member function mean?

### Homework
1. Solve all 11 practice questions above and submit your `.cpp` file.
2. Create a class `BankAccount` with `accountNumber`, `holderName` and `balance` (private), a **parameterized constructor**, and functions `deposit()`, `withdraw()` (don't allow overdraw) and `display()`.
3. Create a class `Book` with `title`, `author` and `price`. Take the details of **5 books** from the user, store the objects in an **array (or vector)**, and print the details of the most expensive book.
4. Add a **copy constructor** to the `Student` class and print a message inside it. Find out the situations in which the copy constructor gets called (pass by value, return by value, object initialization).
5. Create a class `Counter` with a **static** data member that counts how many objects have been created. Learn how `static` members work first.
6. **Theory:**
   1. What are the four pillars of OOP? Explain each in one line.
   2. What is the difference between procedural programming and OOP? Give an example.
   3. Can a constructor be `private`? Can a constructor have a return type? Why or why not?
   4. What is the difference between a shallow copy and a deep copy?
   5. What happens if we don't write any constructor in a class?
7. Read about the **`new` and `delete`** operators and **pointers to objects**, as preparation for the next OOP topics: inheritance and polymorphism.