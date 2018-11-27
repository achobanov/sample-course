[slide]
# What it means "to program"?

**To program** means to give commands to the computer, for example "*to play a sound*", "*to print something on the screen*" or "*to multiply two numbers*". When the commands are one after another, they are called **a computer program**. The text of the computer programs is called **a program code** (or **a source code**, or even shorter - **code**).

## Computer programs

**Computer programs** represent **a sequence of commands**, which are written in a previously chosen **programming language**, like C#, Java, JavaScript, Python, Ruby, PHP, C, C++, Swift, Go or another. In order to write commands, we have to know **the syntax and the semantics of the language** which we are working with, in our case - **C#**. That is why we are going to get familiar with the syntax and the semantics of the language  C#, and with programing generally, in the current book  by learning step by step code writing from the simpler to the more complex programming constructions.

## Algorithms

Computer programs usually execute some algorithm. **Algorithms** are a sequence ot steps, necessary for the completion of a certain task and for gaining some expected result, something like a "recipe". For example, if we fry eggs, we follow some recipe (an algorithm): we warm up the oil in a pan, break the eggs inside it, wait for them to fry and move them away from the stove. Analogically, in programming **the computer programs execute algorithms**: a sequence of commands, necessary for the completion of a certain task. For example, to order a sequence of numbers in an increasing order, an algorithm is needed, in order to find the smallest number and print it, then find the smallest number amongst the rest and print it and this is repeated until there are no more numbers.

For convinience when creating programs, for writing programming code, for execution of programs and other operations related to programming, we need a **development environment**, for example Visual Studio.
[/slide]

[slide]
# Programming languages, compilers, interpeters and environments for development

**A programming language** is an artificial language (syntax for expressing), meant for **giving commands**        which we want the computer to read, process and execute.Through programming languages we write sequences of commands (**programs**), which **define what the computer should do**. The execution of computer programs can be done with **acompiler** or with **an interpreter**.

**The compiler** translates the code from programming lagnuage to **machine code**, as for each of the constructions (commands) in the code, it chooses a proper, preveiously prepared fragment of machine code and in the meantime it **checks the text of the program for errors**. Together, the compiled fragments comprise the program into a machine code, as the microprocessor of the computer expects it. After the program has been compiled, it can be executed directly from the microprocessor in cooperation with the operating system. With compiled programming languages **the compilation of the program** is done mandatorily before its execution and during compile time can be found syntax errors (wrong commands). Languages like C++, C#, Java, Swift and Go work with a compiler.

Some programming languages do not use a compiler and are being **interpreted directly** form a specialized software,  called an "interpreter". **The interpreter** is  "**a program for executing programs**", written in some programming language. It executes the commands in the program one after another, as it understands not only a single command and sequences of commands, but also other language constructions (evaluations, iterations, functions, etc.). Languages like PHP, Python and JavaScript work with an interpreter and are being executed whithout being compiled. Due to the absence of previous compilation, with inerpreted languages **the errors are being found during runtime**, after the program starts running, not previously.

**An environment for development** (Integrated Development Environment - **IDE**) is an union of taditional tools for development of software applications. In the environment for development we write code, compile and execute the programs. Environments for development integrate in them **a text editor** for writing code, **a programming language**, **a complier or an interpreter** and **a runtime environment** for executing programs, **a debugger** for tracking the program and seeking out errors, **tools for user interface design** and other tools and add-ons.

**Environments for development** are convinient, because they integrate everything necessary for the development of the program, whithout the need to exit the environment. If we don't use an environment for development, we will have write the code in a text editor, to compile it with a command in the console, to run it with another command in the console and to write more additional commands when we need to and that would waste us time. That is why most of the programmers use an IDE in their everyday work.

For programming with **the language C#** it is mostly used  **Visual Studio** IDE, which is  developed and spread freely by Microsoft and can be downloaded from: [anchor href=https://www.visualstudio.com/downloads/]https://www.visualstudio.com/downloads/[/anchor]. Alternatives of Visual Studio are **Rider** ([anchor href=https://www.jetbrains.com/rider/]https://www.jetbrains.com/rider/[/anchor]) и **MonoDevelop** / **Xamarin Studio** ([anchor href=http://www.monodevelop.com]http://www.monodevelop.com[/anchor]) and **SharpDevelop** ([anchor href=http://www.icsharpcode.net/OpenSource/SD/]http://www.icsharpcode.net/OpenSource/SD/[/anchor]). In the current book, we are going to use the development enivironment Visual Studio.
[/slide]

[slide]
# Low and high level languages, runtime environments

The program in its core is a **sequence of instructions**, which make the computer do a certain task. They are being entered by the programmer and **are being executed unconditionally by the machine**.

There are different kinds of **programming languages**. With languages of the lowest level can be written **the instructions** that **manage the processor**, for example with the language "**assembler**". With a bit higher level languages, like **C** и **C++**, can be created an operating system, drivers for hardware management (for example a video card driver), web browsers, compilers, engines for graphics and games (game engines) and other system components and programs. With languages from even higher level, like **C#**, **Python** and **JavaScript** are being created applicable programs, for example a program for reading emails or a chat program.

**The languages from low level** manage the hardware directly and require a lot of effort and a large count of commands to do a single task. **Languages of higher level** require less code for a single task, but do not have a direct access to hardware. With them is being developed an application software, for example web applications and mobile applications.

The majority of software that we use daily, like a music player, a video player, a GPS program, etc., is written with **languages for application programming**, which are high level, like C#, Java, Python, C++, JavaScript, PHP and others.

**C# is a compiled language**, and that means that we write commands which are being compiled before they're being executed. Exactly these commands, through a help program (a compiler), are being transformed into a file, which can be executed (executable). To write a language like **C#** we need a text editor or an environment for development and **.NET Runtime Environment**.

**.NET Runtime Environment** represents a virtual machine, something like a computer in the computer, which can run a compiled C# code. With the risk of going too deep into details, we have to explain that the language C# is compiled into an intermediary .NET code and is executed from the .NET environment, which compiles this intermediary code additionally into machine instructions (machine code) in order to be executed by the microprocessor. .NET environment contains libraries with classes, **CSC** compiler, **CLR** (Common Language Runtime - CLR) and other components, which are required for working with the language C# and run C# programs.

**The environment .NET** is available as a free software with open source code for every modern operating system (like Windows, Linux and Mac OS X). It has two variations, **.NET Framework** (the older) and **.NET Core** (the newer), but none of that is of essential meaning when it comes to getting into programming. Let us focus on writing programs with the language C#.
[/slide]

[slide]
# Computer programs - compilation and execution

As we have already mentioned, the program is **a sequence of commands**, otherwise said, it describes a sequence of calculations, evaluations, iterations and all kinds of similar operations, which aim to accomplish some kind of result.

The program is written in a text format, and the text of the program itself is called **a source code**. It gets compiled to an **executable file** (for example `Program.cs` gets compiled to `Program.exe`) or it it is **executed directly** from the .NET environment.

The process of **compilation** of the code before  its execution is used only in compiled languages like C#, Java and C++. With **scripts and interpreted languages**, like JavaScript, Python and PHP, the source code gets executed step by step by an interpreter.
[/slide]

[slide]
# Computer programs – examples

Let's start with a very simple example of a short C# program.

## Example: a program that plays the musical note "la"

[code-task title="Program That Plays the Musical Note "la"" executionStrategy="csharp-dot-net-core-code"]

[code-editor language=csharp]
Console.Beep(432, 500);
[/code-editor]

[task-description]
Our first program is going to be a single C# command, that plays the musical note "la" (432 Hz) with a duration of half a second (500 miliseconds):
[/task-description]

[code-io /]

[/code-task]

In a short time we will find out how we can execute this command and hear the sound of the note, but for now let's just look at what the commands in programming represent. Let's get to know a couple of more examples.
[/slide]

[slide]
# Example: a program that plays a sequence of musical notes

[code-task title="Program That Plays a Sequence of Musical Notes" executionStrategy="csharp-dot-net-core-code"]

[code-editor language=csharp]
for (i = 200; i <= 4000; i += 200)
{
    Console.Beep(i, 100);
}
[/code-editor]

[task-description]
We can complicate the previous program by giving for execution repeating commands in a loop for playing a sequence of notes with rising height.
[/task-description]

[code-io /]

[/code-task]

In the example above we made the computer play one after another for a very short time (100 miliseconds) all of the notes with height 200, 400, 600 etc. Hz until they reach 4000 Hz. The result of the program is playing something like a melody.

How do iterations (cycles) work in programming, we will learn in the **chapter "[anchor href=#]Loops[/anchor]"**, but for now just accept that we repeat some command many times.
[/slide]

[slide]
# Example: a program that converts from leva to euro

[code-task title="Program That Converts From Leva to Euro" executionStrategy="csharp-dot-net-core-code" requiresInput]

[code-editor language=csharp]
var leva = int.Parse(Console.ReadLine());
var euro = leva / 1.95583;
Console.WriteLine(euro);
[/code-editor]

[task-description]
Let's take a look at another simple program that reads from the user some amount of money in leva (an integer number), converts it into euro (by dividing it by the euro's rate) and prints the received result. This is a program of 3 consecutive commands.
[/task-description]

[code-io /]

[/code-task]

We looked at **three examples of computer programs**: a single command, series of commands in a loop and 3 consecutive commands. Now let's get to the more intersting part: how can we write our own programs in **C#** and how can we compile them and run them?
[/slide]