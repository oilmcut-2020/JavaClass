# 5.1) Introduction
This chapter continues our presentation of structured programming theory and principles
by introducing all but one of Java’s remaining control statements.

# 5.2) Essentials of Counter-Controlled Repetition
Elements required to perform counter-controlled repetition, which requires :

1. a control variable (or loop counter)

2. the initial value of the control variable

3. the increment by which the control variable is modified each time through theloop (also known as each iteration of the loop)

4. the loop-continuation condition that determines if looping should continue.
Example which uses a loop to display the numbers from 1 through 10.

```
// Counter-controlled repetition with the while repetition statement.
public class WhileCounter
{
  public static void main(String[] args)
  {
    int counter = 1; // declare and initialize control variable
    while ( counter <= 10 ) // loop-continuation condition
    {
      System.out.printf("%d ", counter);
    ++counter; // increment control variable
    }
    
  System.out.println();
  }
} // end class WhileCounter
```

Output :
```
    1  2  3  4  5  6  7  8  9  10
```
# 5.3) for Repetition Statement 
The while statement can be used to implement any counter-controlled loop. Java also provides the for repetition statement, which specifies the counter-controlled-repetition details in a single line of code.

```
// Counter-controlled repetition with the for repetition statement.
public class ForCounter
{
    public static void main(String[] args)
    {
    
    // for statement header includes initialization,
    // loop-continuation condition and increment
    
    for (int counter = 1; counter <= 10; counter++)
      System.out.printf("%d ", counter);
      System.out.println();
    }
} // end class ForCounter
```
Output :
```
    1  2  3  4  5  6  7  8  9  10
```

When the for statement (lines 10–11) begins executing, the control variable counter is declared and initialized to 1 .
Next, the program checks the loop-continuation condition, counter <= 10 , which is between the two required semicolons. Because the initial value of counter is 1 , the condition initially is true. Therefore, the body statement (line 11) displays control variable counter ’s value, namely 1 . After executing the loop’s body, the program increments counter in the expression counter++ , which appears to the right of the second semicolon. Then the loop-continuation test is performed again to determine whether the program should continue with the next iteration of the loop.

# 5.4) do ... while Repetition Statement
The do ... while repetition statement is similar to the while statement. In the while , the program tests the loop continuation condition at the beginning of the loop, before executing the loop’s body; if the condition is false, the body never executes. The do ... while statement tests the loop-continuation condition after executing the loop’s body; therefore, the body always executes at least once.

```
          do {
              statement
            } while (expression) 
```

# 5.5) switch Multiple-Selection Statement

The switch multiple-selection statement performs different actions based on the possible values of a constant integral expression of type byte , short , int or char

```
  //switch (variable or an integer expression)
    {
      case constant:
      //C++ code
      ;
       case constant:
      //C++ code
      ;
     default:
     //C++ code
     ;
    }
 ```   

Switch Case statement is mostly used with break statement even though the break statement is optional.
Example of Switch Case:
```
      #include <iostream>
      using namespace std;
      int main(){
           int num=5;
           switch(num+2) {
              case 1: 
                cout<<"Case1: Value is: "<<num<<endl;
              case 2: 
               cout<<"Case2: Value is: "<<num<<endl;
              case 3: 
                 cout<<"Case3: Value is: "<<num<<endl;
              default: 
                  cout<<"Default: Value is: "<<num<<endl;
                }
              return 0;
            }
```

Output :

    Default: Value is: 5
    
<p align="center">
  <img src="https://github.com/oilmcut-2020/JavaClass/blob/master/Chapter-5%20Logical%20Operators/switch.png">
</p>

# 5.6) break and continue Statements

*break statement:*

The break statement, when executed in a while , for , do ... while or switch , causes immediate exit from that statement. Execution continues with the first statement after the control statement. Common uses of the break statement are to escape early from a loop or to skip the remainder of a switch.

```
// break statement exiting a for statement.
    public class BreakTest
  {
    public static void main(String[] args)
  {
  int count; // control variable also used after loop terminates
  
  for (count = 1; count <= 10; count++) // loop 10 times
  {
  if (count == 5)
    break; // terminates loop if count is 5
      System.out.printf("%d ", count);
  }
      System.out.printf("%nBroke out of loop at count = %d%n", count);
  }
  } // end class BreakTest
```
Output :

    1 2 3 4
    Broke out of loop at count = 5
    
    
*continue statement:*

The continue statement, when executed in a while , for or do ... while , skips the remaining statements in the loop body and proceeds with the next iteration of the loop. In while and do ... while statements, the program evaluates the loop-continuation test immediately after the continue statement executes. In a for statement, the increment expression executes, then the program evaluates the loop-continuation test

```
  // continue statement terminating an iteration of a for statement.
  public class ContinueTest
  {
  public static void main(String[] args)
  {
    for (int count = 1; count <= 10; count++) // loop 10 times
  {
    if (count == 5)
    continue; // skip remaining code in loop body if count is 5
      System.out.printf("%d ", count);
  }
    System.out.printf("%nUsed continue to skip printing 5%n");
}
} // end class ContinueTest
```
Output :

    1 2 3 4 6 7 8 9 10
    Used continue to skip printing 5
    
 #  5.7) Logical Operators
 
The if , if ... else , while , do ... while and for statements each require a condition to de-termine how to continue a program’s flow of control. So far, we’ve studied only simple conditions, such as count <= 10 , number != sentinelValue and total > 1000 . Simple conditions are expressed in terms of the relational operators > , < , >= and <= and the equality operators == and != , and each expression tests only one condition. To test multiple conditions in the process of making a decision, we performed these tests in separate statements or in nested if or if ... else statements.

<p align="center">
  <img src="https://github.com/oilmcut-2020/JavaClass/blob/master/Chapter-5%20Logical%20Operators/logical.png">
</p>

**Conditional AND ( && ) Operator**
In this case, we can use the && (conditional AND) operator, as follows:

    if (gender == FEMALE && age >= 65)
    ++seniorFemales;
    
**Conditional OR ( || ) Operator**    
In this case, we use the || (conditional OR) operator, as in the following program segment:

    if ((semesterAverage >= 90) || (finalExam >= 90))
    System.out.println ("Student grade is A");
    
**Boolean Logical AND ( & ) and Boolean Logical Inclusive OR ( | ) Operators**    
The boolean logical AND ( & ) and boolean logical inclusive OR ( | ) operators are identical to the && and || operators, except that the & and | operators always evaluate both of their operands (i.e., they do not perform short-circuit evaluation). So, the expression:

    (gender == 1) & (age >= 65)
    
evaluates age >= 65 regardless of whether gender is equal to 1 . This is useful if the right operand has a required side effect—a modification of a variable’s value. For example, the expression: 

    (birthday == true) | (++age >= 65)
    
    
**Precedence and Associativity of the Operators**
The operators are shown from top to bottom in decreasing order of precedence.

<p align="center">
  <img src="https://github.com/oilmcut-2020/JavaClass/blob/master/Chapter-5%20Logical%20Operators/Precedence.png">
</p>

<p align="center">
  <img src="https://github.com/oilmcut-2020/JavaClass/blob/master/Chapter-5%20Logical%20Operators/Associate.png">
</p>






