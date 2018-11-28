[slide]
# Exercises: complex conditions

Now let's exercise the work with complex conditions. Let's solve a few practical tasks.

## Problem: cinema

[code-task title="Cinema" executionStrategy="csharp-dot-net-core-code" requiresInput]

[code-editor language=csharp]
[/code-editor]

[task-description]
In a cinema hall the chairs are order in a **rectangle** shape in **r** rows and **c** columns. There are three types of projections with tickets of **different** prices:

- **Premiere** – a premiere projection, with price **12.00** levs.
- **Normal** – a standart projection, with price **7.50** levs.
- **Discount** – a projection for children and students on a reduced price - **5.00** levs.

Wirte a program, that enters a **type of projection** (string), count of **rows** and count of **columns** in the hall (integer numbers) and calculates **the total income** from tickets from a **full hall**. The result has to printed in the same format as in the examples below - with 2 digits after the decimal sign.
[/task-description]

[code-io /]
[/code-task]

## Sample Input and Output
 
|        Input       |   Output   |       Input      |   Output   |
|--------------------|------------|------------------|------------|
|Premiere<br>10<br>12|1440.00 leva|Normal<br>21<br>13|2047.50 leva|

## Hints and Guidelines 

While reading the input, we could convert the type of the projcection into small letters (with the function `.ToLower()`). We create and initialize a varibale, which will store the calculated income. In another variable we calculate the full capacity of the hall. We use a `switch-case` conditional statement to calculate the income according to the type of the projection and we print the result on the console in the given format. (look for the needed **C#** functionality on the internet). 

Sample code (parts of the code are blurred with the purpose of stimulating the thinking and solving skills):

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-4-images/11.Cinema-01.png alt="Code" /]

## Testing in the Judge System

Test your solution here: [anchor href=https://judge.softuni.bg/Contests/Practice/Index/508#10]https://judge.softuni.bg/Contests/Practice/Index/508#10[/anchor].
[/slide]

[slide]
# Problem: volleyball

[code-task title="Volleyball" executionStrategy="csharp-dot-net-core-code" requiresInput]

[code-editor language=csharp]
[/code-editor]

[task-description]
Vladi is a student, lives in Sofia and goes to his hometown from time to time. He is very keen on volleyball, but is busy during weekdays and plays **volleyball** only during **weekends** and on **holidays**. Vladi plays **in Sofia** every **Saturday**, when **he is not working** and **he is not travelling to his hometown** and also during **2/3 of the holidays**. He travels to his **hometown h times** a year, where he plays volleyball with his old friends on **Sunday**. Vladi **is not working 3/4 of the weekends**, during which he is in Sofia. Furhter more, during **leap years** Vladi plays **15% more** volleyball than the usual. We accept, that the year has exactly **48 weekends**, suitable for volleyball. 
Write a program, which calculates **how many times Vladi has played volleyball** through the year. **Round the result** down to the nearest whole number (e.g. 2.15 -> 2; 9.95 -> 9).

The input data is read from the console:

- The first row contains the word “**leap**” (leap year) or “**normal**” (a normal year with 365 days).
- The second row contains the whole number **p** – the count of holidays in the year (which are not Saturday or Sunday).
- The third row contains the whole number **h** – the count of weekends, in which Vladi travels to his hometown.
[/task-description]

[code-io /]
[/code-task]

## Sample Input and Output

|     Input    | Output |      Input     | Output |
|--------------|--------|----------------|--------|
|leap<br>5<br>2|45      |normal<br>3<br>2|38      |

|      Input      | Output |      Input     | Output |
|-----------------|--------|----------------|--------|
|normal<br>11<br>6|44      |leap<br>0<br>1  |41      |

## Hints and Guidelines

As usual we read the input data from the console and to avoid making errors, we convert the text into small letters with the function `.ToLower()`. Consequently, we calculate **the weekends spent in Sofia**, **the time for playing in Sofia** and **the common playtime**. At last, we check whether the year is **leap**, we make additional calculation when necessary and we print the result on the console **rounded down** to the nearest **whole number** (look for a **C#** class with such functionality).

A sample code (parts of the code are blurred on purpose to stimulate the independent thinking and solving skills):

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-4-images/11.Volleyball-01.png alt="Code" /]

## Testing in the Judge System

Tets your solution here: [anchor href=https://judge.softuni.bg/Contests/Practice/Index/508#11]https://judge.softuni.bg/Contests/Practice/Index/508#11[/anchor].
[/slide]

[slide]
# Problem: * point in the figure

The figure consists of **6 blocks with size h \* h**, placed as in the figure. The lower left angle of the building is on position {0, 0}. The upper right angle of the figure is on position {**2\*h**, **4\*h**}. The coordinates given in the figure are for **h = 2**:

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-4-images/13.Point-in-the-figure-01.png alt="Code" /]

[code-task title="Point in the Figure" executionStrategy="csharp-dot-net-core-code" requiresInput]

[code-editor language=csharp]
[/code-editor]

[task-description]
Write a program that enters a whole number **h** and the coordinates of a given **point {x, y}** (whole numbers) and prints whether the point is inside the figure(**inside**), outside of the figure (**outside**) or on any of the borders of the figure (**border**).
[/task-description]

[code-io /]
[/code-task]

## Sample Input and Output

|    Input   | Output |   Input   | Output |
|------------|--------|-----------|--------|
|2<br>3<br>10|outside |2<br>3<br>1|inside  |

|    Input   | Output |   Input   | Output |
|------------|--------|-----------|--------|
|2<br>2<br>2 |border  |2<br>6<br>0|border  |

|    Input   | Output |     Input    | Output |
|------------|--------|--------------|--------|
|2<br>0<br>6 |outside |15<br>13<br>55|outside |

|     Input    | Output |     Input    | Output |
|--------------|--------|--------------|--------|
|15<br>29<br>37|inside  |15<br>37<br>18|outside |

|     Input   | Output |    Input    | Output |
|-------------|--------|-------------|--------|
|15<br>-4<br>7|outside |15<br>30<br>0|border  |

## Hints and Guidelines

A possible logic for solving the task (not the only correct one):

- We might split the figure into **two rectangles** with a common side:

<p align="center"><img src="https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-4-images/13.Point-in-the-figure-03.png" /></p>

- A point is **outer (outside)** for the figure, when it is **outside** both of the rectangles.
- A point is **inner (inside)** for the figure, if it is inside some of the rectangles (excluding their borders) or lies on their common side.
- In **other case** the point lies on the border of the rectangle (**border**).

## Implementing the Proposed Idea

An examplary implementation of the described idea (parts of te code are blurred with the purpose of stimulating the logical thinking and solving skills):

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-4-images/13.Point-in-the-figure-02.png alt="Code" /]

## Testing in the Judge System

Test your solution here: [anchor href=https://judge.softuni.bg/Contests/Practice/Index/508#12]https://judge.softuni.bg/Contests/Practice/Index/508#12[/anchor].
[/slide]