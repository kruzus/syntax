# Java

Now people hate java all they want, but hey man it feeds like what? Approx 17 million people? thats crazy! 

Certainly! Let's provide a review of Java syntax and key concepts with examples to help you learn Java.

1. **Hello, World!**:
   - The traditional "Hello, World!" program in Java.

   ```java
   public class HelloWorld {
       public static void main(String[] args) {
           System.out.println("Hello, World!");
       }
   }
   ```

2. **Variables and Data Types**:
   - Java supports various data types, including int, double, boolean, and char.

   ```java
   int age = 30;
   double price = 19.99;
   boolean isJavaFun = true;
   char grade = 'A';
   ```

3. **Control Structures**:
   - Java has control structures like if, else, switch, while, for, and more.

   ```java
   if (score >= 90) {
       System.out.println("A Grade");
   } else {
       System.out.println("B Grade");
   }

   for (int i = 0; i < 5; i++) {
       System.out.println("Iteration " + i);
   }
   ```

4. **Methods**:
   - Functions in Java are called methods.

   ```java
   public int add(int a, int b) {
       return a + b;
   }
   int sum = add(3, 4);
   ```

5. **Classes and Objects**:
   - Java is an object-oriented language. You define classes and create objects from them.

   ```java
   class Car {
       String make;
       int year;

       void start() {
           System.out.println("Car started");
       }
   }

   Car myCar = new Car();
   myCar.make = "Toyota";
   myCar.year = 2022;
   myCar.start();
   ```

6. **Inheritance**:
   - Java supports inheritance to create subclasses and superclasses.

   ```java
   class Animal {
       void sound() {
           System.out.println("Animal makes a sound");
       }
   }

   class Dog extends Animal {
       @Override
       void sound() {
           System.out.println("Dog barks");
       }
   }
   ```

7. **Interfaces**:
   - Java uses interfaces to define contracts for classes.

   ```java
   interface Shape {
       double area();
   }

   class Circle implements Shape {
       double radius;

       @Override
       public double area() {
           return Math.PI * radius * radius;
       }
   }
   ```

8. **Exception Handling**:
   - Java has robust exception handling with try-catch blocks.

   ```java
   try {
       int result = 5 / 0;
   } catch (ArithmeticException e) {
       System.out.println("Error: " + e.getMessage());
   }
   ```

9. **Collections**:
   - Java offers a wide range of data structures like ArrayList, HashMap, and LinkedList for managing collections of data.

   ```java
   List<String> names = new ArrayList<>();
   names.add("Alice");
   names.add("Bob");
   String first = names.get(0);

   Map<String, Integer> scores = new HashMap<>();
   scores.put("Alice", 90);
   int aliceScore = scores.get("Alice");
   ```

10. **File I/O**:
    - Java provides classes for file input and output operations.

    ```java
    try (FileWriter writer = new FileWriter("file.txt")) {
        writer.write("Hello, Java!");
    } catch (IOException e) {
        e.printStackTrace();
    }
    ```

11. **Threads and Concurrency**:
    - Java supports multithreading and concurrent programming.

    ```java
    class MyThread extends Thread {
        public void run() {
            System.out.println("Thread is running");
        }
    }
    MyThread thread = new MyThread();
    thread.start();
    ```

12. **Generics**:
    - Java supports generics to create reusable and type-safe code.

    ```java
    class Box<T> {
        private T content;

        public void set(T value) {
            content = value;
        }

        public T get() {
            return content;
        }
    }
    ```

13. **Lambda Expressions**:
    - Java 8 introduced lambda expressions for concise functional programming.

    ```java
    List<String> names = Arrays.asList("Alice", "Bob", "Charlie");
    names.forEach(name -> System.out.println(name));
    ```

14. **Java Standard Library**:
    - Java comes with a rich standard library for various tasks, including data manipulation, networking, and more.

15. **Development Tools**:
    - Java development typically involves using tools like Eclipse, IntelliJ IDEA, or the command-line compiler.

 
 Java syntax is very simple so i'll keep this short.