[slide]
# Complex conditions

Let's take a look at how we can make more complex logical conditions. We can use the logical "**AND**" (`&&`), the logical "**OR**" (`||`), the logical **negation** (`!`) and **brackets** (`()`).

## Logical "AND"

As we saw, in some tasks we have to make **many evaluations at once**. But waht happens, whenever in order to execute some code, **more** conditions have to be executed and we **don't want to** make a **negation** (`else`) for every one of them? The option with nested `if` blocks** is valid, but the code would look very **unordered** and for sure - **hard** to read and maintain.  

The logical "**AND**" (opreator `&&`) means a few conditions have to be **fulfiled simultaneously**. The following table of thruthfulness is applicable:

|               a              |               b              |             a && b            |
|:----------------------------:|:----------------------------:|:-----------------------------:|
|true<br>true<br>false<br>false|true<br>false<br>true<br>false|true<br>false<br>false<br>false|

### How does logical && work ?

The operator `&&` accepts **a couple of boolean** (conditional) statements, which have a `true` value or `false`, and returns to us **one** boolean statement as a **result**. Using it **instead** of couple of nested `if` blocks, makes the code **more readable**, **ordered** and **easy** to maintain. But how does it **work**, when we put a **few** conditions one after another? As we saw above, the logical **"AND"** returns `true`, **only** when it accepts as **arguments statements** with value `true`. Respectively, when we have a **sequence** of arguments, the logical "AND" **checks** either until one of the arguments is **over**, or until it **meets** an argument with value `false`. 

**Example**:

```csharp
bool a = true;
bool b = true;
bool c = false;
bool d = true;
bool result = a && b && c && d;
// false (as d is not being checked)
```

The program will run in the **folowing** way: **It starts** the evaluation form `а`, **reads** it and accpets, that it has a `true` value, after which it **checks** `b`. After it has **accepted**, that `a` and `b` return `true`, **it checks the next** argument. It gets to `c` and sees, that the variable has a `false` value. After the program accepts, taht the agrument `c` has a `false` value, it calculates the expression **until `c`, **independent** of what the value of `d` is. That is why the evaluation of `d` is being **skipped** and the whole expression is calculated as `false`.

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-4-images/00.Logical-and-01.png alt="Code" /]
[/slide]

[slide]
# Example: a point in a rectangle

[code-task title="Point in a Rectangle" executionStrategy="csharp-dot-net-core-code" requiresInput]

[code-editor language=csharp]
var x1 = double.Parse(Console.ReadLine());
var y1 = double.Parse(Console.ReadLine());
var x2 = double.Parse(Console.ReadLine());
var y2 = double.Parse(Console.ReadLine());

var x = double.Parse(Console.ReadLine());
var y = double.Parse(Console.ReadLine());

if (x => x1 && x <= x2 && y => y1 && y <= y2)
{
    // TODO
}
[/code-editor]

[task-description]
Checks whether **point {x, y}** are placed **insie the rectangle {x1, y1} – {x2, y2}**. The input data is read from the console and consists of 6 rows: the decimal numbers **x1**, **y1**, **x2**, **y2**, **x** и **y** (as it is garanteed, that **x1 < x2** and **y1 < y2**).
[/task-description]

[code-io /]
[/code-task]

## Sample Input and Output

|             Input           | Output |                        Visualization                         |
|-----------------------------|--------|:------------------------------------------------------------:|
|2<br>-3<br>12<br>3<br>8<br>-1|Inside  |[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-4-images/03.Point-in-rectangle-01.png alt="Visualization" /]|

## Solution

A point is internal for a given quadrangle, if **at the same time** the following four conditions are applied:

- The point is placed rigth from the left side of the rectangle.
- The point is placed left from the right side of the rectangle.
- The point is placed down from the upper side of the rectangle.
- The point is placed up from the down side of the rectangle.

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-4-images/03.Point-in-rectangle-03.PNG alt="Code" /]

## Testing in the Judge System

Test your solution here:[anchor href=https://judge.softuni.bg/Contests/Practice/Index/508#2]https://judge.softuni.bg/Contests/Practice/Index/508#2[/anchor].
[/slide]

[slide]
# Logical "OR"

The logical **"OR"** (operator `||`) means that **at least one** amongst a few conditions is fulfilled. Similar to the operator `&&`, the logical **"OR"** accepts a few arguments of **boolean** (conditional) type and returns `true` or `false`. We can easily guess, that we **receive** a value `true`, everytime when at least **one** of the arguments has a `true` value. Typical example for the logic of this operator is the following:

At school the teacher says: "John or Peter to clean the board". To fulfill this condition (to clean the board), it is possible either just for John to clean it, or just for Peter to clean it or both of them to do it.

|              a               |               b              |       a &#124;&#124; b      |
|:----------------------------:|:----------------------------:|:---------------------------:|
|true<br>true<br>false<br>false|true<br>false<br>true<br>false|true<br>true<br>true<br>false|

## How does the || operator work ?

We have already learned what the logical**"OR" represents**. But how is it actually being achieved? Just like with the logical **"AND"**, the program **checks** from left to right **the arguments**, which are given. In order ro receive `true` from the expression, it is necessary fоr **just one** argument to have a `true` value, respectively the evaluation **continues** until an **argument** with **such** value is met or until the arguments **are over**.

Here is one **example** for the operator `||` in action:

```csharp
bool a = false;
bool b = true;
bool c = false;
bool d = true;
bool result = a || b || c || d;
// true (as c and d are not being checked)
```

The programs **checks `а`, accepts, that it has a value `false` and continues. Reaching `b`, it evaluates, that it has a `true` value and the whole **expression** receives a value `true`, **without** having to check `c` or `d`, because their values **wouldn't change** the result of the expression.
[/slide]

[slide]
# Example: a fruit or a vegetable

[code-task title="Fruit or a Vegetable" executionStrategy="csharp-dot-net-core-code" requiresInput]

[code-editor language=csharp]
var s = Console.ReadLine();

if (s == "banana" || s == "apple" || s == "kiwi" ||
    s == "cherry" || s == "lemon" || s == "grapes")
{
    Console.WriteLine("fruit");
}
// TODO
[/code-editor]

[task-description]
Let us check wheter a given **product** is **a fruit** or **a vegetable**. The "**fruit**" are **banana**, **apple**, **kiwi**, **cherry**, **lemon** and **grapes**. The "**vegetables**" are **tomato**, **cucumber**, **pepper** and **carrot**. Everything else is "**unknown**".
[/task-description]

[code-io /]
[/code-task]

## Sample Input and Output

|          Input         |            Output           |
|------------------------|-----------------------------|
|banana<br>tomato<br>java|fruit<br>vegetable<br>unknown|

## Solution

We have to use a few conditional statements with logical "**OR**" (`||`):

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-4-images/04.Fruit-or-vegetable-01.png alt="Code" /]

## Testing in the Judge System

Test your solution here: [anchor href=https://judge.softuni.bg/Contests/Practice/Index/508#3]https://judge.softuni.bg/Contests/Practice/Index/508#3[/anchor].
[/slide]

[slide]
# Logical negation

**Logical negation** (operator `!`) means a given condition is **is not fulfilled**.

|   a  |  !a  |
|:----:|:----:|
|true  |false |

The operator `!` accepts as an **argument** a boolean variable and **returns** its value.

# Operator parantheses `()`

Like the rest of the operators in programming, the operators `&&` and `||` have a priority, like in the case `&&` is with bigger priority from the `||`. The operator `()` serves for **a change of priority of the operators** and is being calculated first, just like in math. Using parentheses also gives the code better readability and is considered a good practice.
[/slide]

[slide]
# Example: invalid number

[code-task title="Invalid Number" executionStrategy="csharp-dot-net-core-code" requiresInput]

[code-editor language=csharp]
[/code-editor]

[task-description]
A given **number is valid**, if it is in the range [**100 … 200**] or it is **0**. Make a validation for an **invalid** number.
[/task-description]

[code-io /]
[/code-task]

## Sample Input and Output

| Input |   Output   |
|-------|------------|
|75     |invalid     |
|150    | (no output)|
|220    |invalid     |

## Solution

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-4-images/05.Invalid-number-01.png alt="Code" /]

## Testing in the Judge System

Test your solution here: [anchor href=https://judge.softuni.bg/Contests/Practice/Index/508#4]https://judge.softuni.bg/Contests/Practice/Index/508#4[/anchor].
[/slide]