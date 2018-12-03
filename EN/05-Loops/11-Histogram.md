[slide]
# Exam Problems

Lets solve a few problems with loops from exams in SoftUni. 

## Problem: Histogram
	
[code-task title="Histogram" executionStrategy="csharp-dot-net-core-code" requiresInput]

[code-editor language=csharp]
[/code-editor]

[task-description]
We have **n integer numbers** within the range [**1 … 1000**]. From them some percent **p1** are under 200, percent __p2__ are from 200 to 399, percent **p3** are from 400 to 599, percent **p4** are from 600 to 799 and the rest **p5** percentages are from 800 upwards. Write a program, that calculates and prints the percentages **p1**, **p2**, **p3**, **p4** and **p5**.

**Example**: we have n = **20** numbers: 53, 7, 56, 180, 450, 920, 12, 7, 150, 250, 680, 2, 600, 200, 800, 799, 199, 46, 128, 65. We get the following distribution and visualization:
                          
|  **Group**  |                 **Numbers**                     | **Count numbers** |          **Percent**            |
|-------------|-------------------------------------------------|-------------------|---------------------------------|
| < 200       | 53, 7, 56, 180, 12, 7, 150, 2, 199, 46, 128, 65 | 12                | p1 = 12 / 20 * 100 = 60.00%     |
| 200 … 399   | 250, 200                                        | 2                 | p2 = 2 / 20 * 100 = 10.00%      |
| 400 … 599   | 450                                             | 1                 | p3 = 1 / 20 * 100 = 5.00%       |
| 600 … 799   | 680, 600, 799                                   | 3                 | p4 = 3 / 20 * 100 = 15.00%      |
| ≥ 800       | 920, 800                                        | 2                 | p5 = 2 / 20 * 100 = 10.00%      |
[/task-description]

[code-io /]
[/code-task]

### Input Data

On the input line is the integer number **n** (1 ≤ **n** ≤ 1000), that represents the count of lines with numbers, which will be given. On the next **n lines** we have **one integer number** within range [**1 … 1000**] – numbers, on which we have to calculate the histogram.

### Output Data

Print on the console **histogram that consists of 5 lines**, each of them containing a number within the range 0% and 100%, formatted to two digits after the decimal point (for example 25.00%, 66.67%, 57.14%).

### Sample Input and Output

|    Input    |    Output     |    Input    |   Output   |
|-------------|---------------|-------------|------------|
| **3**       | 66.67%        | **4**       | 75.00%     |
| 1           | 0.00%         | 53          | 0.00%      |
| 2           | 0.00%         | 7           | 0.00%      |
| 999         | 0.00%         | 56          | 0.00%      |
| ≥ 800       | 33.33%        | 999         | 25.00%     |

|    Input    |    Output     |    Input    |   Output   |
|-------------|---------------|-------------|------------|
| **7**       | 14.29%        | **9**       | 33.33%     |
| 800         | 28.57%        | 367         | 33.33%     |
| 801         | 14.29%        | 99          | 11.11%     |
| 250         | 14.29%        | 200         | 11.11%     |
| 199         | 28.57%        | 799         | 11.11%     |
| 399         |               | 999         |            |
| 599         |               | 333         |            |
| 799         |               | 555         |            |
|             |               | 111         |            |
|             |               | 9           |            |

### Hints and Guidelines

The program that solves this problem, we can split in three parts:

- **Reading the input data** – in the current problem this includes reading of the number **n**, following by **n count integer numbers**, each on a single line.
- **Processing the input data** – in this case that means allocating the numbers into groups and calculating the percentage breakdown by groups.
- **Printing the output** – print the histogram on the console in the specified format.
  
Before we proceed forward, we will make a small deviation from the current topic, that is, we will briefly mention that in programming every variable is from some **type of data**. In this problem we will use the numeral types `int` for **integer numbers** and `double` for **real numbers**. Often, for making it easier, programmers miss the explicit specification of the type by replacing it with the keyword `var`.  For better understanding we will write the type in the variable declaration.

We will now proceed to the implementation of each of the above points.

#### Reading the Input Data
  
Before we proceed to the reading of the input data, we must **declare the variables**, in which we will store them. This means choosing the right type of data and appropriate names.
  
[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-5-2-images/01.Histogram-01.png alt="Code" /]

In the variable `n` we will store the count of numbers, which we will read from the console. We choose `int` type**, because in the description is said, that `n` is integer number** within the range from 1 to 1000. For the variables, in which we will store the percentages, we choose `double` type**, because **they are not expected** to be always **integer numbers** . Additionally, we declare the variables `cntP1`, `cntP2` etc., in which we will keep count of the numbers from the respective group, and we choose again `int` type**.

After we have declared the needed variables, we can read the number `n` from the console:

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-5-2-images/01.Histogram-02.png alt="Code" /]

#### Separate numbers in groups

To read and separate every number in its corresponding group, we will use `for` loop** froom **0** to `n` (count of numbers). Every iteration of the loop will read and separate **one single** number (`currentNumber`) in its corresponding group. In order to determine if a number belongs to a group, we **perform a check in its respective range**. If it is -  we increase the count of the numbers in the corresponding group (`cntP1`, `cntP2` etc.) with 1.  

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-5-2-images/01.Histogram-03.png alt="Code" /]

#### Calculating percentages

After we have determinated how many numbers there are in each group, we can move on to calculating the percentages, which is the main purpose of the problem. For this we will use the following formula:

<p align="center"><strong>(group percentage) = (count of numbers in group) * 100 / (count of all numbers)</strong></p>

This formula in the program code looks like this:

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-5-2-images/01.Histogram-04.png alt="Code" /]

If we divide by **100** (`int` number type) instead of **100.0** (`double` number type), will be performed the so-called **integer division** and in the variable will be saved only the whole part of the division and this is not the result we want. For Example: **5 / 2 = 2**, but **5 / 2.0 = 2.5**. Considering this, the formula for the first variable will look like this: 

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-5-2-images/01.Histogram-05.png alt="Code" /]

To make it even clearer, let's take a look at the following Example: 

|         Input        |                   Output                  |
|----------------------|-------------------------------------------|
|**3**<br>1<br>2<br>999|66.67%<br>0.00%<br>0.00%<br>0.00%<br>33.33%|

In this case `n = 3`.
For the loop we have:
- `i = 0` - we read the number 1, which is less than 200 and falls into the first group (`p1`), and increase the group counter (`cntP1`) with 1.
- `i = 1` – we read the number 2, which again falls into the first group (`p1`) and increase its counter (`cntP1`) again with 1.
- `i = 2` – we read the number 999, which falls into the last group (`p5`), because its bigger than 800, and increase the counter of the group (`cntP5`) with 1.
   
After reading the numbers in group `p1` we have 2 numbers, and in `p5` we have 1 number. We have **no numbers** in the other groups. By applying the above formula, we calculate the percentages of each group. If we multiply in the formula by **100**, instead of **100.0** we will receive for group `p1` 66%, and for group `p5` – 33% (without fractional part).

#### Printing the output
  
We only have to print out the reults. In the description is said, that the percentages must be with **precision two points after the decimal point**. To achive this , write “:f2”: after the placeholder:

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-5-2-images/01.Histogram-06.png alt="Code" /]

### Testing in the Judge System

Test your solution here: [anchor href=https://judge.softuni.bg/Contests/Practice/Index/511#0]https://judge.softuni.bg/Contests/Practice/Index/511#0[/anchor].
[/slide]