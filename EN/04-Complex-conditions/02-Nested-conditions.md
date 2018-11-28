[slide]
# Nested conditions

Pretty often the program logic inflicts the use of `if` or `if-else` statements, which are contained one inside the other. They are called **nested** `if` or `if-else` statements. As it implied from the title **"nested"**, these are `if` or `if-else` statements, which are placed inside other `if` or `else` statements.

```csharp
if (condition1)
{
    if (condition2)
    {
        // body; 
    }
    else
    {
        // body;
    }
}
```

The nesting of more than three conditional statements inside each other is not considered a good practice and has to be avoided, mostly through optimization of the structure/the algorithm of the code and/or through using another type of conditional statement, which we are going to see below in this chapter.
[/slide]

[slide]
# Example: personal titles

[code-task title="Personal Titles" executionStrategy="csharp-dot-net-core-code" requiresInput]

[code-editor language=csharp]
var age = double.Parse(Console.ReadLine());
var gender = Console.ReadLine();

if(age < 16)
{
    // TODO
}
else
{
    // TODO
}

[/code-editor]

[task-description]
Depending on **age** (decimal number and **gender** (**m** / **f**), print a personal title:
- “**Mr.**” – a man (gender “**m**”) - 16 or more years old.
- “**Master**” – a boy (gender “**m**”) under 16 years.
- “**Ms.**” – a woman (gender “**f**”) - 16 or more years old.
- “**Miss**” – a girl (gender “**f**”) under 16 years.
[/task-description]

[code-io /]
[/code-task]

## Sample Input and Output

| Input | Output |  Input  | Output |
|-------|--------|---------|--------|
|12<br>f|Miss    |17<br>m  |Mr.     |

| Input | Output |  Input  | Output |
|-------|--------|---------|--------|
|25<br>f|Ms.     |13.5<br>m|Master  |

## Solution

We can see, that the **output** from the program **depends on a few things**. **First** we have to check what is the entered **gender** and **then** to check the **age**. Respectively, we are going to use **a few** `if-else` blocks. These blocks will be **nested**, meaning from **the result** of the first, we are going to **define** which one of the **others** to execute.

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-4-images/01.Personal-titles-01.jpg alt="BLock Scheme" /]

After reading the input data from the console, the following program logic should be executed:

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-4-images/01.Personal-titles-02.png alt="Code" /]

## Testing in the Judge System

Test your solution here: [anchor href=https://judge.softuni.bg/Contests/Practice/Index/508#0]https://judge.softuni.bg/Contests/Practice/Index/508#0[/anchor].
[/slide]

[slide]
# Example: a small shop

[code-task title="Small Shop" executionStrategy="csharp-dot-net-core-code" requiresInput]

[code-editor language=csharp]
var product = Console.ReadLine().ToLower();
var town = Console.ReadLine().ToLower();
var quantity = double.Parse(Console.ReadLine());

if (town == "sofia")
{
    if (product == "coffee")
    {
        Console.WriteLine(0.50 * quantity);
    }
    // TODO
}

if (town == "varna")
{
    // TODO
}

// TODO
[/code-editor]

[task-description]
A Bulgarian enterpreneur opens a **small shop** in  **a few cities** with different **prices** for the following **products**:

|               product / city               |                   Sofia                |                  Plovdiv               |  Varna  |
|:------------------------------------------:|:--------------------------------------:|:--------------------------------------:|:-------:|
|coffee<br>water<br>beer<br>sweets<br>peanuts|0.50<br>0.80<br>1.20<br>1.45<br>1.60<br>|0.40<br>0.70<br>1.15<br>1.30<br>1.50<br>|0.45<br>0.70<br>1.10<br>1.35<br>1.55|

Calculate the price by the given **city** (string), **product** (string) and **quantity** (decimal number).
[/task-description]

[code-io /]
[/code-task]

## Sample Input and Output

|        Input       | Output |          Input        | Output |
|--------------------|--------|-----------------------|--------|
|coffee<br>Varna<br>2|0.9     |peanuts<br>Plovdiv<br>1|1.5     |

|       Input      | Output |        Input        | Output |
|------------------|--------|---------------------|--------|
|beer<br>Sofia<br>6|7.2     |water<br>Plovdiv<br>3|2.1     |

## Solution

We **convert** all of the letters in **lower register** with the function `.ToLower()`, to compare products and cities **no matter** what the letters - lower/upper are.

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-4-images/02.Small-shop-01.png alt="Code" /]

## Testing in the Judge System

Test your soluiton here: [anchor href=https://judge.softuni.bg/Contests/Practice/Index/508#1]https://judge.softuni.bg/Contests/Practice/Index/508#1[/anchor].
[/slide]