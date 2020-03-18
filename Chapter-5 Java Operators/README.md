# Content
* [Java Operators](#Java-Operators)
* [1) Arithmetic Operators]((#1)-Arithmetic-Operators)
* [2) Relational Operators]((#2)-Relational-Operators)
* [3) Bitwise Operators]((#3)-Bitwise-Operators)
* [4) Logical Operators]((#4)-Logical-Operators)
* [5) Assignment Operators]((#5)-Assignment-Operators)



## Java Operators
Operators are special symbols (characters) that carry out operations on operands (variables and values). Java provides a rich set of operators to manipulate variables. We can divide all the Java operators into the following groups −

1) Arithmetic Operators
2) Relational Operators
3) Bitwise Operators
4) Logical Operators
5) Assignment Operators
    
## 1) Arithmetic Operators

Arithmetic operators are used to perform common mathematical operations.Arithmetic operators are used in mathematical expressions in the same way that they are used in algebra. 

<p align="center">
  <img src="https://github.com/oilmcut-2020/JavaClass/blob/master/Chapter-5%20Java%20Operators/Arithmetic_operators.png">
</p


Example :
INPUT
```
// Following is an example − Arithmetic Operator

public class Arithmetic{ 
      
    public static void main(String args[]) 
    { 
      
    int a = 10, b = 4, result; 
   
    //printing a and b 
    System.out.println("a is "+a+ " and b is "+ b); 
   
    result = a+b; //addition 
    System.out.println("a+b is "+result); 
   
    result = a-b; //subtraction 
    System.out.println("a-b is "+result); 
   
    result = a*b; //multiplication 
    System.out.println("a*b is "+result); 
   
    result = a/b; //division 
    System.out.println("a/b is "+result); 
   
    result = a%b; //modulus 
    System.out.println("a%b is "+result); 
      
    } 
} 
```

OUTPUT :

```
a + b = 30
a - b = 10
x + y = ThankYou
a * b = 200
a / b = 2
a % b = 0
```

## 2) Relational Operators
These operators are used to check for relations like equality, greater than, less than. They return boolean result after the comparison and are extensively used in looping statements as well as conditional if else statements. General format is, 
                   
           variable **relation_operator** value 
 Some of the relational operators are-

-  **==, Equal to :** returns true of left hand side is equal to right hand side.
- **!=, Not Equal to :** returns true of left hand side is not equal to right hand side.
- **<, less than :** returns true of left hand side is less than right hand side.
- **<=, less than or equal to :** returns true of left hand side is less than or equal to right hand side.
- **>, Greater than :** returns true of left hand side is greater than right hand side.
- **>=, Greater than or equal to:** returns true of left hand side is greater than or equal to right hand side.
 
 <p align="center">
  <img src="https://github.com/oilmcut-2020/JavaClass/blob/master/Chapter-5%20Java%20Operators/Relational_operators.png">
</p


Example :
INPUT
```
// Following is an example − Relational Operator

public class Relational{ 
      
    public static void main(String args[]) 
    { 
      
    int a=10, b=4; 
   
    // relational operators 
    // greater than example 
    if (a > b) 
        System.out.println("a is greater than b"); 
    else System.out.println("a is less than or equal to b"); 
   
    // greater than equal to 
    if (a >= b) 
        System.out.println("a is greater than or equal to b"); 
    else System.out.println("a is lesser than b"); 
   
    // less than example 
    if (a < b) 
        System.out.println("a is less than b"); 
    else System.out.println("a is greater than or equal to b"); 
   
    // lesser than equal to 
    if (a <= b) 
        System.out.println("a is lesser than or equal to b"); 
    else System.out.println("a is greater than b"); 
   
    // equal to 
    if (a == b) 
        System.out.println("a is equal to b"); 
    else System.out.println("a and b are not equal"); 
   
    // not equal to 
    if (a != b) 
        System.out.println("a is not equal to b"); 
    else System.out.println("a is equal b"); 
   
          
    } 
} 
```

OUTPUT :
```
a == b :false
a < b :false
a <= b :false
a > b :true
a >= b :true
a != b :true
x == y : false
condition==true :true
```

## 3) Bitwise Operators
These operators are used to perform manipulation of individual bits of a number. They can be used with any of the integer types. They are used when performing update and query operations of Binary indexed tree.

- **&, Bitwise AND operator:** returns bit by bit AND of input values.
- **|, Bitwise OR operator:** returns bit by bit OR of input values.
- **^, Bitwise XOR operator:** returns bit by bit XOR of input values.
- **~, Bitwise Complement Operator:** This is a unary operator which returns the one’s compliment representation of the input value, i.e. with all bits inversed.

<p align="center">
  <img src="https://github.com/oilmcut-2020/JavaClass/blob/master/Chapter-5%20Java%20Operators/Arithmetic_operators.png">
</p

Example :
INPUT
```
// Following is an example − Bitwise Operator

public class Bitwise { 
    public static void main(String[] args) 
    { 
        // if int a = 010 
        // Java considers it as octal value 
        // of 8 as number starts with 0. 
        int a = 0x0005; 
        int b = 0x0007; 
  
        // bitwise and 
        // 0101 & 0111=0101 
        System.out.println("a&b = " + (a & b)); 
  
        // bitwise and 
        // 0101 | 0111=0111 
        System.out.println("a|b = " + (a | b)); 
  
        // bitwise xor 
        // 0101 ^ 0111=0010 
        System.out.println("a^b = " + (a ^ b)); 
  
        // bitwise and 
        // ~0101=1010 
        System.out.println("~a = " + ~a); 
  
        // can also be combined with 
        // assignment operator to provide shorthand 
        // assignment 
        // a=a&b 
        a &= b; 
        System.out.println("a= " + a); 
    } 
} 
```

OUTPUT:
```
a&b = 5
a|b = 7
a^b = 2
~a = -6
a= 5
```

## 4) Logical Operators
These operators are used to perform “logical AND” and “logical OR” operation, i.e. the function similar to AND gate and OR gate in digital electronics. One thing to keep in mind is the second condition is not evaluated if the first one is false, i.e. it has a short-circuiting effect. Used extensively to test for several conditions for making a decision.
Conditional operators are-

- **&&, Logical AND :** returns true when both conditions are true.
- **||, Logical OR :** returns true if at least one condition is true.

<p align="center">
  <img src="https://github.com/oilmcut-2020/JavaClass/blob/master/Chapter-5%20Java%20Operators/Logical_operators.png">
</p
    
Example :
INPUT
```
//  Following is an example − Logical Operator

public class LogicalOperator {
    public static void main(String[] args) {
    	
    	int number1 = 1, number2 = 2, number3 = 9;
    	boolean result;
    	
    	// At least one expression needs to be true for result to be true
    	result = (number1 > number2) || (number3 > number1);
    	// result will be true because (number1 > number2) is true
    	System.out.println(result);
    			
    	// All expression must be true from result to be true	
    	result = (number1 > number2) && (number3 > number1);
    	// result will be false because	(number3 > number1) is false
    	System.out.println(result);
    }
}
```
OUTPUT:
```
true
false
```

## 5) Assignment Operators
Assignment operator is used to assign a value to any variable. It has a right to left associativity, i.e value given on right hand side of operator is assigned to the variable on the left and therefore right hand side value must be declared before using it or should be a constant.
General format of assignment operator is,

       variable = value;   
Example :
INPUT
```    
//  Following is an example − Assignment Operator

public class Assignment { 
    public static void main(String[] args) 
    { 
        int a = 20, b = 10, c, d, e = 10, f = 4, g = 9; 
  
        // simple assignment operator 
        c = b; 
        System.out.println("Value of c = " + c); 
  
        // This following statement would throw an exception 
        // as value of right operand must be initialised 
        // before assignment, and the program would not 
        // compile. 
        // c = d; 
  
        // instead of below statements, shorthand 
        // assignment operators can be used to 
        // provide same functionality. 
        a = a + 1; 
        b = b - 1; 
        e = e * 2; 
        f = f / 2; 
        System.out.println("a, b, e, f = " + a + ", "
                           + b + ", " + e + ", " + f); 
        a = a - 1; 
        b = b + 1; 
        e = e / 2; 
        f = f * 2; 
  
        // shorthand assignment operator 
        a += 1; 
        b -= 1; 
        e *= 2; 
        f /= 2; 
        System.out.println("a, b, e, f ("
                           + "using shorthand operators)= "
                           + a + ", " + b + ", "
                           + e + ", " + f); 
    } 
} 
```

OUTPUT:
```
Value of c = 10
a, b, e, f = 21, 9, 20, 2
a, b, e, f (using shorthand operators)= 21, 9, 20, 2
```
