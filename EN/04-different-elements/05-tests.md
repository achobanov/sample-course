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
```
using System;
namespace Centuries
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
