# Chapter-2 Content 

* [Variables in Java](#Variables-in-Java)
* [How to declare variables?](#How-to-declare-variables?)
* [Types of Variables](#Types-of-Variables)



## Variables in Java

A variable is a name given to a memory location. It is the basic unit of storage in a program.

- The value stored in a variable can be changed during program execution.
- A variable is only a name given to a memory location, all the operations done on the variable effects that memory location.
- In Java, all the variables must be declared before use.


## How to declare variables?

We can declare variables in java as follows:

img 

type: Type of data that can be stored in this variable.
name: Name given to the variable.
In this way, a name can only be given to a memory location. It can be assigned values in two ways:
- Variable Initialization
- Assigning value by taking input

img 

datatype: Type of data that can be stored in this variable.
variable_name: Name given to the variable.
value: It is the initial value stored in the variable.

Examples :

		float simpleInterest; //Declaring float variable
		int time = 10, speed = 20; //Declaring and Initializing integer variable
		char var = 'h'; // Declaring and Initializing character variable


## Types of Variables		
There are three types of variables in Java:

1) Local Variables
2) Instance Variables
3) Static Variables

*Local Variables:* A variable defined within a block or method or constructor is called local variable.

- These variable are created when the block in entered or the function is called and destroyed after exiting from the block or when the call returns from the function.
- The scope of these variables exists only within the block in which the variable is declared. i.e. we can access these variable only within that block.
- Initilisation of Local Variable is Mandatory.

INPUT :
```
public class StudentDetails { 
		public void StudentAge() 
	{ 
		// local variable age 
		int age = 0; 
		age = age + 5; 
		System.out.println("Student age is : " + age); 
	} 

	public static void main(String args[]) 
	{ 
		StudentDetails obj = new StudentDetails(); 
		obj.StudentAge(); 
	} 
} 
```

OUTPUT :
```
		Student age is : 5
``` 

*Instance Variables:* Instance variables are non-static variables and are declared in a class outside any method, constructor or block.

- As instance variables are declared in a class, these variables are created when an object of the class is created and destroyed when the object is destroyed.
- Unlike local variables, we may use access specifiers for instance variables. If we do not specify any access specifier then the default access specifier will be used.
- Initilisation of Instance Variable is not Mandatory. Its default value is 0
- Instance Variable can be accessed only by creating objects.

INPUT :

```
import java.io.*; 
class Marks { 
	// These variables are instance variables. 
	// These variables are in a class 
	// and are not inside any function 
	int engMarks; 
	int mathsMarks; 
	int phyMarks; 
} 

class MarksDemo { 
	public static void main(String args[]) 
	{ 
		// first object 
		Marks obj1 = new Marks(); 
		obj1.engMarks = 50; 
		obj1.mathsMarks = 80; 
		obj1.phyMarks = 90; 

		// second object 
		Marks obj2 = new Marks(); 
		obj2.engMarks = 80; 
		obj2.mathsMarks = 60; 
		obj2.phyMarks = 85; 

		// displaying marks for first object 
		System.out.println("Marks for first object:"); 
		System.out.println(obj1.engMarks); 
		System.out.println(obj1.mathsMarks); 
		System.out.println(obj1.phyMarks); 

		// displaying marks for second object 
		System.out.println("Marks for second object:"); 
		System.out.println(obj2.engMarks); 
		System.out.println(obj2.mathsMarks); 
		System.out.println(obj2.phyMarks); 
	} 
} 

```

OUTPUT :

```
Marks for first object:
50
80
90
Marks for second object:
80
60
85
```

*Static Variables:* Static variables are also known as Class variables.

- Unlike instance variables, we can only have one copy of a static variable per class irrespective of how many objects we create.
- Static variables are created at the start of program execution and destroyed automatically when execution ends.
- Initilisation of Static Variable is not Mandatory. Its default value is 0
- If we access the static variable like Instance variable (through an object), the compiler will show the warning message and it won’t halt the program. The compiler will replace the object name to class name automatically.
- If we access the static variable without the class name, Compiler will automatically append the class name.


To access static variables, we need not create an object of that class, we can simply access the variable as

		class_name.variable_name;

INPUT :
```
import java.io.*; 
class Emp { 

	// static variable salary 
	public static double salary; 
	public static String name = "Harsh"; 
} 

public class EmpDemo { 
	public static void main(String args[]) 
	{ 

		// accessing static variable without object 
		Emp.salary = 1000; 
		System.out.println(Emp.name + "'s average salary:"
						+ Emp.salary); 
	} 
} 
```

OUTPUT :

```
Harsh's average salary:1000.0
```




