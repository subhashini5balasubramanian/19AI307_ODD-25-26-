# Ex.No:3(A) INHERITANCE AND AGGREGATION

## QUESTION:

Create a Super class **Vehicle** with fields **brand (String)** and **speed (int)**. Create a subclass **Car** that inherits from Vehicle and adds a field **fuelType (String)**.
Implement a method in **Car** called **displayInfo()** that prints the vehicle's brand, speed, and fuel type.
Write a program that:

* Takes input for brand, speed, and fuel type using Scanner.
* Creates a Car object.
* Calls displayInfo() to print the details.

## AIM:

To write a Java program that demonstrates **inheritance** by creating a superclass *Vehicle* and a subclass *Car*, and to display the vehicle details using a method in the subclass.

## ALGORITHM :

1. Start the program.
2. Import the necessary package 'java.util'.
3. Create a **Vehicle** class with fields brand and speed.
4. Create a **Car** class extending Vehicle and add fuelType.
5. Define the **displayInfo()** method to print all details.
6. In the main method, read brand, speed, and fuel type from the user.
7. Create an object of Car and call displayInfo().
8. Stop the program.

## PROGRAM:

```
/*
Program to implement Inheritance and Aggregation using Java
Developed by: Subhashini B
RegisterNumber: 212223040211
*/
```

## SOURCE CODE:

```
import java.util.*;

class Vehicle {
    String brand;
    int speed;
}

class Car extends Vehicle {
    String fuelType;

    void displayInfo() {
        System.out.printf("Brand: %s\nSpeed: %d km/h\nFuel Type: %s", brand, speed, fuelType);
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        Car obj = new Car();
        obj.brand = sc.nextLine();  
        obj.speed = sc.nextInt();  
        sc.nextLine();
        obj.fuelType = sc.nextLine();

        obj.displayInfo();
    }
}
```

## OUTPUT:
<img width="725" height="379" alt="Screenshot 2025-11-24 at 1 35 42 PM" src="https://github.com/user-attachments/assets/d9e784be-7767-41f0-bc9d-80a7a0330eb5" />

## RESULT:

Thus, the Java program demonstrating inheritance using Vehicle and Car classes was successfully executed.


