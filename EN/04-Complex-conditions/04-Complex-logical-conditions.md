[slide]
# Complex logical conditions

Sometimes the conditions might be very complicated, so they can require a long boolean expression or a sequence of evaluations. Let's take a look at a few examples.

## Example: a point on the border of a rectangle

[code-task title="Point on Rectangle Border" executionStrategy="csharp-dot-net-core-code" requiresInput]

[code-editor language=csharp]
[/code-editor]

[task-description]
Write a program that checks whether a **point {x, y}** is placed **onto any of the sides of the rectangle {x1, y1} - {x2, y2}**. The input data is read from the console and  it consists of 6 rows: the decimal numbers **x1**, **y1**, **x2**, **y2**, **x** and **y** (as it is garanteed that **x1 < x2** and **y1 < y2**). Print "**Border**" (if the point lies on any of the sides) or "**Inside / Outside**" (in the opposite case).

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-4-images/06.Point-on-rectangle-border-01.png alt="Rectangle" /]
[/task-description]

[code-io /]
[/code-task]

### Sample Input and Output

|             Input            | Output |             Input           |     Output     |
|------------------------------|--------|-----------------------------|----------------|
|2<br>-3<br>12<br>3<br>12<br>-1|Border  |2<br>-3<br>12<br>3<br>8<br>-1|Inside / Outside|

### Solution

The point lies on any of the sides of the rectangle if:
- **x** coincides with **x1** or **x2** and at the same time **y** is between **y1** and **y2** or
- **y** coincides with **y1** or **y2** and at the same time **x** is between **x1** and **x2**.

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-4-images/06.Point-on-rectangle-border-02.png alt="Code" /]

The previous evaluation might be simplified by the following way:

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-4-images/06.Point-on-rectangle-border-03.png alt="Code" /]

The second way with the additional boolean variables is longer, but much more understandable than th first one, isn't it? We recommend to you when you write boolean conditions, to make them **easy to read and uderstand**, and not short. If you need to, use additional variables with meaningful names. The names of the boolean variables have to hint what the value that is kept in them represents.

It is left to finish writing the code to print “**Inside / Outside**”, if the point is not onto any of the sides of the rectangle.

#### Testing in the Judge System

After you finish writing the solution, you can test it here: [anchor href=https://judge.softuni.bg/Contests/Practice/Index/508#5]https://judge.softuni.bg/Contests/Practice/Index/508#5[/anchor].
[/slide]

[slide]
# Example: fruit store

A fruit store during **week days** sells on the following **prices**:

|                               Fruit                                  |                        Price                       |
|:--------------------------------------------------------------------:|:--------------------------------------------------:|
|banana<br>apple<br>orange<br>grapefruit<br>kiwi<br>pineapple<br>grapes|2.50<br>1.20<br>0.85<br>1.45<br>2.70<br>5.50<br>3.85|

During the weekend days the prices are **higher**:

|                               Fruit                                  |                        Price                       |
|:--------------------------------------------------------------------:|:--------------------------------------------------:|
|banana<br>apple<br>orange<br>grapefruit<br>kiwi<br>pineapple<br>grapes|2.70<br>1.25<br>0.90<br>1.60<br>3.00<br>5.60<br>4.20|

[code-task title="Fruit Store" executionStrategy="csharp-dot-net-core-code" requiresInput]

[code-editor language=csharp]
// TODO: Process input data

if (day == "saturday" || day == "sunday")
{
    if (fruit == "banana")
        price = 2.70;
    else if (fruit == "apple")
        price = 1.25;
    // TODO: Check other fruits
}
// TODO: Check other days
[/code-editor]

[task-description]
Write a program, which **reads** from the console a **fruit** (banana / apple / …), **a day of the week** (Monday / Tuesday / …) and **a quantity (a decimal number)** and **calculates the price** according to the prices from the tables above. The result has to be printed **rounded to 2 digits after the decimal sign**. Print **“error”** at an  **invalid day** from the week or an **ivalid name** of a fruit.
[/task-description]

[code-io /]
[/code-task]

## Sample Input and Output

|        Input        | Output |         Input       | Output |
|---------------------|--------|---------------------|--------|
|orange<br>Sunday<br>3|2.70    |kiwi<br>Monday<br>2.5|6.75    |

|          Input          | Output |          Input        | Output |
|-------------------------|--------|-----------------------|--------|
|grapes<br>Saturday<br>0.5|2.10    |tomato<br>Monday<br>0.5|error   |

#### Solution

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-4-images/07.Fruit-shop-01.png alt="Code" /]

#### Testing in the Judge System

Test your solution here: [anchor href=https://judge.softuni.bg/Contests/Practice/Index/508#6]https://judge.softuni.bg/Contests/Practice/Index/508#6[/anchor].
[/slide]

[slide]
# Example: trade commissions

A company is giving the following **commissions** to its traders according to the **city**, in which they are working in and the **volume of sales s**:
 
|           City          |   0 <= s <= 500  | 500 < s <= 1000 |1000 < s <= 10000|s > 10000          |
|:-----------------------:|:----------------:|:---------------:|:---------------:|:-----------------:|
|Sofia<br>Varna<br>Plovdiv|5%<br>4.5%<br>5.5%|7%<br>7.5%<br>8% |8%<br>10%<br>12% |12%<br>13%<br>14.5%|

[code-task title="Trade Commissions" executionStrategy="csharp-dot-net-core-code" requiresInput]

[code-editor language=csharp]
var comission = -1.0;
if (town == "sofia")
{
    // TODO: Check the price ranges
}
else if (town == "varna")
{
    // TODO: Check the price ranges
}
else if (town == "plovdiv")
{  
    // TODO: Check the price ranges
}

if (comission >= 0)
{
    // TODO: Print
}
else
{
    Console.WriteLine("error");
}
[/code-editor]

[task-description]
Write a **program**, which reads the name of a **city** (string) and a volume of **sales** (decimal number) and calculates the rate of the commission. The result has to be shown rounded **2 decimal digits after the decimal separator**. When there is an **invalid city or a volume of sales** (a negative number), print "**error**".
[/task-description]

[code-io /]
[/code-task]

## Sample Input and Output

|    Input    | Output |      Input      | Output |      Input     | Output |
|-------------|--------|-----------------|--------|----------------|--------|
|Sofia<br>1500|120.00  |Plovdiv<br>499.99|27.50   |Kaspichan<br>-50|error   |

## Solution

When reading the input, we could convert the city into small letters (with the function `.ToLower()`). At first we set the commission to `-1`. It will be changed, if the city and the price range are found in the table of commissions.
To calculate the commission according to the city and volume of sales, we need a few nested `if` statements**, as it is in the sample code below:

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-4-images/08.Trade-comissions-01.png alt="Code" /]

## Testing in the Judge System

Test your solution here: [anchor href=https://judge.softuni.bg/Contests/Practice/Index/508#7]https://judge.softuni.bg/Contests/Practice/Index/508#7[/anchor].

**It is a good practice** to use **blocks**, which we **enclose* with curly braces `{ }` after `if` and `else`. Also, it is recommended during writing to **move aside** the code **after `if` and `else`** with a single tabulation **inward**, in order to make the code more easily readable.
[/slide]