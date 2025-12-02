# Ex.No:3(C) ABSTRACTION

## QUESTION:

Create an abstract class **TaxPayer** with an abstract method `calculateTax()`.
Create two subclasses **SalariedPerson** and **BusinessPerson**, each implementing their respective tax calculation logic.

## AIM:

To write a Java program that demonstrates **abstraction** using an abstract class and method, implemented differently in subclasses for tax calculation.

## ALGORITHM :

1. Start the program.
2. Import the necessary package `java.util`.
3. Create an abstract class `TaxPayer` with an abstract method `calculateTax()`.
4. Create subclasses `SalariedPerson` and `BusinessPerson` that override `calculateTax()` with specific tax rules.
5. Read taxpayer type and income from the user.
6. Use conditional logic to create the appropriate subclass object.
7. Call `calculateTax()` and print the tax.
8. Stop the program.

## PROGRAM:

```
/*
Program to implement Abstraction using Java
Developed by: Subhashini B
RegisterNumber: 212223040211
*/
```

## SOURCE CODE:

```
import java.util.*;

abstract class TaxPayer {
    double income;
    TaxPayer(double income) {
        this.income = income;
    }
    abstract double calculateTax();
}

class SalariedPerson extends TaxPayer {
    SalariedPerson(double income) {
        super(income);
    }
    double calculateTax() {
        return income * 0.10;
    }
}

class BusinessPerson extends TaxPayer {
    BusinessPerson(double income) {
        super(income);
    }
    double calculateTax() {
        return income * 0.15;
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int type = sc.nextInt();
        double income = sc.nextDouble();
        TaxPayer p = (type == 1) ? new SalariedPerson(income) : new BusinessPerson(income);
        System.out.printf("%.2f\n", p.calculateTax());
    }
}
```

## OUTPUT:
<img width="505" height="381" alt="Screenshot 2025-11-24 at 1 39 58 PM" src="https://github.com/user-attachments/assets/e0575e53-a317-4a5c-8294-32c4b4477903" />


## RESULT:

Thus, the Java program implementing **abstraction** using an abstract class TaxPayer and its subclasses was successfully executed.



