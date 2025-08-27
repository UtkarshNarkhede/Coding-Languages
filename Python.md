# 🐍 Python Cheat Sheet

A quick reference guide for Python **data types**, their **common methods**, and **key points**.  
Useful for **GATE DA, coding interviews, and revision**.

---

**Basic Data Types**
```
- int → whole numbers (`x = 10`)
- float → decimal numbers (`y = 3.14`)
-    we can limite the decimal points of float as:
-    round(3.14159, 2)# 3.14
- string → group of characters(`Utkarsh`)
- complex → numbers with real & imaginary part (`z = 2+3j`)

type(10)         # int
int(3.9)         # 3
float(5)         # 5.0
complex(2, 3)    # (2+3j)
abs(-7)          # 7
pow(2, 3)        # 8
round(3.14159, 2)# 3.14
```
**Arithmetic Operators:**
```
a=10, b=3
Addition: (+)        print(a + b)   # 13
Subtraction: (-)     print(a - b)   # 7
Multiplication: (*)  print(a * b)   # 30
Division: (/)        print(a / b)   # 3.333...  (give answer in float)
Floor division: (//) print(a // b)  # 3   (give answer in integer)
Modulus: (%)         print(a % b)   # 1 (gives the remainder)
Exponent: (**)       print(a ** b)  # 1000 (gives the answer of b raised to a)
          pow(a,b) is also used for exponentation  (gives the answer of b raised to a)
```
**Logical Operator**
```
and: True if **both** operands are true
or: True if **at least one** operand is true
not: Inverts the boolean value

Examples:
a, b = True, False
print(a and b)  # False
print(a or b)   # True
print(not a)    # False
```
**Assignment Operators**
```
| Operator | Example (`x=10`) | Equivalent To | Result | Description                    |   |                     |
| -------- | ---------------- | ------------- | ------ | ------------------------------ | - | ------------------- |
| `=`      | `x = 10`         | —             | 10     | Assigns value                  |   |                     |
| `+=`     | `x += 5`         | `x = x + 5`   | 15     | Add & assign                   |   |                     |
| `-=`     | `x -= 3`         | `x = x - 3`   | 7      | Subtract & assign              |   |                     |
| `*=`     | `x *= 2`         | `x = x * 2`   | 20     | Multiply & assign              |   |                     |
| `/=`     | `x /= 4`         | `x = x / 4`   | 2.5    | Divide & assign (float result) |   |                     |
| `//=`    | `x //= 4`        | `x = x // 4`  | 2      | Floor divide & assign          |   |                     |
| `%=`     | `x %= 3`         | `x = x % 3`   | 1      | Modulus & assign               |   |                     |
| `**=`    | `x **= 2`        | `x = x ** 2`  | 100    | Exponent & assign              |   |                     |
| `&=`     | `x &= 3`         | `x = x & 3`   | 2      | Bitwise AND & assign           |   |                     |
| \`       | =\`              | \`x           | = 3\`  | `x = x \| 3`                   | 3 | Bitwise OR & assign |
| `^=`     | `x ^= 3`         | `x = x ^ 3`   | 1      | Bitwise XOR & assign           |   |                     |
| `>>=`    | `x >>= 1`        | `x = x >> 1`  | 5      | Right shift & assign           |   |                     |
| `<<=`    | `x <<= 1`        | `x = x << 1`  | 20     | Left shift & assign            |   |                     |
'+' and '*' are also used for concationation and multiplication of string respectively
```
**Comparison Operators**
```
# ⚖️ Python Comparison Operators (Cheat Sheet in Table Form)

Comparison operators are used to **compare values** and always return `True` or `False`.

Operator Table

| Operator | Name                       | Example (`x=5, y=10`) | Result   |
|----------|----------------------------|-----------------------|----------|
| `==`     | Equal to                  | `x == y` → `5 == 10`   | False    |
| `!=`     | Not equal to              | `x != y` → `5 != 10`   | True     |
| `>`      | Greater than              | `x > y`  → `5 > 10`    | False    |
| `<`      | Less than                 | `x < y`  → `5 < 10`    | True     |
| `>=`     | Greater than or equal to  | `x >= y` → `5 >= 10`   | False    |
| `<=`     | Less than or equal to     | `x <= y` → `5 <= 10`   | True     |

Identity vs Equality

| Operator | Meaning                | Example                          | Result   |
|----------|------------------------|----------------------------------|----------|
| `==`     | Value equality         | `[1,2,3] == [1,2,3]`             | True     |
| `is`     | Identity (same object) | `[1,2,3] is [1,2,3]`             | False    |
| `is not` | Not identical          | `[1,2,3] is not [1,2,3]`         | True     |

Chained Comparisons
print(5 < 10 < 20)   # True
print(5 < 10 > 2)    # True
```
**String**
```
len("hello")        # 5               gives the length of string
str(123)            # "123"           convert into string
type("abc")         # <class 'str'>   to check type of variable
max("abc")          # "c"             gives maximum value in string
min("abc")          # "a"             gives minimum value in string
sorted("cab")       # ['a','b','c']   sort the atring in ascending order

s = "python"
s.upper()       # "PYTHON"            convert whole string into uppercase
s.lower()       # "python"            convert whole string into uppercase
s.title()       # "Python"            capitalize the first character after space
s.capitalize()  # "Python"            capitalize the first character of the string      
s.swapcase()    # "PYTHON" -> "python"convert lowrrcase to upper and uppercase to lower
"abc".isalpha()     # True            check all are characters
"123".isdigit()     # True            check all are numbers
"abc123".isalnum()  # True            check string contains only numbers&characters
" ".isspace()       # True            check spces in string
"HELLO".isupper()   # True            check all are characters are in uppercase
"hello".islower()   # True            check all are characters are in lowercase
"Hello".istitle()   # True            check if the first character is in uppercase or not after space
s = "python is fun"
s.split()           # ['python','is','fun']         split the string from spaces
s.split("i")        # ['python ', 's fun']          split the string from give value        
s.partition("is")   # ('python ', 'is', ' fun')     partition the string from given value(split into 2 no matter how long is the string)
"Name: {0}, Age: {1}".format(name, age)     # positional
"Name: {n}, Age: {a}".format(n=name, a=age) # keyword
string[start:end:step]                for slicing of string
```
**List**
- Ordered, mutable collection 
```
len([1,2,3])        # 3                                   gives length of list
max([1,5,3])        # 5                                   gives the maximum valuefrom list
min([1,5,3])        # 1                                   gives the minimum valuefrom list
sum([1,2,3])        # 6                                   gives the sum of list
sorted([3,1,2])     # [1,2,3]                             sorts the list in ascending order
list("abc")         # ['a','b','c']                       convert into list
any([0,1,0])        # True (at least one True)            to check value is in list or not                         
enumerate(['a','b'])# [(0,'a'), (1,'b')]                  convert the list into list of tuples of (index,value)
zip([1,2],[3,4])    # [(1,3),(2,4)]                       converts the list of lists into the list of tuples
lst = [1,2,3]                                             
lst.append(4)       # [1,2,3,4]                           add the value after the last index
lst.insert(1, 100)  # [1,100,2,3,4]                       insert the value at given index (index,value)
lst.extend([5,6])   # [1,100,2,3,4,5,6]                   add the list at end of first list
lst = [1,2,3,4,2]
lst.remove(2)       # removes first occurrence → [1,3,4,2] removes the particular provided value at its first occurance 
lst.pop()           # removes last element → [1,3,4]       removes the last value
lst.pop(1)          # removes element at index 1 → [1,4]   removes the value of particular provided index
lst.clear()         # []                                   removes all the values from list
lst = [1,2,3,2,4]
lst.index(2)        # 1 (first index of 2)             gives the index of value provided at its first occurance
lst.count(2)        # 2 (frequency of 2)               counts how many times does the value is present 
lst = [3,1,4,2]
lst.sort()          # [1,2,3,4] (ascending)            sort the list in ascending
lst.sort(reverse=True) # [4,3,2,1]                     sort the list and reverse it
lst.reverse()       # reverses in place
lst2 = lst1.copy()     # Shallow copy                  copying the list into other list
```
list slicing is also possible just as string
**Dictionaries**
- Stored in key-value pairs (mapping)  
```
d = {"name": "Alice", "age": 25}
print(d["name"])     # Alice
print(d.get("age"))  # 25          # To get the value of key
print(d.get("city", "Not Found"))  # "Not Found" is default value if key missing
d["city"] = "Delhi"                # add new key
d["age"] = 26                      # update existing key
d = {"a":1,"b":2,"c":3}
d.pop("b")                         # removes 'b' → returns 2
d.popitem()                        # removes last inserted key-value
del d["a"]                         # deletes key 'a'
d.clear()                          # empties dictionary
d = {"x":10, "y":20, "z":30}
d.keys()            # dict_keys(['x','y','z'])                  gives all the kes of dictionary
d.values()          # dict_values([10,20,30])                   gives all the kes of dictionary
d.items()           # dict_items([('x',10),('y',20),('z',30)])  show all the key value pairs of dictionary as list
d.update({"a":100, "x":50})  # merges/updates keys              add the key value pair into the dictionary
d.copy()                                                        shallow copy of dictionary
```
**Tuples**
- Ordered, immutable collection
```
t1 = (1, 2, 3)
t2 = (4, 5)
print(t1 + t2)    # Concatenation → (1,2,3,4,5)   
print(t1 * 2)     # Repetition → (1,2,3,1,2,3)      adds both tuples
print(2 in t1)    # True                            check if value is present or not
print(len(t1))    # 3                               gives the length of tuple
t.count(2)     # 1                                  counts occurrences
t.index(3)     # 2                                  returns index of first match
```
- **packing and unpacking of Tuple**
```
# Packing
person = ("Alice", 25, "Delhi")
# Unpacking
name, age, city = person
print(name)  # Alice
print(age)   # 25
```
**Sets**
- Unordered, mutable collection having all unique elements
```
s = {1, 2, 3}
s.add(4)             # {1,2,3,4}
s.update([5,6])      # {1,2,3,4,5,6}
s.remove(2)          # removes 2 (KeyError if not exists) [note: if .remove not present try .discard]
s.discard(10)        # removes 10 (no error if not exists)
s.pop()              # removes a random element
s.clear()            # empties set
set([1,2,3,2,3,5,2])                                      arrange the list in ascending order and remove all repeating elements
```
```
a = {1,2,3,4}
b = {3,4,5,6}
a | b      # Union → {1,2,3,4,5,6}
a & b      # Intersection → {3,4}
a - b      # Difference → {1,2}
a ^ b      # Symmetric Difference → {1,2,5,6}
                      OR
a.union(b)                       
a.intersection(b)
a.difference(b)
a.symmetric_difference(b)

s = {1,2,3}
s.copy()               # shallow copy                    coping the set
s.issubset({1,2,3,4})  # True                            check if s is subset (s is included in given set) of given set or not
s.issuperset({1,2})    # True                            check if s is superset(s includes the given set) of given set or not
s.isdisjoint({4,5})    # True (no common elements)       check if both sets have different elements or not
```
**Conditional Statements**
- **if**
- Executes block if condition is True
```
Syntax:
if condition:
    # block of code
```
- **if...else**
- Runs one block if True, another if False
```
Syntax:
if condition:
    # block of code
else:
    # block of code
```
- **if...elif...else**
Multiple conditions checked in order
```
Syntax:
if condition:
    # block of code
elif condition2:
    # block of code
else:
    # block of code
```
- **Nested if**
if inside another if
```
Syntax along with example:
if x > 0:                       # Outer condition
    print("Number is positive")

    if x % 2 == 0:               # Inner condition
        print("It is an even number")
    else:
        print("It is an odd number")

else:
    print("Number is not positive")
```
- **Ternary Operator**
One-line shorthand for if-else
```
Syntax:
"output this" if (condition is true) else "this output"
```
**Looping Statements**
- **While loop**
 Repeats while a condition is True
```
Syntax:
while condition:
    # code block
else:                              # else statement is optional and is executed after loop
    ---Code--- 
```
- **For loop**
Iterates over a sequence (list, string, etc.)
```
Syntax:
for i in (list, string, etc.):
    block of code
else:                              # else statement is optional and is executed after loop
    ---Code---            
```
- **Nested loop**
loop inside another loop
```
Syntax:
for i in range(2):
    for j in range(3):
        print(i, j)
```
- **Control Statements**
```
| Statement  | Description                |
| ---------- | -------------------------- |
| `break`    | Exit the loop immediately  |
| `continue` | Skip to the next iteration |
| `pass`     | Do nothing (placeholder)   |
```
**Functions in Python**
- **Defined using keyword "def"**
```
Example:
def factorial(n):                                        function declaration
    return 1 if n == 0 else n * factorial(n-1)

print(factorial(5))   # Output: 120                      function calling
```
here 'n' is argument,
and factorinal(5) is calling of function in which '5' is parameter which is sent to function
- ***args**
  Is used as argument in function to take all possible parameters while calling the function.
- ****kwargs**
  Is used as argument in function to take all possible key-value parameters while calling the function.
- **Function can be nested**
```
Example:
def outer():
    def inner():
        print("Inner function")
    inner()

outer()
```
**Scope of variable**
- **Local Scope**
  A variable created **inside a function**.  
  Accessible only within that function.
```
  def func():
    x = 10   # local variable
    print("Inside function:", x)
func()
# print(x)   # ❌ Error: x is not defined
```
- **Global Scope**
  A variable declared outside functions.
  Accessible throughout the program.
```
x = 50                               # global variable
def func():
    print("Inside function:", x)
func()
print("Outside function:", x)         # Accessible everywhere
```
- **Enclosed Scope**
  Variable from outer function (when functions are nested).
  Inner function can access but not modify unless keyword:'nonlocal' is used.
```
def outer():
    x = "outer"
    
    def inner():
        nonlocal x   # refers to variable from outer function
        x = "inner modified"
        print("Inner:", x)
    
    inner()
    print("Outer:", x)

outer()
```
- **Built-in Scope**
  Reserved names in Python (e.g., len, print, sum).
```
print(len("Python"))   # Built-in function
```
**Object Oriented Programming in Python**
- **It organizes code into classes (blueprints) and objects (real instances).**
- **Helps make programs modular, reusable, and easier to maintain.**
Core concepts:
```
Class
class Student:                                      class declaration
    def __init__(self, name, age):
        self.name = name
        self.age = age
```
(__init__) is a constructor which is a special method that runs automatically when creating objects.
```
Objects :
It is an instance of class which is created to call the class or functions of class
s1 = Student("Utkarsh", 20)
print(s1.name)   # Utkarsh
```
**OOP Principles**
1. Encapsulation
   It is wrapping of data (variables/attributes) and methods (functions) together into a single unit (class) and restricting direct access to     the data from outside the class.
```
Example:
class BankAccount:                 # creating class
    def __init__(self, balance):   # default and auto called constructor
        self.__balance = balance   # private attribute

    def deposit(self, amount):     #function inside a class
        self.__balance += amount

    def get_balance(self):
        return self.__balance

# Output
account = BankAccount(1000)        # creating object
account.deposit(500)               # calling function of a class variables cannot be called like(account.balance)
print(account.get_balance())   # ✅ 1500
# print(account.__balance)     # ❌ Error (cannot access directly)
```
2. Inheritance
   Inheritance allows one class (child/derived class) to acquire the properties and behaviors (variables and methods) of another class            (parent/base class)
```
Example:
# Parent Class
class Person:
    def __init__(self, name, age):
        self.name = name
        self.age = age

    def display(self):
        print(f"Name: {self.name}, Age: {self.age}")

# Child Class (inherits from Person)
class Student(Person):
    def __init__(self, name, age, student_id):
        # Call parent constructor
        super().__init__(name, age)
        self.student_id = student_id

    def display(self):
        # Overriding parent method
        print(f"Student Name: {self.name}, Age: {self.age}, ID: {self.student_id}")

# Another Child Class
class Teacher(Person):
    def __init__(self, name, age, subject):
        super().__init__(name, age)
        self.subject = subject

    def display(self):
        print(f"Teacher Name: {self.name}, Age: {self.age}, Subject: {self.subject}")


# Usage
s1 = Student("Utkarsh", 21, "CS101")
t1 = Teacher("Dr. Sharma", 45, "Data Science")

s1.display()
t1.display()
```
3. Polymorphism
   Similar named method can be created in different different classes
```
Example:
class Dog:
    def sound(self):
        print("Woof!")
class Cat:
    def sound(self):
        print("Meow!")
for animal in [Dog(), Cat()]:
    animal.sound()
# Output:
# Woof!
# Meow!
```
4. Abstraction
   Abstraction means hiding the internal implementation details and showing only the essential features of an object.
```
Example:
from abc import ABC, abstractmethod                     importing abstract method

class Shape(ABC):                                       # Abstract class, Only declaration of methods 
    @abstractmethod                            
    def area(self):
        pass

class Square(Shape):                                   
    def __init__(self, side):
        self.side = side
    def area(self):                                       Overriding method that is declared in abstract class
        return self.side * self.side

# Example
s = Square(4)
print(s.area())  # 16
```
