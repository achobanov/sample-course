[slide]
# Exercises: simple calculations

Let us confirm the knowledge gained througout this chapter with a few more exercises.

## Empty (Blank) Visual Studio Solution

We start by creating an empty solution **(Blank Solution)** in Visual Studio. The solutions in Visual Studio combine **a group of projects**. This opportunity is **very convenient**, when we want to **work on a few projects** and switch quickly between them or we want to **unite logically a few interconnected projects**.
In the current practical exercise we will use a **Blank Solution with a couple of projects** to organize the solutions of the tasks from the exercises - every task in a separate project and all of them in a common solution.

- We start Visual Studio
- We create a new **Blank Solution:** [**File**] -> [**New**] -> [**Project**].

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-2-images/00.Blank-solution-01.png alt="Visual Studio" /]

We choose from the dialogue window [**Templates**] -> [**Other Project Types**] -> [**Visual Studio Solutions**] -> [**Blank Solution**] and we give an appropriate name of the project, for example “Simple-Calculations”:

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-2-images/00.Blank-solution-02.png alt="Visual Studio" /]

Now we have created and **emply Visual Studio Solution** (with 0 projects in it):

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-2-images/00.Blank-solution-03.png alt="Visual Studio" /]

The purpose of this blank solution is to add **a project per problem** from the exercises.
[/slide]

[slide]
# Problem: calculating the area of a square

The first exercise from this theme is the following:

[code-task title="Calculating the area of a square" executionStrategy="csharp-dot-net-core-code" requiresInput]

[code-editor language=csharp]
Console.Write("a = ");
var a = int.Parse(Console.ReadLine());
var area = ...
// TODO: Calculate and print the area
[/code-editor]

[task-description]
Write a console program that  **reads a whole number `a` and calculates the area** of a square with side `a`. The task is trivial and easy: **read a number** from the console, **multiply it by itself** and **print the received result** on the console.
[/task-description]

[code-io /]

[/code-task]

## Hints and Guideliness

We create a **new project** in the existing Visual Studio Solution. In the **Solution Explorer** click the right button of the mouse on **Solution 'Simple-Calculations'**. Choose [**Add**] -> [**New Project…**]:

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-2-images/01.Square-area-01.png alt="Visual Studio" /]

**A dialogue window** is going to be opened for a choice of **project type** for creation. We choose **C# console application** with name “Square-Area”:

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-2-images/01.Square-area-02.png alt="Visual Studio" /]

We already have a solution with one console application in it. It is left to write the **code for solving this problem**.  For this purpose we go to the main method's body `Main(string[] args)` and write the following code:

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-2-images/01.Square-area-03.png alt="Code" /]

The code enters a whole number through `a = int.Parse(Console.ReadLine())`, afterwards it calculates  `area = a * a` and finally prints the value of the variable `area`. **We start** the program with [**Ctrl+F5**] and **test** it with different input values:

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-2-images/01.Square-area-04.png alt="Console" /]

## Tetsing in the Judge System

Test your solution here:  [anchor href=https://judge.softuni.bg/Contests/Practice/Index/504#6]https://judge.softuni.bg/Contests/Practice/Index/504#6[/anchor]. You have to receive  100 points (completely correct solution):

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-2-images/01.Square-area-05.png alt="Judge System" /]

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-2-images/01.Square-area-06.png alt="Judge System" /]
[/slide]

[slide]
# Exercies: from inches to centimeters

[code-task  title="From inches to centimeters" executionStrategy="csharp-dot-net-core-code" requiresInput]
[code-editor language=csharp]
Console.Write("Inches = ");
var inches = double.Parse(Console.ReadLine());

// TODO: Calculate and print centimeters
[/code-editor]
[task-description]
Write a program that **reads a number from the console** (it is not mandatory to be a whole number) and converts the number from **inches to centimeters.** For the purpose **it multiplies the inches by  2.54** (because one inch = 2.54 centimeters).
[/task-description]

[code-io /]

[/code-task]

## Hints and Guideliness

First, we create a **new C# console project** in the solution  “Simple-Calculations”. We click the mouse's right button on the solution in the **Solution Explorer** and we choose [**Add**] -> [**New Project…**]:

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-2-images/02.Inches-to-centimeters-01.png alt="New Project" /]

Choose [**Visual C#**] -> [**Windows**] -> [**Console Application**] and name it “Inches-to-Centimeters”:

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-2-images/02.Inches-to-centimeters-02.png alt="New Project" /]

## Writing the program code and starting the program

Next, we have to write the **program code**:

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-2-images/02.Inches-to-centimeters-03.png alt="Code" /]

**Start the program** with [**Ctrl+F5**]:

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-2-images/02.Inches-to-centimeters-04.png alt="Console" /]

Surprise! What is happening? The program doesn't work correctly… Actually, isn't this the previous program?
In Visual Studio **the current active project** in a solution is marked in half black colour and it could be changed:

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-2-images/02.Inches-to-centimeters-05.png alt="Solution Explorer" /]    

## Setting up a startup project

To switch the mode to **automatically go to current project**, we click on the main solution with the mouse's right button and we choose [**Set StartUp Projects…**]:

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-2-images/02.Inches-to-centimeters-06.png alt="Set Startup Project" /]

A dialogue window will open and you will have to choose from it [**Startup Project**] -> [**Current Selection**]:

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-2-images/02.Inches-to-centimeters-07.png alt="Set Startup Project" /]

And again,  **we run the program**, as usual with [**Ctrl+F5**]. This time it will start **the current open program**, which converts inches to centimeters. It looks like it works correctly:

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-2-images/02.Inches-to-centimeters-08.png alt="Console" /]    

## Switching between programs

Now **lets switch on the previous program** (square area). This happens with a double mouse click  on the file ``Program.cs`` from the previous project **“Square-Area”** in the panel [**Solution Explorer**] of Visual Studio:

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-2-images/02.Inches-to-centimeters-12.png alt="Visual Studio" /]

We press again [**Ctrl + F5**]. This time the other project should start:

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-2-images/02.Inches-to-centimeters-11.png alt="Console" /]

We switch back on the **“Inches-to-Centimeters”** project and start it with [**Ctrl+F5**]:

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-2-images/02.Inches-to-centimeters-09.png alt="Console" /]

**Switching between projects** is very easy, isn't it? Just choose the file with the source code of the program, double click it with the mouse and when it starts, the program from the current file is being executed.        

## Testing the program locally

Let us test with floating-point numbers, for example with **2.5**:

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-2-images/02.Inches-to-centimeters-10.png alt="Console" /]

<table><tr><td><img src="https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/alert-icon.png" style="max-width:50px" /></td><td>Depending on the regional settings of the operational system, it is possible instead of using a <b>decimal point </b> (US settings), to be used a <b>decimal comma</b> (BG settings).</td></tr></table>

If the program expects a decimal point and instead a number with a decimal comma is entered or the opposite (to enter a decimal point, when a decimal comma is expected), the following error will be received:

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-2-images/02.Inches-to-centimeters-13.png alt="Console" /]

It is recomended to **change the settings of our computer** to use a **decimal point**:

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-2-images/02.Inches-to-centimeters-14.png alt="Region Settings" /]

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-2-images/02.Inches-to-centimeters-15.png alt="Region Settings" /]

## Testing in the Judge System

Test your solution here: [anchor href=https://judge.softuni.bg/Contests/Practice/Index/504#1]https://judge.softuni.bg/Contests/Practice/Index/504#1[/anchor].

The solution should be received as a completely correct one:

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-2-images/02.Inches-to-centimeters-16.png alt="Judge System" /]
[/slide]

[slide]
# Problem: greeting by name

[code-task title="Greeting by name" executionStrategy="csharp-dot-net-core-code" requiresInput]

[code-editor language=csharp]
[/code-editor]

[task-description]
Write a program that  **reads a person's  name** and prints `Hello, <name>!`, where `<name>` is the name entered earlier.
[/task-description]

[code-io /]

[/code-task]

## Hints and Guideliness

First, we create a **new C# console project** with name “Greeting” in the solution “Simple-Calculations”:

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-2-images/03.Greeting-by-name-01.png alt="Visual Studio" /]

**Next we have to write the code** of the program. If you feel any difficulties, you can use the code from the example below:

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-2-images/03.Greeting-by-name-02.png alt="Visual Studio" /]

**Run** the program with [**Ctrl+F5**] and test if it works:

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-2-images/03.Greeting-by-name-03.png alt="Console" /]


## Testing in the Judge System

Test your solution here: [anchor href=https://judge.softuni.bg/Contests/Practice/Index/504#2]https://judge.softuni.bg/Contests/Practice/Index/504#2[/anchor].

[/slide]

[slide]
# Problem: concatenation of text and numbers

[code-task title="Concatenation of text and numbers" executionStrategy="csharp-dot-net-core-code" requiresInput]

[code-editor language=csharp]
[/code-editor]

[task-description]
Write a C# program, that reads a name, a last name, an age and a city from the console and prints a message of the following kind: `You are <firstName> <lastName>, a <age>-years old person from <town>`.

Message should be in the following format: `You are <firstName> <lastName>, a <age>-years old person from <town>`
[/task-description]

[code-io /]

[/code-task]

## Hints and Guideliness

We add to the exististing Visual Studio solution one more console C# project with name “Concatenate-Data”.	We **write the code** which reads the input from the console:

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-2-images/04.Concatenate-data-01.png alt="Code" /]

**The code** which prints the described in the condition of the problem message should be finished.

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-2-images/04.Concatenate-data-02.png alt="Code" /]

In the picture above the code is blurred on purpose, in order for you to think of a way to finish it yourself.

Next, the solution should be tested locally with [**Ctrl+F5**] and by entering an exemplary input data.

## Testing in the Judge System

Test your solution here: [anchor href=https://judge.softuni.bg/Contests/Practice/Index/504#3]https://judge.softuni.bg/Contests/Practice/Index/504#3[/anchor].
[/slide]

[slide]
# Problem: trapezoid area

Write a program that reads three numbers from the console **b1, b2 and h and calculates the area of a trapezoid** with bases **b1 and b2 and height h. The formula for trapezoid area is  (b1 + b2) * h / 2**.

In the figure bellow is shown a trapezoid with bases 8 and 13 and height 7. It has an area **(8 + 13) * 7 / 2 = 73.5**.

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-2-images/05.Trapezoid-area-01.png alt="Trapezoid" /]

[code-task title="Trapezoid area" executionStrategy="csharp-dot-net-core-code" requiresInput]

[code-editor language=csharp]
var b1 = double.Parse(Console.ReadLine());
// TODO: Calculate and print the area
[/code-editor]

[task-description]
Multiplication in programming is performed by `*` operator.
[/task-description]

[code-io /]

[/code-task]

## Hints and Guideliness

Again, we have to add to the existing Visual Studio solution another **console C# project** with name "Trapezoid-Area" and write the **code that reads the input from the console, calculates the trapezoid area and prints it**:
[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-2-images/05.Trapezoid-area-02.png alt="Code" /])

The code in the picture is purposely blurred, in order for you to give it a thought and finish it yourself.

**Test** your solution locally with [**Ctrl+F5**] and enter an examplary data.

## Testing in the Judge System

Test your solution here: [anchor href=https://judge.softuni.bg/Contests/Practice/Index/504#4]https://judge.softuni.bg/Contests/Practice/Index/504#4[/anchor].

[/slide]

[slide]
# Problem: circle area and perimeter

Write a program that reads from the console a **number r** and calculates and prints **the circle's area and perimeter** with **radius r**.

[code-task title="Print out Hello World" executionStrategy="csharp-dot-net-core-code" requiresInput]
[code-editor language=csharp]
[/code-editor]

[task-description]
        For the calculations you may use the following formulas:
        -	`Area = Math.PI * r * r`.
        -	`Perimeter = 2 * Math.PI * r`.
[/task-description]

[code-io /]

[/code-task]

## Input and output

| Input |                       Output                             |    
|-------|----------------------------------------------------------|
| 3     | Area = 28.2743338823081 <br> Perimeter = 18.8495559215388|
| 4.5   | Area = 63.6172512351933 <br> Perimeter = 28.2743338823081|

## Testing in the Judge System

Test your solution here: [anchor href=https://judge.softuni.bg/Contests/Practice/Index/504#5]https://judge.softuni.bg/Contests/Practice/Index/504#5[/anchor].
[/slide]

[slide]
# Problem: rectangle area in a coordinate plane

**A Rectangle** is given with the **coordinates** of both of its opposite angles (x1, y1) – (x2, y2). Calculate its  **area and perimeter**. **The input** is read from the console. The numbers **x1, y1, x2 and y2** are given one per line. **The output** is printed on the console and it has to contain two lines, each with one number - the area and the perimeter.

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-2-images/07.Rectangle-area-01.png alt="Rectangle Figure" /]

[code-task title="Rectangle area in a coordinate plane" executionStrategy="csharp-dot-net-core-code" requiresInput]

[code-editor language=csharp]
[/code-editor]

[task-description]
**The output** is printed on the console and it has to contain two lines, each with one number - the area and the perimeter.
[/task-description]

[code-io /]

[/code-task]

## Sample Input and Output

|               Input                   |       Output       |
|---------------------------------------|--------------------|
|60<br>20<br>10<br>50                   |1500<br>160         |
|30<br>40<br>70<br>-10                  |2000<br>180         |
|600.25<br>500.75<br>100.50<br>-200.5   |350449.6875<br>2402 |

## Testing in the Judge System

Test your solution here: [anchor href=https://judge.softuni.bg/Contests/Practice/Index/504#6]https://judge.softuni.bg/Contests/Practice/Index/504#6
[/anchor].
[/slide]

[slide]
# Problem: triangle area

[code-task title="Triangle area" executionStrategy="csharp-dot-net-core-code" requiresInput]
[code-editor language=csharp]
[/code-editor]

[task-description]
Write a program that reads from the console **a side and a height of a triangle** and calculates its area. Use the **formula** for triangle area: **area = a * h / 2**. Round the result to **2 digits after the decimal separator using `Math.Round(area, 2)**.

Use the **formula** for triangle area: **area = a * h / 2**.
[/task-description]

[code-io /]

[/code-task]

## Sample Input and Output

|       Input          |         Output        |
|----------------------|-----------------------|
| 20 <br>30            | Triangle area = 300   |
| 15 <br>35            | Triangle area = 262.5 |
| 7.75 <br>8.45        | Triangle area = 32.74 |
| 1.23456 <br>4.56789  | Triangle area = 2.82  |

## Testing in the Judge System

Test your solution here: [anchor href=https://judge.softuni.bg/Contests/Practice/Index/504#7]https://judge.softuni.bg/Contests/Practice/Index/504#7[/anchor].
[/slide]

[slide]
# Problem: console converter - from degrees on °C to degrees on °F

[code-task title="Console converter - from degrees on °C to degrees on °F" executionStrategy="csharp-dot-net-core-code" requiresInput]

[code-editor language=csharp]
[/code-editor]

[task-description]
Write a program that reads **degrees on Celsius scale** (°C) and converts them to **degrees on Fahrenheit** (°F). Look on the Internet for a proper [anchor href=http://bfy.tw/3rGh]formula[/anchor] to do the calculations. Round the result to **2 digits after the decimal separator**. Below are a few examples.

Use the **formula** °F = °C × 1,8 + 32
[/task-description]

[code-io /]

[/code-task]

## Sample Input and Output

| Input | Output |
|-------|--------|
|  25   |   77   |
|   0   |   32   |
| -5.5  |  22.1  |
| 32.3  | 90.14  |

## Testing in the Judge System

Test your solution here: [anchor href=https://judge.softuni.bg/Contests/Practice/Index/504#8]https://judge.softuni.bg/Contests/Practice/Index/504#8[/anchor].
[/slide]

[slide]
# Problem: console converter - from radians to degrees

[code-task title="Console converter - from radians to degrees" executionStrategy="csharp-dot-net-core-code" requiresInput]

[code-editor language=csharp]
[/code-editor]

[task-description]

Write a program, that reads **an angle in [anchor href=https://en.wikipedia.org/wiki/Radian]radians[/anchor]** (`rad`) and converts it to **[anchor href=https://en.wikipedia.org/wiki/Degree_(angle)]degrees[/anchor]** (`deg`). Look for a proper formula on the Internet. The number **π** in C# programs is available through `Math.PI`. Round the result to the nearest whole number using the `Math.Round(…)` method.

The number **π** in C# programs is available through `Math.PI`.
[/task-description]

[code-io /]

[/code-task]

## Sample Input and Output

|  Input | Output |
|--------|--------|
| 3.1416 |  180   |       
| 6.2832 |  360   |
| 0.7854 |   45   |
| 0.5236 |   30   |

## Testing in the Judge System

Test your solution here: [anchor href=https://judge.softuni.bg/Contests/Practice/Index/504#9]https://judge.softuni.bg/Contests/Practice/Index/504#9[/anchor].
[/slide]

[slide]
# Problem: console converter - USD to BGN

[code-task title="Converter - USD to BGN" executionStrategy="csharp-dot-net-core-code" requiresInput]

[code-editor language=csharp]
[/code-editor]

[task-description]
Write a program for **conversion of US dollars** (USD) **in bulgarian levs** (BGN). **Round** the result to **2 digits** after the decimal separator. Use a fixed rate between a dollar and a lev: **1 USD = 1.79549 BGN**.

**1 USD = 1.79549 BGN**
[/task-description]

[code-io /]

[/code-task]

## Sample Input and Output

| Input |   Output  |
|-------|-----------|
|  20   | 35.91 BGN |      
|  100  | 179.55 BGN|
|  12.5 | 22.44 BGN |

## Testing in the Judge System

Test your solution here: [anchor href=https://judge.softuni.bg/Contests/Practice/Index/504#10]https://judge.softuni.bg/Contests/Practice/Index/504#10[/anchor].
[/slide]

[slide]
# Problem: \* console currency converter

[code-task title="Currency converter" executionStrategy="csharp-dot-net-core-code" requiresInput]

[code-editor language=csharp]
[/code-editor]

[task-description]
Write a program for **conversion of money from one currency to another**. It has to maintain the following currencies: **BGN, USD, EUR, GBP**. Use the following fixed currency rates:

|  Курс  |   USD   |   EUR   |   GBP   |
|:------:|:-------:|:-------:|:-------:|
| 1 BGN  | 1.79549 | 1.95583 | 2.53405 |

**The input** is **sum for conversion**, **input currency** and **output currency**. **The output** is one number – the converted value of the above currency rates, rounded **2 digits** after the decimal point.
[/task-description]

[code-io /]

[/code-task]

## Sample Input and Output

|        Input       |  Output  |
|--------------------|----------|
|   20<br>USD<br>BGN |35.91 BGN |     
|  100<br>BGN<br>EUR |51.13 EUR |
| 12.35<br>EUR<br>GBP|9.53 GBP |  
|150.35<br>USD<br>EUR|138.02 EUR|

## Testing in the Judge System

Test your solution here: [anchor href=https://judge.softuni.bg/Contests/Practice/Index/504#11]https://judge.softuni.bg/Contests/Practice/Index/504#11[/anchor].
[/slide]

[slide]
# Problem: ** calcutations with dates - 1000 days on Earth

[code-task title="Calculations with dates" executionStrategy="csharp-dot-net-core-code" requiresInput]

[code-editor language=csharp]
[/code-editor]

[task-description]
Write a program that enters Напишете програма, която въвежда **a birthdate** in format `dd-MM-yyyy` and calculates the date on which are turned и пресмята датата, на която се навършват **1000 days** from this birthdate and prints it in the same format.
[/task-description]

[code-io /]

[/code-task]

## Sample Input and Output

|   Input  |  Output  |
|----------|----------|
|25-02-1995|20-11-1997|
|07-11-2003|02-08-2006|
|30-12-2002|24-09-2005|
|01-01-2012|26-09-2014|
|14-06-1980|10-03-1983|

## Hints and Guidelines

- Look for information about the data type `DateTime` in C# and in particular look at the methods `.ParseExact(str, format)`, `.AddDays(count)` and `.ToString(format)`. With their help you can solve the problem without the need to calculate days, months and leap years.
- **Don't print** anything additional on the console except for the wanted data!

## Testing in the Judge System

Test your solution here: [anchor href=https://judge.softuni.bg/Contests/Practice/Index/504#12]https://judge.softuni.bg/Contests/Practice/Index/504#12[/anchor].
[/slide]
