[slide]
# Switch-case construction

The construction `switch-case` works as a sequence of `if-else` blocks. Whenever the work of our program depends on the value of **one variable**, instead of making consecutive conditions with `if-else` blocks, we can **use** the conditional `switch` statement. It is being used for a **choice between a list of possibilities**. The statement compares a given value with defined constants and depending on the result, takes an action.

We put **the variable**, which we want to **compare**, inside the **brackets after the operator `switch` and it is called a "**selector**". Here **the type must be comparable** (numbers, strings). **Consecutively** begins the **comparing** of each **value**, which **is found** after the `case` labels**. On a match, the execution of the code from the respective place begins and continues until it reaches the operator `break`. In some programming languages (like C and C++) `break` might be skipped, in order to execute a code from other `case` construction, until it reaches another operator. In C# though, the presence of `break` is **mandatory** for **every `case`, which contains a program logic. When **no matches** are **found**, the `default` construction is being executed, **if** such **exists**.

```csharp
switch (selector)
{
    case value1:
        construction;
        break;
    case value2:
        construction;
        break;
    case value3:
        construction;
        break;
    …
    default:
        construction;
        break;
}
```
[/slide]

[slide]
# Example: day of week

[code-task title="Day of Week" executionStrategy="csharp-dot-net-core-code" requiresInput]

[code-editor language=csharp]
int day = int.Parse(Console.ReadLine());

switch (day)
{
    case 1: 
        Console.WriteLine("Monday");
        break;
    case 2: 
        // TODO
    // ...
    default: 
        Console.WriteLine("Error!");
        break;
}
[/code-editor]

[task-description]
Let's write a program that prints **the day of the week** depending on the **given number** (1 … 7) or "**Error!**", if an invalid input is given.
[/task-description]

[code-io /]
[/code-task]

## Sample Input and Output

|    Input   |          Output          |
|------------|--------------------------|
|1<br>7<br>-1|Monday<br>Sunday<br>Error!|

## Solution

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-4-images/09.Day-of-week-01.png alt="Code" /]

**A good practice** is to put on **first** place  those `case` **statement**, which process **the most common situations**, and the `case` **constructions**, processing **the more rear situations** to leave at **the end, before  the `default` construction**. Another **good practice** is to **arrange the `case` labels** in **ascending order**, no mather is they are integral or symbolic.

## Testing in the Judge System

Test your solution here: [anchor href=https://judge.softuni.bg/Contests/Practice/Index/508#8]https://judge.softuni.bg/Contests/Practice/Index/508#8[/anchor].
[/slide]

[slide]
# Multiple cases in switch-case

In **C#** we have the possibility to **use multiple `case` labels, when they have to execute **the same code**. By this way, when our **program** finds a **match**, it will execute the **next** code, because **after** the respective `case` label **there is no code** for execution and a `break` operator.

```csharp
switch (selector)
{
    case value1:
    case value2:
    case value3:
        construction;
        break;
    case value4:
    case value5:
        construction;
        break;
    …
    default:
        construction;
        break;
}
```
[/slide]

[slide]
# Example: animal type

[code-task title="Animal Type" executionStrategy="csharp-dot-net-core-code" requiresInput]

[code-editor language=csharp]
switch (animal)
{
    case "dog":
        Console.WriteLine("mammal");
        break;
    case "crocodile":
    case "tortoise":
    case "snake":
        Console.WriteLine("reptile");
        break;
    default:
        Console.WriteLine("unknown");
        break;
}
[/code-editor]

[task-description]
Write a program, that prints the type of the animal depending on its name: 

- dog -> **mammal**
- crocodile, tortoise, snake -> **reptile**
- others -> **unknown**
[/task-description]

[code-io /]
[/code-task]

## Sample Input and Output

|  Input  | Output | Input | Output |  Input  | Output |
|---------|--------|-------|--------|---------|--------|
|tortoise |reptile |dog    |mammal  |elephant |unknown |

## Solution

We can solve the task with `switch-case` conditions with multiple labels in the following way:

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-4-images/10.Animal-type-01.png alt="Code" /]

## Testing in the Judge System

Test your solution here: [anchor href=https://judge.softuni.bg/Contests/Practice/Index/508#9]https://judge.softuni.bg/Contests/Practice/Index/508#9[/anchor].
[/slide]