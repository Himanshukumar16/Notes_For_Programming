
-------------------------
| Basics Of Core Java ! |
-------------------------

1) running of java code:->

first we write java code(.java), the compliers compiles or convert the java code into byte code(.class) because JVM understands only the byte code and then the execution starts with the main function.

JRE(Java Runtime Environment) consists of JVM(Java Virtual Machine) + Other Libraries.         
												                                                                        
JDK(Java Development Kit) has JRE. JRE has JVM & Libraries.

	or we can say, 

JVM = the engine that runs Java bytecode.							                                        
												                                                                        
JRE = JVM + standard libraries → what you need to run Java programs.				                    
												                                                                        
JDK = JRE + compilers and tools → what you need to write, compile, and package Java programs.	

Java is a strictly typed (or strongly typed) language. because:-Every variable and expression has a defined type. You cannot use a variable without declaring its type. The compiler checks all types at compile time. You cannot mix incompatible types without explicit type casting.

when the main method is not found in a Java program, the application cannot start its execution, resulting in a runtime error.

Java is a object oriented programming.

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
2) variables:->

int num = 5;
here int is datatype.
num is variable name.
5 is value of the variable.

by default decimal number is double in java.
for char we use single quote.
for Boolean use boolean, the default value for a boolean variable is indeed false.
```
float f = 5.5f; //declaring a float value.

int i = 5,j = '5'; // ascii of 5 is 53.
sout(i + j); //58
```
--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
3) Literal :-> Fixed value directly written in your program (not a variable or expression)

in java 2.5e2 means 2.5 × 10²,e2 refers to 10 power 2..

-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
4) type conversion :->
smaller datatype can easily converted to bigger by the compiler. but to convert bigger to smaller we need to convert, example: int x = (int)5.6;
here 5.6 is float but it is converted to int (5) and stress in x.

when you cast an int to a byte in Java, and the value is outside the byte range (-128 to 127), it behaves like a modulo operation with 256.

-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
5) type promotion :->
Type promotion in Java is the process where smaller data types are automatically converted to larger data types during arithmetic or expression evaluation to avoid data loss. for example:
```
byte a = 10;
byte b = 20;
// byte c = a + b; ❌ Error
int c = a + b; // ✅ Automatically promoted to int.
```
-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
6) operators :-> operators are special symbols used to perform operations on variables and values. Java supports several types of operators. types:-

| Category      | Operators                          |
|---------------|------------------------------------|
| Arithmetic    | `+`, `-`, `*`, `/`, `%`            |
| Relational    | `==`, `!=`, `>`, `<`, `>=`, `<=`   |
| Logical       | `&&`, `||`, `!`                    |
| Assignment    | `=`, `+=`, `-=`, `*=`, `/=`, `%=`  |
| Unary         | `+`, `-`, `++`, `--`, `!`          |
| Bitwise       | `&`                                |
| Ternary       | `?:`                               |
| Type Checking | `instanceof`                      |


-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
7) loops & conditional statement:->
	for loop -> for(conditions){}             entry controlled loop.
	while loop -> while(condition){}          entry controlled loop.
	do-while loop -> do{}while(condition);    exit controlled loop, it will run minimum one time because the condition is checked at the last.
conditional statement : if-else; if else-if else.

--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
8) class and object :->

class : A class is a blueprint or template for creating objects. It defines properties (variables) and behaviors (methods). it Doesn't occupy memory when declared it defines structure.

Objects : An object is an instance of a class. It represents real-world entities. An object is created using the new keyword. Each object has its own copy of class variables and can call class methods.

The main() method is static, so it belongs to the class itself, not to any object. Because of that, the JVM can directly run main() without creating an object.

---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
9) Methods :-> A method in Java is a block of code that performs a specific task, encapsulated under a name, and belonging to a class (or interface).

Method overloading :-> Method Overloading in Java is a form of compile‑time (or static) polymorphism where you can have multiple methods in the same class with The same name Different parameter
 lists (different in number, type, or order of parameters),The return type may be the same or different, but return type alone cannot distinguish overloaded methods.

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

10) Arrays :-> an array is a container object that holds a fixed‐number of values of a single type. each identified by an integer index, all storing the same kind of item.

Types of arrays :-

Linear array :- Normal Array....

2D Array :- Array having both rows and column....

ragged Array :- Array with constant row number but different column number....

| Feature         | Description                               |
|-----------------|-------------------------------------------|
| Fixed Size      | Array size cannot change after creation   |
| Same Data Type  | All elements must be of same type         |
| Indexing        | Starts from 0                             |
| Stored In       | Heap memory                               |
| Access Elements | Using `array[index]`                      |



-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

11) Enhanced For loop :->

The for-each loop in Java (also called the enhanced for loop) is a simple and clean way to iterate through arrays or collections (like ArrayList, HashSet, etc.) without using an index.
```
ex:-	for (dataType variable : collection Or Array) {
    		// use variable (each element)
	}
```
----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
12) Strings :->

In Java, String is a built-in class (not a primitive type) that represents a sequence of characters. Strings are immutable (unchangeable once created) and are used to store and manipulate text.
How to Create Strings:- 1)String s1 = "Hello";   // stored in string pool.
			2)String s2 = new String("Hello");   // creates a new object in heap.

| Type of Comparison   | Operator/Method | What it Checks                                       |
|----------------------|-----------------|------------------------------------------------------|
| Reference Comparison | `==`             | Do both variables point to the same memory location? |
| Content Comparison   | `.equals()`      | Do both variables have the same characters/text?     |



| Method                | What it Does                        | Example                                    |
|-----------------------|-------------------------------------|--------------------------------------------|
| `length()`            | Returns number of characters        | `"hello".length()` → `5`                   |
| `charAt(int index)`   | Gets character at index             | `"cat".charAt(0)` → `'c'`                  |
| `toUpperCase()`       | Converts to uppercase               | `"hi".toUpperCase()` → `"HI"`              |
| `toLowerCase()`       | Converts to lowercase               | `"HI".toLowerCase()` → `"hi"`              |
| `substring(int start)`| Gets part of string                 | `"hello".substring(1)` → `"ello"`          |
| `substring(a, b)`     | From index a to b-1                 | `"hello".substring(1, 4)` → `"ell"`        |
| `equals(str)`         | Compares strings (case-sensitive)   | `"Hi".equals("hi")` → `false`              |
| `equalsIgnoreCase(str)` | Compares strings (case-insensitive) | `"Hi".equalsIgnoreCase("hi")` → `true`   |
| `contains(str)`       | Checks if a string is inside        | `"apple".contains("pp")` → `true`          |
| `replace(a, b)`       | Replaces one char/word with another | `"hi hi".replace("hi", "bye")` → `"bye bye"` |
| `trim()`              | Removes spaces from both ends       | `"  hi  ".trim()` → `"hi"`                 |
| `split(" ")`          | Splits into array                   | `"a b c".split(" ")` → `[a, b, c]`         |


```
String s1 = "Java";
String s2 = new String("Java");
System.out.println(s1 == s2);         // ❌ false checks address
System.out.println(s1.equals(s2));    // ✅ true check equality
```
here, What is happening? s1 = "Java"; 👉 This uses a string literal. Java stores it in the String pool (shared area in memory). s2 = new String("Java"); 👉 This creates a new object in
 heap memory, even though the text is the same.

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

13) String builder & string buffer:->

Java String is immutable — you cannot change it after it's created.To modify strings efficiently, we use: 1) StringBuffer → Thread-safe (used in multi-threaded programs)....
													  2) StringBuilder → Faster, but not thread-safe....

StringBuffer :- Thread-safe
```
StringBuffer sb = new StringBuffer("Hello");
sb.append(" World");
System.out.println(sb);  // Output: Hello World
```
-------------------------------------------------------------
| Method                   | Description                    |
| ------------------------ | ------------------------------ |
| append(String)           | Adds text at the end           |
| insert(index, text)      | Inserts text at given position |
| replace(start, end, str) | Replaces part of text          |
| delete(start, end)       | Deletes part of text           |
| reverse()                | Reverses the string            |
| length()                 | Returns length                 |
-------------------------------------------------------------

StringBuilder :- Faster, but not thread-safe
```
StringBuilder sb = new StringBuilder("Hello");
sb.append(" Java");
System.out.println(sb);  // Hello Java
```
✅ All methods are same as StringBuffer (append, insert, delete, etc.)

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

14) Static :-> Belongs to a class not to a object....

if you make something static, it means- There is only one copy, shared by all objects. You can access it without creating an object. Access static members using class name...

we can use a static variable inside static method but can not use non static variables inside static method...

A static block in Java is a special block of code that runs only once, when the class is loaded into memory. It starts with the keyword static. Runs before the main() method. 
Used for initializing static variables or code that must run once. 
--------------------------------------------------------------
| Term              | Meaning                                |
|-------------------|----------------------------------------|
| Class is loaded   | JVM brings the .class file into memory |
| Static block runs | Automatically after class is loaded    |
| Main runs         | After static block, main() starts      |
--------------------------------------------------------------

When you run a Java program (following things takes place):-
```
Class Loading :-
	The .class file (like Demo.class) is loaded into RAM by a part of the JVM called the Class Loader.
Static Block Runs (if any) :-
	As soon as the class is loaded, all static blocks run once (before main() or any object is created).
Main Method Starts :-
	After loading and static initialization, the JVM calls the main() method to start execution.
```
----------------------------------------------------------------------
| Part                       | Meaning                               |
| -------------------------- | ------------------------------------- |
| Class.forName("MyClass")   | Loads MyClass into memory             |
| Returns                    | A Class object that describes MyClass |
| Use                        | Useful in reflection, dynamic loading |
----------------------------------------------------------------------

--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

15) Encapsulation :-> Encapsulation is a fundamental concept in object-oriented programming (OOP) in Java. It involves hiding the internal details of an object and exposing only the
necessary parts to the outside world.

This is achieved by:
	• Declaring the class variables as private, which makes them accessible only within the	class.
	• Providing public methods (getters and setters) to access and modify these private variables.
```
getter: example - public String getName() {
        		return name;
    		  }
setter : example - public void setName(String name) {
        		this.name = name;
    		   }
```
here,this keyword refers to the current object of the class....

---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

16) Constructor :-> A constructor in Java is a special method that is automatically called when you create an object of a class. It is used to initialize the object — 
i.e., give values to the object’s variables when it's created.
------------------------------------------------------------------------------------------------
| Type                               | Description                                             |
| ---------------------------------- | ------------------------------------------------------- |
| 1. Default constructor             | No parameters, sets default values                      |
| 2. Parameterized constructor       | Takes arguments to set custom values                    |
| 3. Copy constructor (not built-in) | Used to copy another object's values (manually written) |
------------------------------------------------------------------------------------------------

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

17) Naming Conventions in Java :-> 
-------------------------------------------------
| Item        | Convention | Example            |
| ----------- | -----------| -------------------|
| Class       | PascalCase | EmployeeDetails    |
| Method      | camelCase  | calculateSalary()  |
| Variable    | camelCase  | totalMarks         |
| Constant    | UPPER_CASE | PI, MAX_VALUE      |
| Package     | lowercase  | com.myproject.demo |
| Interface   | PascalCase | Runnable           |
| Constructor | PascalCase | Student()          |
-------------------------------------------------

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

18) Anonymous Object in Java :-> An anonymous object in Java is an object that is created without assigning it a name (reference variable). it can be used only once....
Syntax :-  new ClassName().methodName();

------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

19) Inheritence :-> Inheritance in Java means one class can use (or inherit) the properties and methods of another class. 

class Parent {
    // parent class (superclass)
}

class Child extends Parent {
    // child class (subclass) inherits from parent
}
--------------------------------------------------------------------------------------------------------------
| Type                           | Supported in Java?                   | Example                            |
| ------------------------------ | -------------------------------------| -----------------------------------|
| Single Inheritance             |    Yes                               | One child inherits one parent      |
| Multilevel Inheritance         |    Yes                               | Child → Parent → Grandparent       |
| Hierarchical                   |    Yes                               | Multiple classes inherit one parent|
| Multiple Inheritance (classes) |    No (but possible using interfaces)| -                                  |
--------------------------------------------------------------------------------------------------------------
java does not support multiple inheritence.....

-------------------------------------------------------------------------------------------
|Keyword| Refers To           | Common Use Cases                                          |
|-------| ------------------- | --------------------------------------------------------- |
| this()| Current class       | Access current object fields, call same class constructor |
|super()| Parent (superclass) | Call parent constructor, access parent method/variable    |
-------------------------------------------------------------------------------------------

-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

20) Method Overriding :-> Method Overriding in Java means defining a method in a child class with the same name, return type, and parameters as in its parent class — 
so that the child class version gets called instead of the parent version.... 

In inheritance jo method refrence main hoga uska method dekha jaiga aur jo overridden hoga wo bs baki main compilation error aa jaega....

--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
21) Packages :-> A package in Java is a group of related classes and interfaces. Think of it as a folder on your computer that organizes files (Java classes) neatly.

Types of Packages:
	Built-in packages (from Java itself)
	User-defined packages (created by you)

Built-in packages:
-------------------------------------------------------------------
| Package   | Use                                                 |
|-----------|---------------------------------------------------- |
| java.lang | Core classes (String, Math, System) — auto imported |
| java.util | Utility classes like ArrayList, Date, Scanner       |
| java.io   | Input/Output classes like File, BufferedReader      |
| java.sql  | Database connectivity                               |
-------------------------------------------------------------------

-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

22) Access Modifiers :-> Access Modifiers in Java are keywords used to set the accessibility (visibility) of classes, constructors, methods, and variables...
-----------------------------------------------------
|Modifier |Class |Package |Subclass |Outside Package|
|---------|------|--------|---------|---------------|
|public   |✔     |✔      | ✔       |✔             |
|protected|✔     |✔      | ✔       |✘             |
|default  |✔     |✔      | ✘       |✘             |
|private  |✔     |✘      | ✘       |✘             |
-----------------------------------------------------
public:
	Access Level: Everywhere (within the same class, package, subclass, and outside package).
	Keyword: public
	Use Case: When you want your method/class to be accessible from anywhere.

Protected:
	Access Level: Within the same package and subclasses (even if they are in different packages).
	Keyword: protected
	Use Case: When you want to allow access to subclasses and same package but restrict it from other packages.

Default (Package-Private):
	Access Level: Only within the same package.
	Keyword: No modifier (just omit the access keyword)
	Use Case: When you want to restrict access to classes in the same package only.

private:
	Access Level: Only within the same class.
	Keyword: private
	Use Case: For internal data hiding, to enforce encapsulation.

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

23) Polymorphism :-> Polymorphism means “many forms”. In Java, it allows a single action to behave differently based on the object that is invoking it. 
It is one of the core principles of Object-Oriented Programming (OOP)..
It has 2 types:
	----------------------------------------------------------------------------------
	| Type                      | Description      | Implemented By                  |
	|---------------------------|------------------| --------------------------------|
	| Compile-time Polymorphism |Method Overloading| Within the same class           |
	| Runtime Polymorphism      |Method Overriding | Between parent and child classes|
	----------------------------------------------------------------------------------

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

24) Final Keyword :-> 
----------------------------------------------------------------------------
| `final` in Java  | Real Life Equivalent                                  |
| ---------------- | ----------------------------------------------------- |
| `final` variable | A **PIN code**: cannot be changed after set           |means variable value cannot be changed. used for constants...
| `final` method   | A **sealed company policy**: no modifications         |means method cannot be overridden. prevent overriding...
| `final` class    | A **sealed product**: no further additions or changes |means class cannot be extended, prevent inheritance...
----------------------------------------------------------------------------

-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

25) toString() :-> it gives output as Classname@hashcode which is equal to if we print the object we made for any class . although we can override it to print anything we want...

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

26) upcasting and downcasting :-> Upcasting means assigning a child class object to a parent class reference. Downcasting means assigning a parent class reference back to a child class reference.
--------------------------------------------------------------------------
| Feature   | Upcasting                 | Downcasting                    |
| --------- | ------------------------- | ------------------------------ |
| Direction | Child → Parent            | Parent → Child                 |
| Syntax    | `Parent p = new Child();` | `Child c = (Child) parentRef;` |
| Type      | Implicit (Automatic)      | Explicit (Manual)              |
| Safe?     | Yes                       |    Risky (must be checked)     |
| Use Case  | Polymorphism              | Access child-specific features |
--------------------------------------------------------------------------

---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
27) Wrapper Classes :-> In Java, wrapper classes are used to convert primitive data types into objects... 

-------------------------------------------------------------------------------
| Wrapper Class | Method Example                 | Description                |
| ------------- | ------------------------------ | -------------------------- |
| `Integer`     | `Integer.parseInt("123")`      | Converts String to int     |
| `Double`      | `Double.parseDouble("2.3")`    | Converts String to double  |
| `Boolean`     | `Boolean.parseBoolean("true")` | Converts String to boolean |
-------------------------------------------------------------------------------

boxing : converting primitive value to object by wrapper class.. it is of 2 types:- Autoboxing and Unboxing.

Autoboxing:
	Automatically converts primitive → object 
	int a = 10;
	Integer obj = a;

Unboxing:
	Automatically converts object → primitive
	Integer obj = 10;
	int a = obj;

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
28) Abstract Keyword :-> The abstract keyword in Java is used to declare abstract classes and abstract methods.

  Abstract Class:-
	An abstract class is a class that cannot be instantiated (you cannot create objects of it directly). It can have abstract methods (methods without a body) as well as concrete methods (methods with a body). It is meant to be extended by subclasses that provide implementations for its abstract methods.
```
example :-
abstract class Animal {
    abstract void sound(); // abstract method
    void eat() {  // concrete method
        System.out.println("Eating...");
    }
}
```
Abstract Method :-
	An abstract method is a method that does not have a body — only its signature is declared. It must be overridden in a subclass. If a class has at least one abstract method, then the class must be declared abstract. 

Cannot instantiate an abstract class, very important means we cannot make direct object of the abstract class !!.

--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

29) Inner Class :-> An Inner Class in Java is a class defined inside another class. 
 you create an inner class object with OuterClas.InnerClass obj = outerClassObject.new InnerClass();
if we make inner class static then to create inner class object we use: OuterClas.InnerClass obj = new OuterClass.InnerClass();

remember we cannotmake outer class static...

-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

30) Anonymous Inner Class :-> creating inner class at the time of object creation so that no class keyword and name is used !
```
// Anonymous Inner Class.

public static void main(String[] args) {
     A obj = new A(){// Declared at the time of making object...
     	public void show(){
         	System.out.println("In Show 2.");
     	}
     };
     obj . show();
}
class A{
    public void show(){
        System.out.println("in Show");
    }
}
```
--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

31) Interface :-> It is 100% abstract by design (before Java 8) — it only contains abstract methods (method signatures without a body) and constants (public, static, final variables). we cannot create a interface object.

	Methods in an interface are public and abstract by default.
	Fields are public, static, and final by default.
	A class implements an interface using the implements keyword.
	A class can implement multiple interfaces — this achieves multiple inheritance in Java.
	From Java 8, interfaces can have default and static methods with a body.
	From Java 9, interfaces can also have private methods.
	we can extend two interfaces or inheritance is possible here.

```
interface Animal {
    void eat(); // abstract method
    void sleep();
}

class Dog implements Animal {
    public void eat() {
        System.out.println("Dog eats bones");
    }
    public void sleep() {
        System.out.println("Dog sleeps");
    }
}
```

------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

32) Enum:-> An enum (enumeration) in Java is a special type that represents a group of named constants (fixed set of values).
 	Enum constants are public, static, and final by default. In Java, enum constants are themselves objects, and they are created automatically when the enum type is loaded.

| Method                 | Description                                       |
| ---------------------- | ------------------------------------------------- |
| `values()`             | Returns all enum constants as an array            |
| `valueOf(String name)` | Converts a String to enum constant                |
| `ordinal()`            | Returns the position (index) of the enum constant |

we can use if-else and switch here. Enums implicitly extend java.lang.Enum class. Enums cannot extend other classes because Java does not support multiple inheritance for classes.

------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

33) Annotation :-> Annotations are a form of metadata — they provide information about your code, but do not change how the code runs directly. Think of them as tags or markers you attach to classes, methods, variables, etc. to instruct the compiler or frameworks/tools to do something special.
```
Some annotations are only for compile-time checks (like @Override). But some can be used at runtime
by tools or frameworks using Reflection. Example: @Entity in Hibernate, @RestController in Spring Boot.
```
-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

34) Types Of Interface :-> 

| Type                               | Description                                                                                                                                                   |
| ---------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 1️⃣ **Normal (Regular) Interface** | Has only abstract methods (Java 7 and earlier). From Java 8 onwards, can have default & static methods too.                                                   |
| 2️⃣ **Marker Interface**           | Empty interface — has no methods or fields. Acts as a *tag* for the compiler/JVM. Example: `Serializable`, `Cloneable`.                                       |
| 3️⃣ **Functional Interface**       | Interface with **only one abstract method** (SAM — *Single Abstract Method*). Can have default/static methods. Example: `Runnable`, `Callable`, `Comparator`. |
| 4️⃣ **Nested Interface**           | Interface defined inside a class or another interface.                                                                                                        |

```
Normal Interface :- 

interface Animal {
    void eat();
    void sleep();
}

class Dog implements Animal {
    public void eat() {
        System.out.println("Dog eats");
    }
    public void sleep() {
        System.out.println("Dog sleeps");
    }
}
```
```
Marker Interface :-

interface Serializable { } // Marker

class Student implements Serializable {
    int id;
    String name;
}
```
Serializable is example of this interface(Marker).

```
Functional Interface :-

@FunctionalInterface
interface MyFunctional {
    void show();
}

public class Test {
    public static void main(String[] args) {
        MyFunctional f = () -> System.out.println("Lambda executed!");
        f.show();
    }
}
```
some common example of this interface(functional) is: Runnable — public void run(); Callable — public V call(); Comparator — int compare(T o1, T o2);
```
Nested Interface

class Outer {
    interface Nested {
        void display();
    }
}

class Inner implements Outer.Nested {
    public void display() {
        System.out.println("Nested Interface implemented");
    }
}
```
------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

35) Lambda Expression :-> only applicable in functional interface.
```
regular expression.

@FunctionalInterface
interface A {
    void show();
}

public class Test {
    public static void main(String[] args) {
        A f = new A(){
 	    System.out.println("hello!");
	};
    }
}
```
```
lambda expression

@FunctionalInterface
interface A {
    void show();
}

public class Test {
    public static void main(String[] args) {
        A f = () -> System.out.println("hello!");
    }
}
```
```
lambda with return

        A obj = (String n) ->{
            return n;
        };
        System.out.println(obj.show("this is a sample code !"));
```
------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

36) Exceptions in Java :->

An Exception is an unexpected event that disrupts the normal flow of a program during execution. 

| Type                 | Meaning                                                 | Examples                                      |
| -------------------- | ------------------------------------------------------- | --------------------------------------------- |
| **Error**            | Serious problems, not meant to be caught by application | `OutOfMemoryError`, `StackOverflowError`      |
| **Exception**        | Problems that can be handled                            | `IOException`, `SQLException`                 |
| **RuntimeException** | Unchecked exceptions that occur during runtime          | `NullPointerException`, `ArithmeticException` |

| Type                    | Example                                                  | Must be handled?                                    |
| ----------------------- | -------------------------------------------------------- | --------------------------------------------------- |
| **Checked Exception**   | `IOException`, `SQLException`                            | ✅ Must handle at compile time (try-catch or throws) |
| **Unchecked Exception** | `NullPointerException`, `ArrayIndexOutOfBoundsException` | ❌ Not required to handle explicitly                 |

| Keyword   | Meaning                                        |
| --------- | ---------------------------------------------- |
| `try`     | Block of code to monitor for exceptions        |
| `catch`   | Block to handle the exception                  |
| `finally` | Block that always executes (clean-up code)     |
| `throw`   | To explicitly throw an exception               |
| `throws`  | Declares which exceptions a method might throw |

--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
37) try and catch :-> 

try and catch demo :

```
public class ExceptionDemo {
    public static void main(String[] args) {
        try {
            int a = 10 / 0;  // ArithmeticException
        } catch (ArithmeticException e) {
            System.out.println("Cannot divide by zero: " + e);
        }
        System.out.println("Program continues...");
    }
}
```
--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

38) Exception hierarchy :-> 

```
Throwable
├── Error
│   ├── OutOfMemoryError
│   ├── StackOverflowError
│   ├── VirtualMachineError
│   └── ...
└── Exception
    ├── IOException
    │   ├── FileNotFoundException
    ├── SQLException
    ├── ClassNotFoundException
    ├── RuntimeException
    │   ├── NullPointerException
    │   ├── ArithmeticException
    │   ├── ArrayIndexOutOfBoundsException
    │   ├── NumberFormatException
    │   └── ...

```
--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

39) throw & throws :->

throw :- Used to explicitly throw an exception inside a method or block. You create an exception object and throw it immediately. Only one exception can be thrown at a time using throw.
```
class TestThrow {
    static void checkAge(int age) {
        if (age < 18) {
            throw new ArithmeticException("Not eligible to vote");
        } else {
            System.out.println("Eligible to vote");
        }
    }

    public static void main(String[] args) {
        checkAge(15);  // This will throw an exception
    }
}
```
throws :- Used in a method signature to declare that the method might throw certain checked exceptions. It tells the compiler that this method is not handling the exception itself — so the caller must handle it. You can declare multiple exceptions separated by commas.

```
import java.io.*;

class TestThrows {
    void readFile() throws IOException {
        FileReader fr = new FileReader("file.txt"); // might throw FileNotFoundException
        fr.read(); // might throw IOException
        fr.close();
    }

    public static void main(String[] args) {
        TestThrows t = new TestThrows();
        try {
            t.readFile();  // caller must handle exception
        } catch (IOException e) {
            System.out.println("Exception handled: " + e);
        }
    }
}
```
--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

40) custom exception :-> 
```
class InvalidAgeException extends Exception {
    public InvalidAgeException(String message) {
        super(message);  // Call parent constructor
    }
}
```
--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
41) Scanner and bufferedReader class :-> 

| Feature     | `Scanner`                      | `BufferedReader`        |
| ----------- | ------------------------------ | ----------------------- |
| Introduced  | Java 5                         | Java 1.1                |
| Package     | `java.util`                    | `java.io`               |
| Reads       | Primitive types + strings      | Strings only            |
| Parsing     | Built-in                       | Must parse manually     |
| Reads by    | Tokens or lines                | Only lines              |
| Performance | Slightly slower for huge data  | Faster for huge input   |
| Common use  | User input, competitive coding | File reading, big input |

--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
42) finally :-> It will run whether there is exception or not...
```
try {
    // code that might throw an exception
} catch (ExceptionType e) {
    // code to handle the exception
} finally {
    // code that will always run
}
```
--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
43) Threads :-> A thread is the smallest unit of execution in a program. Java supports multithreading, which means you can run multiple tasks at the same time inside a single program.

Why use Threads?
	To do multiple tasks concurrently (like downloading a file and showing a progress bar at the same time).
	To make applications faster and more responsive.
	To utilize multi-core CPUs efficiently.
 we need to extend Thread class for this...

some common method for threads are :-

| Method      | Use                                      |
| ----------- | ---------------------------------------- |
| `start()`   | Starts a new thread.                     |
| `run()`     | Code executed by thread (called by JVM). |
| `sleep(ms)` | Pause thread for `ms` milliseconds.      |
| `join()`    | Wait for another thread to finish.       |
| `yield()`   | Pause to let other threads run.          |
| `isAlive()` | Check if thread is still running.        |


```
class MyThread extends Thread {}
```
in every thread we need to have run() method in class and start()...
```
class Mythread1 extends Thread{
    public void run(){
        System.out.println("Hello ! ");
    }
}
class Mythread2 extends Thread{
    public void run(){
        System.out.println("Hey !");
    }
}
public static void main(String[] args) {
        Mythread1 obj = new Mythread1();
        Mythread2 obj2 = new Mythread2();
        for(int i = 1; i <= 10; i++){
            obj.start();
            obj2.start();
        }
    }
```
It will print consecutive Hello and hi...
we can set and get priority of the threads by setPriority() and getPriority()...

to print in consecutive manner we can use: Threads.sleep(time in ms); method.

we can also do it using runnable interface :
```
class MyRunnable implements Runnable {
    public void run() {
        System.out.println("Runnable is running");
    }
}

public class TestRunnable {
    public static void main(String[] args) {
        MyRunnable myRunnable = new MyRunnable();
        Thread t1 = new Thread(myRunnable);
        t1.start();
    }
}
```
Thread Safe:-

A piece of code, method, class, or data structure is called thread-safe if it behaves correctly when accessed by multiple threads at the same time, without causing: Data corruption; Unexpected results; Crashes

In simple words: Thread-safe code works properly even when multiple threads use it at the same time.

we can use two threads by using sncronized method , it locks one threads while while other thread is running in the system....

thread state :-

```
+---------+      start()     +----------+
|  New    |  ------------->  | Runnable |
+---------+                  +----------+
                                 |
                           CPU picks up
                                 ↓
                            +---------+
                            | Running |
                            +---------+
                                 |
                      +----------------------+
                      |                      |
                waiting, blocked         run() ends
                      ↓                      ↓
             +----------------+         +------------+
             | Waiting/Blocked| ----->  | Terminated |
             +----------------+         +------------+
```
```
Thread Lifecycle:-

New: Thread created.
Runnable: Ready to run.
Running: Actively executing run().
Blocked/Waiting: Paused temporarily.
Terminated: Done forever.
```
--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
44) Collections :->

| Term           | What it is                                                | Example                                                |
| -------------- | --------------------------------------------------------- | ------------------------------------------------------ |
| `Collection`   | **Root interface** for all data structures (except `Map`) | `Collection<String> c = new ArrayList<>();`            |
| Collection API | **Whole framework** (interfaces + classes + utilities)    | `List`, `Set`, `Map`, `Queue` + `ArrayList`, `HashMap` |
| `Collections`  | **Utility class** with static methods                     | `Collections.sort(list)`                               |

--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
45) interface linked with the collections :->

```
java.lang.Iterable
  └── java.util.Collection
         ├── List
         │     ├── ArrayList
         │     ├── LinkedList
         │     ├── Vector
         │     │     └── Stack
         ├── Set
         │     ├── HashSet
         │     ├── LinkedHashSet
         │     ├── SortedSet (interface)
         │     │     └── NavigableSet (interface)
         │     │             └── TreeSet
         ├── Queue
         │     ├── LinkedList
         │     ├── PriorityQueue
         │     ├── Deque (interface)
         │     │     ├── LinkedList
         │     │     ├── ArrayDeque

java.util.Map (separate hierarchy)
  ├── HashMap
  ├── LinkedHashMap
  ├── SortedMap (interface)
  │     └── NavigableMap (interface)
  │             └── TreeMap
  ├── Hashtable
  │     └── Properties
```
--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
46) ArrayList :-> ArrayList is a class in java.util that implements the List interface. If more space is needed, it creates a bigger array and copies old elements.
```
List<String> list = new ArrayList<>();
```

| Method                | Description                |
| --------------------- | -------------------------- |
| `add(E e)`            | Adds element to end        |
| `add(int index, E e)` | Inserts at specific index  |
| `get(int index)`      | Gets element at index      |
| `set(int index, E e)` | Replaces element           |
| `remove(int index)`   | Removes element by index   |
| `remove(Object o)`    | Removes first occurrence   |
| `clear()`             | Removes all elements       |
| `size()`              | Returns number of elements |
| `contains(Object o)`  | Checks if element exists   |
| `isEmpty()`           | Checks if empty            |
| `indexOf(Object o)`   | First index of element     |

we can directly print the list or use for each loop for printing...

--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
47) Set :-> Set is an interface in java.util that extends Collection. It represents a collection of unique elements — no duplicates allowed. Unlike List, a Set does not guarantee any specific order (unless you use certain implementations).

```
Set<String> names = new HashSet<>();
```

| Method               | Purpose                  |
| -------------------- | ------------------------ |
| `add(E e)`           | Add element              |
| `remove(Object o)`   | Remove element           |
| `contains(Object o)` | Check if element exists  |
| `size()`             | Number of elements       |
| `isEmpty()`          | Checks if empty          |
| `clear()`            | Removes all elements     |
| `iterator()`         | Iterate through elements |

in tree set we get sorted set but in hashset we get unordered set...

we can also use iterator as :
```
	Iterator<String> itor = list.iterator();
        while(itor.hasNext()){
            System.out.println(itor.next());
        }
```
--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
48) Map :-> Map is an interface in java.util — not a sub interface of Collection (it’s separate). It stores key-value pairs. Each key maps to one value. Keys must be unique, but values can be duplicated.
```
Map<Integer, String> map = new HashMap<>();
```

| Method                   | Purpose                               |
| ------------------------ | ------------------------------------- |
| `put(K key, V value)`    | Add/update key-value pair             |
| `get(K key)`             | Get value by key                      |
| `remove(K key)`          | Remove entry by key                   |
| `containsKey(K key)`     | Check if key exists                   |
| `containsValue(V value)` | Check if value exists                 |
| `keySet()`               | Get all keys                          |
| `values()`               | Get all values                        |
| `entrySet()`             | Get all key-value pairs (`Map.Entry`) |
| `size()`                 | Number of pairs                       |
| `isEmpty()`              | Check if empty                        |

--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
49) Comparator and Comparable :-> Both are interfaces in java.lang and java.util that help Java know how to compare objects — especially for sorting. 

comparable :-
	Interface: java.lang.Comparable<T>
	Used for: Natural ordering — defines the default way objects should be compared.
	You make your class itself implement Comparable and define compareTo().
	Collections.sort(list);

Comparator :-
	Interface: java.util.Comparator<T>
	Used for: Custom ordering — define multiple different ways to compare objects, outside the class.
	You do not change the class itself — you write separate Comparator logic.
 
use of comparator:
```
Comparator<Student> nameComparator = new Comparator<Student>() {
    @Override
    public int compare(Student s1, Student s2) {
        return s1.name.compareTo(s2.name); // sort by name
    }
};
```
in comparator 1 means swap and -1 means leave...
example : 
```
    public static void main(String[] args) {
        List<String> list = new ArrayList<>();

        list.add("hello");
        list.add("This");
        list.add("is");
        list.add("a");
        list.add("sample");
        list.add("code");

        Comparator <String> com = (o1,o2) -> o1.length() < o2.length() ? 1 : -1;

        Collections.sort(list,com);
        System.out.println(list);

    }

```
--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
50) Stream API :-> Part of Java 8+ (java.util.stream). A modern, functional-style way to process collections (lists, sets, arrays, etc.).
```
Makes it easy to:

	Filter
	Transform (map)
	Sort
	Aggregate (reduce)
	Collect results

```

It Lets you write declarative code instead of manual loops.

| Type         | Operation   | Purpose                                     |
| ------------ | ----------- | ------------------------------------------- |
| Intermediate | `filter()`  | Selects elements that match a condition     |
| Intermediate | `map()`     | Transforms each element                     |
| Intermediate | `sorted()`  | Sorts the elements                          |
| Terminal     | `collect()` | Gathers results into `List`, `Set`, etc.    |
| Terminal     | `forEach()` | Runs an action for each element             |
| Terminal     | `reduce()`  | Combines elements to produce a single value |
| Terminal     | `count()`   | Counts elements                             |

we can use one stream object only once...
--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
51) Optional class in java :-> when we use stream or do anything which can be null then there is chances of getting nullpointexception hence to prevent it this came in in Java 8 ...
 It may or may not contain a non-null value.
```
Optional<String> name = getNameOptional();
name.ifPresent(n -> System.out.println(n.toUpperCase()));
```
this will prevent from nullpointexception ...

 these are the methods used in this :-

| Method          | What it does                                                                       |
| --------------- | ---------------------------------------------------------------------------------- |
| `of()`          | Wrap a **non-null** value. Throws `NullPointerException` if value is null.         |
| `ofNullable()`  | Wrap a **nullable** value — can hold `null`.                                       |
| `empty()`       | Creates an empty `Optional`.                                                       |
| `isPresent()`   | Checks if a value is present.                                                      |
| `ifPresent()`   | Runs code if value is present.                                                     |
| `get()`         | Returns the value — throws `NoSuchElementException` if empty (should be avoided!). |
| `orElse()`      | Return value if present, else return default.                                      |
| `orElseGet()`   | Same as `orElse` but takes a **Supplier**.                                         |
| `orElseThrow()` | Throws custom exception if value is absent.                                        |
| `map()`         | Transform the value inside if present.                                             |
| `flatMap()`     | Similar to `map` but flattens nested `Optional`s.                                  |
| `filter()`      | Filters the value with a condition.                                                |

--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
52) Method Reference :-> A Method Reference is a shorthand for a lambda expression that simply calls an existing method. It’s a cleaner, shorter way to write lambdas that just call a method.

with lambda expression :
```
list.forEach(name -> System.out.println(name));
```
with Method refrence :
```
list.forEach(System.out::println);
```
Works perfectly with Streams, Lambdas, and functional interfaces (Predicate, Function, Consumer, etc)...

--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
53) Constructor References :-> A Constructor Reference is a method reference that points to a class constructor, instead of a method.

```
syntax : ClassName::new
```

```
	List<Person> people = names.stream()
              .map(Person::new)  // calls Person(String name)    
              .collect(Collectors.toList());

```
--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

```
				THE END! THANK YOU !
```
--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

```for Handwritten short note :```

[📄 View File on Google Drive](https://drive.google.com/file/d/19XVT6gk_G_er3VA67wtwfZYwnk0if7Fh/view?usp=sharing)
