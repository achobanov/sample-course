[slide]
# System Console 

Simply called "**console**", the system, also the computer console, represents the tool by which we give the computer commands in a text format and receive the results from their execution again as a text. 

Generally the system console represents a text terminal, which means that it accpets and visualizes just **text** without any graphical elements like buttons, menus, etc. It usually looks like a black coloured window like this one: 

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-2-images/00.Console-example.png alt="Console" /]

In most operating systems, the **console** is available as a standalone application on which we write console commands. It is called a **Command Prompt** in Windows, and in Linux and Mac a **Terminal**. The console runs console applications. They read text from the command line and print text on the console. In this book we are going to learn programming mostly through creating **console applications**.
[/slide]

[slide]
# Reading Integers From The Console

In order to read an **integer** (not a float) **number** from the console, we have to **declare a variable**, declare the **number type** and use the standart command for reading information from the system console: 

```csharp
var num = int.Parse(Console.ReadLine());
```
[/slide]

[slide]
# Example: calculating a square area with side а

For example, let us look at the following program, which reads an integer from the console, multiplies it by itself (squares it) and prints the result from the multiplication. This way we can calculate the square area by the given length of the side:

```csharp
Console.Write("a = ");              
var a = int.Parse(Console.ReadLine());
var area = a * a;
Console.Write("Square area = ");
Console.WriteLine(area);
```

Here is how the program would work when we have a square with a side length equal to 3:

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-2-images/00.Square-area-01.jpg alt="Console" /]

Try to write a wrong number, for example "**hello**". You will receive an error message during runtime (exception). This is normal. Later on, we will find out how we can catch this kinds of errors and make the user enter a number again. 

## Testing in the Judge system

Test your solution here: [anchor href=https://judge.softuni.bg/Contests/Practice/Index/504#0]https://judge.softuni.bg/Contests/Practice/Index/504#0[/anchor].

## How does the example work?

The first row `Console.Write("a = ");` prints an informative message, which invites the user to enter the side of the square  **a**. After the output is printed, the cursor stays on the same row. Staying on the same row is more convinient for the user, visually. We use `Console.Write(…)`, and not `Console.WriteLine(…)` and this way the cursor stays on the same row.

The next row `var a = int.Parse(Console.ReadLine());` reads an integer from the console. Actually, it reads a text first (string) using `Console.ReadLine()` and after that it gets converted to an integer (it is parsed) using `int.Parse(…)`. The result is kept in a variable with name `a`.

The next command `var area = a * a;` keeps in a new variable `area` the result of the multiplication of `a` by `a`.

The next command `Console.Write("Square area = ");` prints the given text without goint to the next line. Again, it is used  `Console.Write(…)`, and not `Console.WriteLine(…)` and this way the cursor stays on the same row in order to print the calculated area of the square afterwards. 

The last command `Console.WriteLine(area);` prints the calculated value of the variable  `area`.
[/slide]

[slide]
# Reading Floating-Point Numbers From the Console

To read a **real number** from the console, it is necessary to а **declare a variable** again, define its **numeric type**, and also use the standart command for reading information from the console:

```csharp
var num = double.Parse(Console.ReadLine());
``` 
[/slide]

[slide]
# Example: converting inches to centimeters

Let us write a program, which reads a floating-point number in inches and converts it to centimeters:

```csharp
Console.Write("Inches = ");              
var inches = double.Parse(Console.ReadLine());
var centimeters = inches * 2.54;
Console.Write("Centimeters = ");
Console.WriteLine(centimeters);
```

Let us start the program and make sure that when a value in inches is entered, we receive a correct answer in centimeters:

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-2-images/00.Inches-to-centimeters-01.jpg alt="Code" /] 

## Testing in the Judge System

Test your solution here: [anchor href=https://judge.softuni.bg/Contests/Practice/Index/504#1]https://judge.softuni.bg/Contests/Practice/Index/504#1[/anchor].
[/slide]

[slide]
# Reading a Text

To read a text (string) from the console, again, we have to **declare a new variable** and use the standart  **command for reading information from the console**:

```csharp
var str = Console.ReadLine();
```

Let us pay attention to the fact that the **reading of  text is not declared** in any way as a type "`string`" (text). The reason is because by default the  `Console.ReadLine(…)` method returns a **text result**. Additionally, you can parse the text to an integer by `int.Parse(…)` or a real number by `double.Parse(…)`. If this is not done, for the program **every number** will be just **text**, and we **cannot do** arithmetic operations with it.
[/slide]

[slide]
# Example: greeting by name

Let us write a program that asks the user for his name and salutes him with the text "**Hello, *name***".

```csharp           
var name = Console.ReadLine();
Console.WriteLine("Hello, {0}!", name);
```

In this case `{0}` is replaced with the **first** given argument, which holds the variable `name`:

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-2-images/00.Greeting-by-name-01.jpg alt="Console" /]  

## Testing in the Judge System

Test your solution here: [anchor href=https://judge.softuni.bg/Contests/Practice/Index/504#2]https://judge.softuni.bg/Contests/Practice/Index/504#2[/anchor].
[/slide]

[slide]
# Printing Text and Numbers

When printing a text, numbers and other data on the console,  **we can join them** by using templates `{0}`, `{1}`, `{2}` etc. In programming, these templates are called **placeholders**.

```csharp
var firstName = Console.ReadLine();
var lastName = Console.ReadLine();
var age = int.Parse(Console.ReadLine());
var town = Console.ReadLine();
Console.WriteLine("You are {0} {1}, a {2}-years old person from {3}.",
firstName, lastName, age, town);
```

Here is the result we are going to receive after the execution of this example: 

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-2-images/00.Placeholders-01.jpg alt="Console" /]

Notice how every variable should be given in the **order, in which we want it to be printed**. Practically, the template (**placeholder**) **accepts variables from every type**.

It is possible for a template to be used multiple times and it is not necessary for the templates to be numbered sequentially. Here is an example:

```csharp
Console.WriteLine("{1} + {1} = {0}", 1+1, 1);
```

The result is:

```
1 + 1 = 2
```

## Testing in the Judge System

Test your solution here: [anchor href=https://judge.softuni.bg/Contests/Practice/Index/504#3]https://judge.softuni.bg/Contests/Practice/Index/504#3[/anchor].
[/slide]