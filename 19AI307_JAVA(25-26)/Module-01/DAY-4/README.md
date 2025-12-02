# Ex.No:1(D) ARRAYS

## QUESTION:

Write a Java program to count the number of **positive**, **negative**, and **zero** elements in an array.

Example:

| Input                        | Result                                                  |
| ---------------------------- | ------------------------------------------------------- |
| 5<br>1<br>-2<br>0<br>-3<br>4 | Positive count: 2<br>Negative count: 2<br>Zero count: 1 |

---

## AIM:

To write a Java program that reads an array of integers and counts how many elements are positive, negative, and zero.

---

## ALGORITHM :

1. Start the program.
2. Import the necessary package `java.util`.
3. Read the size of the array from the user.
4. Read all array elements inside a loop.
5. For each element, check if it is positive, negative, or zero and increment the respective counter.
6. Display the counts of positive, negative, and zero elements.
7. End the program.

---

## PROGRAM:

```

Program to implement a Array concept using Java
Developed by: Subhashini B
RegisterNumber: 212223040211

```

---

## SOURCE CODE:

```
import java.util.*;

public class Main {
    public static void main(String args[]) {
        int n, pos=0, neg=0,zero=0;
        Scanner sc = new Scanner(System.in);
        n = sc.nextInt();
        int[] arr = new int[n];
        for(int i = 0; i < n; i++) {
            arr[i] = sc.nextInt();
            if(arr[i] > 0) pos++;
            else if(arr[i]< 0) neg++;
            else zero++;
        }
        System.out.println("Positive count: " + pos);
        System.out.println("Negative count: " + neg);
        System.out.println("Zero count: " + zero);
        sc.close();
    }
}
```

---

## OUTPUT:
<img width="621" height="544" alt="Screenshot 2025-11-24 at 1 16 32 PM" src="https://github.com/user-attachments/assets/213d5d6c-a0b0-4dd5-b346-b2407599e98c" />

---

## RESULT:

Thus, the Java program to count positive, negative, and zero elements in an array was successfully executed and verified.



