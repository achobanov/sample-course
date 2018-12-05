[slide]
# Chapter 6.1. Nested Loops

In the current chapter we will be looking at **nested loops** and how to use `for` loops to **draw** different **figures on the console**, which contain symbols and signs, ordered in rows and columns in the console. We will use **single** and **nested loops** (loops, which are in other loops), **calculations** and **checks**, in order to print on the console simple and not so simple figures by previously given sizes.


## Video

[youtube-video videoId=x7zXRCpkebo /]
[/slide]

[slide]
# Example: Rectangle of 10 x 10 Stars

[code-task title="Rectangle of 10 x 10 Stars" executionStrategy="csharp-dot-net-core-code"]

[code-editor language=csharp]
[/code-editor]

[task-description]
Print in the console a rectangle of **10 x 10** stars.
[/task-description]

[code-io /]
[/code-task]

### Input
(none)

### Output

\*\*\*\*\*\*\*\*\*\*  
\*\*\*\*\*\*\*\*\*\*  
\*\*\*\*\*\*\*\*\*\*  
\*\*\*\*\*\*\*\*\*\*  
\*\*\*\*\*\*\*\*\*\*  
\*\*\*\*\*\*\*\*\*\*  
\*\*\*\*\*\*\*\*\*\*  
\*\*\*\*\*\*\*\*\*\*  
\*\*\*\*\*\*\*\*\*\*  
\*\*\*\*\*\*\*\*\*\*  

|  Input |   Output   |
|--------|------------|
| (none) |<code>\*\*\*\*\*\*\*\*\*\*</code><br><code>\*\*\*\*\*\*\*\*\*\*</code><br><code>\*\*\*\*\*\*\*\*\*\*</code><br><code>\*\*\*\*\*\*\*\*\*\*</code><br><code>\*\*\*\*\*\*\*\*\*\*</code><br><code>\*\*\*\*\*\*\*\*\*\*</code><br><code>\*\*\*\*\*\*\*\*\*\*</code><br><code>\*\*\*\*\*\*\*\*\*\*</code><br><code>\*\*\*\*\*\*\*\*\*\*</code><br><code>\*\*\*\*\*\*\*\*\*\*</code>|

## Hints and Guidelines

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-6-images/01.Rectangle-of-10-x-10-stars-01.png alt="Code" /]

How does the example work? We initialize **a loop with a variable `i = 1`, which increases with each iteration of the loop, while it is **less or equal to 10**. This way the code in the body of the loop is executed **10 times**. In the body of the loop we print a new line in the console `new string('*', 10)`, which creates a string of 10 stars.

## Testing in the Judge System

Test your solution here: [anchor href=https://judge.softuni.bg/Contests/Practice/Index/512#0]https://judge.softuni.bg/Contests/Practice/Index/512#0[/anchor].
[/slide]

[slide]
# Example: Rectangle of N x N Stars

[code-task title="Rectangle of N x N Stars" executionStrategy="csharp-dot-net-core-code" requiresInput]

[code-editor language=csharp]
[/code-editor]

[task-description]
Write a program, which gets a positive integer **n** and prints in the console **a rectangle of N x N stars**.
[/task-description]

[code-io /]
[/code-task]

## Input
2

## Output
**
**

## Input
3

## Output
***
***
***

## Input
4

## Output
****
****
****
****

|Input|                Output                |Input|                              Output                             |Input|Output|
|-----|--------------------------------------|-----|-----------------------------------------------------------------|-----|------|
|  2  |<code>\*\*</code><br><code>\*\*</code>|  3  |<code>\*\*\*</code><br><code>\*\*\*</code><br><code>\*\*\*</code>|  4  |<code>\*\*\*\*</code><br><code>\*\*\*\*</code><br><code>\*\*\*\*</code><br><code>\*\*\*\*</code>|

## Hints and Guidelines

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-6-images/02.Rectangle-of-N-x-N-stars-01.png alt="Code" /]

## Testing in the Judge System

Test your solution here: [anchor href=https://judge.softuni.bg/Contests/Practice/Index/512#1]https://judge.softuni.bg/Contests/Practice/Index/512#1[/anchor].
[/slide]

[slide]
# Nested Loops

Nested loops are a construction where **in the body of one loop** (outer) **another loop is run** (inner). For each iteration of the outer loop, **the whole** of the inner loop is executed. This happens in the following way:

- When nested loops start executing **the outer loop starts** first: the controlling variable is **initialized** and after a check for ending the loop the code in its body is executed.
- After this **the inner loop is executed**. The controlling variables start position is initialized, a check for ending the loop is made and the code in its body is executed.
- When reaching the set value for  **ending the loop**, the program goes back one step up and continues executing the previous (outer) loop. The controlling variable of the outer loop changes with one step, a check is made to see if the condition for ending the loop is met and **a new execution of the nested (inner) loop is started**.
- This is repeated until the variable of the outer loop meets the condition to **end the loop**.
[/slide]

[slide]
# Example: Square of Stars

[code-task title="Square of Stars" executionStrategy="csharp-dot-net-core-code" requiresInput]

[code-editor language=csharp]
[/code-editor]

[task-description]
Print in the console a square of **N x N** stars:
[/task-description]

[code-io /]
[/code-task]

|Input|                 Output                 |Input|                                 Output                                |Input|Output|
|-----|----------------------------------------|-----|-----------------------------------------------------------------------|-----|------|
|  2  |<code>\* \*</code><br><code>\* \*</code>|  3  |<code>\* \* \*</code><br><code>\* \* \*</code><br><code>\* \* \*</code>|  4  |<code>\* \* \* \*</code><br><code>\* \* \* \*</code><br><code>\* \* \* \*</code><br><code>\* \* \* \*</code>|

## Hints and Guidelines

The problem is similar to the last one. The difference here is that we need to figure out how to add a white space after the stars so that there aren't any excess white spaces in the beginning or the end.

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-6-images/03.Square-01.png alt="Code" /]

## Testing in the Judge System

Test your solution here: [anchor href=https://judge.softuni.bg/Contests/Practice/Index/512#2]https://judge.softuni.bg/Contests/Practice/Index/512#2[/anchor].
[/slide]

[slide]
# Example: A Triangle of Dollars

[code-task title="Triangle of Dollars" executionStrategy="csharp-dot-net-core-code" requiresInput]

[code-editor language=csharp]
[/code-editor]

[task-description]
Write a program , which takes the number **n** and prints **a triangle of dollars**.
[/task-description]

[code-io /]
[/code-task]


|Input|                         Output                         |Input|Output|Input|Output|
|-----|--------------------------------------------------------|-----|------|-----|------|
|  3  |<code>$</code><br><code>$ $</code><br><code>$ $ $</code>|  4  |<code>$</code><br><code>$ $</code><br><code>$ $ $</code><br><code>$ $ $ $</code>|  5  |<code>$</code><br><code>$ $</code><br><code>$ $ $</code><br><code>$ $ $ $</code><br><code>$ $ $ $ $</code>|

## Hints and Guidelines

The problem is **similar** to the draw **a rectangle** and **square** ones. We will use **nested loops** again, but there is **a  catch** here. The difference is that **the number of columns** which we need to print depends on **the row**, on which we are and not on the input number `n`. From the example input and output data we see that **the count of the dollars depends** on which **row** we are on at the moment of the printing, i.e. 1 dollar means first row, 3 dollars mean third row and so on. Let's see the following example in detail. We see that **the variable** of **the nested** loop is connected with the variable of **the outer**. This way our program prints the triangle.

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-6-images/04.Triangle-of-dollars-01.png alt="Code" /]

## Testing in the Judge System

Test your solution here: [anchor href=https://judge.softuni.bg/Contests/Practice/Index/512#3]https://judge.softuni.bg/Contests/Practice/Index/512#3[/anchor].
[/slide]

[slide]
# Example: A Square Frame

[code-task title="Square Frame" executionStrategy="csharp-dot-net-core-code" requiresInput]

[code-editor language=csharp]
[/code-editor]

[task-description]
Write a program, which takes a positive integer **n** and draws on the console **a square frame** with a size of **n \* n**.
[/task-description]

[code-io /]
[/code-task]
 
|Input|                                  Output                                |Input|    Output    |
|-----|------------------------------------------------------------------------|-----|--------------|
|  3  |<code>+ - +</code><br><code>&#124; - &#124;</code><br><code>+ - +</code>|  4  |<code>+ - - +</code><br><code>&#124; - - &#124;</code><br><code>&#124; - - &#124;</code><br><code>+ - - +</code>|

|Input|          Output       |Input|          Output       |
|-----|-----------------------|-----|-----------------------|
|  5  |<code>+ - - - +</code><br><code>&#124; - - - &#124;</code><br><code>&#124; - - - &#124;</code><br><code>&#124; - - - &#124;</code><br><code>+ - - - +</code>|6|<code>+ - - - - +</code><br><code>&#124; - - - - &#124;</code><br><code>&#124; - - - - &#124;</code><br><code>&#124; - - - - &#124;</code><br><code>&#124; - - - - &#124;</code><br><code>+ - - - - +</code>|

## Hints and Guidelines

We can solve the problem in the following way:
- We read from the console the number `n`.
- We print **the upper part**: first a `+` sign, then **n-2** times `-` and in the end a  `+` sign.
- We print **the middle part**: we print **n-2** rows, as we first print a  `|` sign, then **n-2** times `-` and in the end again a `|` sign. We can do this with nested loops.
- We print **the lower part**: first a `+` sign, then **n-2** times `-` and in the end a  `+` sign.

Here is an example implementation of the above idea with nested loops:

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-6-images/05.Square-frame-01.png alt="Code" /]

## Testing in the Judge System

Test your solution here: [anchor href=https://judge.softuni.bg/Contests/Practice/Index/512#4]https://judge.softuni.bg/Contests/Practice/Index/512#4[/anchor].
[/slide]

[slide]
# Example: Rhombus of Stars

[code-task title="Rhombus of Stars" executionStrategy="csharp-dot-net-core-code" requiresInput]

[code-editor language=csharp]
[/code-editor]

[task-description]
Write a program, which takes a positive integer **n** and prints **a rhombus of stars** with size **n**.
[/task-description]

[code-io /]
[/code-task]


|Input|     Output    |Input|                                         Output                                          |
|-----|---------------|-----|-----------------------------------------------------------------------------------------|
|  1  |<code>\*</code>|  2  |<code>&nbsp;\*&nbsp;</code><br><code>\*&nbsp;\*</code><br><code>&nbsp;\*&nbsp;</code><br>|


|Input|Output|Input|Output|
|-----|------|-----|------|
|  3  |<code>&nbsp;&nbsp;\*&nbsp;&nbsp;</code><br><code>&nbsp;\*&nbsp;\*&nbsp;</code><br><code>\*&nbsp;\*&nbsp;\*</code><br><code>&nbsp;\*&nbsp;\*&nbsp;</code><br><code>&nbsp;&nbsp;\*&nbsp;&nbsp;</code>|  4  |<code>&nbsp;&nbsp;&nbsp;\*&nbsp;&nbsp;&nbsp;</code><br><code>&nbsp;&nbsp;\*&nbsp;\*&nbsp;&nbsp;</code><br><code>&nbsp;\*&nbsp;\*&nbsp;\*&nbsp;</code><br><code>\*&nbsp;\*&nbsp;\*&nbsp;\*</code><br><code>&nbsp;\*&nbsp;\*&nbsp;\*&nbsp;</code><br><code>&nbsp;&nbsp;\*&nbsp;\*&nbsp;&nbsp;</code><br><code>&nbsp;&nbsp;&nbsp;\*&nbsp;&nbsp;&nbsp;</code>|

## Hints and Guidelines

To solve this problem we need to mentally **divide** **the rhombus** into **two parts** - **upper**, which **also**includes the middle row, and **lower**. For **the printing** of each part we will use **two** separate loops, as we leave the reader to decide the dependency between `n` and the variables of the loops. For the first loop we can use the following tips:

- We print `n-row` white spaces.
- We print `*`.
- We print `row-1` times `*`.

**The second** (lower) part will be printed **similarly**, which again we leave to the reader to do.

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-6-images/06.Rhombus-of-stars-01.png alt="Code" /]

## Testing in the Judge System

Test your solution here: [anchor href=https://judge.softuni.bg/Contests/Practice/Index/512#5]https://judge.softuni.bg/Contests/Practice/Index/512#5[/anchor].
[/slide]

[slide]
# Example: Christmas Tree

[code-task title="Christmas Tree" executionStrategy="csharp-dot-net-core-code" requiresInput]

[code-editor language=csharp]
[/code-editor]

[task-description]
Write a program, which takes a number **n** (1 ≤ n ≤ 100) and prints a Christmas tree with height **n+1**.
[/task-description]

[code-io /]
[/code-task]

|Input|                                        Output                                    |Input|     Output     |
|-----|----------------------------------------------------------------------------------|-----|----------------|
|  1  |<code>&nbsp;&nbsp;&#124;&nbsp;&nbsp;</code><br><code>\*&nbsp;&#124;&nbsp;\*</code>|  2  |<code>&nbsp;&nbsp;&nbsp;&#124;&nbsp;&nbsp;&nbsp;</code><br><code>&nbsp;\*&nbsp;&#124;&nbsp;\*&nbsp;</code><br><code>\*\*&nbsp;&#124;&nbsp;\*\*</code>|

|Input|  Output  |Input|  Output  |
|-----|----------|-----|----------|
|  3  |<code>&nbsp;&nbsp;&nbsp;&nbsp;&#124;&nbsp;&nbsp;&nbsp;&nbsp;</code><br><code>&nbsp;&nbsp;\*&nbsp;&#124;&nbsp;\*&nbsp;&nbsp;</code><br><code>&nbsp;\*\*&nbsp;&#124;&nbsp;\*\*&nbsp;</code><br><code>\*\*\*&nbsp;&#124;&nbsp;\*\*\*</code>|  4  |<code>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&#124;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</code><br><code>&nbsp;&nbsp;&nbsp;\*&nbsp;&#124;&nbsp;\*&nbsp;&nbsp;&nbsp;</code><br><code>&nbsp;&nbsp;\*\*&nbsp;&#124;&nbsp;\*\*&nbsp;&nbsp;</code><br><code>&nbsp;\*\*\*&nbsp;&#124;&nbsp;\*\*\*&nbsp;</code><br><code>\*\*\*\*&nbsp;&#124;&nbsp;\*\*\*\*</code>|

## Hints and Guidelines

From the examples we see that **the Christmas tree** can be **divided** into **three** logical parts. **The first** part is **the stars and the white spaces before and after them**, **the middle** part is ` | `, and **the last** part is again **stars**, but this time there are **white spaces** only **before** them. The printing can be done with only **one loop** and the constructor `new string(…)`, which we will use once for the stars and once for the white spaces. 

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-6-images/07.Christmas-tree-01.png alt="Code" /]

## Testing in the Judge System

Test your solution here: [anchor href=https://judge.softuni.bg/Contests/Practice/Index/512#6]https://judge.softuni.bg/Contests/Practice/Index/512#6[/anchor].
[/slide]

[slide]
# Drawing More Complex Figures

Let's look at how to draw figures with more complex logic of construction in the console, for which we need to start thinking more before starting to write.

## Example: Sunglasses

[code-task title="Sunglasses" executionStrategy="csharp-dot-net-core-code" requiresInput]

[code-editor language=csharp]
[/code-editor]

[task-description]
Write a program, which takes an integer **n** (3 ≤ n ≤ 100) and prints sunglasses with size of **5\*n x n** as found in the examples below.
[/task-description]

[code-io /]
[/code-task]

|Input|      Output     |Input|      Output     |
|-----|-----------------|-----|-----------------|
|  3  |<code>\*\*\*\*\*\*&nbsp;&nbsp;&nbsp;\*\*\*\*\*\*</code><br><code>\*////\*&#124;&#124;&#124;\*////\*</code><br><code>\*\*\*\*\*\*&nbsp;&nbsp;&nbsp;\*\*\*\*\*\*</code>|  4  |<code>\*\*\*\*\*\*\*\*&nbsp;&nbsp;&nbsp;&nbsp;\*\*\*\*\*\*\*\*</code><br><code>\*//////\*&#124;&#124;&#124;&#124;\*//////\*</code><br><code>\*//////\*&nbsp;&nbsp;&nbsp;&nbsp;\*//////\*</code><br><code>\*\*\*\*\*\*\*\*&nbsp;&nbsp;&nbsp;&nbsp;\*\*\*\*\*\*\*\*</code><br>|

|Input|     Output     |
|-----|----------------|
|  5  |<code>\*\*\*\*\*\*\*\*\*\*&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;\*\*\*\*\*\*\*\*\*\*</code><br><code>\*////////\*&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;\*////////\*</code><br><code>\*////////\*&#124;&#124;&#124;&#124;&#124;\*////////\*</code><br><code>\*////////\*&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;\*////////\*</code><br><code>\*\*\*\*\*\*\*\*\*\*&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;\*\*\*\*\*\*\*\*\*\*</code><br>|

### Printing the Top and Bottom Rows

From the examples we can see that the sunglasses can be divided into  **three parts** – upper, middle and lower. A part of the code with which the problem can be solved is given below.

When drawing the upper and lower rows we need to print `2 * n` stars, `n` white spaces and `2 * n` stars.

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-6-images/08.Sunglasses-01.png alt="Code" /]

### Printing the Middle Rows

When drawing **the middle** part we need to **check** if the row is `(n-1) / 2 - 1`, because in the examples we can see that in **this row** we need to print **pipes** instead of white spaces.

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-6-images/08.Sunglasses-02.png alt="Code" /]

### Testing in the Judge System

Test your solution here: [anchor href=https://judge.softuni.bg/Contests/Practice/Index/512#7]https://judge.softuni.bg/Contests/Practice/Index/512#7[/anchor].
[/slide]

[slide]
# Example: House

[code-task title="House" executionStrategy="csharp-dot-net-core-code" requiresInput]

[code-editor language=csharp]
[/code-editor]

[task-description]
Write a program, which takes a number **n** (2 ≤ **n** ≤ 100) and prints **a house** with size **n x n**, just as in the examples below.
[/task-description]

[code-io /]
[/code-task]

|Input|                     Output                     |Input|                                Output                                 |Input| Output |
|-----|------------------------------------------------|-----|-----------------------------------------------------------------------|-----|--------|
|  2  |<code>**</code><br><code>&#124;&#124;</code><br>|  3  |<code>-\*-</code><br><code>\*\*\*</code><br><code>&#124;\*&#124;</code>|  4  |<code>-\*\*-</code><br><code>\*\*\*\*</code><br><code>&#124;\*\*&#124;</code><br><code>&#124;\*\*&#124;</code>

|Input|  Output  |Input|  Output  |
|-----|----------|-----|----------|
|  5  |<code>--\*--</code><br><code>-\*\*\*-</code><br><code>\*\*\*\*\*</code><br><code>&#124;\*\*\*&#124;</code><br><code>&#124;\*\*\*&#124;</code>|  8  |<code>---\*\*---</code><br><code>--\*\*\*\*--</code><br><code>-\*\*\*\*\*\*-</code><br><code>\*\*\*\*\*\*\*\*</code><br><code>&#124;\*\*\*\*\*\*&#124;</code><br><code>&#124;\*\*\*\*\*\*&#124;</code><br><code>&#124;\*\*\*\*\*\*&#124;</code><br><code>&#124;\*\*\*\*\*\*&#124;</code><br>|

## Hints and Guidelines

We take from the problem explanation that the house is with size of `n` x `n`. What we see from the example input and output is that:

- The house is divided into two parts: **roof and base**. 

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-6-images/09.House-01.png alt="House" /]

- When `n` is an even number, the point of the house is "dull".
- When `n` is odd, **the roof** is one row larger than the **base**.

### Roof

- It is comprised of **stars** and **dashes**.
- In the top part there are one or two stars, depending on if **n** is even or odd (also related to the dashes).
- In the lowest part there are many stars and no dashes.
- With each lower row, **the stars** increase by 2 and **the dashes** decrease by 2.

### Base

- The height is `n` rows.
- It is made out of **stars** and **pipes**.
- Each row is comprised of 2 **pipes** - one in the beginning and one in the end of the row, and also **stars** between the pipes with string length of `n - 2`.  

### Reading the Input Data

We take `n` from the console and we save it in a variable of type `int`.  

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-6-images/09.House-02.png alt="Code" /]

**It is very important to check if the input data is correct!** In these problems it is not a problem to directly convert the data from the console into `int`, because it is said that we will receive valid integers. If you are making more complex programs it is a good practice to check the data. What will happen if istead of the character "А" the user inputs a number?

### Calculating the Length of the Roof

In order to draw **the roof**, we write down how many **stars** we start with in a variable called `stars`:

- If `n` i **an even** number, there will be 2 stars.
- If it is **odd**, there will be 1.

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-6-images/09.House-03.png alt="Code" /]

Calculate the length of **the roof**. It equals half of `n`. Write the result in the variable  `roofLength`.

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-6-images/09.House-04.png alt="Code" /]

It is important to note that when `n` is an odd number, the length of the roof is one row more than that of the **base**. In **C#** when you divide two numbers with a remainder, the result will be the number without remainder.

Example:

```csharp
int result = 3 / 2; // 1
```

If we want to round up, we need to use the method `Math.Ceiling(…)`: `int result = (int)Math.Ceiling(3 / 2f);`. In this example the division isn't between two integers. "`f`" after a number shows that this number is of type `float` (a floating point number). The result of `3 / 2f` is `1.5f`. `Math.Ceiling(…)` rounds the division up. In this case `1.5f` will become 2. `(int)` is used so that we can transfer the type back to `int`.

### Printing the Roof

After we have calculated the length of the roof we make a loop from 0 to `roofLength`. On each iteration we will:

- Calculate the number of **dashes** we need to draw. The number will be equal to `(n - stars) / 2`. We write it down in a variable `padding`.

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-6-images/09.House-05.png alt="Code" /]

- We print in the console: "**dashes**" (`padding / 2` times) + "**stars**" (`stars` times) + "**dashes**" (`padding / 2` times). 

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-6-images/09.House-06.png alt="Code" /]

- Before the iteration is over we add 2 to `stars` (the number of **the stars**).

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-6-images/09.House-07.png alt="Code" /]

It is not a good idea to add many character strings as it is shown above because this leads to <strong>performance issues</strong>. For more information visit: [anchor href=https://bg.wikipedia.org/wiki/%D0%9D%D0%B8%D0%B7#String_Builder]https://bg.wikipedia.org/wiki/%D0%9D%D0%B8%D0%B7#String_Builder[/anchor].

### Printing the Base

After we have finished with the **roof**, it is time for **the base**. It is easier to print:

- We start with a loop from 0 to n (not inclusive).
- We print in the console: `|` + `*` (`n - 2` times) + `|`.

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-6-images/09.House-08.png alt="Code" /]

If you have written everything as it is here the problem should be solved.

## Testing in the Judge System

Test your solution here: [anchor href=https://judge.softuni.bg/Contests/Practice/Index/512#8]https://judge.softuni.bg/Contests/Practice/Index/512#8[/anchor].
[/slide]

[slide]
# Example: Diamond

[code-task title="Diamond" executionStrategy="csharp-dot-net-core-code" requiresInput]

[code-editor language=csharp]
[/code-editor]

[task-description]
Write a program, which takes an integer **n** (1 ≤ **n** ≤ 100) and prints a diamond with size **n**, as in the examples below.
[/task-description]

[code-io /]
[/code-task]

|Input|Output|Input|Output|Input|Output|
|---|---|---|---|---|---|
|1|<code>\*</code><br>|2|<code>\*\*</code>|3|<code>-\*-</code><br><code>\*-\*</code><br><code>-\*-</code>|

|Input|Output|Input|Output|Input|Output|
|---|---|---|---|---|---|
|4|<code>-\*\*-</code><br><code>\*--\*</code><br><code>-\*\*-</code>|5|<code>--\*--</code><br><code>-\*-\*-</code><br><code>\*---\*</code><br><code>-\*-\*-</code><br><code>--\*--</code><br>|6|<code>--\*\*--</code><br><code>-\*--\*-</code><br><code>\*----\*</code><br><code>-\*--\*-</code><br><code>--\*\*--</code><br>|

|Input|Output|Input|Output|Input|Output|
|---|---|---|---|---|---|
|7|<code>---\*---</code><br><code>--\*-\*--</code><br><code>-\*---\*-</code><br><code>\*-----\*</code><br><code>-\*---\*-</code><br><code>--\*-\*--</code><br><code>---\*---</code><br>|8|<code>---\*\*---</code><br><code>--\*--\*--</code><br><code>-\*----\*-</code><br><code>\*------\*</code><br><code>-\*----\*-</code><br><code>--\*--\*--</code><br><code>---\*\*---</code><br>|9|<code>----\*----</code><br><code>---\*-\*---</code><br><code>--\*---\*--</code><br><code>-\*-----\*-</code><br><code>\*-------\*</code><br><code>-\*-----\*-</code><br><code>--\*---\*--</code><br><code>---\*-\*---</code><br><code>----\*----</code>|

## Hints and Guidelines

What we know from the problem explanation is that the diamond is with size `n` x `n`.

From the example input and output we can conclude that all rows contain exactly `n` symbols and all the rows, with the exception of the top and bottom, have **2 stars**. We can mentally divide the diamond into 2 parts:

- **Upper** part. It starts from the upper tip down to the middle.
- **Lower** part. It starts from the row below the middle and goes down to the lower tip (inclusive).

### Upper Part

- If **n** is **odd**, it starts with **1 star**.
- If **n** is **even**, it starts with **2 stars**.
- With each row down the stars get further away from each other.
- The space between, before and after **the stars** is filled with **dashes**.

### Lower Part

- With each row down the stars get closer to each other. This means that the space (**the dashes**) between them is getting smaller and the space (**the dashes**) in the left and in the right is getting larger.
- The bottom-most part is with 1 or 2 **stars**, depending on if **n** is even or odd.

### Upper and Lower Parts of the Diamond

- On each row, except the middle row, the stars are surrounded by inner and outer **dashes**.
- On each row there is space between the two **stars**, except on the first and the last row (sometimes **the star is 1**).

### Reading the Input Data and Drawing the Upper Part of the Diamond

We read **n** from the console and we write it down in a variable of type `int`.  

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-6-images/10.Diamond-01.png alt="Code" /]

We start to draw the upper part of the diamond. The first thing we need to do is to calculate the number of the outer **dashes `leftRight` (the dashes on the outer side of **the stars**). It is equal to `(n - 1) / 2`, rounded down.

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-6-images/10.Diamond-02.png alt="Code" /]

After we have calculated `leftRight`, we start to draw **the upper part** of the diamond. We can start by making a **loop** from `0` to `n / 2 + 1` (rounded down).  

At each iteration of the loop the following steps must be taken:

- We draw on the console the left **dashes** (with length `leftRight`) and right after them the first **star**.

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-6-images/10.Diamond-03.png alt="Code" /]

- We will calculate the distance between the two **stars**. We can do this by subtracting from **n** the number of the outer **dashes**, and the number 2 (the number of **the stars**, i.e. the diamonds outline). The result of the subtraction we write down in a variable `mid`. 

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-6-images/10.Diamond-04.png alt="Code" /]

- If `mid` is lower than 0, we know that on the row there should be only 1 star. If it is higher or equal to 0 then we have to print **dashes** with length `mid` and one **star** after them.
- We draw on the console the right outer **dashes** with length `leftRight`. 

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-6-images/10.Diamond-05.png alt="Code" /]

- In the end of the loop we decrease `leftRight` by 1 (**the stars** are moving away from each other).

We are ready with the upper part.

### Drawing the Lower Part of the Diamond

Drawing the lower part is very similar to that of the upper part. The difference is that instead of decreasing `leftRight` with 1 in the end of the loop, we will increase `leftRight` with 1 in the beginning of the loop. Also, **the loop will be from 0 to `(n - 1) / 2`.   

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-6-images/10.Diamond-06.png alt="Code" /]

**Repeating a code is considered bad practice**, because the code becomes very hard to maintain. Let's imagine that we have a piece of code (e.g. the logic for drawing a row from the diamond) at a few more places and we decide to change it. For this we will have to go through all the places and change it everywhere. Now let's imagine that you need to reuse a piece of code not 1, 2 or 3 times but tens of times. A way to overcome this problem is to use **methods**. You can look for additional information for methods in the Internet or to look at [anchor href=#]Chapter 10 (Methods)[/anchor].

If we have written all correctly, then the problem is solved.

## Testing in the Judge System

Test your solution here: [anchor href=https://judge.softuni.bg/Contests/Practice/Index/512#9]https://judge.softuni.bg/Contests/Practice/Index/512#9[/anchor].
[/slide]

[slide]
# What We Learned in This Chapter?

We became acquainted with the constructor `new string`:

```csharp
string printMe = new string('*', 5);
```

We learned to draw figures with nested `for` loops:

```csharp
for (var r = 1; r <= 5; r++)
{
   Console.Write("*");
   for (var c = 1; c < 5; c++)
        Console.Write(" *");
   Console.WriteLine();
}
```
[/slide]

[slide]
# Exercises: Drawing Figures in Web Environment

Now that we got used to **nested loops** and how to use them to draw figures on the console, we can get ourselves into something even more interesting: we can see how loops can be used to **draw in web environment**. We will make a web application, which visualizes a number rating (a number from 0 to 100) with stars. This kind of visualization is common in e-commerce sites, reviews of products, event rating, rating of apps and others.

Don't worry if you don't understand all of the code, how exactly it is written and how the project works. It is normal, now we are learning to write code and we are a long way from the web development technologies. If you are struggling to write your project by following the steps, **watch the video** from the beginning of the chapter or ask in the [anchor href=https://softuni.bg/forum]SoftUni forum[/anchor].
[/slide]

[slide]
# Problem: Ratings – Visualization in Web Environment

Create an ASP.NET MVC web application for visualizing a rating (a number from 0 to 100). 1 to 10 stars should be drawn (with halves). The stars should be generated with a `for` loop.

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-6-images/11.Ratings-01.png alt="Ratings App" /]

## Creating a New C# Project

Create a new ASP.NET MVC web app with C# in Visual Studio. We add a new project from [**Solution Explorer**] -> [**Add**] -> [**New Project…**] . Give it a meaningful name, for example "WebApp-Ratings".

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-6-images/11.Ratings-02.png alt="Visual Studio" /]

Choose the type of the app to be **MVC**.

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-6-images/11.Ratings-03.png alt="Visual Studio" /]

## Creating a Web Form

Open and redact the file `Views/Home/Index.cshtml`. Delete everything and insert the following code:

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-6-images/11.Ratings-04.png alt="Visual Studio" /]

This code creates a web form `<form>` with a field `"rating"` for inputting a number in the interval [**0 … 100**] and a button [**Draw**] to send data from the form to the server. The action which will process the data is called `/Home/DrawRatings`, which means method `DrawRatings` in controller `Home`, which is in the file `HomeController.cs`. After the form the contents of `ViewBag.Stars` are printed. The code, which will be inside, will be dynamically generated by the HTML controller with a series of stars.

## Adding the DrawRatings Method

Add a method `DrawRatings` in the controller `HomeController`. Open the file `Controllers/HomeController.cs` and add the following code:

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-6-images/11.Ratings-05.png alt="Code" /]

The above code takes the number `rating`, makes some calculations to find the number of **full stars**, the number of **empty stars** and the number of **half-full stars**, after which it generates an HTML code, which orders a few pictures of stars one after the other so that it can make the rating picture from them. The ready HTML code is written down in `ViewBag.Stars` to visualize the view `Index.cshtml`. Additionally the sent rating is kept (as a number) in `ViewBag.Rating`, so that it can be put in the field for rating in the view. In order to orientate yourself better, you can help yourself with the picture of Visual Studio below:

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-6-images/11.Ratings-06.png alt="Visual Studio" /]

## Adding the Pictures With the Stars

Create a new folder **images** from [**Solution Explorer**]:
  
[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-6-images/11.Ratings-07.png alt="Visual Studio" /]

Now add **the pictures with the stars** (they are a part of the files with this project and can be downloaded from [anchor href=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/tree/master/assets/chapter-6-assets]here[/anchor]). Copy them from Windows Explorer and paste them in folder **images** in [**Solution Explorer**] in Visual Studio.

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-6-images/11.Ratings-08.png alt="Visual Studio" /]

## Starting the Project

Start the project with [**Ctrl + F5**] and enjoy:

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-6-images/11.Ratings-09.png alt="Ratings Web App" /]

If you have a problem with the example project above, **watch the video** in the beginning of the chapter. There the application is made live and step by step with much explanation. Or ask in the [anchor href=https://softuni.bg/forum]SoftUni forum[/anchor].**.
[/slide]