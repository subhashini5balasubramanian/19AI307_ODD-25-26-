# Ex.No:2(E) ACCESS MODIFIERS

## QUESTION:

Create a Java program that defines a class **Calculator** with one non-static method `add(int a, int b)` that returns the sum of two integers, and one static method `info()` that prints **"Calculator is ready"**. The program should read two integers from the user, call the static method, invoke the non-static method using an object, and display the sum.

## AIM:

To write a Java program that demonstrates the use of static and non-static methods by implementing a Calculator class with an addition function and an informational static method.

## ALGORITHM :

1. Start the program.
2. Import the necessary package `java.util`.
3. Create the `Calculator` class with:

* A non-static method `add()` to return the sum of two numbers.
* A static method `info()` to print a message.

4. In the main method, read two integers from the user.
5. Call the static method `info()` directly using the class name.
6. Create an object of `Calculator` and call the `add()` method.
7. Display the sum.
8. Stop the program.

## PROGRAM:

```
/*
Program to implement a Access Modifiers using Java
Developed by: Subhashini B
RegisterNumber: 212223040211
*/
```

## SOURCE CODE:

```
import java.util.Scanner;

class Calculator {
    int add(int a, int b) {
        return a+b;
    }
    static void info() {
        System.out.println("Calculator is ready");
    }
}

class prog {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        Calculator.info();
        Calculator obj = new Calculator();
        System.out.println("Sum: " + obj.add(sc.nextInt(), sc.nextInt()));
    }
}
```

## OUTPUT:
<img width="580" height="314" alt="Screenshot 2025-11-24 at 1 32 25 PM" src="https://github.com/user-attachments/assets/f163daee-ea73-4130-83e3-804512be9688" />


## RESULT:

Thus, the Java program demonstrating static and non-static methods using a Calculator class was successfully executed and verified.


