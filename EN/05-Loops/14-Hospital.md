[slide]
# Problem: Hospital

[code-task title="Hospital" executionStrategy="csharp-dot-net-core-code" requiresInput]

[code-editor language=csharp]
[/code-editor]

[task-description]
For a certain period of time, patients arrive at the hospital each day for a treatment. It has **initially 7 doctors**. Every doctor can treat only **one pacient per day**, but sometimes there is a shortage of doctors, so the **remaining patients are sent to other hospotals**. **Every third day** the hospital makes calculations and  **if count of untreated patients is greater than the count of treated, another doctor is appointed**. Appointment takes place before the daily patient intake begins.

Write a program, that calculates **for the given period of time count of treated and untreated patients**.
[/task-description]

[code-io /]
[/code-task]

## Input Data

Input is read from the **console** and contains:

- On the first line – **The period**, for which you need to make calculations. **Integer number** in range [**1 … 1000**].
- On the next lines (equals to the count of days) – **count of the patients**, who arrive for treatment for the **current day**. Integer number in range [**0 … 10 000**].

## Output Data

Print **on the console 2 lines**:

- On the **first line**: “**Treated patients: {count of treated patients}.**”
- On the **second line**: “**Untreated patients: {count of untreated patients}.**”

## Sample Input and Output

|          Input         |                        Output                     |  Comments  |
|------------------------|---------------------------------------------------|------------|
| 4<br>7<br>27<br>9<br>1 | Treated patients: 23.<br>Untreated patients: 21.  | **1 day**>: 7 treated and 0 untreated patients for the day<br>**2 day**: 7 treated and 20 untreated patients for the day<br>**3 day**: By this moment the treated patiens are 14,<br> and untreated – 20 –> Appointed new doctor.<br>–> 8 treated and 1 untreated patient for the day<br>**4 day**: 1 treated and 0 untreated patients for the day<br>**Total**: **23 treated** and **21 untreated patiens.**|

|                Input                 |                        Output                     |  
|--------------------------------------|---------------------------------------------------|
| 6<br>25<br>25<br>25<br>25<br>25<br>2 | Treated patients: 40.<br>Untreated patients: 87.  | 
| 3<br>7<br>7<br>7                     | Treated patients: 21.<br>Untreated patients: 0.   |

### Reading the Input Data

Again, we begin by **declaring and initializing** the necessary variables:

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-5-2-images/04.Hospital-01.png alt="Code" /]

The period in which we have to make the calculations is read from the console and saved in the `period` variable. We will also need some helping variables: the number of treated patients (`treatedPatients`), the number of untreated patients (`untreatedPatients`) and the number of doctors (`countOfDoctors`), which is initially 7. 

### Calculating treated and untreated patients

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-5-2-images/04.Hospital-02.png alt="Code" /]

With the help of `for` loop** we iterate through all days in the given period (`period`). For every day we read from the console the count of the patients (`currentPatients`). Increasing doctors by condition can be done **every third day**, **BUT** only if the count of untreated patients is **greater** than the count of treated. For this purpose, we check if the day is third - with the arithmetical operator for division with remainder (`%`): `day % 3 == 0`.

For Example:
- If the day is **third**, remainder of the division by **3** will be **0** (`3 % 3 = 0`) and the check `day % 3 == 0` will return `true`.
- If the day is **second**, remainder of the division by **3** will be **2** (`2 % 3 = 2`) and the check will return `false`.
- If the day is **forth**, remainder of the division will be **1** (`4 % 3 = 1`) and the check will return again `false`.

If `day % 3 == 0` return `true`, it will be checked whether the count of untreated patients is greater than the count of treated: `untreatedPatients > treatedPatients`. If the result is again `true`, then the count of doctors will be increased (`countOfDoctors`).

Then we check if the count of the patients for the day (`currentPatients`) is greater than the count of doctors (`countOfDoctors`). If the count of the patiens is **greater**:
- Increase value of the variable `treatedPatients` with the count of doctors (`countOfDoctors`).
- Increase value of the variable `untreatеdPatients` with the count of the remaining patients, which we calculate, by subtracting count of  doctors from count of patients (`currentPatients - countOfDoctors`).
 
If the count of patients **is not greater**, increase only the variable `treatedPatients` with the count of patients for the day (`currentPatients`).

Finally we need to print the count of treated and count of untreated patients.

## Testing in the Judge System

Test your solution here: [anchor href=https://judge.softuni.bg/Contests/Practice/Index/511#3]https://judge.softuni.bg/Contests/Practice/Index/511#3[/anchor].
[/slide]