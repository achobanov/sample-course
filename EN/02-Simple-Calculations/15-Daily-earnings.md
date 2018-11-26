[slide]
# Problem: Daily Earnings

[code-task title="Daily Earnings" executionStrategy="csharp-dot-net-core-code"]

[code-editor language=csharp]
[/code-editor]

[task-description]
Ivan is a programmer in an **American company** and he **works** at home **approximately N days per month** by earning **approximately M dollars per day**. At the end of the year, Ivan **receives a bonus**, which **equals 2.5 of his monthly salaries. 25% of his annual salary goes for taxes**. Write a program that calculates **how much are Ivan' s net average earnings in lev per day**, as he spends them in Bulgaria. It is accepted that **one year has exactly 365 days. The exchange rate of dollar** to lev will be **read from the console**.
[/task-description]

[code-io /]

[/code-task]

## Input Data

**Three numbers** are read from the console.
- On the first line – **work days per month**. An integer in the range of [**5 … 30**].
- On the second line – **daily earnings**. A floating-point number in the range of [**10.00 … 2000.00**].
- On the third line – **exchange rate of dollar to lev** /1 dollar = X lev/. A floating-point number in the range of [**0.99 … 1.99**].

## Output Data

Print **one number** on the console - **the daily earnings in lev**. The result will be **rounded to the second decimal point**.

## Sample Input and Output

|       Input       | Output |
|-------------------|--------|
|21<br>75.00<br>1.59|74.61   |

**Explanation**:
- **One monthly salary** = 21 \* 75 = 1575 dollars.
- **Annual income** = 1575 \* 12 + 1575 \* 2.5 = 22837.5 dollars.
- **Taxes** = 25% of 22837.5 = 5709.375 levs.
- **Net annual income** = 17128.125 dollars = 27233.71875 levs.
- **Average earnings per day** = 27233.71875 / 365 = 74.61 levs.

|      Input      | Output |       Input        | Output |
|-----------------|--------|--------------------|--------|
|15<br>105<br>1.71|80.24   |22<br>199.99<br>1.50|196.63  |

## Hints and Guidelines

Firstly, we have to analyze the task and think of a way to solve it. Then, we will choose data types and, finally, we will write the code.

### Idea for Solution

Let' s first calculate **how much the monthly salary** of Ivan is. We do that by **multiplying the working days per month by his daily earnings**. Firstly, we multiply the number by 12, so as to calculate his salary for 12 months, and then, we multiply it **by 2.5 ** in order to calculate the bonus. After having summed the two values, we calculate his **annual income**. Then, we **divide 25% of it**. We can do that by multiplying the total income by **0.25** and divide the result by it. Depending on the exchange rate, we **exchange the dollars to levs** and after that we **divide the result by 365 (days per year)**.  

### Choosing Data Types

**The working days** per month are given as **an integer**, therefore, we can declare a variable of **type `int` to store their value. For both **the earned money** and **the exchange rate of dollar to lev**, we will receive **a floating-point number**, therefore, we will use `double`. As `double` is the data type with **the higher scope**, and the output should also be **a floating-point number**, we use `double` for the other variables that we create as well.

### Reading the Input Data and Doing the Calculations

Again: after we have an idea on how to solve the problem and we have considered the data types that we are going to use, we can start **writing the program**. As in the previous tasks, we can divide the solution into three smaller tasks:
- **Reading the input from the console**.
- **Doing the calculations**.
- **Printing the output** on the console.

**We declare the variables** that we are going to use by trying to choose **meaningful names**. With `Console.ReadLine(…)` we read the input numbers from the console and we **convert** the input string to `int` or `double` with `int/double.Parse(…)`.

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-2-2-images/05.Daily-earnings-01.png alt="Code" /]

We do the calculations:  

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-2-2-images/05.Daily-earnings-02.png alt="Code" /]

We could write an expression that calculates the annual income without brackets as well. As multiplication is an operation that has a higher priority over addition, it will be performed first. Despite that, **writing brackets is recommended** when using more operators, as this way, the code is **easily readable** and chances of making a mistake are smaller.

### Printing the Result

Finally, we have to print the result on the console. We notice that **the number has to be rounded to the second decimal point**. In order to do that, we can use a **placeholder - a place that will be replaced by a paricular value when printing**. In C#, a digit surrоunded by curly brackets, is used for a **placeholder**. As **in programming counting starts from 0**, the expression `{0}` means that it will be replaced by the first given argument. An integer or a floating-point number we can format by using **F** or **f**. That is followed by a whole positive number, which specifies the number of digits after the point (you can read more about formatting here: [anchor href=http://www.introprogramming.info/intro-csharp-book/read-online/glava4-vhod-i-izhod-ot-konzolata/#_Toc298863992]Svetlin Nakov, Veselin Kolev and team: "Programming Basics with C#", page. 155-158[/anchor]):  

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-2-2-images/05.Daily-earnings-03.png alt="Code" /]

## Test in the Judge system

Test your solution here: [anchor href=https://judge.softuni.bg/Contests/Practice/Index/505#4]https://judge.softuni.bg/Contests/Practice/Index/505#4[/anchor].
[/slide]
