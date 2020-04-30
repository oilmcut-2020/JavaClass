**Managed By- Shivani (M07158025)**

**Chapter : 03 "Introduction to Classes,Objects, Methods and Strings"**

Classes and Objects in Java. Classes and Objects are basic concepts of Object Oriented Programming which revolve around the real life entities. A class is a user defined blueprint or prototype from which objects are created. It represents the set of properties or methods that are common to all objects of one type.

## 3.1 Instance Variables, set Methods and get Methods
In this section, you’ll create two classes— Account (Fig. 3.1) and AccountTest (Fig. 3.2)Class AccountTest is an application class in which the main method will create and use an Account object to demonstrate class Account ’s capabilities.

<p align="center">
  <img src="https://github.com/oilmcut-2020/JavaClass/blob/master/Chapter-3%20Introduction%20to%20Classes%2CObjects%2CMethods%20%26%20Strings/FIG-3.1.png">
</p>

## 3.2.1 Account Class with an Instance Variable, a set Method and a get
Method Different accounts typically have different names. For this reason, class Account (Fig. 3.1) contains a name instance variable. A class’s instance variables maintain data for each object (that is, each instance) of the class.


**Class Declaration**

		public class Account

The keyword public is an access modifier. For now, we’ll simply declare every class public . Each public class declaration must be stored in a file
having the same name as the class and ending with the .java filename extension; otherwise,a compilation error will occur.

**Identifiers and Camel Case Naming**	

Class names, method names and variable names are all identifiers and by convention all use the 'same camel case' naming scheme we discussed in Chapter 2. Also by convention, class names begin with an initial uppercase letter, and method names and variable names begin with an initial lowercase letter.

**Instance Variable name**

Instance variables exist before methods are called on an object, while the methods are executing and after the methods complete exe-
cution. Each object (instance) of the class has its own copy of the class’s instance variables. A class normally contains one or more methods that manipulate the instance variables be- longing to particular objects of the class. Instance variables are declared inside a class declaration but outside the bodies of theclass’s methods.

		private String name; // instance variable


**Access Modifiers public and private**
Like public , private is an access modifier. Variables or methods declared with access modifier private are accessible only to methods of the class in which they’re declared. So, the variable name can be used only in each Account object’s methods ( setName and getName in this case).

The method’s return type (which appears before the method name) specifies the type of data the method returns to its caller after performing its task. The return type void (line 10) indicates that setName will perform a task but will not return (i.e., give back) anY information to its caller.

Method setName receives parameter name of type String —which represents the name that will be passed to the method as an argument.

**Parameters Are Local Variables**

Variables declared in a particular method’s body (such as main ) are local variables which can be used only in that method. Each method can access only its own local variables, not those of other methods. When a method terminates, the values of its local variables are lost. A method’s parameters also are local variables of the method.


## 3.2.2 AccountTest Class That Creates and Uses an Object of Class Account
Class Account cannot execute by itself because it does not contain a main method—if you type java Account in the command window, you’ll get an error indicating “ Main method not found in class Account .” To fix this problem, you must either declare a separate class that contains a main method
or place a main method in class Account .


**Driver Class AccountTest**

Once main begins executing, it may call other methods in this and other classes; those may, in turn, call other methods, and so on. Class AccountTest ’s main method creates one Account object and calls its getName and setName methods. Such a class is some times called a driver class—just as a Person object drives a Car object by telling it what to do (go faster, go slower, turn left, turn right, etc.), class AccountTest drives an Account object, telling it what to do by calling its methods.

<p align="center">
  <img src="https://github.com/oilmcut-2020/JavaClass/blob/master/Chapter-3%20Introduction%20to%20Classes%2CObjects%2CMethods%20%26%20Strings/FIG-3.2.png">
</p>


**Scanner Object for Receiving Input from the User**

Line 10 creates a Scanner object named input for inputting the name from the user. Line 19 prompts the user to enter a name. Line 20 uses the Scanner object’s nextLine method to read the name from the user and assign it to the local variable theName . You type the name and press Enter to submit it to the program. Pressing Enter inserts a newline character after the characters you typed. Method nextLine reads characters (including white-space charac-
ters, such as the blank in "Jane Green" ) until it encounters the newline, then returns a String containing the characters up to, but not including, the newline, which is discarded. Class Scanner provides various other input methods, as you’ll see throughout the book. A method similar to nextLine —named next —reads the next word. When you press Enter after typing some text, method next reads characters until it encounters a white-space character (such as a space, tab or newline), then returns a String containing the characters up to, but not including, the white-space character, which is discarded. All information after the first white-space character is not lost—it can be read by subsequent statements that call the Scanner ’s methods later in the program.


**Instantiating an Object—Keyword new and Constructors**


Variable myAccount is initialized with the result of the class instance creation expression new Account() . Keyword new creates a new object of the specified class—in this case, Ac- count . The parentheses to the right of Account are required.

**Calling Class Account ’s getName Method**

Line 16 displays the initial name, which is obtained by calling the object’s getName method. Just as we can use object System.out to call its methods print , printf and println , we can use object myAccount to call its methods getName and setName . Line 16 calls getName using the myAccount object created in line 13, followed by a dot separator ( . ), then the method name getName and an empty set of parentheses because no arguments are
being passed. When getName is called:
1. The app transfers program execution from the call (line 16 in main ) to method get- Name ’s declaration (lines 16–19 of Fig. 3.1). Because getName was called via the my- Account object, getName “knows” which object’s instance variable to manipulate.

2. Next, method getName performs its task—that is, it returns the namae, When the return statement executes, program execution continues
where getName was called (line 16 in Fig. 3.2).

3. System.out.printf displays the String returned by method getName , then the program continues executing at line 19 in main .


## 3.2.3 Compiling and Executing an App with Multiple Classes

You must compile the classes in Figs. 3.1 and 3.2 before you can execute the app. This is the first time you’ve created an app with multiple classes. Class AccountTest has a main method; class Account does not. To compile this app, first change to the directory that contains the app’s source-code files. Next, type the command

		javac Account.java AccountTest.java

to compile both classes at once. If the directory containing the app includes only this app’s files, you can compile both classes with the command.

		javac *.java


The asterisk ( * ) in *.java indicates that all files in the current directory ending with the filename extension “ .java ” should be compiled. If both classes compile correctly—that is, no compilation errors are displayed—you can then run the app with the command.

		java AccountTest


## 3.2.4 Account UML Class Diagram with an Instance Variable and set and get Methods


We’ll often use UML class diagrams to summarize a class’s attributes and operations. In industry, UML diagrams help systems designers specify a system in a concise, graphical, programming-language-independent manner, before programmers implement the system in a specific programming language. Figure 3.3 presents a UML class diagram for class Account of Fig. 3.1.

**Top Compartment**

In the UML, each class is modeled in a class diagram as a rectangle with three compartments. In this diagram the top compartment contains the class name Account centered horizontally in boldface type.

<p align="center">
  <img src="https://github.com/oilmcut-2020/JavaClass/blob/master/Chapter-3%20Introduction%20to%20Classes%2CObjects%2CMethods%20%26%20Strings/FIG-3.3.png">
</p>

**Middle Compartment**
The middle compartment contains the class’s attribute name , which corresponds to the instance variable of the same name in Java. Instance variable name is private in Java, so the UML class diagram lists a minus sign ( – ) access modifier before the attribute name. Following the attribute name are a colon and the attribute type, in this case String .

**Bottom Compartment**
The bottom compartment contains the class’s operations, setName and getName , which correspond to the methods of the same names in Java. The UML models operations by listing the operation name preceded by an access modifier, in this case + getName . This plus sign ( + ) indicates that getName is a public operation in the UML (because it’s a public method in Java). Operation getName does not have any parameters, so the parentheses fol-
lowing the operation name in the class diagram are empty, just as they are in the method’s declaration in line 16 of Fig. 3.1. Operation setName , also a public operation, has a String parameter called name .

**Return Types**
The UML indicates the return type of an operation by placing a colon and the return type after the parentheses following the operation name. Account method getName (Fig. 3.1) has a String return type. Method setName does not return a value (because it returns void in Java), so the UML class diagram does not specify a return type after the parentheses of this operation. 

**Parameters**
The UML models a parameter a bit differently from Java by listing the parameter name, followed by a colon and the parameter type in the parentheses after the operation name. The UML has its own data types similar to those of Java, but for simplicity, we’ll use the
Java data types.

# 3.3 Primitive Types vs. Reference Types

Java’s types are divided into primitive types and reference types. The other primitive types are boolean , byte , char , short , long , float and double.
All nonprimitive types are reference types, so classes, which specify the types of objects, are reference types.
A primitive-type variable can hold exactly one value of its declared type at a time. For example, an int variable can store one integer at a time. When another value is assigned to that variable, the new value replaces the previous one—which is lost.
Primitive-type instance variables are initialized by default—instance variables of types byte , char , short , int , long , float and double are initialized to 0, and variables of type boolean are initialized to false . You can specify your own initial value for a primitive-type variable by assigning the variable a value in its declaration, as in

		private int numberOfStudents = 10;

Programs use variables of reference types (normally called references) to store the addresses of objects in the computer’s memory. Such a variable is said to refer to an object in the program. Objects that are referenced may each contain many instance variables.

		Scanner input = new Scanner(System.in);

creates an object of class Scanner , then assigns to the variable Scanner object.

		Account myAccount = new Account();


# 3.4 Account Class: Initializing Objects with Constructors
		
Each class you declare can optionally provide a constructor with parameters that can be used to initialize an object of a class when the object is created. Java requires a constructor call for every object that’s created, so this is the ideal point to initialize an object’s instance variables.

## 3.4.1 Declaring an Account Constructor for Custom Object Initialization

When you declare a class, you can provide your own constructor to specify custom initialization for objects of your class.

		Account account1 = new Account("Jane Green");
		
In this case, the String argument "Jane Green" is passed to the Account object’s construc- tor and used to initialize the name instance variable. The preceding statement requires that the class provide a constructor that takes only a String parameter.

<p align="center">
  <img src="https://github.com/oilmcut-2020/JavaClass/blob/master/Chapter-3%20Introduction%20to%20Classes%2CObjects%2CMethods%20%26%20Strings/FIG-3.4.png">
</p>

**Fig. 3.4 Account class with a constructor that initializes the name**

**Account Constructor Declaration**

Lines 9–12 of Fig. 3.4 declare Account ’s constructor. A constructor must have the same name as the class. A constructor’s parameter list specifies that the constructor requires one or more pieces of data to perform its task. Line 9 indicates that the constructor has a String parameter called name .

# 3.5 (Optional) GUI and Graphics Case Study: Using Dialog Boxes
 
This optional case study is designed for those who want to begin learning Java’s powerful capabilities for creating graphical user interfaces (GUIs) and graphics early in the book, before the deeper discussions of these topics later in the book. This case study features Java’s mature Swing technology, which as of this writing is still a bit more popular than the newer JavaFX technology presented in later chapters.

**Displaying Text in a Dialog Box**

The programs presented thus far display output in the command window. Many apps use windows or dialog boxes (also called dialogs) to display output. Web browsers such as Chrome, Firefox, Internet Explorer, Safari and Opera display web pages in their own win- dows. E-mail programs allow you to type and read messages in a window. Typically, dialog boxes are windows in which programs display important messages to users. Class JOption- Pane provides prebuilt dialog boxes that enable programs to display windows containing messages—such windows are called message dialogs.

<p align="center">
  <img src="https://github.com/oilmcut-2020/JavaClass/blob/master/Chapter-3%20Introduction%20to%20Classes%2CObjects%2CMethods%20%26%20Strings/FIG-3.5.png">
</p>

**Fig. 3.5 Account class with a constructor that initializes the name . **

**JOptionPane Class static Method showMessagDialog**
Line 3 indicates that the program uses class JOptionPane from package javax.swing . This package contains many classes that help you create graphical user interfaces (GUIs). GUI components facilitate data entry by a program’s user and presentation of outputs to the user. Line 10 calls JOptionPane method showMessageDialog to display a dialog box containing a message. The method requires two arguments. The first helps the Java app de- termine where to position the dialog box. A dialog is typically displayed from a GUI app with its own window. The first argument refers to that window (known as the parent win-
dow) and causes the dialog to appear centered over the app’s window. If the first argument is null , the dialog box is displayed at the center of your screen. The second argument is the String to display in the dialog box.

**Introducing static Methods**
JOptionPane method showMessageDialog is a so-called static method. Such methods often define frequently used tasks. For example, many programs display dialog boxes, and the code to do this is the same each time. Rather than requiring you to “reinvent the wheel” and create code to display a dialog, the designers of class JOptionPane declared a static method that performs this task for you. A static method is called by using its class name followed by a dot ( . ) and the method name, as:

	ClassName . methodName ( arguments )
	
**Enetring Text in a Dialog**

It uses another predefined JOptionPane dialog called an input dialog that allows the user to enter data into a program. The program asks for the user’s name and responds with a message dialog containing a greeting and the name that the user entered

<p align="center">
  <img src="https://github.com/oilmcut-2020/JavaClass/blob/master/Chapter-3%20Introduction%20to%20Classes%2CObjects%2CMethods%20%26%20Strings/FIG-3.6.png">
</p>

**Fig.3.6 Obtaining user input from a dialog. **

