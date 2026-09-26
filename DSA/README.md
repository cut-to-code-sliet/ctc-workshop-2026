# CTC DSA Workshop 2026

*Click on the session name below to jump to that session.*

## Table of Contents
- [Session 1: C++ Basics, Memory, Operators & Conditionals (17 Sep 2026)](#session-1-c-basics-memory-operators--conditionals-17-sep-2026)
- [Session 2: Switch Case, Bitwise Operators, Loops & Pattern Printing (18 Sep 2026)](#session-2-switch-case-bitwise-operators-loops--pattern-printing-18-sep-2026)
- [Session 3: Arrays (1D & 2D), Break & Continue, STL Intro & Searching (19 Sep 2026)](#session-3-arrays-1d--2d-break--continue-stl-intro--searching-19-sep-2026)
- [Session 4: Time & Space Complexity, Linear & Binary Search (20 Sep 2026)](#session-4-time--space-complexity-linear--binary-search-20-sep-2026)
- [Session 5: Contest Review, Vectors & Selection Sort (23 Sep 2026)](#session-5-contest-review-vectors--selection-sort-23-sep-2026)
- [Session 6: Functions, Call Stack, Call by Value vs Reference (26 Sep 2026)](#session-6-functions-call-stack-call-by-value-vs-reference-26-sep-2026)

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

## Session 6: Functions, Call Stack, Call by value vs Reference (26 Sep 2026)

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
