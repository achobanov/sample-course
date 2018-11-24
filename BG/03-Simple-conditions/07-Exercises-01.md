[slide]
# Exercises: Simple Conditions

To verified our knowledge of conditional constructions `if` and `if-else`, we will solve a few practical exercises.

## Problem: bonus score

You have an **integer** - the number of points. **Bonus scores** are charged on it, according to the rules described below. Write a program that calculates **bonus scores** for this figure and **total points** with bonuses.- Ако числото е **до 100** включително, бонус точките са 5.

- If the number is **up to 100** including, bonus points are 5.
- If the number is **larger than 100**, bonus points are **20%** from the number.
- If the number is **larger than 1000**, bonus points are **10%** from the number.
- Additional bonus points (accrues separately from the previous ones):
- for **even** number -> + 1 p.
- for number, that **ends with 5** -> + 2 p.

[task]  
    [code-editor language=csharp]
        var num = int.Parse(Console.ReadLine());
        var bonusScore = 0.0;
        // TODO
    [/code-editor]

    [task-description]
        We can calculate the basic and additional bonus points with a series of `if-else-if-else` conditions. For **the main bonus points we have 3 cases** (when the entered number is up to 100, between 100 and 1000 and larger than 1000), and for **extra bonus points - 2 more cases** (when the number is even and odd).
    [/task-description]
[/task]
 
### Sample Input and Output

| Input |       Output      |
|-------|-------------------|
| 20    | 6<br>26           |
| 175   | 37<br>212         |
| 2703  | 270.3<br>2973.3   |
| 15875 | 1589.5<br>17464.5 |

### Hints and Guidelines

We can calculate the basic and additional bonus points with a series of `if-else-if-else` conditions. For **the main bonus points we have 3 cases** (when the entered number is up to 100, between 100 and 1000 and larger than 1000), and for **extra bonus points - 2 more cases** (when the number is even and odd).

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-3-images/06.Bonus-score-01.png alt="Code" /]

Here's an example solution::

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-3-images/06.Bonus-score-02.png alt="Console" /]

Note that for this exercise, the Judge is set to ignore anything that is not a number, so we can print not only the numbers, but also the specifying text.

### Testing in the Judge System

Test your solution  here: [anchor href=https://judge.softuni.bg/Contests/Practice/Index/506#3]https://judge.softuni.bg/Contests/Practice/Index/506#3[/anchor].
[/slide]

[slide]
# Problem: sum seconds

Three athletes finish for a few **seconds** (between **1** and **50**). Write a program that introduces the times of the contestants and calculates their **total time** in "minutes:seconds". Seconds need to be **zeroed at the front** (2 -> "02", 7 -> "07", 35 -> "35").

[task]  
    [code-editor language=csharp]
    [/code-editor]
[/task]	

## Sample Input and Output

|      Input     | Output |
|----------------|--------|
| 35<br>45<br>44 | 2:04   |
| 22<br>7<br>34  | 1:03   |
| 50<br>50<br>49 | 2:29   |
| 14<br>12<br>10 | 0:36   |

## Hints and Guidelines

First we sum the three numbers to get the total result in seconds. Since **1 minute = 60** seconds, we will have to calculate the number of minutes and seconds in the range 0 to 59:- Ако резултатът е между 0 и 59, отпечатваме 0 минути + изчислените секунди.
- If the result is between 0 and 59, we print 0 minutes + calculated seconds.
- If the result is between 60 and 119, we print 1 minute + calculated seconds minus 60.
- If the result is between 120 and 179, we print 2 minutes + calculated seconds minus 120.
- If the seconds are less than 10, we print the number with zero in front.

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-3-images/07.Sum-seconds-01.png alt="Code" /]

## Testing in the Judge System

Test your solution here: [anchor href=https://judge.softuni.bg/Contests/Practice/Index/506#6]https://judge.softuni.bg/Contests/Practice/Index/506#6[/anchor].
[/slide]

[slide]
# Problem: metric converter

Write a program that **convert a distance** between the following **8 units of measure**: `m`, `mm`,` cm`, `mi`, `in`, `km`,` ft `,` yd`. Use the below table:

|  Input measure  |       Output measure      |
|:---------------:|:-------------------------:|
| 1 meter (m)     | 1000 millimeters (mm)     |
| 1 meter (m)     | 100 centimeters (cm)      |
| 1 meter (m)     | 0.000621371192 miles (mi) |
| 1 meter (m)     | 39.3700787 inches (in)    |
| 1 meter (m)     | 0.001 kilometers (km)     |
| 1 meter (m)     | 3.2808399 feet (ft)       |
| 1 meter (m)     | 1.0936133 yards (yd)      |

You have three input lines:

- First line: number for converting.
- Second line: input unit.
- Third line: output unit (the result).

[task]  
    [code-editor language=csharp]
        var size = double.Parse(Console.ReadLine());
        var sourceMetric = Console.ReadLine().ToLower();
        var destMetric = Console.ReadLine().ToLower();

        if (sourceMetric == "km")
        {
            size = size / 0.001;
        }

        // TODO: Check the other metrics
    [/code-editor]

    [task-description]
        We read the input data, and we can add `.ToLower()` method when we read the measure units, which will make all letters small.
    [/task-description]
[/task]	

## Sample Input and Output

|       Input       |      Output      |
|-------------------|------------------|
| 12  <br>km <br>ft | 39370.0788       |
| 150 <br>mi <br>in | 9503999.99393599 |
| 450 <br>yd <br>km | 0.41147999937455 |

## Hints and Guidelines

We read the input data, and we can add `.ToLower()` method when we read the measure units, which will make all letters small. As we can see from the table in the condition, we can only do converting **between meters and some other measure unit**. Then, first we have to calculate the number for converting in meters. That's why, we need to make a set of checks to define the input unit and then the output unit.

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-3-images/08.Metric-converter-01.png alt="Code" /]

## Testing in the Judge System

Test your solution here: [anchor href=https://judge.softuni.bg/Contests/Practice/Index/506#7]https://judge.softuni.bg/Contests/Practice/Index/506#7[/anchor].
[/slide]