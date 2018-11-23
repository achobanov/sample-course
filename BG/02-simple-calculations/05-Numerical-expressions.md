[slide]
# Numerical Expressions

In programming, we can calculate **numerical expressions**, for example:

```csharp
var expr = (3 + 5) * (4 – 2);
```

The standart rule for priorities of the arithmetic operations is applied: **multiplying and dividing are always done before adding and substracting**. In case of an **expression in brackets, it is calculated first**, but we already know all of that from school math.
[/slide]

[slide]
# Example: calculating a trapezoid area

Let us write a program that takes the lengths of the two bases of a trapezoid and its height (one floating-point number per row) and calculates the **area of the trapezoid** by the standart math formula: 

```csharp
var b1 = double.Parse(Console.ReadLine());
var b2 = double.Parse(Console.ReadLine());
var h = double.Parse(Console.ReadLine());
var area = (b1 + b2) * h / 2.0;
Console.WriteLine("Trapezoid area = " + area);
```

If we start the program and enter values for the sides 3, 4 and 5, we will receive the following result:

```
3
4
5
Trapezoid area = 17.5
```

## Testing in the Judge System

Test your solution here : [anchor href=https://judge.softuni.bg/Contests/Practice/Index/504#4]https://judge.softuni.bg/Contests/Practice/Index/504#4[/anchor].
[/slide]

[slide]
# Example: perimeter and area of a circle

Let us write a program that calculates  **a circle area and a perimeter** by reading its **radius r** .

Formulas:
- Area = π \* r \* r
- Perimeter = 2 \* π \* r
- π ≈ 3.14159265358979323846…

```csharp
Console.Write("Enter circle radius. r = ");
var r = double.Parse(Console.ReadLine());
Console.WriteLine("Area = " + Math.PI * r * r); 
// Math.PI - built in constant for π in C#
Console.WriteLine("Perimeter = " + 2 * Math.PI * r);
```
Let us test the program with **radius `r = 10`:

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-2-images/00.Circle-area-01.jpg alt="Console" /] 

## Testing in the Judge System

Test your solution here: [anchor href=https://judge.softuni.bg/Contests/Practice/Index/504#5]https://judge.softuni.bg/Contests/Practice/Index/504#5[/anchor].
[/slide]

[slide]
# Example: area of a rectangle on a coordinate plane

There is a given rectangle with the **coordinates of two of its opposite angles**. Calculate the  **area and its perimeter**:

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-2-images/00.Rectangle-area-01.png alt="Console" /]

In this task, we have to consider that if we substract the smaller `x` from the bigger `x`, we will receive the length of the rectangle. Analogically, if we substract the smaller `y` from the bigger `y` , we will receive the height of the rectangle. What is left is to multiply both sides. Here is an example of an implementation of the described logic: 

```csharp
var x1 = double.Parse(Console.ReadLine());
var y1 = double.Parse(Console.ReadLine());
var x2 = double.Parse(Console.ReadLine());
var y2 = double.Parse(Console.ReadLine());

// Calculating the sides of the rectangle:
var width = Math.Max(x1, x2) - Math.Min(x1, x2);
var height = Math.Max(y1, y2) - Math.Min(y1, y2);

Console.WriteLine("Area = " + width * height);
Console.WriteLine("Perimeter = " + 2 * (width + height));
```

We use `Math.Max(a, b)`, to find the bigger value `a` and `b` and analogically `Math.Min(a, b)` to find the smaller of both values. 

When the program is executed with the values from the coordinate system given in the condition, we receive the following result:

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-2-images/00.Rectangle-area-02.jpg alt="Console" /]

## Testing in the Judge System

Test your solution here: [anchor href=https://judge.softuni.bg/Contests/Practice/Index/504#6]https://judge.softuni.bg/Contests/Practice/Index/504#6[/anchor].
[/slide]