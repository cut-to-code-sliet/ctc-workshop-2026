# CTC Workshop 2026

*Click on the session name below to jump to that session.*

## Table of Contents
- [Session 1: C++ Basics, Memory, Operators & Conditionals (17 Sep 2026)](#session-1-c-basics-memory-operators--conditionals-17-sep-2026)
- [Session 2: Switch Case, Bitwise Operators, Loops & Pattern Printing (18 Sep 2026)](#session-2-switch-case-bitwise-operators-loops--pattern-printing-18-sep-2026)
- [Session 3: Arrays (1D & 2D), Break & Continue, STL Intro & Searching (19 Sep 2026)](#session-3-arrays-1d--2d-break--continue-stl-intro--searching-19-sep-2026)

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
