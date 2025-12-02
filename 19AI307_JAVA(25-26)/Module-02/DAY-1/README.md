# Ex.No:2(A) CLASS AND OBJECT

## QUESTION:

Create a class **Course** with attributes **code**, **title**, and **credits**.
Read details for two courses and display them in the following format:

Example:

| Input                          | Result                                                 |
| ------------------------------ | ------------------------------------------------------ |
| CS101 Java 4<br>CS102 Python 3 | CS101 | Java | 4 credits<br>CS102 | Python | 3 credits |

---

## AIM:

To write a Java program that creates a class with attributes and demonstrates object creation, attribute assignment, and displaying object data.

---

## ALGORITHM :

1. Start the program.
2. Import the necessary package `java.util`.
3. Create a `Course` class with attributes: code, title, credits.
4. In the main method, create two Course objects.
5. Read input values for both objects.
6. Display the course details in the required format.
7. End the program.

---

## PROGRAM:

```
/*
Program to implement a Class and Objects using Java
Developed by: Subhashini B
RegisterNumber: 212223040211
*/
```

---

## SOURCE CODE:

```
import java.util.Scanner;

class Course {
    String code;
    String title;
    int credits;
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        Course c1 = new Course();
        c1.code = sc.next();
        c1.title = sc.next();
        c1.credits = sc.nextInt();

        Course c2 = new Course();
        c2.code = sc.next();
        c2.title = sc.next();
        c2.credits = sc.nextInt();

        System.out.println(c1.code + " | " + c1.title + " | " + c1.credits + " credits");
        System.out.println(c2.code + " | " + c2.title + " | " + c2.credits + " credits");

        sc.close();
    }
}
```

---

## OUTPUT:
<img width="739" height="278" alt="Screenshot 2025-11-24 at 1 23 13 PM" src="https://github.com/user-attachments/assets/eb7b2153-ed2e-4031-8b7c-76154665ab59" />

---

## RESULT:

Thus, the Java program to implement classes and objects using the Course example was successfully executed and verified.


