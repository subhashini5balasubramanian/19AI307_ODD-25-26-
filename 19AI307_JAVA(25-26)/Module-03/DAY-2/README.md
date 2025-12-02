# Ex.No:3(B) POLYMORPHISM

## QUESTION:

Write a Java program to create a class **Vehicle** with a method called `speedUp()`. Create two subclasses **Car** and **Bicycle**.
Override the `speedUp()` method in each subclass to increase the vehicle's speed differently.

The program should:

* Take the vehicle type and speed input from the user.
* Create the appropriate object (Car or Bicycle).
* Call the overridden method to display the updated speed.

## AIM:

To write a Java program that demonstrates **polymorphism** by overriding the `speedUp()` method in subclasses Car and Bicycle, each implementing different behaviors for increasing speed.

## ALGORITHM :

1. Start the program.
2. Import the necessary package `java.util`.
3. Create a base class `Vehicle` with a default `speedUp()` method.
4. Create subclasses `Car` and `Bicycle` that override `speedUp()` with different implementations.
5. Read user input for vehicle type and speed.
6. Based on input, create the appropriate subclass object.
7. Invoke the overridden `speedUp()` method.
8. Display the result.
9. Stop the program.

## PROGRAM:

```
/*
Program to implement Polymorphism using Java
Developed by: Subhashini B
RegisterNumber: 212223040211
*/
```

## SOURCE CODE:

```
import java.util.*;
class Vehicle {
    int speed;

    void speedUp() {
        speed = 10;
    }
}

class Car extends Vehicle {
    void speedUp(int s) {
        speed = s*2; 
        System.out.printf("Car speed increased to: %d km/h",speed);
    }
}

class Bicycle extends Vehicle {
    void speedUp(int s) {
        speed = s; 
        System.out.printf("Bicycle speed increased to: %d km/h",speed);
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String veh = sc.nextLine();
        int s = sc.nextInt();
        if (veh.equals("car")){
            Car obj = new Car();
            obj.speedUp(s);
        }
        else if(veh.equals("bicycle")){
            Bicycle obj = new Bicycle();
            obj.speedUp(s);
        }
        else System.out.println("Invalid");
    }
}
```

## OUTPUT:
<img width="819" height="334" alt="Screenshot 2025-11-24 at 1 38 02 PM" src="https://github.com/user-attachments/assets/71d306c0-4a5e-4f98-a8ce-533dace63fdc" />

## RESULT:

Thus, the Java program demonstrating **polymorphism** through method overriding in Car and Bicycle classes was successfully executed.


