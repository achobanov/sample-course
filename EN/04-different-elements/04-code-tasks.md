[slide]
# Regular code task

[code-task title="Print out Hello World" executionStrategy="csharp-dot-net-core-code" requiresInput]
[code-editor language=csharp]
```
using System;
public class App
{
    public static void Main()
    {
        var a = ...;

        var square = a * a;

        // Print square
    }
}
```

[/code-editor]
[/code-task]

[/slide]

[slide]
# Code task with hidden code

[code-task title="Print out Hello World" executionStrategy="csharp-dot-net-core-code" requiresInput]
[code-editor language=csharp has-hidden]
```
[hidden]
using System;
public class App
{
    public static void Main()
    {
        [/hidden]
        var a = ...;

        [hidden]
        var square = a * a;

        [/hidden]
        // Print square
        [hidden]
    }
}
[/hidden]
```
[/code-editor]
[/code-task]
[/slide]

[slide]

# Live code example
```csharp must-run title="Print out Hello World" executionStrategy="csharp-dot-net-core-code"
[hidden]
using System;
public class App
{
    public static void Main()
    {
[/hidden]   
        Console.WriteLine("Hello");
[hidden]
    }
}
[/hidden]
```
[/slide]
