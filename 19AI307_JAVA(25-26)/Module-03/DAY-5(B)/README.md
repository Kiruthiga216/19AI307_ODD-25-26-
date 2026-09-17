# Ex.No:3(F) WRAPPER CLASS

## QUESTION:

Write a Java program that uses the Boolean wrapper class in conditional logic to determine a pass/fail result.


## AIM:

To demonstrate using the Boolean wrapper class in conditional logic to determine pass/fail in Java.




## ALGORITHM :

Start the program.

Create a Scanner object to take input from the user.

Read the integer value marks from the user.

Use the Boolean wrapper class to store the condition marks >= 50 in isPass.

If isPass is true, print "Result: Pass".

Otherwise, print "Result: Fail".

Close the scanner.

End the program.





## PROGRAM:
 ```
/*
Program to implement a Wrapper Class using Java
Developed by: KIRUTHIGA.B
RegisterNumber:  212224040160
*/
```

## SOURCE CODE:

```
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int marks = sc.nextInt();

        Boolean isPass = marks >= 50;  

        if (isPass) {
            System.out.println("Result: Pass");
        } else {
            System.out.println("Result: Fail");
        }

        sc.close();
    }
}
```







## OUTPUT:

<img width="488" height="263" alt="image" src="https://github.com/user-attachments/assets/a5432712-17eb-42a7-b3cb-70ff62468d49" />




## RESULT:

The program evaluates a Boolean condition using Boolean and displays whether the student passed or failed.
