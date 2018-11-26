[slide]
# Problem: Money

Some time ago, **Pesho bought himself bitcoins**. Now, he is going on a tour in Europe and **he needs euro**. Apart from bitcoins, he has **Chinese yuan** as well. Pesho wants to **exchange his money in euro** for the tour. Write a program that calculates **how much euro he can buy, depending on the following exchange rates**:  
- **1 bitcoin = 1168 levs.**
- **1 Chinese yuan = 0.15 dollars.**
- **1 dollar = 1.76 levs.**
- **1 euro = 1.95 levs.**

The exchange office has **commission from 0 to 5 percent from the final sum in euro**.

## Input Data

Three numbers are read from the console:
- On the first line – **number of bitcoins**. Integer in the range of [**0 … 20**].
- On the second line – **number of Chinese yuan**. Floating-point number of [**0.00 … 50 000.00**].
- On the third line – **commission**. Floating-point number of [**0.00 … 5.00**].

## Output Data

Print one number on the console - **the result of the exchange of the currencies**. Rounding is not necessary.

[code-task title="Money" executionStrategy="csharp-dot-net-core-code"]

[code-editor language=csharp]
[/code-editor]

[task-description]
[/task-description]

[code-io /]
[/code-task]

## Sample Input and Output

|   Input   |     Output     |
|-----------|----------------|
|1<br>5<br>5|569.668717948718|

**Explanation**:
- 1 bitcoin = 1168 levs
- 5 Chinese yuan = 0.75 dollars
- 0.75 dollars = 1.32 levs
- **1168 + 1.32 = 1169.32 levs = 599.651282051282 euro**
- **Commission:** 5% от 599.651282051282 = **29.9825641025641**
- **Result**: 599.651282051282 - 29.9825641025641 = **569.668717948718 euro**

|      Input      |     Output     |      Input       |     Output     |
|-----------------|----------------|------------------|----------------|
|20<br>5678<br>2.4|12442.2442010256|7<br>50200.12<br>3|10659.4701177436|

## Hints and Guidelines

Let's first think of the way we can solve the task again, before having started to write code.

### Idea for Solution

We see that the **number of bitcoins** and the **number of Chinese yuans** will be given in the input. The **output** should be in **euro**. The exchange rates that we have to work with, are specified in the task. We notice that we can only exchange the sum in lev to euro, therefore, we **first have to calculate the whole sum that Pesho has in lev**, and **then calculate the output**.

As we have information for the exhange rate of bitcoins to levs, we can directly exchange them. On the other hand, in order to get the value of **Chinese yuans in levs**, first we have to **exchange them in dollars**, and then **the dollars to levs**. Finally, we will **sum the two values** and calculate how much euro that is.

Only the final step is left: **calculating the commission** and subtracting the new sum from the total one. We will receive **an integer** for the commission, which will be a particular **percent from the total sum**. Let' s divide it by 100, so as to calculate its **percentage value** and then multiply it by the sum in euro. We will divide the result from the same sum and print the final sum on the console.

### Choosing Data Types

**Bitcoins** are given as **an integer**, therefore, we can declare a **variable of type `int` for their value. For **Chinese yuan and commission** we receive **a floating-point number**, therefore, we are going to use `double`. As `double` is the data type with bigger scope, and the **output** should also be **a floating-point number**, we will use it for the other variables we create as well.

### Sample Implementation of the Solution

After we have build an idea on how to solve the task and we have chosen the data structures that we are going to use, it is time to get to **writing the code**. As in the previous tasks, we can divide the solution into three smaller tasks:
- **Reading input from the console**.
- **Doing the calculations**.
- **Printing the output** on the console.

**We declare the variables** that we are going to use and again we have to choose **meaningful names**, which are going to give us hints about the values they stpre. We initialize their values: with `Console.ReadLine(…)`, we read the input numbers from the console and convert the entered by the user string to `int` or `double`.

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-2-2-images/04.Money-01.png alt="Code" /]

We do the necessary calculations:

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-2-2-images/04.Money-02.png alt="Code" /]

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-2-2-images/04.Money-03.png alt="Code" /]

Finally, we **calculate the commission value** and **subtract it from the sum in euro**. Let' s pay attention to the way we could write this: `euro -= commission * euro` is the short way to write `euro = euro - (commission * euro)`. In this case, we use **a combined assignment operator** (`-=`) that **subtracts the value of the operand to the right from the one to the left**. The operator for multiplication (`*`) has a **higher priority** than the combined operator, this is why, the expression `commission * euro` is performed first and then its value is divided. (you can read more about operators here [anchor href=http://www.introprogramming.info/intro-csharp-book/read-online/glava3-operatori-i-izrazi/#_Toc298863965]Svetlin Nakov, Veselin Kolev and team: "Programming Basics with C#", page. 150[/anchor])

The task does not specify special string formatting or rounding the result, therefore, we just have to calculate the output and print it on the console.

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-2-2-images/04.Money-04.png alt="Code" /]

Let' s pay attention to something that applies to all other problems of this type: written like that, the solution of the task is pretty detailed. As the task itself is not too complex, in theory, we could write one big expression, where right after having received the input, we calculate the output. For example, such expression would look like this:

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-2-2-images/04.Money-05.png alt="Code" /]

This code would print a correct result, but it is **hard to read**. It won't be easy to find out how it works and whether it contains any mistakes, as well as finding one and correcting it. **Instead of one complex expression, it is better to write a few simpler ones** and store their values in variables with appropriate names. This way, the code is more clean and easily maintainable.  

## Test in the Judge system

Test your solution here: [anchor href=https://judge.softuni.bg/Contests/Practice/Index/505#3]https://judge.softuni.bg/Contests/Practice/Index/505#3[/anchor]
[/slide]
