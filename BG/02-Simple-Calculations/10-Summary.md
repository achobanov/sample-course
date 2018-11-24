[slide]
# Reading Numbers from the Console

Before going to the tasks, we are going to revise the most important aspects of what we have studied in the previous chapter. We will start with reading numbers from the console.

## Reading an integer

We need to create a variable to store the integer (for example, `num`) and use a standard command for reading input from the console, combined with the function `int.Parse(…)` which converts string to an integer:

```csharp
var num = int.Parse(Console.ReadLine());
```

## Reading a decimal number

We read a decimal number, the same way we read an integer one, but this time we use the function `double.Parse(…)`:

```csharp
var num = double.Parse(Console.ReadLine());
```
[/slide]

[slide]
# Using placeholders

**Placeholder** is an expression which is replaced with a particular value while printing an output. The methods `Console.Write(…)` / `WriteLine(…)` support printing a string pattern, where the first argument is the formatted string, followed by the number of arguments, equal to the number of placeholders.

```csharp
Console.WriteLine("You are {0} {1}, a {2}-years old person from {3}.",
    firstName, lastName, age, town);
```
[/slide]

[slide]
# Arithmetical operators

Let' s revise the main arithmetical operators for simple calculations.

## Operator +

```csharp
var result = 3 + 5; // the result is 8
```

## Operator -

```csharp
var result = 3 - 5; // the result is -2
```

## Operator *

```csharp
var result = 3 * 5; // the result is 15
```

## Operator /

```csharp
var result = 7 / 3;     // the result is 2 (integer division)
var result2 = 5 / 2.0;  // the result is 2.5 (floating-point division)
```
[/slide]

[slide]
# Concatenation

By using the operator `+` between string variables (or between a string and a number), concatenation is being made (combining strings).

```csharp
var firstName = "Ivan";
var lastName = "Ivanov";
var age = 19;
var str = firstName + " " + lastName + " is " + age + " years old";
// Ivan Ivanov is 19 years old
```
[/slide]