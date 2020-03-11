# Content


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

**3)Int**

The int data type can store whole numbers from -2147483648 to 2147483647. In general, and in our tutorial, the int data type is the preferred data type when we create variables with a numeric value.
```
int myNum = 100000;
System.out.println(myNum);
```

**4)Long**

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
**8) Char**



