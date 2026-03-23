# Python Basics for LeetCode: Complete Crash Course
## Week 1: Python Fundamentals (Learn These First!)

---

## DAY 1-2: Variables & Data Types (30 mins each day)

### What are Variables?
Think of variables as **containers that hold values**. Like labeled boxes.

```python
# Creating variables (assigning values)
name = "Alice"           # String (text)
age = 25                 # Integer (whole number)
height = 5.8             # Float (decimal number)
is_student = True        # Boolean (True/False)

# Printing to see output
print(name)              # Output: Alice
print(age)               # Output: 25
print(age + 10)          # Output: 35
```

### Common Data Types

| Type | Example | Use Case |
|------|---------|----------|
| **String (str)** | "Hello", "Python" | Text/words |
| **Integer (int)** | 5, -10, 0 | Whole numbers |
| **Float (float)** | 3.14, -2.5 | Decimal numbers |
| **Boolean (bool)** | True, False | Yes/No conditions |
| **List (list)** | [1, 2, 3, "a"] | Multiple items |
| **Dictionary (dict)** | {"name": "Ali", "age": 25} | Key-value pairs |

### Practice: Variables
```python
# Try these yourself:
favorite_color = "blue"
favorite_number = 42
temperature = 98.6
is_raining = False

print(favorite_number * 2)  # What's the output?
print(favorite_color.upper())  # What about this?
```

---

## DAY 3-4: Lists - Your Most Important Data Structure (30 mins each)

### What is a List?
An **ordered collection of items**. Think of a shopping list.

```python
# Creating lists
fruits = ["apple", "banana", "orange"]
numbers = [10, 20, 30, 40, 50]
mixed = [1, "hello", 3.14, True]

# Accessing items (IMPORTANT - counting starts at 0!)
print(fruits[0])         # Output: apple
print(fruits[1])         # Output: banana
print(fruits[-1])        # Output: orange (last item)

# Finding length
print(len(fruits))       # Output: 3

# Adding items
fruits.append("grape")
print(fruits)            # Output: ["apple", "banana", "orange", "grape"]

# Removing items
fruits.remove("banana")
print(fruits)            # Output: ["apple", "orange", "grape"]

# Checking if item exists
print("apple" in fruits) # Output: True
```

### List Operations (YOU WILL USE THESE A LOT!)
```python
nums = [1, 2, 3, 4, 5]

# Loop through items
for num in nums:
    print(num)

# Change an item
nums[0] = 100
print(nums)              # Output: [100, 2, 3, 4, 5]

# Get multiple items (slicing)
print(nums[1:3])         # Output: [2, 3] (items at index 1,2)
print(nums[:3])          # Output: [100, 2, 3] (first 3 items)
```

### Practice: Lists
```python
# Create a list of 5 numbers
my_list = [10, 20, 30, 40, 50]

# Print the first item
# Print the last item  
# Add 60 to the list
# Check if 30 is in the list
# Get items from index 1 to 3
```

---

## DAY 5-6: Dictionaries - Key-Value Storage (30 mins each)

### What is a Dictionary?
Like a real dictionary - you look up a **key** to find its **value**.

```python
# Creating a dictionary
person = {
    "name": "Alice",
    "age": 25,
    "city": "New York",
    "is_student": False
}

# Accessing values using keys
print(person["name"])    # Output: Alice
print(person["age"])     # Output: 25

# Adding new key-value pair
person["email"] = "alice@example.com"
print(person)

# Changing a value
person["age"] = 26
print(person["age"])     # Output: 26

# Checking if key exists
print("name" in person)  # Output: True
print("phone" in person) # Output: False

# Getting all keys and values
print(person.keys())     # Output: dict_keys(['name', 'age', ...])
print(person.values())   # Output: dict_values(['Alice', 25, ...])
```

### Practice: Dictionaries
```python
# Create a dictionary for a student
student = {
    "name": "Bob",
    "roll_number": 101,
    "marks": 85
}

# Print name
# Add a new key "subject" with value "Math"
# Change marks to 90
# Check if "phone" exists in dictionary
```

---

## DAY 7: IF-ELSE Statements - Making Decisions (30 mins)

### What is if-else?
Program makes **different decisions** based on conditions.

```python
# Simple if
age = 20
if age >= 18:
    print("You are an adult")

# if-else (pick one or other)
score = 45
if score >= 50:
    print("You passed!")
else:
    print("You failed.")

# if-elif-else (multiple conditions)
grade = 75
if grade >= 90:
    print("Grade: A")
elif grade >= 80:
    print("Grade: B")
elif grade >= 70:
    print("Grade: C")
else:
    print("Grade: F")

# Combining conditions with AND, OR
age = 25
has_license = True

if age >= 18 and has_license:
    print("You can drive!")

temperature = 15
if temperature < 0 or temperature > 30:
    print("Stay indoors")
else:
    print("Go outside")
```

### Comparison Operators (CRITICAL FOR CODING!)
```python
# ==  equals
# !=  not equals
# >   greater than
# <   less than
# >=  greater or equal
# <=  less or equal

5 == 5          # True
5 != 3          # True
10 > 5          # True
3 < 8           # True
"hello" == "hello"  # True
```

### Practice: if-else
```python
# Write code for:
# 1. Check if number is positive, negative, or zero
# 2. Check if person is eligible to vote (age >= 18)
# 3. Check if temperature is cold (<0), normal, or hot (>30)
```

---

# WEEK 2: Loops - Repeating Code

---

## DAY 8-9: For Loops (30 mins each)

### What is a For Loop?
**Repeat something** multiple times without writing the same code again.

```python
# Loop through numbers
for i in range(5):
    print(i)
# Output: 0, 1, 2, 3, 4

# Loop through a list
fruits = ["apple", "banana", "orange"]
for fruit in fruits:
    print(fruit)
# Output: apple, banana, orange

# Loop with custom range
for i in range(1, 6):
    print(i)
# Output: 1, 2, 3, 4, 5

# Loop with step
for i in range(0, 10, 2):
    print(i)
# Output: 0, 2, 4, 6, 8
```

### Practical Examples
```python
# Sum all numbers in a list
numbers = [1, 2, 3, 4, 5]
total = 0
for num in numbers:
    total = total + num
print(total)  # Output: 15

# Count how many items
items = ["a", "b", "c", "d"]
count = 0
for item in items:
    count = count + 1
print(count)  # Output: 4

# Double each number
numbers = [1, 2, 3, 4]
doubled = []
for num in numbers:
    doubled.append(num * 2)
print(doubled)  # Output: [2, 4, 6, 8]
```

### Practice: For Loops
```python
# 1. Print numbers from 1 to 10
# 2. Sum all numbers from 1 to 100
# 3. Find the largest number in a list
# 4. Count how many numbers are greater than 5 in [3, 8, 1, 9, 2, 7]
```

---

## DAY 10: While Loops (30 mins)

### What is a While Loop?
Repeat **until a condition becomes false**.

```python
# Simple while loop
count = 0
while count < 5:
    print(count)
    count = count + 1
# Output: 0, 1, 2, 3, 4

# Another example
num = 10
while num > 0:
    print(num)
    num = num - 1
# Output: 10, 9, 8, 7, ..., 1

# Practical example - finding a number
target = 42
guess = 0
while guess != target:
    guess = guess + 1
    if guess == target:
        print(f"Found it! The number is {guess}")
```

### For vs While - When to Use?
```python
# Use FOR when you know how many times to repeat
for i in range(5):
    print(i)

# Use WHILE when you repeat until a condition is met
while user_input != "quit":
    user_input = input("Type 'quit' to exit: ")
```

---

## DAY 11-12: Practice & Consolidation (30 mins each)

### Combined Practice Problems

```python
# PROBLEM 1: Find the sum of all even numbers in a list
def sum_evens(numbers):
    total = 0
    for num in numbers:
        if num % 2 == 0:  # % is modulo (remainder)
            total = total + num
    return total

print(sum_evens([1, 2, 3, 4, 5, 6]))  # Output: 12

# PROBLEM 2: Reverse a string
def reverse_string(text):
    reversed_text = ""
    for char in text:
        reversed_text = char + reversed_text
    return reversed_text

print(reverse_string("hello"))  # Output: olleh

# PROBLEM 3: Find duplicate in a list
def has_duplicate(nums):
    for i in range(len(nums)):
        for j in range(i + 1, len(nums)):
            if nums[i] == nums[j]:
                return True
    return False

print(has_duplicate([1, 2, 3, 2]))  # Output: True

# PROBLEM 4: Find if list has target sum pair
def has_pair_sum(nums, target):
    seen = {}
    for num in nums:
        complement = target - num
        if complement in seen:
            return True
        seen[num] = True
    return False

print(has_pair_sum([1, 2, 3, 4, 5], 7))  # Output: True (3+4=7)
```

---

# WEEK 3-4: Functions & Introduction to Problem Solving

---

## DAY 13-14: Functions (30 mins each)

### What is a Function?
A **reusable block of code** that does one specific task.

```python
# Define a function
def greet(name):
    print(f"Hello, {name}!")

# Call the function
greet("Alice")  # Output: Hello, Alice!
greet("Bob")    # Output: Hello, Bob!

# Function that returns a value
def add(a, b):
    return a + b

result = add(5, 3)
print(result)  # Output: 8

# Function with multiple parameters
def calculate_grade(score):
    if score >= 90:
        return "A"
    elif score >= 80:
        return "B"
    elif score >= 70:
        return "C"
    else:
        return "F"

print(calculate_grade(85))  # Output: B

# Function with default parameter
def power(base, exponent=2):
    return base ** exponent

print(power(5))      # Output: 25 (5^2)
print(power(5, 3))   # Output: 125 (5^3)
```

### Important Function Concepts
```python
# RETURN statement - function gives you a value back
def multiply(a, b):
    result = a * b
    return result

answer = multiply(4, 5)
print(answer)  # Output: 20

# Functions can call other functions
def square(num):
    return multiply(num, num)

print(square(5))  # Output: 25

# Functions can return multiple values
def get_min_max(nums):
    return min(nums), max(nums)

minimum, maximum = get_min_max([3, 1, 4, 1, 5])
print(minimum, maximum)  # Output: 1, 5
```

---

## DAY 15-16: Common String Methods (You'll Use These!) (30 mins)

```python
# String is a sequence of characters
text = "Hello World"

# Length
print(len(text))  # Output: 11

# Change case
print(text.upper())      # Output: HELLO WORLD
print(text.lower())      # Output: hello world
print(text.title())      # Output: Hello World

# Find and replace
print(text.find("World"))      # Output: 6 (position)
print(text.replace("World", "Python"))  # Output: Hello Python

# Check conditions
print(text.startswith("Hello"))  # Output: True
print(text.endswith("World"))    # Output: True
print("o" in text)               # Output: True

# Split and join
words = text.split()             # Output: ["Hello", "World"]
joined = " ".join(words)         # Output: "Hello World"

# Strip whitespace
messy = "  Hello  "
print(messy.strip())   # Output: "Hello"
```

---

## DAY 17-18: Real LeetCode-Style Problems in Python (30 mins)

### PROBLEM 1: Two Sum (EASIEST)
```python
# Problem: Find two numbers that add up to target
# Example: [2, 7, 11, 15], target = 9 → [0, 1]

def twoSum(nums, target):
    seen = {}
    for i in range(len(nums)):
        complement = target - nums[i]
        if complement in seen:
            return [seen[complement], i]
        seen[nums[i]] = i
    return []

# Test
print(twoSum([2, 7, 11, 15], 9))  # Output: [0, 1]
print(twoSum([3, 2, 4], 6))       # Output: [1, 2]
```

### PROBLEM 2: Palindrome (EASY)
```python
# Problem: Check if number reads same forwards & backwards
# Example: 121 → True, 123 → False

def is_palindrome(n):
    # Convert to string and reverse it
    text = str(n)
    reversed_text = text[::-1]  # Slicing trick!
    return text == reversed_text

# Test
print(is_palindrome(121))   # Output: True
print(is_palindrome(123))   # Output: False
```

### PROBLEM 3: Contains Duplicate (EASY)
```python
# Problem: Check if array has duplicate values
# Example: [1, 2, 3, 1] → True, [1, 2, 3] → False

def contains_duplicate(nums):
    seen = set()
    for num in nums:
        if num in seen:
            return True
        seen.add(num)
    return False

# Test
print(contains_duplicate([1, 2, 3, 1]))  # Output: True
print(contains_duplicate([1, 2, 3]))     # Output: False
```

---

## DAY 19-20: Advanced Concepts (Sets & String Slicing)

### Sets - Unique Collections
```python
# Set - collection with NO duplicates
numbers = {1, 2, 3, 3, 4, 4, 5}
print(numbers)  # Output: {1, 2, 3, 4, 5}

# Operations
print(1 in numbers)  # Output: True
numbers.add(6)
numbers.remove(1)

# Convert list to set to remove duplicates
nums = [1, 1, 2, 2, 3, 3]
unique = set(nums)
print(unique)  # Output: {1, 2, 3}
```

### String Slicing - Extract Parts of Strings
```python
text = "Python"

# text[start:end] - gets characters from start to end-1
print(text[0:2])    # Output: "Py"
print(text[2:6])    # Output: "thon"
print(text[:3])     # Output: "Pyt" (from beginning)
print(text[3:])     # Output: "hon" (to end)
print(text[-3:])    # Output: "hon" (last 3 characters)
print(text[::-1])   # Output: "nohtyP" (REVERSE!)

# Useful for problems
word = "hello"
print(word[::-1])   # Output: "olleh"
```

---

## DAY 21-22: Consolidation Week - Review Everything (30 mins)

### Quick Review Checklist
- [ ] Create and use variables
- [ ] Work with lists (add, remove, access items)
- [ ] Use dictionaries (add, access, check keys)
- [ ] Write if-else statements
- [ ] Use for and while loops
- [ ] Create and call functions
- [ ] Use string methods
- [ ] Understand sets
- [ ] Use string slicing

### Mini Project: Password Validator
```python
def is_valid_password(password):
    # At least 8 characters
    if len(password) < 8:
        return False
    
    # Has at least one number
    has_number = False
    for char in password:
        if char.isdigit():
            has_number = True
            break
    
    if not has_number:
        return False
    
    # Has at least one uppercase letter
    has_upper = False
    for char in password:
        if char.isupper():
            has_upper = True
            break
    
    return has_upper

# Test
print(is_valid_password("Test1234"))     # Output: True
print(is_valid_password("test1234"))     # Output: False
print(is_valid_password("Test"))         # Output: False
```

---

## KEY PYTHON TRICKS FOR LEETCODE

```python
# 1. len() - get length
len([1, 2, 3])  # 3
len("hello")    # 5

# 2. range() - create sequence
range(5)        # 0, 1, 2, 3, 4
range(1, 5)     # 1, 2, 3, 4
range(0, 10, 2) # 0, 2, 4, 6, 8

# 3. in operator - check membership
3 in [1, 2, 3]  # True
"a" in "apple"  # True

# 4. append() - add to list
nums = [1, 2]
nums.append(3)  # [1, 2, 3]

# 5. Indexing & slicing
text = "hello"
text[0]     # "h"
text[-1]    # "o"
text[1:3]   # "el"
text[::-1]  # "olleh" (reverse)

# 6. Loops
for i in range(5):
    print(i)

for item in [1, 2, 3]:
    print(item)

# 7. Conditions
if x > 5:
    print("big")
elif x > 2:
    print("medium")
else:
    print("small")

# 8. Functions
def my_function(parameter):
    return parameter * 2

# 9. f-strings (print with variables)
name = "Alice"
age = 25
print(f"My name is {name} and I'm {age}")

# 10. List comprehension (advanced, learn later)
squares = [x**2 for x in range(5)]  # [0, 1, 4, 9, 16]
```

---

# WEEK 4: Transition to LeetCode

## DAY 23: Your First Easy Problems

### Problem 1: Running Sum of 1d Array
```python
def runningSum(nums):
    result = []
    total = 0
    for num in nums:
        total = total + num
        result.append(total)
    return result

# Test
print(runningSum([1, 2, 3, 4]))  # Output: [1, 3, 6, 10]
print(runningSum([3, 1, 2, 10, 1]))  # Output: [3, 4, 6, 16, 17]
```

### Problem 2: Richest Customer Wealth
```python
def maximumWealth(accounts):
    max_wealth = 0
    for account in accounts:
        wealth = 0
        for amount in account:
            wealth = wealth + amount
        if wealth > max_wealth:
            max_wealth = wealth
    return max_wealth

# Test
print(maximumWealth([[1, 2, 3], [3, 2, 1]]))  # Output: 6
```

### Problem 3: Palindrome Number
```python
def isPalindrome(n):
    text = str(n)
    return text == text[::-1]

# Test
print(isPalindrome(121))  # Output: True
print(isPalindrome(123))  # Output: False
```

---

## DAY 24-25: More Easy Problems

### Problem 4: Valid Anagram
```python
def isAnagram(s, t):
    # Two strings are anagrams if they have same characters
    return sorted(s) == sorted(t)

# Alternative approach
def isAnagram(s, t):
    if len(s) != len(t):
        return False
    
    char_count = {}
    for char in s:
        char_count[char] = char_count.get(char, 0) + 1
    
    for char in t:
        if char not in char_count:
            return False
        char_count[char] = char_count[char] - 1
        if char_count[char] < 0:
            return False
    
    return True

# Test
print(isAnagram("anagram", "nagaram"))  # Output: True
print(isAnagram("rat", "car"))          # Output: False
```

### Problem 5: Contains Duplicate (Now YOU know this!)
```python
def containsDuplicate(nums):
    seen = set()
    for num in nums:
        if num in seen:
            return True
        seen.add(num)
    return False

# Test
print(containsDuplicate([1, 2, 3, 1]))  # Output: True
```

---

## DAY 26-28: Practice & Review

### Your Daily Routine (After This Guide)
1. **5 mins**: Read the problem carefully (2-3 times)
2. **10 mins**: Think about solution on paper
3. **15 mins**: Write the code
4. **10 mins**: Test with examples
5. **15 mins**: Look at discussion if stuck
6. **5 mins**: Note down any new patterns

### Key Takeaway
- **Understand first, code second**
- **Test manually before submitting**
- **Read solutions to learn patterns**
- **Practice consistently**

---

## QUICK REFERENCE SHEET

```python
# DATA STRUCTURES
list = [1, 2, 3]                    # Ordered, changeable
dict = {"key": "value"}             # Key-value pairs
set = {1, 2, 3}                     # Unique items
tuple = (1, 2, 3)                   # Ordered, unchangeable

# STRING OPERATIONS
text.upper()                        # UPPERCASE
text.lower()                        # lowercase
text.strip()                        # Remove spaces
text.split()                        # Split by spaces
text[::-1]                          # Reverse
text[0]                             # First character
text[-1]                            # Last character

# LIST OPERATIONS
list.append(4)                      # Add item
list.remove(2)                      # Remove item
list[0]                             # First item
list[-1]                            # Last item
list[1:3]                           # Items 1-2
len(list)                           # Length
2 in list                           # Check membership

# LOOPS
for i in range(5):                  # 0 to 4
for item in list:                   # Each item
while condition:                    # Until condition false

# CONDITIONS
if x > 5:
elif x > 2:
else:

# FUNCTIONS
def function_name(param):
    return result
```

---

**Now you're ready! After completing this guide, go solve your first LeetCode problem! 🚀**
