[slide]
# Simple conditions

In programming we often **check the conditions** and perform different actions, depending on the result of the check. This is done by **if** verification, which has the following construction:

```csharp
if (condition)
{
    // condition body;  
}
```

## Example: excellent grade

[code-task title="Excellent Grade" executionStrategy="csharp-dot-net-core-code" requiresInput]

[code-editor language=csharp]
[/code-editor]

[task-description]
We read the grade from the console and check if it's excellent (`≥ 5.50`).

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-3-images/01.Еxcellent-result-01.png alt="Code" /]

Test the code from the example locally. Try entering different grades, for example **4.75**, **5.49**, **5.50** and **6.00**. For grades **less than 5.50**, the program will not give any output, however if the grade is **5.50 or greater**, the output would be "**Excellent!**".
[/task-description]

[code-io /]
[/code-task]

### Testing in the Judge System

Test your solution here: [anchor href=https://judge.softuni.bg/Contests/Practice/Index/506#0]https://judge.softuni.bg/Contests/Practice/Index/506#0[/anchor].
[/slide]
