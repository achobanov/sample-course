[slide]
# Problem: Vegetable Market

[code-task title="Vegetable Market" executionStrategy="csharp-dot-net-core-code"]  

[code-editor language=csharp]
[/code-editor]

[task-description]
A gardener is selling his harvest on the vegetable market. He is selling **vegetables for N levs per kilogram** and **fruits for M levs per kilogram**. Write a program that **calculates the earnings of the harvest in euro** (if **one euro** equals **1.94 lv.**).
[/task-description]

[code-io /]

[/code-task]

## Input Data

**Four numbers** are read from the console, one per line:

- First line - Price per kilogram for vegetables - a floating-point number.
- Second line - Price per kilogram for fruits - a floating-point number.
- Third line - Total kilograms of vegetables - an integer.
- Fourth line - Total kilograms of fruits - an integer.

**Constraints: All numbers will be in the interval between 0.00 and 1000.00**

## Output Data

Print on the console **one floating-point number: the earnings of all fruits and vegetables in euro**.

## Sample Input and Output

|          Input          | Output |
|-------------------------|--------|
|0.194<br>19.4<br>10<br>10|101     |

**Clarification for the first example:**

- Vegetables cost: 0.194 lv. \* 10 kg. = **1.94 lv.**
- Fruits cost: 19.4 lv. \* 10 kg.  = **194 lv.**
- Total: **195.94 lv. = 101 euro**.

|        Input         |    Output      |
|----------------------|----------------|
|1.5<br>2.5<br>10<br>10|20.6185567010309|

## Hints and Guidelines

First, we will give a few ideas and particular hints for solving the problem, followed by the essential part of the code.  

### Idea for Solution

Let' s first go through the problem requirements. In this case, we have to calculate the **total income** from the harvest. It equals **the sum of the earnings from the fruits and the vegetables** which we can calculate by multiplying **the price per kilogram by the quantity**. The input is received in lev and the output should be in euro. It is accepted that 1 euro equals 1.94 lev, therefore, in order to get the wanted **output value, we have to divide the sum by 1.94**.

### Choosing Data Types

After we have a clear idea on how to solve the task, we can continue with choosing appropriate data types. Let' s go through the **input**: we have **two integers** for total kilograms of vegetables and fruits, therefore, the variables we declare to store their values will be of type `int`. The prices of the fruits and vegetables are said to be floating-point numbers, therefore, the variables will be of type `double`.

We can also declare two variables to store the income from the fruits and vegetables separately. As we are multiplying a variable of type `int` (total kilograms) with one of type `double` (price), the result should also be of type `double`. Let' s clarify that: generally, **operators work with arguments of the same type**. Therefore, in order to multiply values from different data types, we have to convert them to the same type. When there are types of different scopes in one expression, the one with the highest scope is the one the other types are converted to, in this case, `double`. As there isn' t danger of data loss, **the conversion is implicit** and is automatically done by the compiler.

The **output** should also be a **floating-point number**, therefore, the result will be stored in a variable of type `double`.

### Solution

It is time to get to the solution. We can divide it into three smaller tasks:  
- **Reading input from the console**.
- **Doing the calculations**.
- **Printing the output on the console**.

In order to read the input, we declare variables, which we have to name carefully, so that they can give us a hint about the values they store. With `Console.ReadLine(…)`, we read values from the console and with the the functions `int.Parse(…)` and `double.Parse(…)`, we convert the particular string value into `int` and `double`.

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-2-2-images/02.Vegetable-market-01.png alt="Code" /]

We do the necessary calculations:  

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-2-2-images/02.Vegetable-market-02.png alt="Code" /]

The task does not specify special output format, therefore, we just have to calculate the wanted value and print it on the console. As in mathematics and so in programming, division has a priority over addition. However, in this task, first we have to **calculate the sum** of the two received values and then **divide by 1.94**. In order to give priority to addition, we can use brackets. With `Console.WriteLine(…)` we print the output on the console.

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-2-2-images/02.Vegetable-market-03.png alt="Code" /]

## Test in the Judge system

Test your solution here: [anchor href=https://judge.softuni.bg/Contests/Practice/Index/505#1]https://judge.softuni.bg/Contests/Practice/Index/505#1[/anchor].
[/slide]
