[slide]
# Graphical Applications with Numerical Expressions

To exercise working with variables and calculations with operators and numerical expressions, we will make something interesting: we will develop a **desktop application** with graphical user interface. In it, we will use calculations with floating-point numbers.

## Graphical application: converter from BGN to EUR

It is expected of us to create **a graphical application** (GUI application), which calculates the value in **euro** (EUR) of money amount, given in **leva** (BGN). By changing the amount in leva, the amount in euro has to recalculate itself automatically (we use rate leva / euro: **1.95583**).

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-2-images/13.Currency-converter-01.png alt="BGN to EUR Converter App" /]

This exercise goes beyond the material learned in this book and its purpose is not to teach you how to program GUI applications, but to enlighten your interest in software development. Let's get to work.

### Creating a new C# project

We add to the existing Visual Studio solution one more project. This time we creatе **Windows Forms** application with C# named "BGN-to-EUR-Converter":

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-2-images/13.Currency-converter-02.png alt="Create New Project" /]

### Adding controls

We arrange the following UI controls in the format: 

- `NumericUpDown` with name `numericUpDownAmount` – it will enter the amount for conversion
- `Label` with name `labelResult` – it will show the result after conversion
- Two more `Label` components, serving only for static representation of a text

The graphical editor for user interface might look similar to this:
[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-2-images/13.Currency-converter-03.png alt="Graphical UI Editor" /] 

We set the following settings of the format and the separate controls:

|                                             Setting                                                 | Picture |
|:---------------------------------------------------------------------------------------------------:|:-------:|
|`FormConverter`:<br>Text = "BGN to EUR",<br>Font.Size = 12,<br>MaximizeBox = False,<br>MinimizeBox = False,<br>FormBorderStyle = FixedSingle | [image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-2-images/13.Currency-converter-04.png alt="Form Converter" /]  |
|`numericUpDownAmount`:<br>Value = 1,<br>Minimum = 0,<br>Maximum = 10000000,<br>TextAlign = Right,<br>DecimalPlaces = 2 | [image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-2-images/13.Currency-converter-05.png  alt="Numeric Up Down" /] |
|`labelResult`:<br>AutoSize = False,<br>BackColor = PaleGreen,<br>TextAlign = MiddleCenter,<br>Font.Size = 14,<br>Font.Bold = True| [image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-2-images/13.Currency-converter-06.png alt="Label Result" / |

### Events and eventhandlers

We difine the following **eventhandlers** in the controls:

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-2-images/13.Currency-converter-07.png alt="EventHandler" /] 

After this we catch the following events:
- `FormConverter.Load` (by clicking on the form twice with the mouse)
- `numericUpDownAmount.ValueChanged` (by clicking on `NumericUpDown` control twice)
- `numericUpDownAmount.KeyUp` (we choose `Events` from the dashboard `Properties` and click twice on `KeyUp`)

The event `Form.Load` is executed when the program is started, before the window of the application is shown. The event `NumericUpDown.ValueChanged` is executed when a change in the value inside the field for entering a number occurs. The event `NumericUpDown.KeyUp` is executed after pressing a key in the field that enters a number. On the occurance of each of these events, we will recalculate the result.

To **catch an event** we use the events icon (Events) in the **Properties**  window in Visual Studio:

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-2-images/13.Currency-converter-08.png alt="Events in Visual Studio" /] 
[/slide]

### Writing the program code and testing the application

We will use the following **C# code** for handling events:

```csharp
private void FormConverter_Load(object sender, EventArgs e)
{
    ConvertCurrency();
}

private void numericUpDownAmount_ValueChanged(object sender, EventArgs e)
{
    ConvertCurrency();
}

private void numericUpDownAmount_KeyUp(object sender, KeyEventArgs e)
{
    ConvertCurrency();
}
```

All of the caught events call out the method `ConvertCurrency()`, which converts the given sum from levs to euro and shows the result int the green box.

We have to wrtite the **code** (program logic) for converting from levs to euro: 

```csharp
private void ConvertCurrency()
{
    var amountBGN = this.numericUpDownAmount.Value;
    var amountEUR = amountBGN * 1.95583m;
    this.labelResult.Text = 
    amountBGN + " BGN = " + 
    Math.Round(amountEUR, 2) + " EUR";
}
```

In the end **we start the project** with [**Ctrl + F5**] and test if it works correctly.

If you have any problems with the example above, **watch the video** in the begging of this chapter. There, the application is being built live, step by step, with a lot of explanations. Or ask a question in the [anchor href=https://softuni.bg/forum]**forum of SoftUni**[/anchor].
[/slide]

[slide]
# Graphical application: \*\*\* Catch the button!

Create a fun graphical application **„catch the button“**: a form consisting of one button. By moving the mouse cursor onto the button, it moves on random position. This way it creates the impression that **„the button runs form the mouse and it is hard to catch"**. When the button gets „caught“, a congratulations message is shown.

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-2-images/14.Catch-the-button-01.png alt="Catch the Button App" /]

**Hint**: write an eventhandler `Button.MouseEnter` and move the button on random position. Use the generator for random numbers `Random`. The position of the button is set from the property `Location`. To make sure the new position of the button is in the form's borders, you can make calculations based on the size of the form, which is available from the `ClientSize` property. You may use the following sample code:

```csharp
private void buttonCatchMe_MouseEnter(object sender, EventArgs e)
{
    Random rand = new Random();
    var maxWidth = this.ClientSize.Width - buttonCatchMe.ClientSize.Width;
    var maxHeight = this.ClientSize.Height - buttonCatchMe.ClientSize.Height;
    this.buttonCatchMe.Location = new Point(
        rand.Next(maxWidth), rand.Next(maxHeight));
}
```
[/slide]