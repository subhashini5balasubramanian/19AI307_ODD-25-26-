# Ex.No:5(B) SERIALIZATION AND DESERIALIZATION

## QUESTION:

Write a Java program to serialize a collection of objects (like `ArrayList<Student>`) into a file and then deserialize it back.

### Example

| **Input**                                       | **Result**                                                                                                                                                                                                                         |
| ----------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 2<br>101<br>Alice<br>89.5<br>102<br>Bob<br>92.0 | Students serialized successfully into: students.dat<br>Students deserialized successfully from: students.dat<br><br>Deserialized Students:<br>Student{id=101, name='Alice', marks=89.5}<br>Student{id=102, name='Bob', marks=92.0} |

## AIM:

To write a Java program that serializes a list of Student objects into a file and later deserializes the file content back into objects, demonstrating object serialization and deserialization in Java.

## ALGORITHM :

1. Start the program.
2. Import necessary packages such as `java.util` and `java.io`.
3. Create a `Student` class implementing `Serializable`.
4. Read user input and create Student objects.
5. Store Student objects in an ArrayList.
6. Serialize the ArrayList into a file using `ObjectOutputStream`.
7. Deserialize the file back into an ArrayList using `ObjectInputStream`.
8. Display the deserialized objects.
9. End the program.

## PROGRAM:

```
/*
Program to implement a Serialization and Deserialization using Java
Developed by: Subhashini B
RegisterNumber: 212223040211
*/
```

## SOURCE CODE:

```
import java.io.*;
import java.util.*;

// Student class must implement Serializable
class Student implements Serializable {
    private static final long serialVersionUID = 1L;

    private int id;
    private String name;
    private double marks;

    public Student(int id, String name, double marks) {
        this.id = id;
        this.name = name;
        this.marks = marks;
    }

    @Override
    public String toString() {
        return "Student{id=" + id + ", name='" + name + "', marks=" + marks + "}";
    }
}

public class StudentSerializationUserInput {

    // Serialize list of students
    public static void serializeStudents(List<Student> students, String fileName) {
        try (ObjectOutputStream oos = new ObjectOutputStream(new FileOutputStream(fileName))) {
            oos.writeObject(students);
            System.out.println("Students serialized successfully into: " + fileName);
        } catch (IOException e) {
            System.out.println("Error during serialization: " + e.getMessage());
        }
    }

    // Deserialize list of students
    @SuppressWarnings("unchecked")
    public static List<Student> deserializeStudents(String fileName) {
        List<Student> students = null;
        try (ObjectInputStream ois = new ObjectInputStream(new FileInputStream(fileName))) {
            students = (List<Student>) ois.readObject();
            System.out.println("Students deserialized successfully from: " + fileName);
        } catch (IOException | ClassNotFoundException e) {
            System.out.println("Error during deserialization: " + e.getMessage());
        }
        return students;
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        List<Student> students = new ArrayList<>();

        int n = scanner.nextInt();
        scanner.nextLine(); // consume newline

        // Write your code here
        for (int i = 0; i < n; i++) {
            int id = scanner.nextInt(); scanner.nextLine();
            String name = scanner.nextLine();
            double marks = scanner.nextDouble();
            students.add(new Student(id, name, marks));
        }
        serializeStudents(students, "students.dat");
        List<Student> deserializedStudents = deserializeStudents("students.dat");

        // Display deserialized data
        if (deserializedStudents != null) {
            System.out.println("\nDeserialized Students:");
            for (Student s : deserializedStudents) {
                System.out.println(s);
            }
        }

        scanner.close();
    }
}
```

## OUTPUT:
<img width="1135" height="769" alt="Screenshot 2025-11-24 at 2 09 00 PM" src="https://github.com/user-attachments/assets/67dc13af-88ab-43dc-a56f-200e04a95150" />

## RESULT:

Thus, the Java program for serializing and deserializing a collection of Student objects was successfully executed and verified.


