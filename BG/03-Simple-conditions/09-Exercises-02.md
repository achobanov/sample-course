[slide]
# Exercises: simple conditions

Now let's practise the lessons learned in this chapter with a few exercises.

## Empty Visual Studio solution (Blank Solution)

We create a blank solution (**Blank Solution**) in Visual Studio to organize better the task solutions from the exercise  - each task will be in a separate project and all projects will be in common solution.

We run Visual Studio and create new **Blank Solution:** [**File**] -> [**New**] -> [**Project**].

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-3-images/00.Visual-studio-01.png alt="Empty VS Solution" /]

Choose from the dialog box [**Templates**] -> [**Other Project Types**] -> [**Visual Studio Solutions**] -> [**Blank Solution**] and give a appropriate project name, for example: “Simple-Conditions”:

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-3-images/00.Visual-studio-02.png alt="Empty VS Solution" /]

Now we have empty Visual Studio Solution (no projects in it):

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-3-images/00.Visual-studio-03.png alt="Empty VS Solution" /]
[/slide]

[slide]
# Problem: excellent grade

The first exercise for this topic is to write a **console program** that **inputs the grade** (decimal number) and prints **Excellent!** if the grade is **5.50** or high.

[task]  
    [code-editor language=csharp]
        var grade = double.Parse(Console.ReadLine());
    [/code-editor]

    [task-description]
    [/task-description]
[/task]	

## Sample Input and Output

| Input |    Output   |
|-------|-------------|
| 6     | Excellent!  |
| 5     | (no output) |
| 5.5   | Excellent!  |
| 5.49  | (no output) |

## Create a new C # project

We create **a new project** in the existing Visual Studio solution. In **Solution Explorer**, right-click on **Solution 'Simple-Conditions'**. Then choose [**Add**] -> [**New Project**]:
 
[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-3-images/09.Excellent-result-01.png alt="New Console Project" /]

A dialog box will open for selecting a project. We choose **C # console application** and create a name, for example "Excellent-Result":
 
[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-3-images/09.Excellent-result-02.png alt="New Console Project" /]
 
Now we have a solution with one console application in it. It remains to write the code to solve the problem.

## Writing the code

For this purpose we go into the body of the `Main (string [] args)` method and write the following code:

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-3-images/09.Excellent-result-03.png alt="Code" /]

**Run** the program with [**Ctrl+F5**], to test it with different input values:

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-3-images/09.Excellent-result-04.png alt="Console" /]

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-3-images/09.Excellent-result-05.png alt="Console" /]

## Testing in the Judge System

Test your solution here: [anchor href=https://judge.softuni.bg/Contests/Practice/Index/506#0]           https://judge.softuni.bg/Contests/Practice/Index/506#0[/anchor].

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-3-images/09.Excellent-result-06.png alt="Judge System" /]

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-3-images/09.Excellent-result-07.png alt="Judge System" /]
[/slide]

[slide]
# Problem: excellent grade or not

The next exercise from this topic is to write a **console program** that **inputs the grade** (decimal number) and prints **Excellent!** if the rating is **5.50** or higher , otherwise "**Not excellent.**".

[task]  
    [code-editor language=csharp]
        var grade = double.Parse(Console.ReadLine());
    [/code-editor]
[/task]	

## Sample Input and Output

| Input |     Output     |
|-------|----------------|
| 6     | Excellent!     |
| 5     | Not excellent. |
| 5.5   | Excellent!     |
| 5.49  | Not excellent. |

## Create a new C # project

First we create **a new C# console project** in the **Simple-Conditions** solution.

- We click on the solution in Solution Explorer and choose [**Add**] -> [**New Project**].
- We choose [**Visual C#**] -> [**Windows**] -> [**Console Application**] and create a name, for example: “Excellent-or-Not”.
 
Now we have to **write the code** of the program. We can help with the sample code from the picture:  

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-3-images/02.Excellent-or-not-01.png alt="Code" /]

## Auto set startup the project

We turn on mode to **automatic switching to the current project** by clicking on the main Solution with the right mouse button and choosing [**Set StartUp Projects...**]:

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-3-images/02.Excellent-or-not-02.png alt="Set Startup Project" /]

A dialog box will appear and you have to choose [**Startup Project**] -> [**Current selection**]:
 
[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-3-images/02.Excellent-or-not-03.png alt="Set Startup Project" /]

## Test the app

Now **we run the program** as usual with [**Ctrl + F5**] and test it if it works correctly:

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-3-images/02.Excellent-or-not-04.png alt="Console" /]
[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-3-images/02.Excellent-or-not-05.png alt="Console" /]

## Testing in the Judge System

Test your solution here: [anchor href=https://judge.softuni.bg/Contests/Practice/Index/506#1]https://judge.softuni.bg/Contests/Practice/Index/506#1[/anchor].

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-3-images/02.Excellent-or-not-06.png alt="Judge System" /]
[/slide]

[slide]
# Problem: even or odd

Write a program that checks whether an **integer** is **even** or **odd**.

[task]  
    [code-editor language=csharp]
    [/code-editor]

    [task-description]
        Checking if the given number is even can be done with the operator `%`.
    [/task-description]
[/task]	

## Sample Input and Output

| Input | Output |
|-------|--------|
| 2     | even   |
| 3     | odd    |
| 25    | odd    |
| 1024  | even   |

## Hints and Guidelines

Again, first we add **a new C # console project** in the existing solution. In the `static void Main ()` method, we have to write the program code. Checking if the given number is even can be done with the operator `%`, which will return the **remainder from an integer divided by 2** as follows: `var isEven = (num % 2 == 0)`.

Now we **run** the program with [**Ctrl + F5**] and test it:

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-3-images/03.Even-or-odd-01.png alt="Console" /]

## Testing in the Judge System

Test your solution here: [anchor href=https://judge.softuni.bg/Contests/Practice/Index/506#2]https://judge.softuni.bg/Contests/Practice/Index/506#2[/anchor].
[/slide]

[slide]
# Problem: Greater number

Write a program that inputs **two integers** and prints the larger one.

[task]  
    [code-editor language=csharp]
    [/code-editor]
[/task]	

## Sample Input and Output

|  Input | Output |
|--------|--------|
|5<br>3  | 5      |
|3<br>5  | 5      |
|10<br>10| 10     |
|-5<br>5 | 5      |

## Hints and Guidelines

As usual, first we need to add a **new C # console project** to the existing solution. For the code of the program we need a single `if-else` construction. You can partially help with the code from the picture that is deliberately blurred to think about how to write it yourself:

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-3-images/04.Greater-number-02.png alt="Code" /]

When we are done with the implementation of the solution, we **run** the program with [**Ctrl + F5**] and test it:

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-3-images/04.Greater-number-01.png alt="Console" /]

## Testing in the Judge System

Test your solution here: [anchor href=https://judge.softuni.bg/Contests/Practice/Index/506#3]https://judge.softuni.bg/Contests/Practice/Index/506#3[/anchor].
[/slide]

[slide]
# Problem: digit in english

Write a program that inputs **an integer in the range** [**0 ... 9**] and output it **with words** in English. If the number is out of range, print "**too large a number**".

[task]  
    [code-editor language=csharp]
    [/code-editor]

    [task-description]
        You can use a series of `if-else` conditions to create the possible **11 cases**.
    [/task-description]
[/task]	

## Sample Input and Output

| Input |     Output     |
|-------|----------------|
| 5     | five           |
| 1     | one            |
| 9     | nine           |
| 10    | number too big |

## Hints and Guidelines

We can use a series of `if-else` conditions to create the possible **11 cases**.

## Testing in the Judge System

Test your solution here: [anchor href=https://judge.softuni.bg/Contests/Practice/Index/506#4]https://judge.softuni.bg/Contests/Practice/Index/506#4[/anchor].
[/slide]

[slide]
# Problem: guess the password

Write a program that **inputs a password** (one line with random text) and checks if the input **matches** with the phrase "**s3cr3t! P @ ssw0rd**". If it matches, print "**Welcome**", otherwise "**Wrong password!**".

[task]  
    [code-editor language=csharp]
    [/code-editor]
[/task]	

## Sample Input and Output

|      Input      |      Output     |
|-----------------|-----------------|
| qwerty          | Wrong password! |
| s3cr3t!P@ssw0rd | Welcome         |
| s3cr3t!p@ss     | Wrong password! |

## Hints and Guidelines

Use the `if-else` construction.

## Testing in the Judge System

Test your solution here: [anchor href=https://judge.softuni.bg/Contests/Practice/Index/506#8]https://judge.softuni.bg/Contests/Practice/Index/506#8[/anchor].
[/slide]

[slide]
# Problem: number from 100 to 200

Write a program that **inputs an integer** and checks if it is **below 100**, **between 100 and 200** or **over 200**. Print the appropriate message as in the examples below.

[task]  
    [code-editor language=csharp]
    [/code-editor]
[/task]	

## Sample Input and Output

| Input |        Output       |
|-------|---------------------|
| 95    | Less than 100       |
| 120   | Between 100 and 200 |
| 210   | Greater than 200    |

## Testing in the Judge System

Test your solution here: [anchor href=https://judge.softuni.bg/Contests/Practice/Index/506#9]https://judge.softuni.bg/Contests/Practice/Index/506#9[/anchor].
[/slide]

[slide]
# Problem: equal words

Write a program that **inputs two words** and checks if they are the same. Do not make difference between uppercase and lowercase letters. You have to print "**yes**" or "**no**".

[task]  
    [code-editor language=csharp]
    [/code-editor]
[/task]	

## Sample Input and Output

|        Input       | Output |
|--------------------|--------|
| Hello<br>Hello     | yes    |
| SoftUni<br>softuni | yes    |
| Soft<br>Uni        | no     |
| beer<br>vodka      | no     |
| HeLlO<br>hELLo     | yes    |

## Hints and Guidelines

Before comparing the words, turn them to a lowercase to avoid the letter size influence (uppercase / lowercase): `word = word.ToLower()`.

## Testing in the Judge System

Test your solution here: [anchor href=https://judge.softuni.bg/Contests/Practice/Index/506#10]https://judge.softuni.bg/Contests/Practice/Index/506#10[/anchor].
[/slide]

[slide]
# Problem: speed info

Write a program that **inputs the speed** (decimal number) and prints **speed information**. For speed **up to 10** (inclusive), print "**slow**". For speed **over 10** and **up to 50**, print "**average**". For speed **over 50 and up to 150**, print "**fast**". For speed **over 150 and up to 1000**, print "**ultra fast**". For higher speed, print "**extremely fast**".

[task]  
    [code-editor language=csharp]
    [/code-editor]
[/task]	

## Sample Input and Output

| Input |    Output     |
|-------|---------------|
| 8     | slow          |
| 49.5  | average       |
| 126   | fast          |
| 160   | ultra fast    |
| 3500  | extremely fast|

## Testing in the Judge System

Test your solution here: [anchor href=https://judge.softuni.bg/Contests/Practice/Index/506#11]https://judge.softuni.bg/Contests/Practice/Index/506#11[/anchor].
[/slide]

[slide]
# Problem: area of figures

Write a program that ** inputs the sizes of a geometric figure** and **calculates its face**. The figures are four types: **square**, **rectangle**, **circle** and **triangle**.

The first line of the entrance reads the type of the figure (`square`, `rectangle`, `circle`, `triangle`).
- If the figure is **square**, the next row reads one number - the length of its side.
- If the figure is a **rectangle**, on the next two rows we read two numbers - the lengths of its sides.
- If the figure is **circle**, the next row reads one number - the radius of the circle.
- If the figure is **triangle**, on the next two rows we read two numbers - the length of the side and the length of its height.

Round the result up to the **third digit after the decimal point**.

[task]  
    [code-editor language=csharp]
    [/code-editor]
[/task]	

## Sample Input and Output

|         Input         |  Output |
|-----------------------|---------|
| square<br>5           | 25      |
| rectangle<br>7<br>2.5 | 17.5    |
| circle<br>6           | 113.097 |
| triangle<br>4.5<br>20 | 45      |

## Testing in the Judge System

Test your solution here: [anchor href=https://judge.softuni.bg/Contests/Practice/Index/506#12]https://judge.softuni.bg/Contests/Practice/Index/506#12[/anchor].
[/slide]

[slide]
# Problem: time plus 15 minutes

Write a program that **inputs hours and minutes** from a 24-hour day and calculates how much it will be **after 15 minutes**. Print the result in **hh: mm** format. Hours are always between 0 and 23, and minutes are always between 0 and 59. Hours are written with one or two digits. Minutes are always written with two digits and zero at the front when needed.

[task]  
    [code-editor language=csharp]
    [/code-editor]
[/task]	

## Sample Input and Output

|   Input  | Output |
|----------|--------|
| 1<br>46  | 2:01   |
| 0<br>01  | 0:16   |
| 23<br>59 | 0:14   |
| 11<br>08 | 11:23  |
| 12<br>49 | 13:04  |

## Hints and Guidelines

Add 15 minutes and write a few conditions. If minutes are over 59, **increase hours** with 1 and **reduce minutes** with 60. Thereby look at the case when hours are over 23. When you print the minutes you should **check for zero at the front**.

## Testing in the Judge System

Test your solution here: [anchor href=https://judge.softuni.bg/Contests/Practice/Index/506#13]https://judge.softuni.bg/Contests/Practice/Index/506#13[/anchor].
[/slide]

[slide]
# Problem: equal numbers

Write a program that inputs **3 numbers** and prints whether they are the same (**yes** / **no**).

[task]  
    [code-editor language=csharp]
    [/code-editor]
[/task]	

## Sample Input and Output

|    Input    | Output |
|-------------|--------|
| 5<br>5<br>5 | yes    |
| 5<br>4<br>5 | no     |
| 1<br>2<br>3 | no     |

## Testing in the Judge System

Test your solution here: [anchor href=https://judge.softuni.bg/Contests/Practice/Index/506#14]https://judge.softuni.bg/Contests/Practice/Index/506#14[/anchor].
[/slide]

[slide]
# Problem: \* number to words

Write a program that converts a number in the range of [**0 ... 100**] into text.

[task]  
    [code-editor language=csharp]
    [/code-editor]
[/task]	

## Sample Input and Output

| Input |    Output   |
|-------|-------------|
| 25    | twenty five |
| 42    | forty two   |
| 6     | six         |

## Hints and Guidelines

First check for **one-digit numbers** and if the number is one-digit, print the appropriate word for it. Then check for **two-digit numbers**. Print them in two parts: left part (**tenth** = number / 10) and right part (**units** = number % 10). If the number has 3 digits, it must be 100 and can be considered as a special case.

## Testing in the Judge System

Test your solution here: [anchor href=https://judge.softuni.bg/Contests/Practice/Index/506#15]           https://judge.softuni.bg/Contests/Practice/Index/506#15[/anchor].
[/slide]