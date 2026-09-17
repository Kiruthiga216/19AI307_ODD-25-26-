# Ex.No:2(B) METHODS

## QUESTION:

Write a method int cube(int x) that calls a method int square(int x) internally to calculate the cube as x * square(x).


## AIM:

To write a Java program that defines a method cube(int x) which internally calls the method square(int x) to compute the cube of a number.


## ALGORITHM :

Define a class demo with two methods:

square(int n) → returns n * n. cube(int n) → returns n * square(n) by calling the square() method internally.

In the main class, read an integer input from the user.

Create an object of the demo class.

Call the cube() method using the object and print the result.

End the program.





## PROGRAM:
 ```
/*
Program to implement a Methods using Java
Developed by: KIRUTHIGA.B
RegisterNumber:  212224040160
*/
```

## SOURCE CODE:

```
import java.util.*;
class demo
{
    public int square(int n)
    {
        return n*n;
    }
    public int cube(int n)
    {
        return n*square(n);
    }
    
}
public class main
{
    public static void main(String[] args)
    {
        Scanner sc=new Scanner(System.in);
        int n=sc.nextInt();
        demo d=new demo();
        System.out.println(d.cube(n));
    }
}
```







## OUTPUT:

<img width="415" height="172" alt="image" src="https://github.com/user-attachments/assets/d8011192-2961-48fe-8b1e-c09c5e8351be" />




## RESULT:

Therefore the program successfully computes the cube of a number by internally using the square method.
