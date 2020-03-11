# Content

* [Java Data Types](#Java-Data-Types)
* [Primitive Data Types](#Primitive-Data-Types)
* [Non-Primitive Data Types](#Non-Primitive-Data-Types)

## Java Data Types
Data types specify the different sizes and values that can be stored in the variable.


        int myNum = 5;               // Integer (whole number)

        float myFloatNum = 5.99f;    // Floating point number

        char myLetter = 'D';         // Character

        boolean myBool = true;       // Boolean

        String myText = "Hello";     // String
       
        
        
There are two types of data types in Java:

1) **Primitive data types:** The primitive data types include boolean, char, byte, short, int, long, float and double.

2) **Non-primitive data types:** The non-primitive data types include Classes, Interfaces, and Arrays.
       
<p align="center">
  <img src="https://github.com/oilmcut-2020/JavaClass/blob/master/Chapter-4%20Data%20Types/data-types.png">
</p>

## Primitive Data Types

There are eight primitive datatypes supported by Java. Primitive datatypes are predefined by the language and named by a keyword.
<p align="center">
  <img src="https://github.com/oilmcut-2020/JavaClass/blob/master/Chapter-4%20Data%20Types/table.png">
</p>

*Integer Types*

**1) Byte**

The byte data type can store whole numbers from -128 to 127. This can be used instead of int or other integer types to save memory when you are certain that the value will be within -128 and 127:
```
byte myNum = 100;
System.out.println(myNum);
```

**2) Short**

The short data type can store whole numbers from -32768 to 32767:
```
short myNum = 5000;
System.out.println(myNum);
```

**3) Int**

The int data type can store whole numbers from -2147483648 to 2147483647. In general, and in our tutorial, the int data type is the preferred data type when we create variables with a numeric value.
```
int myNum = 100000;
System.out.println(myNum);
```

**4) Long**

The long data type can store whole numbers from -9223372036854775808 to 9223372036854775807. This is used when int is not large enough to store the value. Note that you should end the value with an "L":
```
long myNum = 15000000000L;
System.out.println(myNum);
```

*Floating Point Types*

**5) Float**

The float data type can store fractional numbers from 3.4e−038 to 3.4e+038. Note that you should end the value with an "f":
```
float myNum = 5.75f;
System.out.println(myNum);
```
**6) Double**

The double data type can store fractional numbers from 1.7e−308 to 1.7e+308. Note that you should end the value with a "d":
```
double myNum = 19.99d;
System.out.println(myNum);
```

**7) Booleans**

A boolean data type is declared with the boolean keyword and can only take the values true or false:
```
boolean isJavaFun = true;
boolean isFishTasty = false;
System.out.println(isJavaFun);     // Outputs true
System.out.println(isFishTasty);   // Outputs false
```

**8) Char**

The char data type is used to store a single character. The character must be surrounded by single quotes, like 'A' or 'c':
```
char myGrade = 'B';
System.out.println(myGrade);
```

## Non-primitive Data Types
Non-primitive data types are called reference types because they refer to objects.

The main difference between primitive and non-primitive data types are:

- Primitive types are predefined (already defined) in Java. Non-primitive types are created by the programmer and is not defined by Java (except for String).
- Non-primitive types can be used to call methods to perform certain operations, while primitive types cannot.
- A primitive type has always a value, while non-primitive types can be null.
- A primitive type starts with a lowercase letter, while non-primitive types starts with an uppercase letter.
- The size of a primitive type depends on the data type, while non-primitive types have all the same size.


**1) Strings**

Strings are defined as an array of characters. The difference between a character array and a string is the string is terminated with a special character ‘\0’. 
```
// Declare String without using new operator 
String s = "programming"; 

// Declare String using new operator 
String s1 = new String("Welcome to Java Programming"); 
```
**2) Arrays**

An array is a group of like-typed variables that are referred to by a common name.Arrays in Java work differently than they do in C/C++. In Java all arrays are dynamically allocated.
- Since arrays are objects in Java, we can find their length using member length. This is different from C/C++ where we find length using sizeof.
- A Java array variable can also be declared like other variables with [] after the data type.
- The variables in the array are ordered and each have an index beginning from 0.
- Java array can be also be used as a static field, a local variable or a method parameter.
- The size of an array must be specified by an int value and not long or short.
- The direct superclass of an array type is Object. 

**3) Class**

A class is a user-defined blueprint or prototype from which objects are created.  It represents the set of properties or methods that are common to all objects of one type. In general, class declarations can include these components, in order:

- Modifiers : A class can be public or has default access (Refer this for details).
- Class name: The name should begin with a initial letter (capitalized by convention).
- Superclass(if any): The name of the class’s parent (superclass), if any, preceded by the keyword extends. A class can only extend (subclass) one parent.
- Interfaces(if any): A comma-separated list of interfaces implemented by the class, if any, preceded by the keyword implements. A class can implement more than one interface.
- Body: The class body surrounded by braces, { }.
