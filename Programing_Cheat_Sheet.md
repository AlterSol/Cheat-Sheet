## Introduction

This cheat sheet provides a quick reference guide for essential programming concepts, syntax, and common functions across different programming languages. It covers various topics such as variables, data types, control structures, loops, functions, object-oriented programming, file handling, error handling, and useful tips and tricks. Organized to cater to beginners and experienced programmers, this guide helps you understand the fundamentals and enhance your coding efficiency.

Whether you are just starting out or looking for a quick refresher, this guide offers a structured approach to quickly finding the needed information.

## Table of Contents

- [Python Cheat Sheet](#python-cheat-sheet)
  - [Variables and Data Types](#1-variables-and-data-types)
  - [Conditional Statements](#2-conditional-statements)
  - [Loops](#3-loops)
  - [Math Operations](#4-math-operations)
  - [Lists](#5-lists)
  - [Strings](#6-strings)
  - [Queues](#7-queues)
  - [Sets](#8-sets)
  - [Dictionaries](#9-dictionaries)
  - [Tuples](#10-tuples)
  - [Heaps](#11-heaps)
  - [Functions](#12-functions)
  - [Advanced Functions](#13-advanced-functions)
  - [Object-Oriented Programming (OOP)](#14-object-oriented-programming-oop)
  - [File Handling](#15-file-handling)
  - [Exception Handling](#16-exception-handling)
  - [List Comprehensions](#17-list-comprehensions)
  - [Generators and Iterators](#18-generators-and-iterators)
  - [Modules and Packages](#19-modules-and-packages)
  - [Common Libraries](#20-common-libraries)
  - [Regular Expressions](#21-regular-expressions)
  - [Useful Tips and Tricks](#22-useful-tips-and-tricks)

- [PHP Cheat Sheet](#php-cheat-sheet)
  - [Variables and Data Types](#1-variables-and-data-types-1)
  - [Strings](#2-strings)
  - [Arrays](#3-arrays)
  - [Control Structures](#4-control-structures)
  - [Loops](#5-loops)
  - [Functions](#6-functions)
  - [Object-Oriented Programming (OOP)](#7-object-oriented-programming-oop)
  - [File Handling](#8-file-handling)
  - [Error Handling](#9-error-handling)
  - [Common Libraries and Functions](#10-common-libraries-and-functions)
  - [Superglobals](#11-superglobals)
  - [Useful Tips and Tricks](#12-useful-tips-and-tricks)

- [C Programming Cheat Sheet](#3-c-programing-sheet)
  - [Basic Structure of a C Program](#1-basic-structure-of-a-c-program)
  - [Data Types](#2-data-types)
  - [Control Structures](#3-control-structures)
  - [Functions](#4-functions)
  - [Pointers](#5-pointers)
  - [Arrays](#6-arrays)
  - [Strings](#7-strings)
  - [Standard Input/Output](#8-standard-inputoutput)
  - [File Handling](#9-file-handling)
  - [Preprocessor Directives](#10-preprocessor-directives)
  - [Structs](#11-structs)
  - [Common Functions in `<string.h>`](#12-common-functions-in-stringh)
  - [Memory Management](#13-memory-management)
  - [Common Errors](#14-common-errors)
  - [Miscellaneous](#15-miscellaneous)

---

# Python Cheat Sheet

#### 1. **Variables and Data Types**

Variables are containers for storing data values. Python supports various data types such as integers, floats, strings, lists, dictionaries, tuples, and sets.

```python
# Integer, String, and Multiple Assignments
# Variables are dynamically typed in Python
n = 0  # Assign an integer value to n
print('n =', n)  # Output: n = 0

n = "abc"  # n is now a string
print('n =', n)  # Output: n = abc

# Multiple assignments
n, m = 0, "abc"  # n is an integer, m is a string
n, m, z = 0.125, "abc", False  # Multiple variables assigned different data types

# Incrementing values
n = n + 1  # Increment n by 1 (good)
n += 1     # Another way to increment n by 1 (good)
# n++ is invalid in Python (bad, will cause an error)

# None represents a null value (absence of value)
n = 4  # Assign an integer to n
n = None  # n is now None (no value)
print("n =", n)  # Output: n = None
```

#### 2. **Conditional Statements**

Conditional statements allow you to execute different code blocks based on certain conditions.

```python
# If statements don't need parentheses or curly braces
n = 1  # Initialize n to 1
if n > 2:  # If n is greater than 2
    n -= 1  # Subtract 1 from n
elif n == 2:  # Else if n equals 2
    n *= 2  # Multiply n by 2
else:  # Otherwise
    n += 2  # Add 2 to n

# Parentheses are needed for multi-line conditions.
# "and" is equivalent to "&&", "or" is equivalent to "||"
n, m = 1, 2  # Assign 1 to n and 2 to m
if ((n > 2 and
    n != m) or n == m):  # Multi-line condition using parentheses
    n += 1  # Increment n by 1
```

#### 3. **Loops**

Loops are used to execute a block of code repeatedly.

```python
# While Loop
n = 5  # Initialize n to 5
while n < 5:  # This condition is false, so the loop will not execute
    print(n)  # This line will not execute
    n += 1  # This line will not execute

# For loop from i = 0 to i = 4 (5 iterations)
for i in range(5):
    print(i)  # Output: 0, 1, 2, 3, 4

# For loop from i = 2 to i = 5 (4 iterations)
for i in range(2, 6):
    print(i)  # Output: 2, 3, 4, 5

# For loop from i = 5 to i = 2 (counts downwards)
for i in range(5, 1, -1):  # -1 indicates the decrement
    print(i)  # Output: 5, 4, 3, 2
```

#### 4. **Math Operations**

Basic math operations such as addition, subtraction, multiplication, and division.

```python
# Division in Python is floating-point by default
print(5 / 2)  # Output: 2.5

# Double slash performs floor division (rounds down)
print(5 // 2)  # Output: 2

# Negative numbers also round down in floor division
print(-3 // 2)  # Output: -2

# Workaround for rounding towards zero using int conversion
print(int(-3 / 2))  # Output: -1

# Modulus operation (remainder of division)
print(10 % 3)  # Output: 1

# Modulus with negative values
print(-10 % 3)  # Output: 2

# Using math.fmod for modulo operation consistent with other languages
import math
print(math.fmod(-10, 3))  # Output: -1

# Other math functions
print(math.floor(3 / 2))  # Output: 1 (rounds down)
print(math.ceil(3 / 2))  # Output: 2 (rounds up)
print(math.sqrt(2))  # Output: 1.414... (square root)
print(math.pow(2, 3))  # Output: 8.0 (2^3)

# Max and Min float values
print(float("inf"))  # Represents positive infinity
print(float("-inf"))  # Represents negative infinity

# Python handles large numbers natively
print(math.pow(2, 200))  # A very large number

# Comparison of large number with infinity
print(math.pow(2, 200) < float("inf"))  # Output: True
```

#### 5. **Lists**

Lists are mutable sequences used to store collections of items.

```python
# Arrays are called lists in Python
arr = [1, 2, 3]  # Create a list with 3 elements
print(arr)  # Output: [1, 2, 3]

# Lists can be used as a stack
arr.append(4)  # Add 4 to the end of the list
arr.append(5)  # Add 5 to the end of the list
print(arr)  # Output: [1, 2, 3, 4, 5]

arr.pop()  # Remove the last element (5)
print(arr)  # Output: [1, 2, 3, 4]

arr.insert(1, 7)  # Insert 7 at index 1
print(arr)  # Output: [1, 7, 2, 3, 4]

arr[0] = 0  # Change the first element to 0
arr[3] = 0  # Change the fourth element to 0
print(arr)  # Output: [0, 7, 2, 0, 4]

# Initialize a list of size n with a default value
n = 5
arr = [1] * n  # List of size 5 with all elements as 1
print(arr)  # Output: [1, 1, 1, 1, 1]
print(len(arr))  # Output: 5 (length of the list)

# Negative indexing: -1 refers to the last element
arr = [1, 2, 3]
print(arr[-1])  # Output: 3 (last element)

# Index -2 is the second-to-last element, etc.
print(arr[-2])  # Output: 2

# Slicing lists (sub-lists)
arr = [1, 2, 3, 4]
print(arr[1:3])  # Output: [2, 3] (from index 1 to 2)

# Slicing is non-inclusive of the last index
print(arr[0:4])  # Output: [1, 2, 3, 4]

# No out-of-bounds error when slicing
print(arr[0:10])  # Output: [1, 2, 3, 4]

# Unpacking list elements into variables
a, b, c = [1, 2, 3]
print(a, b, c)  # Output: 1 2 3

# Be careful with unpacking:
# a, b = [1, 2, 3]  # Error: too many values to unpack

# Loop through lists
nums = [1, 2, 3]

# Using index
for i in range(len(nums)):
    print(nums[i])  # Output: 1 2 3

# Without index
for n in nums:
    print(n)  # Output: 1 2 3

# With both index and value
for i, n in enumerate(nums):
    print(i, n)  # Output: 0 1, 1 2, 2 3

# Loop through multiple lists simultaneously with unpacking
nums1 = [1, 3, 5]
nums2 = [2, 4, 6]
for n1, n2 in zip(nums1, nums2):
    print(n1, n2)  # Output: 1 2, 3 4, 5 6

# Reversing a list
nums = [1, 2, 3]
nums.reverse()
print(nums)  # Output: [3, 2, 1]

# Sorting lists
arr = [5, 4, 7, 3, 8]
arr.sort()  # Sort in ascending order
print(arr)  # Output: [3, 4, 5, 7, 8]

arr.sort(reverse=True)  # Sort in descending order
print(arr)  # Output: [8, 7, 5, 4, 3]

arr = ["bob", "alice", "jane", "doe"]
arr.sort()  # Sort alphabetically
print(arr)  # Output: ['alice', 'bob', 'doe', 'jane']

# Custom sort (by length of string)
arr.sort(key=lambda x: len(x))
print(arr)  # Output: ['bob', 'doe', 'jane', 'alice']

# List comprehension to create a list
arr = [i for i in range(5)]  # List from 0 to 4
print(arr)  # Output: [0, 1, 2, 3, 4]

# 2-D lists (matrix)
arr = [[0] * 4 for i in range(4)]  # 4x4 matrix initialized with 0
print(arr)  # Output: [[0, 0, 0, 0], [0, 0, 0, 0], [0, 0, 0, 0], [0, 0, 0, 0]]
print(arr[0][0], arr[3][3])  # Output: 0 0

# Be careful with creating 2-D lists this way:
# arr = [[0] * 4] * 4  # This creates references to the same list, not independent lists
```

#### 6. **Strings**

Strings are sequences of characters used to store and manipulate text.

```python
# Strings are similar to lists (arrays of characters)
s = "abc"
print(s[0:2])  # Output: 'ab' (substring from index 0 to 1)

# Strings are immutable
# s[0] = "A"  # This will cause an error

# Concatenation creates a new string
s += "def"  # Appends "def" to s
print(s)  # Output: 'abcdef'

# Valid numeric strings can be converted to integers
print(int("123") + int("123"))  # Output: 246

# Numbers can also be converted to strings
print(str(123) + str(123))  # Output: '123123'

# Getting ASCII value of a character
print(ord("a"))  # Output: 97
print(ord("b"))  # Output: 98

# Combine a list of strings with a delimiter
strings = ["ab", "cd", "ef"]
print("".join(strings))  # Output: 'abcdef'
```

#### 7. **Queues**

Queues follow the First-In-First-Out (FIFO) principle.

```python
# Queue (double-ended queue) in Python using collections.deque
from collections import deque

queue = deque()  # Initialize an empty deque
queue.append(1)  # Add 1 to the right end
queue.append(2)  # Add 2 to the right end
print(queue)  # Output: deque([1, 2])

queue.popleft()  # Remove from the left end (FIFO)
print(queue)  # Output: deque([2])

queue.appendleft(1)  # Add 1 to the left end
print(queue)  # Output: deque([1, 2])

queue.pop()  # Remove from the right end
print(queue)  # Output: deque([1])
```

#### 8. **Sets**

Sets are unordered collections of unique elements.

```python
# HashSet
# Sets are collections of unique elements
mySet = set()  # Initialize an empty set

mySet.add(1)  # Add 1 to the set
mySet.add(2)  # Add 2 to the set
print(mySet)  # Output: {1, 2}
print(len(mySet))  # Output: 2 (number of elements in the set)

# Check if an element is in the set
print(1 in mySet)  # Output: True
print(2 in mySet)  # Output: True
print(3 in mySet)  # Output: False

mySet.remove(2)  # Remove 2 from the set
print(2 in mySet)  # Output: False

# Convert a list to a set (removes duplicates)
print(set([1, 2, 3]))  # Output: {1, 2, 3}

# Set comprehension (similar to list comprehension)
mySet = {i for i in range(5)}  # Creates a set with elements 0 to 4
print(mySet)  # Output: {0, 1, 2, 3, 4}
```

#### 9. **Dictionaries**

Dictionaries are collections of key-value pairs.

```python
# Dictionaries are collections of key-value pairs
myMap = {}  # Initialize an empty dictionary
myMap["alice"] = 88  # Add a key-value pair ("alice", 88)
myMap["bob"] = 77  # Add a key-value pair ("bob", 77)
print(myMap)  # Output: {'alice': 88, 'bob': 77}
print(len(myMap))  # Output: 2 (number of key-value pairs)

# Update the value for a key
myMap["alice"] = 80  # Change "alice" to 80
print(myMap["alice"])  # Output: 80

# Check if a key is in the dictionary
print("alice" in myMap)  # Output: True
myMap.pop("alice")  # Remove the key "alice"
print("alice" in myMap)  # Output: False

# Initialize a dictionary with key-value pairs
myMap = {"alice": 90, "bob": 70}
print(myMap)  # Output: {'alice': 90, 'bob': 70}

# Dictionary comprehension
myMap = {i: 2 * i for i in range(3)}  # Creates {0: 0, 1: 2, 2: 4}
print(myMap)  # Output: {0: 0, 1: 2, 2: 4}

# Looping through dictionaries
myMap = {"alice": 90, "bob": 70}
for key in myMap:  # Loop through keys
    print(key, myMap[key])  # Output: 'alice 90', 'bob 70'

for val in myMap.values():  # Loop through values
    print(val)  # Output: 90, 70

for key, val in myMap.items():  # Loop through key-value pairs
    print(key, val)  # Output: 'alice 90', 'bob 70'
```

#### 10. **Tuples**

Tuples are immutable ordered collections.

```python
# Tuples are like lists but immutable (cannot be modified)
tup = (1, 2, 3)  # Initialize a tuple
print(tup)  # Output: (1, 2, 3)
print(tup[0])  # Output: 1 (access by index)
print(tup[-1])  # Output: 3 (last element)

# Can't modify tuples
# tup[0] = 0  # This will cause an error

# Tuples can be used as keys in dictionaries or sets
myMap = {(1, 2): 3}  # Tuple as key
print(myMap[(1, 2)])  # Output: 3

mySet = set()  # Initialize an empty set
mySet.add((1, 2))  # Add a tuple to the set
print((1, 2) in mySet)  # Output: True

# Lists can't be keys in dictionaries
# myMap[[3, 4]] = 5  # This will cause an error
```

#### 11. **Heaps**

The `heapq` library provides heap-based priority queues.

```python
import heapq  # Import the heapq library

# Min heap implementation
minHeap = []  # Initialize an empty heap
heapq.heappush(minHeap, 3)  # Push 3 onto the heap
heapq.heappush(minHeap, 2)  # Push 2 onto the heap
heapq.heappush(minHeap, 4)  # Push 4 onto the heap

# The smallest element is always at index 0
print(minHeap[0])  # Output: 2

# Pop elements from the heap (always the smallest element)
while len(minHeap):
    print(heapq.heappop(minHeap))  # Output: 2, 3, 4

# Max heap is not directly supported; use negative values to simulate
maxHeap = []
heapq.heappush(maxHeap, -3)  # Push -3 onto the heap
heapq.heappush(maxHeap, -2)  # Push -2 onto the heap
heapq.heappush(maxHeap, -4)  # Push -4 onto the heap

# The largest element is now at index 0 (negated back to positive)
print(-1 * maxHeap[0])  # Output: 3

# Pop elements from the heap
while len(maxHeap):
    print(-1 * heapq.heappop(maxHeap))  # Output: 3, 2, 1

# Build a heap from an existing list
arr = [2, 1, 8, 4, 5]
heapq.heapify(arr)  # Transform the list into a heap
while arr:
    print(heapq.heappop(arr))  # Output: 1, 2, 4, 5, 8
```

#### 12. **Functions**
Define reusable blocks of code with `def`.

```python
# Define a function with parameters n and m
def myFunc(n, m):
    return n * m  # Return the product of n and m

print(myFunc(3, 4))  # Output: 12

# Nested functions have access to variables in the outer function
def outer(a, b):
    c = "c"  # Variable in outer function

    def inner():  # Inner function
        return a + b + c  # Access outer variables a, b, c
    return inner()

print(outer("a", "b"))  # Output: 'abc'

# Functions can modify objects but not reassign them unless using 'nonlocal' or 'global'
def double(arr, val):
    def helper():
        # Modifying a list (mutable object) works
        for i, n in enumerate(arr):
            arr[i] *= 2

        # This won't modify val outside helper's scope (val is local to helper)
        # val *= 2

        # This will modify val outside helper's scope (nonlocal variable)
        nonlocal val
        val *= 2
    helper()
    print(arr, val)

nums = [1, 2]
val = 3
double(nums, val)  # Output: [2, 4] 6
```

#### 13. **Advanced Functions**
Lambda functions and higher-order functions.

```python
# Lambda (anonymous) function
square = lambda x: x * x  # Define a lambda function to square a number
print(square(5))  # Output: 25

# Map and Filter
nums = [1, 2, 3, 4, 5]  # List of numbers
squared_nums = list(map(lambda x: x * x, nums))  # Apply lambda to square each element
even_nums = list(filter(lambda x: x % 2 == 0, nums))  # Filter even numbers
print(squared_nums)  # Output: [1, 4, 9, 16, 25]
print(even_nums)  # Output: [2, 4]

```

#### 14. **Object-Oriented Programming (OOP)**
Python supports OOP with classes and objects.

```python
# Define a class in Python
class MyClass:
    # Constructor method
    def __init__(self, nums):
        # Initialize member variables
        self.nums = nums
        self.size = len(nums)

    # Method to get the length of the nums list
    def getLength(self):
        return self.size

    # Method that calls another method
    def getDoubleLength(self):
        return 2 * self.getLength()

# Instantiate an object of MyClass
myObj = MyClass([1, 2, 3])
print(myObj.getLength())  # Output: 3
print(myObj.getDoubleLength())  # Output: 6
```

#### 15. **File Handling**
Read from and write to files in Python.

```python
# Reading from a file
with open('file.txt', 'r') as file:  # Open file in read mode
    content = file.read()  # Read the entire content

# Writing to a file
with open('file.txt', 'w') as file:  # Open file in write mode
    file.write("Hello, world!")  # Write to the file
```

#### 16. **Exception Handling**
Handle errors gracefully using `try`, `except`, and `finally`.

```python
# Handle exceptions using try-except-finally
try:
    result = 10 / 0  # This will raise a ZeroDivisionError
except ZeroDivisionError as e:  # Handle the specific error
    print(f"Error: {e}")  # Output: Error: division by zero
finally:
    print("This will always execute.")  # Output: This will always execute.
```

#### 17. **List Comprehensions**
Concise way to create lists.

```python
# List comprehension to create a list of squares
squares = [x * x for x in range(10)]  # Squares from 0 to 9
# List comprehension to filter even numbers
evens = [x for x in range(10) if x % 2 == 0]  # Evens from 0 to 9
print(squares)  # Output: [0, 1, 4, 9, 16, 25, 36, 49, 64, 81]
print(evens)  # Output: [0, 2, 4, 6, 8]
```

#### 18. **Generators and Iterators**
Use `yield` for generators and `iter()` for iterators.

```python
# Generator function using 'yield'
def my_generator():
    for i in range(5):  # Loop from 0 to 4
        yield i  # Yield each value one by one

gen = my_generator()  # Create a generator object
print(next(gen))  # Output: 0
print(next(gen))  # Output: 1
```

#### 19. **Modules and Packages**
Organize your code with modules and packages.

```python
# Importing a module
import math  # Import math module
print(math.sqrt(16))  # Output: 4.0 (square root of 16)

# Importing specific functions from a module
from math import pi, sqrt
print(pi, sqrt(25))  # Output: 3.141592653589793 5.0
```

#### 20. **Common Libraries**
Examples of commonly used Python libraries.

```python
# Common Python libraries

# Working with date and time
import datetime
print(datetime.datetime.now())  # Output: current date and time

# Generating random numbers
import random
print(random.randint(1, 10))  # Output: random integer between 1 and 10

# Interacting with the operating system
import os
print(os.getcwd())  # Output: current working directory
```

#### 21. **Regular Expressions**
Pattern matching with the `re` module.

```python
# Regular expressions for pattern matching
import re

pattern = r'\b[A-Za-z]+\b'  # Pattern to match whole words (letters only)
text = "Hello world!"
matches = re.findall(pattern, text)  # Find all matches in text
print(matches)  # Output: ['Hello', 'world']
```

#### 22. **Useful Tips and Tricks**
Handy tips for more Pythonic code.

```python
# Swap two variables
a, b = 1, 2  # Initialize a and b
a, b = b, a  # Swap values
print(a, b)  # Output: 2 1

# Merging two dictionaries
dict1 = {'a': 1}  # First dictionary
dict2 = {'b': 2}  # Second dictionary
merged = {**dict1, **dict2}  # Merge dictionaries
print(merged)  # Output: {'a': 1, 'b': 2}

# Using enumerate to get index and value
letters = ['a', 'b', 'c']  # List of letters
for index, letter in enumerate(letters):  # Enumerate returns index and value
    print(index, letter)  # Output: 0 'a', 1 'b', 2 'c'
```

---

# PHP Cheat Sheet

### 1. **Variables and Data Types**

PHP supports various data types such as integers, floats, strings, booleans, arrays, and objects.

```php
<?php
$intVar = 42; // Integer variable
$floatVar = 3.14; // Float variable
$stringVar = "Hello, World!"; // String variable
$boolVar = true; // Boolean variable
$arrayVar = [1, 2, 3]; // Indexed array
$assocArray = ["key" => "value"]; // Associative array with key-value pairs
$nullVar = null; // Null value, similar to Python's None
?>
```

### 2. **Strings**

Strings are sequences of characters. Common operations include concatenation, length, and case conversion.

```php
<?php
$str = "Hello, World!"; // String initialization
echo strlen($str); // Get the length of the string
echo str_replace("World", "PHP", $str); // Replace "World" with "PHP" in the string
echo strtoupper($str); // Convert string to uppercase
echo strtolower($str); // Convert string to lowercase
echo substr($str, 0, 5); // Extract substring from index 0 to 5
?>
```

### 3. **Arrays**

Arrays are used to store multiple values in a single variable.

```php
<?php
$array = [1, 2, 3]; // Indexed array
array_push($array, 4); // Add 4 to the end of the array
array_pop($array); // Remove the last element from the array
array_unshift($array, 0); // Add 0 to the beginning of the array
array_shift($array); // Remove the first element from the array

$assocArray = ["name" => "John", "age" => 30]; // Associative array with named keys
echo $assocArray["name"]; // Access value by key, outputs: "John"
?>
```

### 4. **Control Structures**

Control structures are used to make decisions in code.

```php
<?php
// If-Else Statement
if ($x > 0) { // If x is greater than 0
    echo "Positive"; // Output "Positive"
} elseif ($x < 0) { // Else if x is less than 0
    echo "Negative"; // Output "Negative"
} else { // Else when x is equal to 0
    echo "Zero"; // Output "Zero"
}

// Switch Statement
$color = "red"; // Color variable
switch ($color) { // Switch case on the variable $color
    case "red":
        echo "Color is red";
        break; // Break to prevent falling through
    case "blue":
        echo "Color is blue";
        break;
    default: // Default case when no other cases match
        echo "Color is not red or blue";
}
?>
```

### 5. **Loops**

Loops execute a block of code repeatedly as long as a specified condition is met.

```php
<?php
// For Loop
for ($i = 0; $i < 5; $i++) { // Loop from 0 to 4
    echo $i; // Output the current value of i
}

// While Loop
$i = 0;
while ($i < 5) { // Continue looping while i is less than 5
    echo $i; // Output the current value of i
    $i++; // Increment i by 1
}

// Foreach Loop
$colors = ["red", "green", "blue"]; // Array of colors
foreach ($colors as $color) { // Loop through each color
    echo $color; // Output the current color
}
?>
```

### 6. **Functions**

Functions are reusable blocks of code that perform a specific task.

```php
<?php
function greet($name) { // Function definition with parameter $name
    return "Hello, $name!"; // Return a greeting message
}

echo greet("Alice"); // Call the function and output the result, outputs: "Hello, Alice!"

function add($a, $b = 10) { // Function with a default parameter value for $b
    return $a + $b; // Return the sum of $a and $b
}

echo add(5); // Output: 15, since $b defaults to 10
?>
```

### 7. **Object-Oriented Programming (OOP)**

OOP is a programming paradigm based on the concept of objects that have properties and methods.

```php
<?php
class Car { // Class definition
    public $color; // Public property
    public $model; // Public property

    public function __construct($color, $model) { // Constructor method
        $this->color = $color; // Initialize color property
        $this->model = $model; // Initialize model property
    }

    public function message() { // Method to return a message about the car
        return "The car is a $this->color $this->model."; // Use class properties in a string
    }
}

$myCar = new Car("red", "Toyota"); // Creating a new instance of Car
echo $myCar->message(); // Call the message method, outputs: "The car is a red Toyota."
?>
```

### 8. **File Handling**

PHP provides built-in functions for reading and writing files.

```php
<?php
// Reading a file
$file = fopen("file.txt", "r"); // Open the file in read mode
while (!feof($file)) { // Loop until end of file
    echo fgets($file); // Read and output each line of the file
}
fclose($file); // Close the file

// Writing to a file
$file = fopen("file.txt", "w"); // Open the file in write mode
fwrite($file, "Hello, PHP!"); // Write a string to the file
fclose($file); // Close the file
?>
```

### 9. **Error Handling**

Error handling is crucial for making programs robust and fault-tolerant.

```php
<?php
try { // Try block to execute potentially error-prone code
    // Code that may throw an exception
    if (!file_exists("file.txt")) { // Check if the file does not exist
        throw new Exception("File not found."); // Throw an exception if the file is not found
    }
} catch (Exception $e) { // Catch block to handle exceptions
    echo "Error: " . $e->getMessage(); // Output the exception message
}
?>
```

### 10. **Common Libraries and Functions**

PHP provides many built-in functions for handling strings, arrays, files, and more.

```php
<?php
// Date and Time
echo date('Y-m-d H:i:s'); // Output the current date and time

// Random Numbers
echo rand(1, 100); // Generate a random number between 1 and 100

// Regular Expressions
$string = "Hello, World!";
if (preg_match("/world/i", $string)) { // Case-insensitive match for 'world' in the string
    echo "Match found!"; // Output if a match is found
}
?>
```

### 11. **Superglobals**

Superglobals are built-in variables that are always accessible, regardless of scope.

```php
<?php
// $_GET and $_POST are used to collect form data
$name = $_GET['name']; // Get data from URL parameters
echo "Name from GET: $name";

// $_SERVER contains information about headers, paths, and script locations
echo $_SERVER['PHP_SELF']; // Outputs the filename of the currently executing script
echo $_SERVER['SERVER_NAME']; // Outputs the name of the server

// $_SESSION is used to manage user sessions
session_start(); // Start a new session
$_SESSION['username'] = 'JohnDoe'; // Set a session variable
echo $_SESSION['username']; // Access the session variable

// $_COOKIE is used to manage cookies
setcookie("user", "John", time() + (86400 * 30), "/"); // Set a cookie named "user"
echo $_COOKIE['user']; // Access the cookie named "user"
?>
```

### 12. **Useful Tips and Tricks**

Tips and tricks to enhance coding efficiency and readability.

```php
<?php
// Null Coalescing Operator
$username = $_GET['user'] ?? 'guest'; // If 'user' is not set in GET request, default to 'guest'

// Ternary Operator
$isAdmin = ($role == 'admin') ? true : false; // Check if role is 'admin', assign true or false

// Spaceship Operator
echo 1 <=> 1; // Output: 0 (equal)
echo 1 <=> 2; // Output: -1 (less than)
echo 2 <=> 1; // Output: 1 (greater than)
?>
```

# C Programming Cheat Sheet

#### 1. **Basic Structure of a C Program**
```c
#include <stdio.h>  // Preprocessor directive for standard I/O

int main() {
    // Your code here
    return 0;  // Exit status of the program
}
```

#### 2. **Data Types**
- **Basic Data Types**
  - `int` - Integer (e.g., `int x = 5;`)
  - `float` - Floating-point number (e.g., `float y = 3.14;`)
  - `double` - Double-precision floating-point (e.g., `double z = 3.14159;`)
  - `char` - Character (e.g., `char c = 'A';`)

- **Derived Data Types**
  - `array` - Collection of elements of the same type (e.g., `int arr[10];`)
  - `pointer` - Stores the address of a variable (e.g., `int *p;`)
  - `struct` - Collection of variables of different types (e.g., `struct Point { int x, y; };`)

#### 3. **Control Structures**
- **Conditional Statements**
  ```c
  if (condition) {
      // Code to execute if condition is true
  } else {
      // Code to execute if condition is false
  }
  ```

- **Switch Case**
  ```c
  switch (variable) {
      case 1:
          // Code to execute for case 1
          break;
      case 2:
          // Code to execute for case 2
          break;
      default:
          // Code to execute if no case matches
  }
  ```

- **Loops**
  - **For Loop**
    ```c
    for (int i = 0; i < 10; i++) {
        // Code to execute
    }
    ```
  - **While Loop**
    ```c
    while (condition) {
        // Code to execute
    }
    ```
  - **Do-While Loop**
    ```c
    do {
        // Code to execute
    } while (condition);
    ```

#### 4. **Functions**
- **Function Definition**
  ```c
  return_type function_name(parameters) {
      // Code to execute
      return value;  // Optional, depending on return_type
  }
  ```

- **Function Declaration (Prototype)**
  ```c
  return_type function_name(parameters);
  ```

- **Function Call**
  ```c
  function_name(arguments);
  ```

#### 5. **Pointers**
- **Definition and Usage**
  ```c
  int *ptr;  // Declares a pointer to an integer
  int value = 5;
  ptr = &value;  // `ptr` now holds the address of `value`
  printf("%d", *ptr);  // Dereferencing `ptr` gives the value stored at the address
  ```

#### 6. **Arrays**
- **One-Dimensional Array**
  ```c
  int arr[5] = {1, 2, 3, 4, 5};  // Declares and initializes an array of 5 integers
  ```
- **Two-Dimensional Array**
  ```c
  int matrix[3][3];  // Declares a 3x3 matrix
  ```

#### 7. **Strings**
- **Character Array**
  ```c
  char str[] = "Hello, World!";  // Declares a string
  ```

#### 8. **Standard Input/Output**
- **Printing to Console**
  ```c
  printf("Hello, World!");  // Prints to console
  printf("%d", x);  // Prints an integer
  printf("%f", y);  // Prints a float
  ```
- **Reading from Console**
  ```c
  scanf("%d", &x);  // Reads an integer from user input
  scanf("%f", &y);  // Reads a float from user input
  ```

#### 9. **File Handling**
- **Opening a File**
  ```c
  FILE *file = fopen("filename.txt", "r");  // Opens a file for reading
  ```
- **Reading/Writing to a File**
  ```c
  fprintf(file, "Hello, World!");  // Writes to a file
  fscanf(file, "%s", str);  // Reads from a file
  ```
- **Closing a File**
  ```c
  fclose(file);  // Closes the file
  ```

#### 10. **Preprocessor Directives**
- **Common Directives**
  ```c
  #include <stdio.h>  // Includes standard input/output library
  #define PI 3.14159  // Defines a constant
  ```

#### 11. **Structs**
- **Defining a Structure**
  ```c
  struct Person {
      char name[50];
      int age;
  };
  ```

- **Using a Structure**
  ```c
  struct Person person1;
  strcpy(person1.name, "John");
  person1.age = 30;
  ```

#### 12. **Common Functions in `<string.h>`**
- `strcpy(destination, source);` - Copy a string
- `strlen(string);` - Get the length of a string
- `strcmp(string1, string2);` - Compare two strings
- `strcat(destination, source);` - Concatenate two strings

#### 13. **Memory Management**
- `malloc(size);` - Allocates memory dynamically
- `free(pointer);` - Frees dynamically allocated memory

#### 14. **Common Errors**
- **Segmentation Fault** - Accessing memory not allocated to the program
- **Syntax Errors** - Incorrect syntax usage
- **Logical Errors** - Errors in program logic

#### 15. **Miscellaneous**
- **`sizeof` Operator**
  ```c
  int size = sizeof(int);  // Returns size of data type in bytes
  ```
- **Type Casting**
  ```c
  float x = 3.14;
  int y = (int)x;  // Type casts `x` to an integer
  ```
