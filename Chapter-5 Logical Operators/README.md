# Introduction
This chapter continues our presentation of structured programming theory and principles
by introducing all but one of Java’s remaining control statements.

# Essentials of Counter-Controlled Repetition
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
# for Repetition Statement 
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

# do ... while Repetition Statement
The do ... while repetition statement is similar to the while statement. In the while , the program tests the loop continuation condition at the beginning of the loop, before executing the loop’s body; if the condition is false, the body never executes. The do ... while statement tests the loop-continuation condition after executing the loop’s body; therefore, the body always executes at least once.

```
          do {
              statement
            } while (expression) 
```








<p align="center">
  <img src="https://github.com/oilmcut-2020/GitHub-Tutorial/blob/master/images/git.png">
</p>

