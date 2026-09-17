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