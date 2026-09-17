# Ex.No:3(E) INNER CLASS

## QUESTION:

Write a Java program where the inner class is declared private and accessed through a method in the outer class.


## AIM:

To demonstrate accessing a private inner class in Java through a public method of the outer class.




## ALGORITHM :

Start the program.

Create a Scanner object to take integer input from the user.

Read an integer value from the user.

Create an object of the OuterClass.

Call the accessInner() method of OuterClass, passing the input value.

Inside accessInner(), create an object of the private inner class InnerClass.

Call the setData() method of InnerClass to store and print the value.

Close the scanner.

End the program.







## PROGRAM:
 ```
/*
Program to implement a InnerClass using Java
Developed by: KIRUTHIGA.B
RegisterNumber: 212224040160 
*/
```

## SOURCE CODE:

```
import java.util.Scanner;

public class OuterClass {
    
    private class InnerClass {
        private int data;

        void setData(int value) {
            data = value;
            System.out.println("Data set inside private inner class: " + data);
        }
    }

    void accessInner(int value) {
        InnerClass inner = new InnerClass();
        inner.setData(value);
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int value = sc.nextInt();
        
        OuterClass outer = new OuterClass();
        outer.accessInner(value);
        
        sc.close();
    }
}
```







## OUTPUT:

<img width="782" height="296" alt="image" src="https://github.com/user-attachments/assets/53d9be93-3757-46f1-b60a-a5be163a0db7" />




## RESULT:

The private inner class is successfully invoked using an outer-class method.
