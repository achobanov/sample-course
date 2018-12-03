[slide]
# Problem: Back to the Past

[code-task title="Back to the Past" executionStrategy="csharp-dot-net-core-code" requiresInput]

[code-editor language=csharp]
[/code-editor]

[task-description]
Ivancho is **18 years old** and receives an inheritance that consists of **X** money and **time machine**. He decides **to return to 1800**, but does not know **if money** will **be enough** to live without working. Write **a program that calculates** if Ivancho **will have enough money**  to not have to work until the given year. Assuming that **for every even** (1800, 1802, etc.) year he **will spend 12 000 dollars**. For **every odd** (1801, 1803, etc.) he will spend **12 000 + 50 * [the age he will have reached in the given year]**.
[/task-description]

[code-io /]
[/code-task]

## Input Data

The input is read from the console and **contains exactly 2 lines**:
- **Inherited money** – a real number in the range [**1.00 … 1 000 000.00**].
- **Year, until to live(inclusive)** – integer number in the range [**1801 … 1900**].

## Output Data

**Print** on the console **1 line**. **Sum** must be **formated** to the **second decimal point**:
  - If **money is enough**:
    - „**Yes! He will live a carefree life and will have {N} dollars left.**“ – when **N** is money, which will remain.
  - If **money is NOT enough**:
    - „**He will need {М} dollars to survive.**“ – where **M** is sum, which **is NOT enough**.

## Sample Input and Output
 
|       Input      |                                  Output                                   |  Explanations  |
|------------------|---------------------------------------------------------------------------|----------------|
| 50000<br>1802    | Yes! He will live a carefree life and<br> will have 13050.00 dollars left.| 1800 &rarr; **even**<br>&nbsp; &nbsp; &nbsp; &nbsp; &rarr; **Spend 12000** dollars<br>&nbsp; &nbsp; &nbsp; &nbsp; &rarr; Remain 50000 – 12000 = **38000**<br>1801 &rarr; **odd**<br>&nbsp; &nbsp; &nbsp; &nbsp; &rarr; **Spend** 12000 + **19*50** = 12950 dollars<br>&nbsp; &nbsp; &nbsp; &nbsp; &rarr; **Remain** 38000 – 12950 = **25050**<br>1802 &rarr;**even**<br>&nbsp; &nbsp; &nbsp; &nbsp; &rarr; **Spend** 12000 dollars<br>&nbsp; &nbsp; &nbsp; &nbsp; &rarr; **Remain** 25050 – 12000 = **13050** |
| 100000.15<br>1808| He will need 12399.85 dollars<br> to survive.                             | 1800 &rarr; **even**<br>&nbsp; &nbsp; &nbsp; &nbsp; &rarr; **Remain** 100000.15 – 12000 = **88000.15**<br>1801 &rarr; **odd**<br>&nbsp; &nbsp; &nbsp; &nbsp; &rarr; **Remain** 88000.15 – 12950 = **75050.15**<br>**…**<br>1808 &rarr; **odd** &rarr; -399.85 - 12000 = **-12399.85**<br>**12399.85 is not enough** |

### Reading the Input Data

The method to solve this task is no different than the previous ones, so we start **declaring and initializing** the necessary variables:

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-5-2-images/03.Back-to-the-past-01.png alt="Code" /]

In the condition is said, that the years of Ivancho are 18, so when declaring the variable `years` we assign it an initial value of **18**. We read the other variables from the console.

### Iterate Years

Using a `for` loop** , we will iterate through all years. We **start from 1800** – the year in that Ivancho returns, and we reach the **year until he must live**. We check in the loop if the current year is **even** or **odd**. We do this through **division with remainder** (`%`) by 2. If the year is **even**, we subtract from `heritage` **12000**, and if is **odd**, we subtract from `heritage` **12000 + 50 * (years)**.

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-5-2-images/03.Back-to-the-past-02.png alt="Code" /]

### Check Heritage and Print Output

Finally we need to print out the results by checking **if the `heritage` is enough to live without working or not. If `heritage` is **positive number** , we print: „`Yes! He will live a carefree life and will have {N} dollars left.`“, and if is **negative number** : „`He will need {М} dollars to survive.`“. Do not forget to format the sum to the second decimal point.

**Hint**: Consider using the `Math.Abs(…)` function when printing the output, if the heritage is not enough.

## Testing in the Judge System

Test your solution here: [anchor href=https://judge.softuni.bg/Contests/Practice/Index/511#2]https://judge.softuni.bg/Contests/Practice/Index/511#2[/anchor].
[/slide]