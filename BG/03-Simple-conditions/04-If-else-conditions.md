[slide]
# The if-else statement

The `if` construction may also contain an `else` clause to give a specific action in case the boolean expression (which is set at the beginning `if (boolean expression)` ) returns a negative result (`false`). Built this way, **the conditional construction** is called `if-else` and its behavior is as follows: if the result of the condition is **positive** (`true`) - we perform some actions, a when it is **negative** (`false`) - others. The format of the construction is:

```csharp
if (condition)
{
    // condition body;
}
else
{
    // еlse construction body;
}

```

## Example: excellent grade or not

[code-task title="Excellent grade or not" executionStrategy="csharp-dot-net-core-code"]

[code-editor language=csharp]
var grade = double.Parse(Console.ReadLine());
// TODO
[/code-editor]

[task-description]
Like the example above, we read the grade from the console and check if it's excellent, but this time we should **output the result in both cases**.
[/task-description]

[code-io /]

[/code-task]

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-3-images/02.Excellent-or-not-01.png alt="Code" /]

### Testing in judge system

Test your solution here: [anchor href=https://judge.softuni.bg/Contests/Practice/Index/506#1]           https://judge.softuni.bg/Contests/Practice/Index/506#1[/anchor].
[/slide]

[slide]
# For curly braces {} after if / other

When we have **only one command** in the body of the ** if construction**, we can **skip the curly brackets**, indicating the conditional operator body. When we want to execute **block of code** (group of commands), curly brackets are **required**. In case we drop them, **only the first line**  after **if clause** will be executed.

<table><tr><td><img src="https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/alert-icon.png" style="max-width:50px" /></td><td>It's a good practice to <strong>always put curly braces,</strong> because it makes our code more readable and clean.</td></tr></table>

Here is an example where dropping curly braces leads to confusion:

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-3-images/00.Brackets-tip-01.png alt="Code" /]

Execute the above code will output the following console result:

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-3-images/00.Brackets-tip-03.png alt="Console" /]

With curly braces:

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-3-images/00.Brackets-tip-02.png alt="Code" /]

The following output will be printed on the console:

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-3-images/00.Brackets-tip-04.png alt="Console" /]
[/slide]

[slide]
# Example: even or odd

Write a program that checks whether an integer is **even** or **odd**.

[code-task title="Even or Odd" executionStrategy="csharp-dot-net-core-code"]

[code-editor language=csharp]
var num = int.Parse(Console.ReadLine());
if (num % 2 == 0)
// TODO
[/code-editor]

[task-description]
We can solve the problem with one `if-else` construction and the operator `%`, which returns a **remainder by dividing** from two numbers.
[/task-description]

[code-io /]

[/code-task]



## Testing in the Judge System

Test your solution here: [anchor href=https://judge.softuni.bg/Contests/Practice/Index/506#2]https://judge.softuni.bg/Contests/Practice/Index/506#2[/anchor].
[/slide]

[slide]
# Example: the larger number

Write a program that reads from the console two integers and takes the larger of them.

[code-task title="The larger number" executionStrategy="csharp-dot-net-core-code"]

[code-editor language=csharp]
[/code-editor]

[task-description]
Our first task is to **read** the two numbers from the console. Then, with a simple `if-else` construction, combined with the **operator for greater than** (`>`), we do check. Part of the code is deliberately blurred to test what we have learned so far.
[/task-description]

[code-io /]

[/code-task]		

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-3-images/04.Greater-number-02.png alt="Code" /]

## Testing in the Judge System

Test your solution here: [anchor href=https://judge.softuni.bg/Contests/Practice/Index/506#3]           https://judge.softuni.bg/Contests/Practice/Index/506#3[/anchor].
[/slide]
