# CTC AIML Workshop 2026

*Click on the session name below to jump to that session.*

## Table of Contents
- [Session 1: Python Basics, Data Types, Mutable vs Immutable, List, Tuple, Set & Dictionary (01 Oct 2026)](#session-1-python-basics-data-types-mutable-vs-immutable-list-tuple-set--dictionary-01-oct-2026)

---

## Session 1: Python Basics, Data Types, Mutable vs Immutable, List, Tuple, Set & Dictionary (01 Oct 2026)

### Topics Covered

#### 1. Python Basics
- **What is Python?** A high-level, **interpreted**, **dynamically typed** language. Code runs line by line and you don't declare variable types. It is the most popular language for AI/ML because of its simple syntax and libraries like NumPy, Pandas, scikit-learn, TensorFlow and PyTorch.
- **Running a program** — `print("Hello, World!")`; no `main()`, no semicolons, no curly braces.
- **Indentation** — Python uses indentation (usually 4 spaces) to define blocks instead of `{ }`.
- **Comments** — `# single line comment`, and `""" multi-line / docstring """`.
- **Variables** — created by assignment; the type is decided by the value and can change later.
- **Taking input** — `input()` always returns a **string**, so convert it when needed.
- **Type casting** — `int()`, `float()`, `str()`, `bool()`, `list()`, `tuple()`, `set()`.
- **Operators** — arithmetic (`+ - * / // % **`), relational (`== != < > <= >=`), logical (`and`, `or`, `not`), membership (`in`, `not in`), identity (`is`, `is not`).
- **f-strings** — easy formatted output.

```python
name = "Aman"            # str
age = 20                 # int
print(f"{name} is {age} years old")

x = int(input("Enter a number: "))   # input() gives a string, so cast it
print(x * 2)

print(7 / 2)    # 3.5  (true division)
print(7 // 2)   # 3    (floor division)
print(2 ** 5)   # 32   (power)
```

#### 2. Data Types
Python has built-in data types. Use `type()` to check the type and `isinstance()` to test it.

| Category | Type | Example |
|---|---|---|
| Numeric | `int`, `float`, `complex` | `10`, `3.14`, `2 + 3j` |
| Text | `str` | `"hello"` |
| Boolean | `bool` | `True`, `False` |
| Sequence | `list`, `tuple`, `range` | `[1, 2]`, `(1, 2)`, `range(5)` |
| Set | `set`, `frozenset` | `{1, 2, 3}` |
| Mapping | `dict` | `{"a": 1}` |
| None | `NoneType` | `None` |

```python
print(type(10))          # <class 'int'>
print(type(3.14))        # <class 'float'>
print(type("hi"))        # <class 'str'>
print(type([1, 2]))      # <class 'list'>
print(isinstance(5, int))  # True
```
- Python integers have **no fixed size limit**, so they don't overflow like `int` in C++.
- **Truthy / falsy:** `0`, `0.0`, `""`, `[]`, `()`, `{}`, `set()` and `None` are treated as `False`; most other values are `True`.

#### 3. Mutable vs Immutable
- **Mutable** objects can be **changed in place** after creation: `list`, `set`, `dict`.
- **Immutable** objects **cannot be changed** after creation; any "change" creates a new object: `int`, `float`, `bool`, `str`, `tuple`, `frozenset`.
- `id()` gives the memory identity of an object, which helps to see whether a change happened in place.

```python
# Immutable: int
a = 10
print(id(a))
a = a + 1          # new object created
print(id(a))       # different id

# Immutable: str
s = "hello"
# s[0] = "H"       # TypeError: 'str' object does not support item assignment

# Mutable: list
lst = [1, 2, 3]
print(id(lst))
lst.append(4)      # changed in place
print(id(lst))     # same id
```
**Why it matters:**
- Only **immutable** (hashable) objects can be **dictionary keys** or **set elements**.
- Two names can point to the same mutable object, so changing one changes the other:
```python
a = [1, 2, 3]
b = a              # b is another name for the same list
b.append(4)
print(a)           # [1, 2, 3, 4]

c = a.copy()       # a real, independent copy
```

#### 4. List
An **ordered**, **mutable** collection that allows **duplicates** and can hold mixed types.

```python
lst = [10, 20, 30, 40]
print(lst[0], lst[-1])     # indexing, negative index starts from the end
print(lst[1:3])            # slicing -> [20, 30]

lst.append(50)             # add at end
lst.insert(1, 15)          # insert at index
lst.extend([60, 70])       # add many elements
lst.remove(20)             # remove first occurrence of a value
lst.pop()                  # remove and return last element
lst.sort()                 # sort in place
lst.reverse()              # reverse in place
print(len(lst), 30 in lst)

squares = [x * x for x in range(5)]   # list comprehension -> [0, 1, 4, 9, 16]
```
Common methods: `append`, `insert`, `extend`, `remove`, `pop`, `clear`, `index`, `count`, `sort`, `reverse`, `copy`.

#### 5. Tuple
An **ordered**, **immutable** collection that allows duplicates. Used for fixed data such as coordinates.

```python
t = (1, 2, 3)
single = (5,)              # a single-element tuple needs the comma(,)
print(t[0], t[-1], t[0:2])
print(t.count(2), t.index(3))

a, b, c = t                # tuple unpacking
# t[0] = 10                # TypeError: tuples cannot be changed
```
- Tuples are **faster** and use **less memory** than lists.
- A tuple can be a dictionary key (if it only contains immutable items); a list cannot.

#### 6. Set
An **unordered** collection of **unique** elements. It is **mutable**, but its elements must be immutable.

```python
s = {1, 2, 3, 3, 2}
print(s)                   # {1, 2, 3}  -> duplicates removed
empty = set()              # {} creates an empty dict, not a set

s.add(4)
s.remove(1)                # error if the element is missing
s.discard(100)             # no error if the element is missing

a = {1, 2, 3}
b = {3, 4, 5}
print(a | b)               # union        -> {1, 2, 3, 4, 5}
print(a & b)               # intersection -> {3}
print(a - b)               # difference   -> {1, 2}
print(a ^ b)               # symmetric difference -> {1, 2, 4, 5}
```
- Membership check (`x in s`) is very fast, about `O(1)` on average.
- Sets have **no indexing** because they are unordered.

#### 7. Dictionary
A collection of **key : value** pairs. Keys are **unique and immutable**; values can be anything. Dictionaries keep **insertion order** (Python 3.7+) and are **mutable**.

```python
student = {"name": "Riya", "age": 20, "city": "Ludhiana"}

print(student["name"])             # Riya
print(student.get("marks", 0))     # 0 -> safe access with a default value

student["age"] = 21                # update
student["marks"] = 88              # add new key
del student["city"]                # delete a key

for key, value in student.items():
    print(key, value)

print(student.keys())              # all keys
print(student.values())            # all values
print("name" in student)           # checks keys -> True
```
Common methods: `get`, `keys`, `values`, `items`, `update`, `pop`, `popitem`, `setdefault`, `clear`, `copy`.

#### 8. Quick Comparison

| Feature | List | Tuple | Set | Dictionary |
|---|---|---|---|---|
| Syntax | `[1, 2]` | `(1, 2)` | `{1, 2}` | `{"a": 1}` |
| Ordered | Yes | Yes | No | Yes (insertion order) |
| Mutable | Yes | No | Yes | Yes |
| Duplicates | Allowed | Allowed | Not allowed | Keys must be unique |
| Indexing | Yes | Yes | No | By key |
| Use case | General-purpose sequence | Fixed data | Unique items, set math | Mapping / lookup |

---

### Resources
- **Python basics**
  - [The Python Tutorial (python.org)](https://docs.python.org/3/tutorial/)
  - [Python Built-in Types (python.org)](https://docs.python.org/3/library/stdtypes.html)
- **Data types and mutability**
  - [Python Data Types – GeeksforGeeks](https://www.geeksforgeeks.org/python/python-data-types/)
  - [Mutable vs Immutable Objects in Python – GeeksforGeeks](https://www.geeksforgeeks.org/python/mutable-vs-immutable-objects-in-python/)
- **List, Tuple, Set, Dictionary**
  - [Python Lists – GeeksforGeeks](https://www.geeksforgeeks.org/python/python-list/)
  - [Python Tuples – GeeksforGeeks](https://www.geeksforgeeks.org/python/tuples-in-python/)
  - [Python Sets – GeeksforGeeks](https://www.geeksforgeeks.org/python/sets-in-python/)
  - [Python Dictionary – GeeksforGeeks](https://www.geeksforgeeks.org/python/python-dictionary/)

---

### Practice Questions
1. Take a number as input and print whether it is even or odd.
2. Predict the output: `print(type(5 / 2))`, `print(5 // 2)`, `print(type(True + 1))`.
3. Create a list of 5 numbers, add one element at the end, remove the second element, and print the list in sorted order.
4. Predict the output and explain why:
```python
a = [1, 2, 3]
b = a
b.append(4)
print(a)
```
5. Create a tuple and try to change one of its elements. What error do you get?
6. Remove duplicates from the list `[1, 2, 2, 3, 4, 4, 5]` using a set.
7. Create a dictionary of 3 students and their marks, then print the name of the student with the highest marks.
8. Given two sets `{1, 2, 3, 4}` and `{3, 4, 5, 6}`, print their union, intersection and difference.
9. Explain with an example why `s[0] = "H"` fails for a string but works for a list.

### Homework
1. Solve all 9 practice questions above and submit your `.py` file.
2. Write a program to find the **largest and smallest** element in a list without using `max()` and `min()`.
3. Write a program to **reverse** a list in two ways: using slicing, and using a loop.
4. Write a program to count the **frequency of each character** in a string using a dictionary.
5. Write a program to find the **common elements** of two lists using sets.
6. Write a program to **swap the keys and values** of a dictionary.
7. Write a program to sort a list of tuples by their **second element**, e.g. `[(1, 3), (2, 1), (3, 2)]`.
8. Create a list of squares of the numbers 1 to 10 using **list comprehension**.
9. **Theory:**
   1. What is the difference between mutable and immutable objects? Give 3 examples of each.
   2. Why can a tuple be a dictionary key but a list cannot?
   3. Why does `{}` create a dictionary and not a set? How do you create an empty set?
   4. What is the difference between `remove()` and `discard()` in a set?
10. Read about **strings** in Python (indexing, slicing and common methods like `split`, `join`, `strip`, `replace`, `upper`, `lower`) for the next session.