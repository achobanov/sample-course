[slide]
# Problem: Logistics

[code-task title="Logistics" executionStrategy="csharp-dot-net-core-code" requiresInput]

[code-editor language=csharp]
[/code-editor]

[task-description]
You are responsible for the logistics of different cargos. **Depending on the weight** of each load is needed **different vehicle** and costs **different price per tonne**:

- Up to **3 tonnes** – **minibus** (200 BGN per tonne).
- From **over 3 and up to 11 tonnes** – **truck** (175 BGN per tonne).
- **Over 11 tonnes – train** (120 BGN per tonne).

Your task is to calculate **the average price per tonne of the cargo**, and also **how much percent of the cargo is transported in each vehicle**.
[/task-description]

[code-io /]
[/code-task]

## Input Data

From the console is read **sequence of numbers**, each on separate line:
- **First line**: **count of the cargos** for carriage – **integer number** in range [**1 … 1000**].
- On the next lines is given **the tonnage of the current cargo** – **integer number** in range [**1 … 1000**].

## Output Data

Print on the console **4 lines**, as follows:
- **Line #1** – **the average price per tonne of the cargo** (rounded to the second place after the decimal point).
- **Line #2** – **percent** of the cargo, carried by **minibus** (between 0.00% and 100.00%, rounded to the second place after the decimal point).
- **Line #3** – **percent** of the cargo, carried by **truck** (between 0.00% and 100.00%).
- **Line #4** – **percent** of the cargo, carried by **train** (between 0.00% and 100.00%).
 
## Sample Input and Output

|         Input          |                Output               |  Explanations  |
|------------------------|-------------------------------------|----------------|
| 4<br>1<br>5<br>16<br>3 | 143.80<br>16.00%<br>20.00%<br>64.00%| By **minibus** are transported two of the cargos **1** + **3**, total **4** tonnes.<br> By **truck** is transportde one of the cargos: **5** tonnes.<br> By **train** is transported one of the cargos: **16** tonnes.<br> **Sum** of all cargos is: 1 + 5 + 16 + 3 = **25** tonnes.<br> Percent of the cargo **by minibus**: 4/25\*100 = **16.00%**<br> Percent of the cargo **by truck**: 5/25*100 = **20.00%**<br> Percent of the cargo **by train**: 16/25*100 = **64.00%**<br> **Average price** per tonne of carried cargo: (4 * 200 + 5 * 175 + 16 * 120) / 25 = **143.80** |

|            Input             |                Output               |           Input           |               Output               |
|------------------------------|-------------------------------------|---------------------------|------------------------------------|
| 5<br>2<br>10<br>20<br>1<br>7 | 140.38<br>7.50%<br>42.50%<br>50.00% | 4<br>53<br>7<br>56<br>999 | 120.35<br>0.00%<br>0.63%<br>99.37% |

## Hints and Guidelines

First **we will read the weigth of every cargo** and **sum** how much tonnes are being transported by **minibus**, **truck** and **train** and we will calculate **total tonnes** of the transported cargos. We will calculate **prices for every type of transport** according to the  transported tonnes and the **total price**. Finally we will calculate and print **the total average price per tonne** and **how much of the cargo is being transported by different types of transport in percents**.

We declare the needed variables, For Example: `countOfLoads` – count of  the cargos for transportation (we read them from the console), `sumOfTons` – sum of the tonnage of all cargos, `microbusTons`, `truckTons`, `trainTons` – variables that keeps the sum of the cargo tonnage , transported by minibus, truck and train.

We sill need `for` loop** from `0` to `countOfLoads-1`, to iterate through all the cargos. For every cargo **we read its weight** (in tonnes) from the console and save it in а variable, for example `tons`. We add to the tonnage sum of all cargos (`sumOfTons`) weight of the current cargo (`tons`). Once we have read the weight of the current cargo **we need to determine which vehicle type will be used** (minibus, truck or train). For this we will need `if-else` checks:

- If the value of the variable `tons` is **less than 3**, increase the value of `microbusTons` with the value of `tons`:
 
   ```csharp
   microbusTons += tons;
   ```
   
- Otherwise, if the value `tons` is **less than 11**, increase `truckTons` with `tons`.
- If `tons` is **more than 11**, increase `trainTons` with `tons`.

Before we print the output  we need to  **calculate percentages of the tonnes, transported by each vehicle** and **average price per tonne**. For the average price per tonne we will declare one more helper variable `totalPrice`, in which we will **sum total price of all transported cargos** (by minibus, truck and train). We will receive average price, by dividing `totalPrice` of `sumOfTons`. You need **to calculate by yourself** percentages of tonnes, transported by each vehicle, and print the results, keeping the specified format in the description.

## Testing in the Judge System

Test your solution here: [anchor href=https://judge.softuni.bg/Contests/Practice/Index/511#5]https://judge.softuni.bg/Contests/Practice/Index/511#5[/anchor].
[/slide]