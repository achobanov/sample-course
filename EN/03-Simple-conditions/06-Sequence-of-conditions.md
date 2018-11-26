[slide]
# Sequence of conditions

Sometimes we need to do a sequnce of conditions before we decide what actions our program will execute. In such cases, we can apply the construct `if-else if ... -else` **in serie**. For this purpose we use the following format:

```csharp
if (condition)
{
    // condition body;
}
else if (second condition)
{
    // condition body;
}
else if (third condition)
{
    // condition body;
}
…
else
{
    // else construction body;
}
```
[/slide]

[slide]
# Example: digit in English

[code-task title="Digit in English" executionStrategy="csharp-dot-net-core-code"]

[code-editor language=csharp]
int num = int.Parse(Console.ReadLine());

if (num == 1)
{
    Console.WriteLine("one");
}
else if (num == 2)
{
    // TODO
}
else if (…)
{
    // TODO
}
else if (num == 9)
{
    Console.WriteLine("nine");
}
else
{
    Console.WriteLine("number too big");
}
[/code-editor]

[task-description]
Print the digits in the range of 1 to 9 (the digit is read from the console). We can read the digit and then, through a **sequence of conditions** we print the relevant English word
[/task-description]

[code-io /]
[/code-task]

The program logic from the above example **sequentially compares** the input number from the console with the digits from 1 to 9, when **each sequent comparison is being performed only in case the previous comparison is not true**. Ultimately, if none of the `if` conditions are not executed, the last `else` **clause` is.

## Testing in the Judge System

Test your solution here: [anchor href=https://judge.softuni.bg/Contests/Practice/Index/506#4]https://judge.softuni.bg/Contests/Practice/Index/506#4[/anchor].
[/slide]
