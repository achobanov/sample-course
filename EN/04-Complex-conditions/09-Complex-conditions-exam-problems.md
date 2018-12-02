[slide]
# Chapter 4.2. More Complex Conditions – Exam Problems

The previous chapter introduced you to **nested conditions** in C#. Via nested conditions, the program logic in a particular application can be represented using `if` conditional statements** that are nested one into another. We also reviewed the `switch-case` conditional statement that allows selecting from a list of options. Now we are going to do some exercises and make sure we have in-depth understanding of the material, by examining a number of more complex problems that had been given to students on exams. Before moving to the tasks, let's first recall what nested conditions are.

## Nested Conditions

```csharp
if (condition1)
{
    if (condition2)
        // body; 
    else
        // body;
}
```

<table><tr><td><img src="https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/alert-icon.png" style="max-width:50px" /></td><td>Remember that it is not a good practice to write <strong>deeply nested conditional statements</strong> (with more than three levels of nesting). Aviod nesting of more than three conditional statements inside one another. This complicates the code and makes its reading and understanding difficult.</td>
</tr></table>

## Switch-case Conditions

When the program operation does not depend on the value of a variable, instead of doing consecutive checks with multiple `if-else` blocks, we can use the `switch-case` conditional statement.

```csharp
switch (selector)
{
    case value1
        statement;
        break;
    case value2
        statement;
        break;
    default
        statement;
        break;
}
```

The structure consists of:
- Selector - an expression that calculates a particular value. The selector type can be an integer, string or enum.
- Multiple `case` labels followed by commands, ending in a `break`.
[/slide]