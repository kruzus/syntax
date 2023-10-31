# C# Notes

Certainly! Here's a review of C# syntax with usage examples:

### 1. Data Types:
C# has various data types for storing different kinds of values.

- **int**: Used to store integer values.
  ```csharp
  int age = 25;
  ```

- **double**: Used to store floating-point numbers.
  ```csharp
  double price = 12.99;
  ```

- **string**: Used to store text.
  ```csharp
  string name = "John";
  ```

- **bool**: Used to store true or false values.
  ```csharp
  bool isStudent = true;
  ```

### 2. Variables:
Variables are used to store data.

```csharp
int x = 10;
string message = "Hello, World!";
```

### 3. Operators:
C# supports various operators like arithmetic, comparison, and logical operators.

- **Arithmetic Operators**:
  ```csharp
  int a = 5;
  int b = 3;
  int sum = a + b;
  int product = a * b;
  ```

- **Comparison Operators**:
  ```csharp
  bool isEqual = (a == b);
  bool isGreaterThan = (a > b);
  ```

- **Logical Operators**:
  ```csharp
  bool andResult = (true && false);
  bool orResult = (true || false);
  ```

### 4. Conditional Statements:
C# allows you to make decisions in your code.

- **if statement**:
  ```csharp
  if (age >= 18)
  {
      Console.WriteLine("You are an adult.");
  }
  ```

- **switch statement**:
  ```csharp
  switch (dayOfWeek)
  {
      case "Monday":
          Console.WriteLine("It's Monday.");
          break;
      default:
          Console.WriteLine("It's another day.");
          break;
  }
  ```

### 5. Loops:
Loops allow you to repeat code blocks.

- **for loop**:
  ```csharp
  for (int i = 0; i < 5; i++)
  {
      Console.WriteLine(i);
  }
  ```

- **while loop**:
  ```csharp
  int i = 0;
  while (i < 5)
  {
      Console.WriteLine(i);
      i++;
  }
  ```

### 6. Methods:
Methods are reusable blocks of code.

```csharp
int Add(int a, int b)
{
    return a + b;
}
int result = Add(3, 4);
```

### 7. Classes and Objects:
C# is an object-oriented language, so you can define classes and create objects from them.

```csharp
class Person
{
    public string Name;
    public int Age;
}

Person person1 = new Person();
person1.Name = "Alice";
person1.Age = 30;
```

### 8. Arrays:
Arrays store collections of data.

```csharp
int[] numbers = { 1, 2, 3, 4, 5 };
string[] fruits = new string[3] { "Apple", "Banana", "Cherry" };
```

### 9. Exception Handling:
C# provides a way to handle exceptions gracefully.

```csharp
try
{
    int result = 10 / 0;
}
catch (DivideByZeroException ex)
{
    Console.WriteLine("Error: " + ex.Message);
}
```

### 10. Comments:
Use comments to add explanations to your code.

```csharp
// This is a single-line comment

/* This is a
   multi-line comment */
```

Certainly, let's continue with more C# syntax and usage examples:

### 11. Lists and Collections:
C# provides various data structures for storing collections of data.

- **List**:
  ```csharp
  List<int> numbers = new List<int>();
  numbers.Add(1);
  numbers.Add(2);
  int firstNumber = numbers[0];
  ```

- **Dictionary**:
  ```csharp
  Dictionary<string, int> ages = new Dictionary<string, int>();
  ages["Alice"] = 30;
  ages["Bob"] = 25;
  int aliceAge = ages["Alice"];
  ```

### 12. Inheritance and Polymorphism:
C# supports object-oriented programming concepts like inheritance and polymorphism.

```csharp
class Animal
{
    public virtual void Speak()
    {
        Console.WriteLine("Animal speaks.");
    }
}

class Dog : Animal
{
    public override void Speak()
    {
        Console.WriteLine("Dog barks.");
    }
}

Animal myPet = new Dog();
myPet.Speak(); // Output: "Dog barks."
```

### 13. Interfaces:
Interfaces define a contract for classes to implement.

```csharp
interface IShape
{
    double CalculateArea();
}

class Circle : IShape
{
    public double Radius { get; set; }

    public double CalculateArea()
    {
        return Math.PI * Radius * Radius;
    }
}
```

### 14. File I/O:
C# allows you to work with files.

```csharp
using System.IO;

string filePath = "data.txt";
string content = "Hello, File I/O!";
File.WriteAllText(filePath, content);
string readContent = File.ReadAllText(filePath);
```

### 15. Delegates and Events:
Delegates and events are used for handling callbacks and events in C#.

```csharp
delegate void MyDelegate(string message);

class EventPublisher
{
    public event MyDelegate MyEvent;

    public void RaiseEvent(string message)
    {
        MyEvent?.Invoke(message);
    }
}
```

### 16. LINQ (Language Integrated Query):
LINQ provides powerful querying capabilities for collections.

```csharp
List<int> numbers = new List<int> { 1, 2, 3, 4, 5 };
var evenNumbers = from num in numbers where num % 2 == 0 select num;
```

### 17. Asynchronous Programming:
C# supports asynchronous programming for tasks that may take time.

```csharp
async Task<string> DownloadDataAsync()
{
    HttpClient client = new HttpClient();
    string result = await client.GetStringAsync("https://example.com");
    return result;
}
```

### 18. Attributes:
Attributes provide metadata to classes, methods, or properties.

```csharp
[Obsolete("This method is deprecated.")]
void DeprecatedMethod()
{
    // Code here
}
```

### 19. Properties:
Properties are used to control access to class fields.

```csharp
private string _name;

public string Name
{
    get { return _name; }
    set { _name = value; }
}
```

### 20. Nullable Types:
C# allows you to assign null to value types using nullable types.

```csharp
int? nullableInt = null;
if (nullableInt.HasValue)
{
    int value = nullableInt.Value;
}
```

 Certainly, there are even more aspects of C# to explore. Here are some additional topics:

### 21. Generics:
Generics allow you to create reusable data structures and methods that work with different data types.

```csharp
public class MyList<T>
{
    private List<T> list = new List<T>();
    
    public void Add(T item)
    {
        list.Add(item);
    }
}
```

### 22. Attributes:
Attributes are used to add metadata to your code, such as specifying how a class or method should be handled by tools.

```csharp
[Serializable]
class MySerializableClass
{
    // Code here
}
```

### 23. Indexers:
Indexers allow you to define how objects of a class can be indexed, similar to arrays.

```csharp
class MyCollection
{
    private string[] data = new string[10];

    public string this[int index]
    {
        get { return data[index]; }
        set { data[index] = value; }
    }
}
```

### 24. Event Handling:
C# provides a way to subscribe and handle events using delegates and event handlers.

```csharp
class Button
{
    public event EventHandler Click;

    public void OnClick()
    {
        Click?.Invoke(this, EventArgs.Empty);
    }
}
```

### 25. LINQ (Language Integrated Query):
LINQ provides powerful querying capabilities for various data sources, including databases.

```csharp
var result = from item in dbContext.Products
             where item.Category == "Electronics"
             select item;
```

### 26. Nullable Value Types:
C# allows you to make value types nullable using the `?` modifier.

```csharp
int? nullableInt = null;
if (nullableInt.HasValue)
{
    int value = nullableInt.Value;
}
```

### 27. Named and Optional Parameters:
You can use named and optional parameters when calling methods, which can make code more readable.

```csharp
void PrintInfo(string name, int age = 30)
{
    Console.WriteLine($"{name}, {age} years old");
}

PrintInfo(name: "Alice");
```

### 28. Reflection:
Reflection allows you to inspect and interact with the metadata of types at runtime.

```csharp
Type type = typeof(MyClass);
MethodInfo methodInfo = type.GetMethod("MyMethod");
```

### 29. Attributes for Customization:
You can create custom attributes to add additional information to your code for various purposes, like serialization.

```csharp
[CustomAttribute("SomeValue")]
class MyClass
{
    // Code here
}
```

### 30. Dynamic Types:
The `dynamic` keyword allows you to work with objects in a more flexible way.

```csharp
dynamic dynamicObject = 42;
string result = dynamicObject.ToString(); // Resolved at runtime
```

Of course! Here are a few more advanced concepts in C#:

### 31. Async and Await Patterns:
Asynchronous programming is essential for handling tasks that may take time to complete without blocking the main thread.

```csharp
async Task<string> DownloadDataAsync()
{
    HttpClient client = new HttpClient();
    string result = await client.GetStringAsync("https://example.com");
    return result;
}
```

### 32. Extension Methods:
Extension methods allow you to add new methods to existing types without modifying their source code.

```csharp
public static class StringExtensions
{
    public static bool IsPalindrome(this string str)
    {
        // Check if the string is a palindrome
    }
}
```

### 33. Garbage Collection:
C# has an automatic garbage collector to manage memory, but understanding it is crucial for efficient resource management.

### 34. Threading and Parallelism:
C# provides support for multithreading and parallel programming to improve performance.

```csharp
Parallel.For(0, 100, i => {
    // Perform work in parallel
});
```

### 35. Unsafe Code and Pointers:
In certain scenarios, you may need to use unsafe code and work with pointers, which is typically not recommended but can be necessary in specific situations.

### 36. Unit Testing:
Writing unit tests is an essential practice for ensuring the quality and reliability of your code.

```csharp
[TestClass]
public class MyTests
{
    [TestMethod]
    public void TestAddition()
    {
        // Perform unit test
    }
}
```

### 37. Dependency Injection:
Dependency injection is a technique for providing dependencies to a class rather than creating them within the class.

```csharp
public class MyClass
{
    private readonly ILogger _logger;

    public MyClass(ILogger logger)
    {
        _logger = logger;
    }
}
```

### 38. Design Patterns:
Familiarize yourself with common design patterns such as Singleton, Factory, Observer, and others, which can help you design more maintainable and scalable applications.

### 39. Entity Framework:
Entity Framework is a popular Object-Relational Mapping (ORM) tool for working with databases in C#.

### 40. ASP.NET Core:
For web development, explore ASP.NET Core, a framework for building web applications and APIs in C#.

### 41. Windows Forms and WPF:
Learn about building desktop applications using Windows Forms or Windows Presentation Foundation (WPF) for creating modern and rich user interfaces.

### 42. Dependency Management:
Utilize dependency management tools like NuGet to manage external libraries and packages.

These advanced topics and concepts in C# can significantly enhance your skills and capabilities as a C# developer. They are often used in real-world applications and projects, so it's worth delving deeper into these areas as you progress in your C# programming journey.

