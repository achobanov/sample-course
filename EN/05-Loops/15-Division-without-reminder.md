[slide]
# Problem: Division without Remainder

[code-task title="Division without Remainder" executionStrategy="csharp-dot-net-core-code" requiresInput]

[code-editor language=csharp]
[/code-editor]

[task-description]
We have **n integers** in the range [**1 ... 1000**]. From them, **some percent p1 are divisible without remainder by 2**, **percent p2** are **divisible withour remainder by 3**, **percent p3** are **divisible without remainder by 4**. Write a program that calculates and prints the p1, p2 and p3 percents.

**Example:** We have **n = 10** numbers: 680, 2, 600, 200, 800, 799, 199, 46, 128, 65. We get the following distribution and visualization:

| Division without remainder by: |             Numbers            | Count |             Percent              |
|--------------------------------|--------------------------------|-------|----------------------------------|
| 2                              | 680, 2, 600, 200, 800, 46, 128 | 7     | p1 = (7 / 10) * 100 = **70.00%** |
| 3                              | 600                            | 1     | p2 = (1 / 10) * 100 = 10.00%     |
| 4                              | 680, 600, 200, 800, 128	      | 5     | p3 = (5 / 10) * 100 = 50.00%     |
[/task-description]

[code-io /]
[/code-task]

## Input Data

On the first line of the input is the integer **n** (1 ≤ **n** ≤ 1000) - count of numbers. In the next **n lines** stands ** one integer** in the range [**1 … 1000**] – numbers, that needs to be checked for division.

## Output Data

Print on the console **3 lines**, each of them containing a percent between 0% and 100%, two places after the decimal point, for example 25.00%, 66.67%, 57.14%.
- On the **first line** – percent of the numbers, that are **divisible by 2**.
- On the **second line** – percent of the numbers, that are **divisible by 3**.
- On the **third line** – percent of the numbers, that are **divisible by 4**.

## Sample Input and Output

|                                 Input                                  |          Output          |       Input        |          Output          |
|------------------------------------------------------------------------|--------------------------|--------------------|--------------------------|
|**10**<br>680<br>2<br>600<br>200<br>800<br>799<br>199<br>46<br>128<br>65|70.00%<br>10.00%<br>50.00%|**3**<br>3<br>6<br>9|33.33%<br>100.00%<br>0.00%|

|    Input    |            Output             |
|-------------|-------------------------------|
| **1**<br>12 | 100.00%<br>100.00%<br>100.00% |

## Hints and Guidelines

For current and next task you will need to write by yourself the program code, following the given guidelines.

The program that solves the current problem is similar with the one from **Histogram** problem, which we reviewed above. That's why we can start declaring the necessary variables:
Sample names of variables may be: `n` – count of numbers (that we need to read from the console) and `divisibleBy2`, `divisibleBy3`, `divisibleBy4` – helping variables, that keeps the count of the numbers in corresponding group.

To read and allocate each number to its corresponding group we have to rotate `for` loop** from `0` to `n` (count of numbers). Each iteration of the loop should read and allocate **one single number**. The difference here is that a **single number can get into several groups at once**, so we have to make **three separate `if` checks for each number** – respectively whether it is divided by 2, 3 and 4 (using `if-else` construction in this case will not work, because after finding a match is interrupted further checking the conditions) and increase the value of the variable that keeps the count of numbers in corresponding group.

Finally you need to print the received results, by following the specified format.

## Testing in the Judge System

Test your solution here: [anchor href=https://judge.softuni.bg/Contests/Practice/Index/511#4]https://judge.softuni.bg/Contests/Practice/Index/511#4[/anchor].
[/slide]