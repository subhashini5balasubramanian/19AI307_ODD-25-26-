# Ex.No:3(F) WRAPPER CLASS

## QUESTION:

Write a Java program to check if a number is an Armstrong number using Math.pow() and the Integer wrapper class. Take input from the user.

| Input | Result                      |
| ----- | --------------------------- |
| 153   | 153 is an Armstrong number. |

## AIM:

To write a Java program to check whether a given number is an Armstrong number using `Math.pow()` and the `Integer` wrapper class.

## ALGORITHM :

1. Start the program.
2. Import the necessary package `java.util`.
3. Read the integer input from the user.
4. Convert the number into an `Integer` object and count its digits.
5. Extract each digit and find the sum of digits raised to the power of number of digits using `Math.pow()`.
6. Compare the computed sum with the original number.
7. Display whether it is an Armstrong number or not.
8. End the program.

## PROGRAM:

```
/*
Program to implement a Wrapper Class using Java
Developed by: Subhashini B
RegisterNumber: 212223040211
*/
```

## SOURCE CODE:

```java
import java.util.Scanner;
public class Main{
    public static void main(String args[]){
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        int temp = n;
        Integer num = Integer.valueOf(n);
        int c = Integer.toString(num).length();
        int sum=0;
        while(n>0){
            int d = n%10;
            sum+=Math.pow(d,c);
            n/=10;
        }
        if (temp==sum)
        {
            System.out.println(temp+" is an Armstrong number.");
        }
        else
        {
            System.out.println(temp+" is not an Armstrong number.");
        }
    }
}
```

## OUTPUT:
<img width="760" height="273" alt="Screenshot 2025-11-24 at 1 48 50 PM" src="https://github.com/user-attachments/assets/90bdc27c-6871-48b7-b2b9-ce7c594fb1d8" />

## RESULT:

Thus, the Java program to check whether a number is an Armstrong number using `Math.pow()` and the `Integer` wrapper class was successfully executed.

---


