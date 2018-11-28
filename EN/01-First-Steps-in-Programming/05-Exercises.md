[slide]
# Exercises: first steps in coding

Welcome to the exercises. Now we are going to write a couple of console applications, with which we are going to make a few more steps into programming, after which we will show how we can program something more complex - programs with graphical user interface.

## Problem: console application “Expression”

[code-task title="Expression" executionStrategy="csharp-dot-net-core-code"]

[code-editor language=csharp]
[/code-editor]

[task-description]
Write a C# console program, which **calculates** and **prints** the value of the following numerical expression:
(3522 + 52353) * 23 - (2336 * 501 + 23432 - 6743) * 3
[/task-description]

[code-io /]

[/code-task]

Warning: **it is not allowed to previously calculate the value** (for example with Windows Calculator).

### Hints and Guidelines

We make **a new  C# console project** with name "**Expression**".	We find the method `static void Main(string[] args)` and **go into its body** between `{` and `}`. After that we have to **write the code**, which calculates the above numerical expression and prints its value on the console. We put the above numerical expression inside the brackets of the command `Console.WriteLine(…)`:

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-1-images/02.Expression-01.png alt="Visual Studio" /]

We start the program with [**Ctrl+F5**] and check if the result is the same as the one in the picture:

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-1-images/02.Expression-02.png alt="Console" /]

### Testing in the Judge System

Test your solution here: [anchor href=https://judge.softuni.bg/Contests/Practice/Index/503#1]https://judge.softuni.bg/Contests/Practice/Index/503#1[/anchor].

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-1-images/02.Expression-03.png alt="Judge System" /]

[/slide]

[slide]
# Problem: numbers from 1 to 20

[code-task title="Numbers from 1 to 20" executionStrategy="csharp-dot-net-core-code"]

[code-editor language=csharp]
Console.WriteLine(1);
Console.WriteLine(2);
// TODO ...
[/code-editor]

[task-description]
Write a C# console program, which **prints the numbers from 1 to 20** on separate rows on the console.
[/task-description]

[/code-task]

## Hints and Guidelines

We create **a C# console application** with name “**Nums1To20**“:

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-1-images/03.Numbers-1-to-20-01.png alt="Visual Studio" /]

Inside the `static void Main()` method we write 20 commands `Console.WriteLine(…)`, each on a separate row, in order to print the numbers from 1 to 20 one after another. Some of you must be aksing themselves if there is a smarter way. Relax, there is, but we will mention it later on.

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-1-images/03.Numbers-1-to-20-02.png alt="Visual Studio" /]

Now **we start the program** and we check if the result is what it is supposed to be:

```
1
2
…
20
```

## Testing in the Judge System

Test your solution here: [anchor href=https://judge.softuni.bg/Contests/Practice/Index/503#2]https://judge.softuni.bg/Contests/Practice/Index/503#2[/anchor].

Now think whether we can write the program **a smarter way**, so we don't repeat the same command 20 times. Seek out information on the Internet about [anchor href=https://www.google.bg/search?q=for+loop+C%23&oq=for+loop+C%23]**for loop C#**[/anchor].
[/slide]

[slide]
# Problem: a triangle of 55 stars

[code-task title="Triangle of 55 Stars" executionStrategy="csharp-dot-net-core-code"]

[code-editor language=csharp]
Console.WriteLine("*");
Console.WriteLine("**");
[/code-editor]

[task-description]
Write a C# console program, which **prints a triangle of 55 stars** on 10 rows.
[/task-description]

[/code-task]


```
*
**
***
****
*****
******
*******
********
*********
**********
```

## Hints and Guidelines

We create **a new console C# application** with name “**TriangleOf55Stars**”. In it we have to write code, which prints the triangle of stars, for example through 10 `Console.WriteLine(…)` commands.

## Testing in the Judge System

Test your solution here: [anchor href=https://judge.softuni.bg/Contests/Practice/Index/503#3]https://judge.softuni.bg/Contests/Practice/Index/503#3[/anchor].

Try to **better your solution**, so that it doesn't have many repeating commands. Could it be done with a `for` loop? Did you find a smart solution (for example with a loop) of the previous task? With this task you can also use something similar, but a bit more complex (two loops, one inside the other). If you don't succeed, there is no problem, we will be learning loops in a few chapters and you will be reminded of this task then.
[/slide]

[slide]
# Problem: rectangle area

[code-task title="Rectangle Area" executionStrategy="csharp-dot-net-core-code"]

[code-editor language=csharp]
[/code-editor]

[task-description]
Write a C# program, which **reads** from the console **two numbers, a and b**, **calculates** and **prints** the are of a rectangle with sides **a** and **b**. 
[/task-description]

[code-io /]

[/code-task]

## Sample Input and Output

|  a | b  | area |
|----|----|------|
| 2  | 7  |  14  |
| 7  | 8  |  56  |
| 12 | 5  |  60  |

## Hints and Guidelines

We make a new **console C# program**. To **read both of the numbers**, we use the folloing commands:

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-1-images/05.Rectangle-area-01.png alt="Code" /]

Its left to finish the program above, to calculate the area of the rectangle and to print it. Use the command that is already known to us `Console.WriteLine()` and put inside its brackets the multiplication of the numbers **a** and **b**. In programming, multiplication is done with the operator `*`.

## Test your solution

Test your solution with a few examples. You have to receive a result, similar to this one (we enter 2 and 7 as  input and the program prints result 14 - their multiplication):

```
2
7
14
```

## Testing in the Judge System

Test your solution here: [anchor href=https://judge.softuni.bg/Contests/Practice/Index/503#4]https://judge.softuni.bg/Contests/Practice/Index/503#4[/anchor].
[/slide]

[slide]
# \* Problem: a square of stars

[code-task title="Square of Stars" executionStrategy="csharp-dot-net-core-code"]

[code-editor language=csharp]
var n = int.Parse(Console.ReadLine());
// TODO: Print the square
[/code-editor]

[task-description]
Write a C# console program, which **reads** from the console **a whole positive number N** and **prints** on the console **a square of N stars**, like in the examples below.
[/task-description]

[code-io /]

[/code-task]

## Sample Input and Output

| Input |    Outup   	| Input |    Output   | Input |    Output   | 
|-------|---------------|-------|-------------|-------|-------------|
|  3  	|<code>\*\*\*</code><br><code>\*&nbsp;\*</code><br><code>\*\*\*</code>|  4  |<code>\*\*\*\*</code><br><code>\*&nbsp;&nbsp;\*</code><br><code>\*&nbsp;&nbsp;\*</code><br><code>\*\*\*\*</code>| 5  |<code>\*\*\*\*\*</code><br><code>\*&nbsp;&nbsp;&nbsp;\*</code><br><code>\*&nbsp;&nbsp;&nbsp;\*</code><br><code>\*&nbsp;&nbsp;&nbsp;\*</code><br><code>\*\*\*\*\*</code>|

## Hints and Guidelines

We create a new **console C# program**. To read the number N (2 ≤ N ≤100), we use the following code:

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-1-images/06.Square-of-stars-01.png alt="Code" /]

Finish the program above, so that it prints a square, made of stars. It might be necessary to use `for` loops. Look for an information in the Internet.

**Attention**: this task is harder than the rest and is given now on puprose and it's marked with a star, in order to provoke you to look for information in the Internet. This is one of the most important skills, which you have to develop while you're learning programing: **looking for information in the Internet**. This is what you're going to do every day, if you work as developers, so don't be scared, try it out. If you have any difficulties you can also ask for help in the [anchor href=https://softuni.bg/forum]SoftUni forum[/anchor].

## Testing in the Judge System

Test your solution here: [anchor href=https://judge.softuni.bg/Contests/Practice/Index/503#5]https://judge.softuni.bg/Contests/Practice/Index/503#5[/anchor].
[/slide]