[slide]
# Problem: Smart Lily

[code-task title="Smart Lily" executionStrategy="csharp-dot-net-core-code" requiresInput]

[code-editor language=csharp]
[/code-editor]

[task-description]
Lily is **N years** old. For each **birthday** she receives a gift. For the **odd** birthdays (1, 3, 5, …, n) she receives **toys**, and for every **even** (2, 4, 6, …, n) she receives **money**. For her **second birthday** she receives **10.00 BGN**, and **the amount is increased by 10.00 BGN for every even birthday** (2 -> 10, 4 -> 20, 6 -> 30 etc.). Over the years Lily has secretly saved her money. Lily's **brother** ,in the years, when she **receives money**, **takes 1.00 BGN** from them. Lily **has sold the toys**, received over the years, **every for P BGN** and added the sum to the amount of saved money. With the money she wanted to **buy a washing machine for X BGN**. Write a program, that calculates **how much money she has saved** and if it is enough **to buy a washing machine**.
[/task-description]

[code-io /]
[/code-task]

## Input Data

We read from the console **3 numbers**, each on separate line:

- **Age** of Lily – **integer number** in range [**1 … 77**].
- **Price of the washing machine** – number in range [**1.00 … 10 000.00**].
- **Unit price of toy** – **integer number** in range [**0 … 40**].

## Output Data

Print on the console one single line:

  - If Lily's money is enough:
    - “**Yes! {N}**” – where **N** is the remaining money after the purchase
  - If money is not enough:
    - “**No! {M}**” – where **M** is the insufficiency amount
    - Numbers **N** and **M** must be **formatted to the second place after decimal point**.

## Sample Input and Output

|        Input       |     Output    |  Comments  |
|--------------------|---------------|------------|
| 10<br>170.00<br>6  | Yes!<br>5.00  | **First birthday** gets **toy**; **2nd** -> 10 BGN; **3th** -> toy; **4th** -> 10 + 10 = 20 BGN.; **5th** -> toy; **6th** -> 20 + 10 = 30 BGN; **7th** -> toy; **8th** -> 30 + 10 = 40 BGN; **9th** -> toy; 10th -> 40 + 10 = 50 .<br>She has **saved** -> 10 + 20 + 30 + 40 + 50 = **150 BGN**. She **sold 5 toys** 6 BGN each = **30 BGN**.<br>**Her brother took** 1 BGN 5 times = **5 BGN**. **Remain** -> 150 + 30 – 5 = **175 BGN**. **175 >= 170** (price of the washing machine) **she managed to buy** it and has **left** 175-170 = **5 BGN**. |
| 21<br>1570.98<br>3 | No!<br>997.98 | She has **saved 550 BGN**. She has **sold 11 toys** 3 BGN each = **33 BGN**. **Her brother** for 10 years, **has taken** 1 BGN each year = **10 BGN**. **Remain** 550 + 33 – 10 = **573 BGN**.<br>**573 < 1570.98** – **She did not managed to buy** a washing machine. The **insufficiency amount** is 1570.98–573 = **997.98 BGN**.|

### Reading the Input Data

The solution of this problem,like the previous one can also be splited into three parts – **reading** input data , **processing** and **outputting** the result.

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-5-2-images/02.Smart-lilly-01.png alt="Code" /]

We start again with the choice of appropriate **data types** and names of the variables. For the Lilly's years (`age`) and the unit price of the toy (`presentPrice`) in the description is given, that they will be **integer numbers**. That's why we will use `int` type**. For the price of the washing machine (`priceOfWashingMachine`) we know, that it is **real number and we choose `double`. Of course, we can skip the explicit specification of type, by using `var`. In the above code we **declare** and **initialize** (assign value) the variables.

### Creating Helper Variables

To solve the problem we will need several helper variables – for the **count of toys** (`numberOfToys`),for the **saved money** (`savedMoney`) and for the  **money, received on each birthday** (`moneyForBirthday`). The initial value of  `moneyForBirthday` is 10, because in the description is given, that the first sum, which Lily gets, is 10 lv:

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-5-2-images/02.Smart-lilly-02.png alt="Code" /]

### Calculating Saved Money

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-5-2-images/02.Smart-lilly-03.png alt="Code" /]

With `for` loop** we iterate through every Lily's birthday. When the leading variable is **even  number**, that means Lily **has received money** and we add this money to her total savings. At the same time we **subtract 1 lev** - the money , that her brother takes. Then we **increase** the value of the variable `moneyForBirthday`, ie. we increase by 10 the sum, which she will receive on her next birthday. Iversely, when the leading variable is **odd number**, we increase the count of **toys**. We do the parity check by **division with remainder** (`%`) **by 2** - when the remainder is 0, the figure is even, and the remainder 1 is odd.

We also add the money from the sold toys to the Lily's savings.

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-5-2-images/02.Smart-lilly-04.png alt="Code" /]

### Formating and Printing The Output

Finally we need to print the received results, taking into account the formating specified in the description, i.e. sum needs to be  **rounded to 2 places after the decimal point**:

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-5-2-images/02.Smart-lilly-05.png alt="Code" /]

In this case we choose to use the **conditional operator (`?:`)** (also called ternary operator), because the recording is shorter. Its syntax is as follows: `operand1 ? operand2 : operand3`. First operand need to be **boolean type** (i.e to return `true/false`). If `operand1` returns `true`, will be executed `operand2`, and if it returns `false` – `operand3`. In our case we check if the **saved money** from Lily is enough for a washing machine. If they are more than or equal to the price of washing machine, the check `savedMoney >= priceOfWashingMachine` will return `true` and will print  „**Yes! …**“, and if is less – the result will be `false` and will print “**No! …**”. Of course, instead of conditional operand, we can use `if` checks.

More about the conditional operator: [anchor href=https://www.dotnetperls.com/ternary]https://www.dotnetperls.com/ternary[/anchor], [anchor href=https://msdn.microsoft.com/en-us/library/ty67wk28.aspx]https://msdn.microsoft.com/en-us/library/ty67wk28.aspx[/anchor].

## Testing in the Judge System

Test your solution here: [anchor href=https://judge.softuni.bg/Contests/Practice/Index/511#1]https://judge.softuni.bg/Contests/Practice/Index/511#1[/anchor].
[/slide]