[slide]
# Problem: graphical application „Sumator for numbers“

Write a **graphical (GUI) application**, which **calculates the sum of two numbers**:

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-1-images/07.Numbers-sum-01.png alt="Sumator" /]

By entering two numbers in the first two fields and pressing the button [**Calculate**] their sum is being calculated and the result is shown in the third text field. For our application we will use **the technology Windows Forms**, which allows the creation of **graphical applications for Windows**, in the environment for development **Visual Studio** and with programming **language** **C#**.

### Creating a new C# project

In Visual Studio we create **a new C# project of type „Windows Forms Application“**:

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-1-images/07.Numbers-sum-02.png alt="Visual Studio" /]

When creating a Windows Forms application **an editor for user interface** will be shown, in which **different visual elements** could be put (for example textboxes and buttons):

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-1-images/07.Numbers-sum-03.png alt="Visual Studio" /]

## Adding text fields and a button

We download from the bar on the left (Toolbox) **three text boxes** (`TextBox`), **two labels** (`Label`) and **a button** (`Button`), afterards we arrange them in the window of the application. After that we **chagne the names of each of the controls**. This is done from **the window “Properties”** on the right, by changing the field (`Name`):

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-1-images/07.Numbers-sum-04.png alt="Visual Studio" /]

-	Names of the text boxes: `textBox1`, `textBox2`, `textBoxSum`
-   Name of the button: `buttonCalculate`
-	Name of the form: `FormCalculate`

**We change the headings** (the `Text` property) of the controls:

-	buttonCalculate -> Calculate
-	label1 -> +
-	label2 -> =
-	Form1 -> Sumator

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-1-images/07.Numbers-sum-05.png alt="Visual Studio" /]

## Resizing the controls and starting the application

**We resize and arrange the controls**, to make them look better:

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-1-images/07.Numbers-sum-06.png alt="Visual Studio" /]

We try to run the application [**Ctrl + F5**]. It should start, but **not function completely**, because we haven't written what happens when we click the button yet.

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-1-images/07.Numbers-sum-07.png alt="Sumator" /]

## Writng the programming code

Now it is time to write the code, which **sums the numbers** from the first two fields and **shows the result** in the third field. For the purpose we click **twice the button [Calculate]**. The place, in which we write what is going to happen by clicking the button will be shown:

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-1-images/07.Numbers-sum-08.png alt="Visual Studio" /]

We write the following C# code between the opening and the closing brackets `{ }`, where the cursor is:

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-1-images/07.Numbers-sum-09.png alt="Visual Studio" /]

This code **takes the first number** from the field `textBox1` and keeps it **in the variable `num1`, keeps **the second number** from the field `textBox2` in **the vriable `num2`, afterwards it **sums `num1` and `num2` in the variable `sum` and in the end **takes the text value of the variable `sum` in the field `textBoxSum`.

## Testing the application

We start the program again with [**Ctrl+F5**] and we check   whether it works correctly. We try to calculate **4 + 5**, and afterwards **-12.5 + 1.3**:

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-1-images/07.Numbers-sum-10.png alt="Sumator" /] [image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-1-images/07.Numbers-sum-11.png alt="Sumator" /]

We try with **ivalid numbers**, for example: “**aaa**” and “**bbb**”. It seems there is a problem: 

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-1-images/07.Numbers-sum-12.png alt="Sumator" /] [image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-1-images/07.Numbers-sum-13.png alt="Sumator" /]

## Solving the problem and re-testing the application

The problem comes from **the conversion of the text field into a number**. If the value inside the field **is not a number, the program throws an exception**. We can rewrite the code in order to fix this problem:

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-1-images/07.Numbers-sum-14.png alt="Code" /]

The code above **catches the errors when working with numbers** (it catches exceptions) and in case of an error **it gives a value `error` in the field with the result . We start the program again with [**Ctrl+F5**] and try if it works. This time **by entering a wrong number the result is `error` and the program doesn't break:

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-1-images/07.Numbers-sum-15.png alt="Sumator" /] [image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-1-images/07.Numbers-sum-16.png alt="Sumator" /]

Is it complicated? It is normal to seem complex, of course. We are just beginning to get into programming. The example above requires much more knowledge and skills, which we are going to develop through this book and even afterwards. Just allow yourself to have some fun with desktop programming. If something doesn't work, watch **the video in the beginning of this chapter** or ask in the [anchor href=https://softuni.bg/forum]forum of SoftUni[/anchor]. Or move on bravely forward to the next example or to the next chapter of the book. A time will come when it is going to be easy for you, but you really have to put **an effort and persistence**. Programming is learnt slowly with lots and lots of practice.
[/slide]