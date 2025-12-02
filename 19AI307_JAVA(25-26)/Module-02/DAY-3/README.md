# Ex.No:2(C) ACCESS SPECIFIERS

## QUESTION:

Write a Java program to create a class **Person** with private instance variables:

* `name`
* `age`
* `country`

Provide **public getter and setter methods** to access and modify these variables.
Read user input for name, age, and country, set the values using setter methods, and display them using getter methods.

---

## AIM:

To implement a Java program demonstrating the concept of **access specifiers**, specifically encapsulation, by using private variables with public getter and setter methods.

---

## ALGORITHM :

1. Start the program.
2. Import the necessary package `java.util`.
3. Create a class `Person` with private variables: name, age, and country.
4. Provide public getter and setter methods for accessing and modifying the private variables.
5. In the main method, read the user inputs for name, age, and country.
6. Create a `Person` object and assign values using setter methods.
7. Display the details using getter methods.
8. End the program.

---

## PROGRAM:

```
/*
Program to implement Access Specifiers using Java
Developed by: Subhashini B
RegisterNumber: 212223040211
*/
```

---

## SOURCE CODE:

```
import java.util.*;
public class Person {
  
    private String name;
    private int age;
    private String country;

    public String getName() {
        return name;
    }
    public void setName(String name) {
        this.name = name;
    }

    public int getAge() {
        return age;
    }
    public void setAge(int age) {
        this.age = age;
    }

    public String getCountry() {
        return country;
    }
    public void setCountry(String country) {
        this.country = country;
    }
    
    public static void main(String args[]) {
        Scanner sc = new Scanner(System.in);
        String name = sc.nextLine();
        int age = sc.nextInt();
        sc.nextLine();
        String country = sc.nextLine();
        
        Person obj = new Person();
        obj.setName(name);
        obj.setAge(age);
        obj.setCountry(country);
        
        System.out.printf("Person 1 \nName: %s\nAge: %d\nCountry: %s", 
                           obj.getName(), obj.getAge(), obj.getCountry());
    }
}
```

---

## OUTPUT:
<img width="747" height="437" alt="Screenshot 2025-11-24 at 1 27 11 PM" src="https://github.com/user-attachments/assets/b2b6d89a-6e24-4a2a-97aa-a84c52bde140" />

---

## RESULT:

Thus, the Java program demonstrating access specifiers using getter and setter methods was successfully executed and verified.


