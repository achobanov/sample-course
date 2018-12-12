[slide]
# Integer Types
- sbyte [-128 …127]: signed 8-bit [-27 … 27-1]
- byte [0 … 255]: unsigned 8-bit [0 … 28-1]
- short [-32 768 … 32 767]: signed 16-bit [-215 … 215-1]
- ushort [0 … 65 535]: unsigned 16-bit [0 … 216-1]
- int [-2 147 483 648 … 2 147 483 647]: signed 32-bit [-231 … 231-1]
- uint [0 … 4 294 967 295]: unsigned 32-bit [0 … 232-1]
- long [-9 223 372 036 854 775 808 … 9 223 372 036 854 775 807]: signed 64-bit [-263 … 263-1]
- ulong [0 … 18 446 744 073 709 551 615]: unsigned 64-bit [0 … 264-1]
[/slide]

[slide]
# Centuries – Example
Depending on the unit of measure we can use different data types:
```csharp
20 centuries = 2000 years = 730484 days = 17531616 hours.
Press any key to continue...
```

```csharp
byte centuries = 20;    // A small number (up to 255)
ushort years = 2000;    // A small number (up to 32767)
uint days = 730484;     // A large number (up to 4.3 billions)
ulong hours = 17531616; // A very big number (up to 18.4*10^18)
Console.WriteLine("{0} centuries = {1} years = {2} days = {3} hours.", centuries, years, days, hours);

```
[/slide]

[slide]
# Test Your Code Here
# Centuries - Example

Create C# console application that prints on the screen for centuries, years and days.

[code-task title="Centuries - Example" executionStrategy="csharp-dot-net-core-code" requiresInput]

[code-editor language=csharp]
```csharp
using System;

namespace App
{
    class Program
    {
        static void Main(string[] args)
        {
		    // enter your code here
		    Console.WriteLine("{0} centuries = {1} years = {2} days = {3} hours.", centuries, years, days, hours);
		}
	}
}
```
[/code-editor]

[task-description]
Print on the screen how many years, days and hours of equal 20 centuries.
[/task-description]

[code-io /]
[/code-task]
[/slide]

[slide]
# Declaring and Invoking Methods

**Methods** are **named pieces of code** that can be invoked later

Sample method **definition**:
```text
static void PrintHeader()
{
  Console.WriteLine("----------");
}
```

**Invoking** (calling) the method several times:
```csharp
PrintHeader();
PrintHeader();
```
[/slide]

[slide]
# Why Use Methods?

- More **managable programming**
    - Splits large problems into small pieces
    - Better organization of the program
    - Improves code readability
    - Improves code understandability
- Avoiding repeating code
    - Improves code maintainability
- Code reusability
    - Using existing methods several times
[/slide]

[slide]
# Defining Methods

Method definitions follow this general structure:

```csharp
[modifiers] [return type] [Name]([parameters])
{
  [method body]
}
```

For example:

```csharp
static double GetSquare(double num)
{
  return num * num;
}
```

Methods are defined **inside a class**

`Main()` is also a method:
```csharp
class Program
{
  static void Main(string[] args)
  {
    // code
  }
}
```

Variables inside a method are **local**
[/slide]

[slide]
# Invoking a Method

Methods are first **defined**, then **invoked** (many times); here's a method definition:

```csharp
static void PrintHeader()
{
  Console.WriteLine("----------");
}
```

Methods can be invoked (called) by their name + `()`:

```csharp
static void Main()
{
  PrintHeader(); // <-- method invocation
}
```
[/slide]

[slide]
# Invoking a Method (2)

A method can be invoked from:

The main method - `Main()`:

```csharp
static void Main()
{
  PrintHeader();
}
```

Some other method:

```csharp
static void PrintHeader()
{
  PrintHeaderTop();
  PrintHeaderBottom();
}
```

Its own body (recursion)

```csharp
static void Crash()
{
  Crash();
}
```
[/slide]
