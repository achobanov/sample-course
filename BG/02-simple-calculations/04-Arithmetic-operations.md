[slide]
# Arithmetic Operations

Let us look at the basic arithmetic operations in programming.

## Addition of Numbers (operator `+`)

We can add a number with the operator `+`:

```csharp
var a = 5;
var b = 7;
var sum = a + b; // the result is 12
``` 

## Substraction of Numbers (operator `-`)

Substracting a number is done by the operator `-`:

```csharp
var a = int.Parse(Console.ReadLine());
var b = int.Parse(Console.ReadLine());
var result = a - b;
Console.WriteLine(result);
```

Here is the result from the execution of this program (with numbers 10 and 3):

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-2-images/00.Subtracting-01.jpg alt="Console" /] 

## Multiplication of Numbers (operator `*`)

For multiplication of numbers we use the operator `*`:

```csharp
var a = 5;
var b = 7;
var product = a * b; // 35
```
[/slide]

[slide]
# Division of Numbers (operator /)

Dividing numbers is done by the operator `/`. It works differently with integers and floating-point numbers.
- When we divide two whole numbers, an **integer divison** is applied and the received output is without its fractional part. Example: 11 / 3 = 3.
- When we divide two numbers and at least one of them is a real number, a **floating division** is applied and the received result is a real number, just as it is in math. Example 11 / 4.0 = 2.75.  When it cannot be done with exact precision, the result is being rounded, for example 11.0 / 3 = 3.66666666666667.
- The integer **division by 0** causes  an **exception** during runtime (runtime exception).
- Real numbers **divided by 0** do not cause an exception and the result is  **+/- infinity** or a special value  **NaN**. Example 5 / 0.0 = &#8734;.

Here are a few examples with the divison operator:

```csharp
var a = 25;
var i = a / 4;      // we are applying an integer division:
                    // the result of this operation will be 6 – the fractional part will be cut, 
                    // because we are dividing integers
var f = a / 4.0;    // 6.25 – floating division. We have set the number 4 to be interpreted 
                    // as a float by adding a decimal separator followed by zero 
var error = a / 0;  // Error: Integer divide by zero
```

Let us look at a few examples for **integer division** (remember that when we **divide integers** in C# the result is a **whole number**):

```csharp
var a = 25;
Console.WriteLine(a / 4);  // Integer result: 6
Console.WriteLine(a / 0);  // Error: divide by 0
```

Let us look at a few examples for **floating division**. When we divide floating-point numbers, the result is always a **real number** and the division never fails and works correct with the special values **+&#8734;** and **-&#8734;**:

```csharp
var a = 15;
Console.WriteLine(a / 2.0);    // Float result: 7.5
Console.WriteLine(a / 0.0);    // Result: Infinity
Console.WriteLine(-a / 0.0);   // Result: -Infinity
Console.WriteLine(0.0 / 0.0);  // Result: NaN (Not a Number), e.g. the result
                               // from the operation is not a valid numeric value
```

When printing the values  **&#8734;** and **-&#8734;**, the console output may be `?`, because the console in Windows does not work correctly with Unicode and breaks most of the non-standart symbols, letters and special signs. The example above would most probably give the following result:

```
7.5
?
-?
NaN
```
[/slide]

[slide]
# Concatenating a Text and a Number

Except for addition of numbers, the operator `+` is used for joining a text (concatenation of two strings one after another). In programming, joining a text with a text is called "**concatenation**". Here is how we can concatenate a text with a number by the `+` operator:

```csharp
var firstName = "Maria";
var lastName = "Ivanova";
var age = 19;
var str = firstName + " " + lastName + " @ " + age;
Console.WriteLine(str);  // Maria Ivanova @ 19
```

Here is another example:

```csharp
var a = 1.5;
var b = 2.5;
var sum = "The sum is: " + a + b;
Console.WriteLine(sum);  // The sum is: 1.52.5
```

Did you notice something strange? May be you expecteded the numbers `a` and  `b` to be summed? Actually the concatenation works from rigth to left and the result above is absolutely correct. If we want to sum the numbers, we have to use **brackets**, in order to change the order of execution of the operations:

```csharp
var a = 1.5;
var b = 2.5;
var sum = "The sum is: " + (a + b);
Console.WriteLine(sum);  // The sum is: 4
``` 
[/slide]