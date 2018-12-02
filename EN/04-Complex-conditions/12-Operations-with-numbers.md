[slide]
# Problem: Operations with Numbers

[code-task title="Operations with Numbers" executionStrategy="csharp-dot-net-core-code" requiresInput]

[code-editor language=csharp]
[/code-editor]

[task-description]
Write a program that reads **two integers (n1 and n2)** and an **operator** that performs a particular **mathematical operation** with them. Possible operations are: **summing up** (`+`), **subtraction** (`-`), **multiplying** (`*`), **division** (`/`) and **modular division** (`%`). Upon summing up, subtracting and multiplying, the console must print the result and display whether it is **even** or **odd** number. Upon regular division – **just the result**, and upon modular division – **the remainder**. You need to take into consideration the fact that **the divisor can be equal to zero** (`= 0`), and dividing by zero is not possible. In this case, a **special notification** must be printed.
[/task-description]

[code-io /]
[/code-task]

## Input Data

**3 rows** are read from the console:

- **N1** – **integer** within the range [**0 … 40 000**].
- **N2** – **integer** within the range [**0 … 40 000**].
- **Operator** – **one character** among: "**+**", "**-**", "**\***", "**/**", "**%**".

## Output Data

Print **one row** in the console:

- If the operation is **summing up**, **subtraction** or **multiplying**:
  - **"{N1} {operator} {N2} = {output} – {even/odd}"**.
- If the operation is **division**:
  - **"{N1} / {N2} = {output}"** – the result is **formatted** up **to the second digit after the decimal point**.
- If the operation is **modular division**:
  - **"{N1} % {N2} = {remainder}"**.
- In case of **dividing by 0 (zero)**:
  - **"Cannot divide {N1} by zero"**.

## Sample Input and Output

|     Input     |     Output     |    Input    |         Output          |
|---------------|----------------|-------------|-------------------------|
|123<br>12<br>/ |123 / 12 = 10.25|112<br>0<br>/|Cannot divide 112 by zero|
|10<br>3<br>%   |10 % 3 = 1      |10<br>0<br>% |Cannot divide 10 by zero |

|     Input    |       Output      |
|--------------|-------------------|
|10<br>12<br>+ |10 + 12 = 22 - even|
|10<br>1<br>-  |10 - 1 = 9 - odd   |
|7<br>3<br>\*  |7 * 3 = 21 - odd   |

## Tips and Tricks

The problem is not complex, but there are a lot of code rows to write.

### Processing the Input Data

Upon reading the requirements, we understand that we expect **three** rows of input data. The first **two** rows pass **integers** (within the specified range), and the third row - **an arithmetical symbol**. 

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-4-2-images/03.Operations-01.png alt="Code" /]

### Condition for 0

Let's create and initialize the variables needed for the logic and calculations. In one variable we will store **the calculations output**, and the other one we will use for the **final output** of the program.

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-4-2-images/03.Operations-02.png alt="Code" /]

When carefully reading the requirements, we understand that there are cases where we don't need to do **any** calculations, and simply display a result.

Therefore, we can first check if the second number is `0` (zero), as well as whether the operation is **division** or **modular division**, and then initialize the output.

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-4-2-images/03.Operations-03.png alt="Code" /]

Let's place the output as a value upon initializing the `output` parameter. This way we can apply **only one condition** - whether it is needed to **recalculate** or **replace** this output. 

Based on the approach that we choose, our next condition will be either a simple `else` or a single `if`. In the body of this condition, using additional conditions regarding the manner of calculating the output based on the passed operator, we can separate the logic based on the **structure** of the expected **output**. 

### Condition for Division and Modular Division

From the requirements we can see that for **summing up** (`+`), **subtraction** (`-`) or **multiplying** (`*`) the expected output has the same structure: **"{n1} {operator} {n2} = {output} – {even/odd}"**, whereas for **division** (`/`) and **modular division** (`%`) the output has a different structure.

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-4-2-images/03.Operations-04.png alt="Code" /]

### Condition for Summing Up, Subtraction and Multiplying

We finish the solution by applying conditions for summing up, subtraction and multiplying:

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-4-2-images/03.Operations-05.png alt="Code" /]

For short and clear conditions, such as the above example for even and odd number, you can use a **ternary operator**. Let's examine the possibility to apply a condition **with** or **without** a ternary operator.

### Using Ternary Operator

**Without using a ternary operator** the code is longer but easier to read:

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-4-2-images/03.Operations-06.png alt="Code" /]

**Upon using a ternary operator** the code is much shorter but may require additional efforts to read and understand the logic:

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-4-2-images/03.Operations-07.png alt="Code" /]

### Printing the Output

Finally, what remains is to print the calculated result in the console:

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-4-2-images/03.Operations-08.png alt="Code" /]

## Testing in the Judge System

Test your solution here: [anchor href=https://judge.softuni.bg/Contests/Practice/Index/509#2]https://judge.softuni.bg/Contests/Practice/Index/509#2[/anchor].
[/slide]