# Ex.No:4(B)  IMPLEMENT SOLID PRINCIPLES IN JAVA PROGRAM

## QUESTION:

In a large office, multiple departments send print jobs to a shared central printer. To manage load and prevent collision, a Print Spooler Manager handles all job submissions.

The IT team insists that there should be only one spooler manager instance in the entire system. Regardless of how many jobs or departments exist, all jobs must pass through this one manager.

Your task is to simulate a singleton print job queue. Each print job submitted increases the queue count.

Hidden Clue:
Use Singleton to manage shared access.

Count and log each print job submission.

Validate that state is preserved across all accesses.

Input Format:
First line: Integer n – number of print jobs

Next n lines: Each line contains the department name submitting the print job.

Output Format:
For each job, print:

## AIM:

To implement the Singleton Design Pattern ensuring that only one Print Spooler Manager instance handles all print jobs.

## ALGORITHM :

1. Start the program.
2. Import the necessary package `java.util`.
3. Create a class with a private static instance and private constructor.
4. Provide a public static method to return the singleton instance.
5. Maintain a print job counter inside the singleton class.
6. Read the number of print jobs from the user.
7. For each department input, access the singleton instance and update the job count.
8. Display the total print job count after each submission.
9. End the program.

## PROGRAM:

```
/*
Program to implement a SOLID Principles in Java Program
Developed by: Subhashini B
RegisterNumber: 212223040211
*/
```

## SOURCE CODE:

```java
import java.util.*;

class PrintSpoolerManager {
    private static PrintSpoolerManager instance;
    private int count = 0;

    public static PrintSpoolerManager getInstance() {
        if(instance == null) {
            instance = new PrintSpoolerManager();
        }
        return instance;
    }

    public int submitJob(String department) {
        return ++count;
    }
}

public class prog {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        sc.nextLine();

        for (int i = 0; i < n; i++) {
            String dept = sc.nextLine();
            PrintSpoolerManager spooler = PrintSpoolerManager.getInstance();
            int total = spooler.submitJob(dept);
            System.out.println(dept + " submitted a print job. Total Jobs in Queue: " + total);
        }
    }
}
```

## OUTPUT:
<img width="1135" height="365" alt="Screenshot 2025-11-24 at 1 53 55 PM" src="https://github.com/user-attachments/assets/310db892-7f0d-4c5e-83dc-a65fe4b35f06" />

## RESULT:

Thus, the Java program implementing the Singleton principle for a shared print spooler manager was successfully executed.


