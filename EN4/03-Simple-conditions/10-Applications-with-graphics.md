[slide]
# Graphical (desktop) application: currency converter

After we've done some exercises on **conditional statements (checks)**, now let's do something more interesting: an application with a graphical user interface for converting currencies. We will use the knowledge from this chapter to choose from several available currencies and make calculations at different rate to the selected currency.

Now let's see how to create a graphical (**GUI**) app for **currency conversion**. The app will look like the picture below:

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-3-images/14.Converter-01.png alt="Currency Converter" /]
[/slide]

[slide]
# Create a new C # project and add controls

This time we create a new **Windows Forms Application** with name “Currency-Converter”:

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-3-images/14.Converter-02.png alt="New Project" /]

**We order the following controls** in the form:
- One box for entering a number (`NumericUpDown`)
- One drop-down list with currencies (`ComboBox`)
- Text block for the result (`Label`) 
- Several inscriptions (`Label`)

We set the **sizes** and their properties to look like the picture below:
 
[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-3-images/14.Converter-03.png alt="Controls" /]
[/slide]

[slide]
# Configuring the controls

We set the **configuring controls**:

- **For the main form** (`Form`), that contains all the controls:
  - `(name)` = `FormConverter`
  - `Text` = "`Currency Converter`"
  - `Font.Size` = `12`
  - `MaximizeBox` = `False`
  - `MinimizeBox` = `False`
  - `FormBorderStyle` = `FixedSingle`
<br>

- For the **field for entering a number** (`NumericUpDown`):
  - `(name)` = `numericUpDownAmount`
  - `Value` = `1`
  - `Minimum` = `0`
  - `Maximum` = `1000000`
  - `TextAlign` = `Right`
  - `DecimalPlaces` = `2`
<br>  

- For the **drop-down list with currencies** (`ComboBox`):
  - `(name)` = `comboBoxCurrency`
  - `DropDownStyle` = `DropDownList`
  - `Items` =
    - **EUR**
    - **USD**
    - **GBP**
<br> 

- For the **result text block** (`Label`):
  - `(name)` = `labelResult`
  - `AutoSize` = `False`
  - `BackColor` = `PaleGreen`
  - `TextAlign` = `MiddleCenter`
  - `Font.Size` = `14`
  - `Font.Bold` = `True`
[/slide]

[slide]
# Events and eventhandlers

We need to take the following **events** to write the C # code that will be executed upon their occurrence:

- The Event `ValueChanged` of numeric entry control `numericUpDownAmount`:

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-3-images/14.Converter-04.png alt="Events" /]

- The event `Load` of the form `FormConverter`
- The event `SelectedIndexChanged` of the drop-down list for choosing the currency `comboBoxCurrency`
  
We will use the following **C# code** for event handling:

```csharp
private void FormConverter_Load(object sender, EventArgs e)
{
    this.comboBoxCurrency.SelectedItem = "EUR";
}
        
private void numericUpDownAmount_ValueChanged(object sender, EventArgs e)
{
    ConvertCurrency();
}
        
private void comboBoxCurrency_SelectedIndexChanged(object sender, EventArgs e)
{
    ConvertCurrency();
}
```

Our task is to select the currency "**EUR**" when we start the program and change the values in the sum or currency field then calculate the result by calling the `ConvertCurrency()` method.
[/slide]

[slide]
# Writing the code

We have to write the event `ConvertCurrency()` to convert the amount of levs in the selected currency:

```csharp
private void ConvertCurrency()
{
    var originalAmount = this.numericUpDownAmount.Value;
    var convertedAmount = originalAmount;

    if (this.comboBoxCurrency.SelectedItem.ToString() == "EUR")
    {
        convertedAmount = originalAmount / 1.95583m;
    }
    else if (this.comboBoxCurrency.SelectedItem.ToString() == "USD")
    {
        convertedAmount = originalAmount / 1.80810m;
    }
    else if (this.comboBoxCurrency.SelectedItem.ToString() == "GBP")
    {
        convertedAmount = originalAmount / 2.54990m;
    }

    this.labelResult.Text = originalAmount + " лв. = " +
    Math.Round(convertedAmount, 2) + " " + this.comboBoxCurrency.SelectedItem;
}
```

The above code takes **the amount** for convert from the field `numericUpDownAmount` and **the selected currency** for the result from the field `comboBoxCurrency`. Then with a **conditional statement**, according to the selected currency, the amount is divided by **the exchange rate** (which is fixed in the source code). Finally, a text **message with the result** (rounded to second digit after the decimal point) is generated and recorded in the green box `labelResult`. Try it!

If you have problems with the example above, **watch the video** at the beginning of this chapter or ask in the [anchor href=https://softuni.bg/forum]**forum of SoftUni**[/anchor].
[/slide]