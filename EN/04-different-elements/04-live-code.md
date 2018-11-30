[slide]
# code-task with hidden code

[code-task title='Print out Hello World' executionStrategy='csharp-dot-net-core-code' requiresInput]
[code-editor language=csharp]
```
using System;
public class App
{
    public static void Main()
    {
        // CODE_VISIBLE_START
        var a = ...;

        // CODE_VISIBLE_END
        var square = a * a;

        // CODE_VISIBLE_START
        // Print square
        // CODE_VISIBLE_END
    }
}
```
[/code-editor]
[/code-task]
[/slide]
