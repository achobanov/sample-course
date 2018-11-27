[slide]
# How to write a console application?

Let's pass through **the steps for creating and executing a computer program**, that reads and writes its data from and on the text console (a window for entering and receivng text). These programs are called "**console**". But before that, we have to **install and prepare the development environment**, in which we are going to write and run the C# programs from this book and the exercises in it.

## Develpment environment (IDE)

As it has already been said, to program we need a **development environment** - **Integrated Development Environment** (IDE). This is actually an editor for programs, in which we write the program code and we can compile it and run it to see the errors, to fix them and to start the program again.

- For programming with C# we use **Visual Studio** IDE for Windows operating system and **MonoDevelop** or **Raider** for Linux or Mac OS X.
- If we program with Java, the environments **IntelliJ IDEA**, **Eclipse** or **NetBeans** are suitable.
- If we write Python, we can use the environment **PyCharm**.
[/slide]

[slide]
# Installation of Visual Studio Community

We begin with the installation of the integrated environment **Microsoft Visual Studio Community** (version 2017, latest until June 2017 г.).

**The Community** version of Visual Studio (VS) is spread freely from Microsoft and can be downloaded from: [anchor href=https://www.visualstudio.com/vs/community]https://www.visualstudio.com/vs/community[/anchor]. The installation is typical for Windows with [**Next**], [**Next**] and [**Finish**], but it's important to include the components for "**desktop development**" and "**ASP.NET**". It is not necessary to chagne the rest of the settings for the installation.

In the next lines are described in details **the steps for the installation of Visual Studio** (version Community 2017). After we download the installation file and start it, the following screen appears:

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-1-images/00.visual-studio-1.png alt="Visual Studio Installer" /]

We press the button [**Continue**] after which we will see the window bellow:

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-1-images/00.visual-studio-2.png alt="Visual Studio Installer" /]

A window with the installation panel of Visual Studio is being loaded.

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-1-images/00.visual-studio-3.png alt="Visual Studio Installer" /]

We put a check on the [**Universal Windows Platform development**], [**.NET desktop development**] and [**ASP.NET and web development**], after which we press the button [**Install**]. Basically, this is everything.

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-1-images/00.visual-studio-4.png alt="Visual Studio Installer" /]

The installation of Visual Studio begins and a screen like the one bellow will appear:

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-1-images/00.visual-studio-5.png alt="Visual Studio Installer" /]

After Visual Studio is installed, an informative screen will appear and we have to press the [**Launch**] button, to start it.

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-1-images/00.visual-studio-6.png alt="Visual Studio Installer" /]

After **the start of VS** a screen appears like the one bellow. From it we can choose whether to enter with our Microsoft account in Visual Studio. For the moment, we choose to continue whithout being logged into our Microsoft account, and this is why we choose the option [**Not now, maybe later.**]. At a later point, if you have such an account, you may log in, and if you don't have and you meet difficulties with its creation, you can always write in the [anchor href=https://softuni.bg/forum]forum of SoftUni[/anchor].

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-1-images/00.visual-studio-7.png alt="Visual Studio Installer" /]

The next step is to choose **the color theme**, with which Visual Studio is visualized. The choice here lays completely on the preferences of the user and it doesn't matter which option will be chosen. 

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-1-images/00.visual-studio-8.png alt="Visual Studio Installer" /]

We press the button [**Start Visual Studio**] and the main view of Visual Studio Community is being displayed:

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-1-images/00.visual-studio-9.png alt="Visual Studio Start Page" /]

This is everything. We are ready for working with Visual Studio.

## Older versions of Visual Studio

We can use older versions of Visual Studio (for example version 2015 or 2013 or even 2010 or 2005), but **it is not recomended**, as they don't contain some of the newer options for development and not all of the examples from the book will start.
[/slide]

[slide]
# Online environments for develepomnet

There are **alternative environments for development  online** dircetly into your web browser. These environments are not very convinient, but if you don't have other opportunity, you can start your training with them and to install Visual Studio later. Here are some useful links:

- For the language C# the site **.NET Fiddle** allows code writing and its execution online: [anchor href=https://dotnetfiddle.net]https://dotnetfiddle.net[/anchor].
- For Java we can use the following online Java IDE: [anchor href=https://www.compilejava.net]https://www.compilejava.net[/anchor].
- For JavaScript we can write a JS code directly in the console of a given browser when you press [**F12**].
[/slide]

[slide]
# Project solutions and projects in Visual Studio

Before we start working with Visual Studio, it is necessary to get familiar with the concepts of a **Visual Studio Solution** and a **Visual Studio Project**, which are an inevitable part of it.

**Visual Studio Project** represents "the project" we are working on. In the beginning, these will be our console applications, which we are going to learn how to write with the help of the current book, the resources in it and  the course Programming Basics in SoftUni. With deeper learning, time and practice, these projects will pass into desktop applications, web applications and other developments. The project in VS **logically groups loads of the files** constructing a given application or a component. One **C# project** contains one or a few **C# source files**, configuration files and other resources. In every C# source file there is one or more **definition of types** (classes or other definitions). In **the classes** there are **methods** (actions), and they contain **a sequence of commands**. It sounds complicated, but with bigger projects, a structure like this one is very convinient and allows a good organization of the work files.

**Visual Studio Solution** represents a container (a work solution), in which **a few projects are logically bound**. The purpose of the binding of these VS Projects is to create an opportunity for the code from any of the projects, to collaborate with the code from the rest VS projects, in order for the application or the website to work correctly. When the software product or a service which we develop is big, it is build as a **VS Solution**, and this Solution is split into **projects** (VS Projects) and inside each project there are **folders with source files**. This hierarchical organization is much more convinient with more serious projects (let's say over 50 000 rows of code).

For **smaller projects** VS Solutions and VS Projects are  **complicating the work**, rather then helping, but you will get used to it quckly.
[/slide]

[slide]
# Example: creating a console application "Hello C#"

[code-task title="Hello C#" executionStrategy="csharp-dot-net-core-code"]

[code-editor language=csharp]
[/code-editor]

[task-description]
Write a console application that prints "Hello C#" message on the console.
[/task-description]

[/code-task]

Let's get back to our console program. We already have Visual Studio and we can start it. Afterwards we create a new console project: [**File**] &rarr; [**New**] &rarr; [**Project**] &rarr; [**Visual C#**] &rarr; [**Windows**] &rarr; [**Console Application**].

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-1-images/01.Hello-csharp-01.png alt="Visual Studio" /]

We set **a meaningful name** to our program, for example `HelloCSharp`:

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-1-images/01.Hello-csharp-02.png alt="Visual Studio" /]

Visual Studio is going to create for us **an empty C# program**, which we have to finish writing (VS Solution with VS Project in it, with C# source file in it, with one C# class in it, with `Main()` method in it).

## Writing the program code

The source code of the C# program is written in the section `Main(string[] args)`, between the opening and the closing parentheses `{ }`. This is the main method (action), that is being executed with the start of a C# program. This `Main()` method can be written two ways:

- `static void Main(string[] args)` - with parameters from the command line (we are not going into details)
- `static void Main()` - without parameters from the command line.

Both ways are valid, as **the second one is recomended**, because it is shorter and clearer. By default, though, when creating a console application,Visual Studio uses the first way, which we can edit manually if we want and delete the part with the parameters `string[] args`.

We press [**Enter**] after **the opening parentheses** `{` and **we start writing**. The code of the program is written **inward**, as this is a part of the convention for the text, for convenience during a review and/or debugging.

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-1-images/01.Hello-csharp-03.png alt="Visual Studio" /]

We write the following command:

```csharp
Console.WriteLine("Hello C#");
```

Here is how our program should look in Visual Studio:

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-1-images/01.Hello-csharp-04.png alt="Visual Studio" /]

The command `Console.WriteLine("Hello C#")` in the language C# means to execute a print (`WriteLine(…)`) on the console (`Console`) and to print the text message `Hello C#`, which we have to surround by quotation marks, in order to clear out, that this is a text. In the end of each command in the language C# the symbol `;` is being put and it says that the command ends in that place (it doesn't continue on the next row).

This command is very typical in programming: we say a given **object** should be found (in this case the console) and some **action** should be executed upon it (in this case it is printing something that is given inside the brackets). More technically explained, we call the method `WriteLine(…)` from the class `Console` and give as a parameter to it a text literal `"Hello C#"`.

## Starting the program

To start the program, we press [**Ctrl + F5**]. If there aren't any errors, the program will be executed. The result will be written on the console (in the black window):

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-1-images/01.Hello-csharp-05.png alt="Console" /]

Notice, that we start it with **[Ctrl+F5]**, and not only **[F5]** or with the start button in Visual Studio. If we use **[F5]**, the program will run shortly and right afterwards the black window will disappear and we are not going to see the result.

Actually, the exit from the program is the following text message:

```csharp
Hello C#
```

The message "**Press any key to continue ...**" is written additionally on the bottom row in the Visual Studio console after the program ends, in order to tell us to see the result from the execution and to press a button to close the console.

## Test the program in the Judge System

The testing of the problems in this book is automated and is done through the Internet, from the site [anchor href=https://judge.softuni.bg]**Judge system**[/anchor]. The evaluation of the tasks is done immediately form the system. Each task goes through a sequence of tests, as every successfully passed test gives the points considered for it. The tests, which are given for the tasks are hidden.

We can test the program above here: [anchor href=https://judge.softuni.bg/Contests/Practice/Index/503#0]https://judge.softuni.bg/Contests/Practice/Index/503#0[/anchor]. We put the source code from the program in the black field and we choose **C# code**, the way it is shown:

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-1-images/01.Hello-csharp-06.png alt="Judge System" /]

We send our solution for evaluation with the button [**Send**]. The system gives a result back in a few seconds in the table with sent solutions. When necessary, we can press the button for renewing the results **[refresh]** in the upper right side of the table with sent solutions:

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-1-images/01.Hello-csharp-07.png alt="Judge System" /]

In the table with the sent solutions the judge system is going to show one of the following **possible results**:

- **Points count** (between 0 and 100), when the turned  in code code gets compiled succesfully (there are no syntax errors) and can be tested.
  - When the **solution is correct** all of the tests are marked in green and we receive **100 points**.
  - When the **solution is incorrect** some of the tests are marked in red and we receive incomplete or 0 points.
- When the program is incorrect we will receive **a compile time error** message.

### How to register in SoftUni Judge?

Using your credentials (username + password) for the site softuni.bg. If you don't have a SoftUni registration, make one. It takes only a minute - a standart registration in an Internet site.
[/slide]

[slide]
# Test the programs that play notes

Now, after **you know how to run programs**, you can test your example programs above, which play musical notes. Have some fun, try these programs out. Try to change them and play with them. Exchange the command `Console.WriteLine("Hello C#");` with the command `Console.Beep(432, 500);` and start the program. Check if the sound of your computer is on and whether its turned up. If you work in an online environment, you will not hear a sound, because the program is not executued on your computer, but elsewhere.
[/slide]

[slide]
# Typical mistakes in C# programs

One of the common mistakes with beginners is **writing outside the body of the `Main()` method**, because the integrated environment or the compiler can't read the given commands in the program correctly. Here is an example for an incorrectly written program  :

```csharp
static void Main(string[] args)
{
}
Console.WriteLine("Hello C#");
```

Other mistake is switching **capital and small letters**, and it matters for calling the commands and their correct functioning. Here is an example of such mistake:

```csharp
static void Main(string[] args)
{
    Console.Writeline("Hello C#");
}
```

In the example above `Writeline` is written wrong and has to be fixed to `WriteLine`.

The absence of **a point and comma** (`;`) in the end of the commands is one of the eternal problems of the beginner programmer. Skipping this sign leads to **incorrect functioning of the program** and **often the problem stays unnoticed**. Here is an example of a mistaken code:

```csharp
static void Main(string[] args)
{
    Console.Writeline("Hello C#")
}
```

The missing **quotation mark** or **the absence of openning or closing parentheses** can also turn out to be problems. The same as the point and the comma, here also the problem leads to **incorrect functioning of the program** or overall to its failure. This mistake is hardly noticeble with a bigger code. Here is an example of  a program with errors:

```csharp
static void Main(string[] args)
{
    Console.WriteLine("Hello C#);
}
```

This program will throw **a compile time error** and the build is going to fail and even before that, the code will become underlined, in order to point the programmer to the mistake that he made (the missing closing quotation mark):

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-1-images/01.Hello-csharp-08.png alt="Visual Studio" /]
[/slide]