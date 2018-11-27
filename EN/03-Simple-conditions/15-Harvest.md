[slide]
# Problem: Harvest

[code-task title="Harvest" executionStrategy="csharp-dot-net-core-code" requiresInput]

[code-editor language=csharp]
[/code-editor]

[task-description]
From **vineyard with area X square meters**, **40% of the harvest goes for wine production**. From **1 sq.m. vineyard**, **Y kilograms of grapes** are extracted. **2,5 kg of grapes** are needed for **1 litre of wine**. **The wanted quantity of wine** for sale is **Z litres**. 

Write **a program** that **calculates how much wine can be produced** and **whether** that quantity **is enough**. **If it is enough, the rest is divided between the vineyard workers equally**. 
[/task-description]

[code-io /]
[/code-task]

## Input Data

The input data is read from the console and consists of **exactly 4 lines**: 
- First line: **X sq.m is the vineyard – an integer in the range of** [**10 … 5000**].
- Second line: **Y grapes for one sq.m. – an integer in the range of** [**0.00 … 10.00**].
- Third line: **Z needed litres of wine – an integer in the range of** [**10 … 600**].
- Fourth line: **number of workers – an integer in the range of** [**1 … 20**].

## Output Data

The following has to be printed on the console:
- If the **produced** wine is **less than the needed**:
  - **“It will be a tough winter! More {wine more needed} liters wine needed.**”  
   \- **The result** has to be **rounded down to the nearest integer**.
- If **the produced** wine is **more than the needed**:
  - **“Good harvest this year! Total wine: {total wine} liters.”**  
   \- **The result** has to be **rounded down to the nearest integer**.
  - **“{Wine left} liters left -> {wine for one worker} liters per person.”**  
   \- **Both of the results** have to be **rounded to the higher integer**.

## Sample Input and Output

|        Input       |                                          Output                                          |         Input         | Output |
|--------------------|------------------------------------------------------------------------------------------|-----------------------|--------|
|650<br>2<br>175<br>3|Good harvest this year! Total wine: 208 liters.<br>33 liters left -> 11 liters per person.|1020<br>1.5<br>425<br>4|It will be a tough winter! More 180 liters wine needed.|

## Hints and Guidelines

In order to solve the task, we will read the input data. Then, we will write a few conditional statements and do some calculations. Finally, we will print the result.

### Processing the Input Data and Doing the Calculations

First we have to **check** what **the input data** will be, so that we can choose what **variables** we will use. 

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-3-2-images/04.Harvest-01.png alt="Code" /]

To solve the problem, based on **the input data**, we have to **calculate** how many **litres of wine** will be produced. From the task requirements, we see that in order to **calculate** the quantity of **wine in litres**, we firstly have to find **the quantity of grapes in kilograms**, which will be received from the harvest. For that, we will **declare** a **variable** that stores a **value**, equal to **40%** of the result from the **multiplication** of the vineyard area by the quantity of grapes, which is extracted from 1 sq. m.

After having done these calculations, we are ready to **calculate the quantity of wine in litres** that will be produced from the harvest as well. For that, we **declare** one more **variable** that stores that **quantity**, which in order to calculate, we have to **divide the quantity of grapes in kg by 2.5**.

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-3-2-images/04.Harvest-02.png alt="Code" /]

### Conditional execution and Processing the Output Data

After having done the necessary calculations, **the next step** is to **check** whether the **litres of wine** that have been produced, **are enough**. For that we will use **a simple conditional statement** of `if-else` type and we will **check** whether **the litres of wine** from the harvest are **more than** or **equal to** the **needed litres**. 

If the condition returns `true`, from the task requirement we see that **on the first line** we have to print **the wine that has been produced from the harvest**. **That value** has to be **rounded down to the nearest integer**, which we will do by using both the method `Math.Floor(…)` and a **placeholder** when printing it. 

On the second line we have to print the results by **rounding them up to the higher integer**, which we will do by using the method `Math.Ceiling(…)`. The values, that we have to print, are of **the quantity of left wine** and **the quantity that each worker gets**. The wine left is equal to **the difference** between **the produced litres of wine** and **the needed litres of wine**. We calculate the value of that quantity in a new variable, which we declare and initialize in the `if` condition body**, before printing the first line. We calculate the quantity of wine that **each worker gets** by subtracting **the wine left** by **the number** of workers.

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-3-2-images/04.Harvest-03.png alt="Code" /]

If the condition returns `false`, we have to **print the difference** between **the needed litres** and the **produced from the harvest litres of wine**. There is a specification that the result has to be **rounded down to the nearest integer**, which we will do by using the method `Math.Floor(…)`.

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-3-2-images/04.Harvest-04.png alt="Code" /]

## Testing in the Judge System

Test your solution here: [anchor href=https://judge.softuni.bg/Contests/Practice/Index/507#3]https://judge.softuni.bg/Contests/Practice/Index/507#3[/anchor].
[/slide]