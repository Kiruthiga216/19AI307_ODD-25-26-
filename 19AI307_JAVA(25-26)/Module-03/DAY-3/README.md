# Ex.No:3(C) ABSTRACTION

## QUESTION:

Create an abstract class Employee with method calculatePay(). Extend it to HourlyEmployee and SalariedEmployee.

Input Format:

The first line contains an integer: 1 → for HourlyEmployee
2 → for SalariedEmployee

If input is 1 (HourlyEmployee): The second line contains two values:

hours worked (integer)
rate per hour (double)
If input is 2 (SalariedEmployee): The second line contains one value:

monthly salary (double)
Output Format:

A single line containing the calculated pay formatted to two decimal places.


## AIM:

To implement an abstract class Employee with a method calculatePay() and extend it to HourlyEmployee and SalariedEmployee to compute employee pay.




## ALGORITHM :

Read the employee type (1 for hourly, 2 for salaried).

If type is 1, read hours worked and rate per hour, then calculate pay = hours × rate.

If type is 2, read monthly salary and set pay = salary.

Use the respective subclass (HourlyEmployee or SalariedEmployee) to compute pay through calculatePay().

Print the final pay formatted to two decimal places.







## PROGRAM:
 ```
/*
Program to implement a Abstraction using Java
Developed by: KIRUTHIGA.B
RegisterNumber:  212224040160
*/
```

## SOURCE CODE:

```
import java.util.Scanner;

abstract class Employee {
    abstract double calculatePay();
}

class HourlyEmployee extends Employee {
    int hoursWorked;
    double ratePerHour;

    HourlyEmployee(int hoursWorked, double ratePerHour) {
        this.hoursWorked = hoursWorked;
        this.ratePerHour = ratePerHour;
    }

    @Override
    double calculatePay() {
        return hoursWorked * ratePerHour;
    }
}

class SalariedEmployee extends Employee {
    double monthlySalary;

    SalariedEmployee(double monthlySalary) {
        this.monthlySalary = monthlySalary;
    }

    @Override
    double calculatePay() {
        return monthlySalary;
    }
}

public class prog {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int type = sc.nextInt();
        double pay = 0.0;

        if (type == 1) {
            int hours = sc.nextInt();
            double rate = sc.nextDouble();
            Employee e = new HourlyEmployee(hours, rate);
            pay = e.calculatePay();
        } else if (type == 2) {
            double salary = sc.nextDouble();
            Employee e = new SalariedEmployee(salary);
            pay = e.calculatePay();
        }

        System.out.printf("%.2f\n", pay);
        sc.close();
    }
}
```







## OUTPUT:

<img width="392" height="277" alt="image" src="https://github.com/user-attachments/assets/09eeac14-533a-499a-b52e-7a45632c6cf2" />




## RESULT:

Successfully calculated and displayed the pay for either an HourlyEmployee or SalariedEmployee based on user input.
