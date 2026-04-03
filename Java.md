# Java
**Data Types**
```
int	        Whole numbers (32-bit)	            int x = 10;
double     	Decimal numbers (64-bit)	          double y = 3.14;
char	      Single character (16-bit Unicode)   char grade = 'A';
boolean	    True or False                	      boolean isJavaFun = true;
String	    Sequence of characters (Object)	    String name = "Utkarsh";
```
```
//Type Casting
double myDouble = 9.78;
int myInt = (int) myDouble;     // Manual casting: 9

String s = "100";
int i = Integer.parseInt(s);     // String to int
```
**Arithmetic Operators:**<br>
    + , - , * , / , % , a++ , ++a , a-- , --a.
    for power Math.pow(a, b) return  double datatye<br><br>

**Logical & Comparison Operators:**<br>
Logical: && (AND), || (OR), ! (NOT).
Comparison: ==, !=, >, <, >=, <=.
**Basic code**
for "Hello, World!"
```public class Main {
    public static void main(String[] args) {
        System.out.println("Hello, World!");
    }
}
```
**String Methods**
Strings in Java are Immutable Objects.
```
String s = " Java Programming ";
s.length();          // 17
s.charAt(0);         // ' '
s.toUpperCase();     // " JAVA PROGRAMMING "
s.trim();            // "Java Programming" (removes leading/trailing spaces)
s.substring(1, 5);   // "Java" (start index, end index)
s.contains("Java");  // true
s.replace('a', 'o'); // " Jovo Progomming "
```
**Arrays & Lists (Collections)**
1. **Array(Fixed Size)**
```
int[] nums = {1, 2, 3};
System.out.println(nums.length);             // 3
```
2. **ArrayList (Dynamic Size - similar to Python List)**
```
import java.util.ArrayList;
ArrayList<String> list = new ArrayList<>();
list.add("Apple");            // append
list.add(0, "Mango");         // insert at index
list.remove("Apple");         // remove by value
list.get(0);                  // access element (list[0])
list.size();                  // length
```
**Dictionaries (HashMap)**
In Java, "Dictionaries" are implemented using the HashMap class.
```
import java.util.HashMap;
HashMap<String, Integer> map = new HashMap<>();
map.put("Alice", 25);
map.get("Alice");           // 25
map.containsKey("Bob");     // false
map.remove("Alice");
map.keySet();               // Get all keys
map.values();               // Get all values
```
**Sets**
Unique elements, unordered.
```
import java.util.HashSet;
HashSet<Integer> set = new HashSet<>();
set.add(1);
set.add(1); // Won't be added (duplicate)
set.contains(1); // true
```
**Control Flow**
Conditional:
```
if (x > 0) {
    System.out.println("Positive");
} else if (x < 0) {
    System.out.println("Negative");
} else {
    System.out.println("Zero");
}

// Ternary
String result = (10 > 5) ? "Greater" : "Smaller";
```
Loops:
```
// For loop
for (int i = 0; i < 5; i++) { ... }

// Enhanced For loop (For-each)
for (String s : list) { ... }

// While loop
while (condition) { ... }
```
**Functions (Methods)**
Methods must be inside a class.
```
public class Main {
    // static means we can call it without creating an object
    public static int add(int a, int b) {
        return a + b;
    }

    public static void main(String[] args) {
        System.out.println(add(5, 10));
    }
}
```
# Object-Oriented Programming (OOP)
1. Class & Object:
```
class Student {
    String name;
    // Constructor
    Student(String name) {
        this.name = name;
    }
}
Student s1 = new Student("Utkarsh");
```
2. Encapsulation: Use private variables and public Getters/Setters.
3. Inheritance: Use extends keyword.
```
class Animal { void eat() { } }
class Dog extends Animal { void bark() { } }
```
4. Abstraction: Use abstract classes or interfaces.
```
interface Shape {
    double getArea(); // Method signature only
}
```
