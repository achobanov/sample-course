[slide]
# Web application: sumator for numbers

Now we are going to write something even more complex, but also more interesting: a web application that **calculates the sum of two numbers**. By **entering two numbers** in the first two text fields and pressing the button [**Calculate**], **their sum is being calculated** and the result is shown in the third text field.

Pay attention that we are creating **a web-bsed application**. This is an application, which is available through a web browser, just like your favorite email or news website. The web application is going to have a server side (back-end), which is written with the language C# with the technology ASP.NET MVC and the client side (front-end), which is written with the language HTML (this is a language for visualization of information in a web browser). 
The web application is expected to look similar to the following:

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-1-images/08.Numbers-sum-web-01.png alt="Sumator" /]

In difference to the console applications, which read and write the data in the form of a text in the console,  web applications have **a web-based user interface**. Web applications **are being loaded from some Internet address** (URL) through a standart web browser. The users write an input data in a page, visualized from the web browser, the data is processed on a web server and the results are shown again in the page of the web browser. For our web application we are going to use **the technology ASP.NET MVC**, which allows the creating of **web applications with the programming language C#** in the environment for development **Visual Studio**.

## Create a new C# project

In Visual Studio we create **a new C# project of type „ASP.NET Web Application“** with name **WebApp**:

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-1-images/08.Numbers-sum-web-02.png alt="Visual Studio" /]

We choose **type** of the application - **“MVC”**:

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-1-images/08.Numbers-sum-web-03.png alt="Visual Studio" /]

## Create a web form

We find the file `Views\Home\Index.cshtml`. **The view (View) of the home page** of our web application is in it:

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-1-images/08.Numbers-sum-web-04.png alt="Visual Studio" /]
We delete the old code from **the file `Index.cshtml` and write the following code: 

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-1-images/08.Numbers-sum-web-05.png alt="Code" /]

This code **creates a web form with three text boxes and a button in it**. Inside the fields, values are being loaded, which are calculated previously in the object `ViewBag`. It is said that with the click of the button [**Calculate**] the action `/home/calculate` (action `calculate` from the `home` controller)** will be called.

Here is how **the file `Index.cshtml` is supposed to look after the change:

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-1-images/08.Numbers-sum-web-06.png alt="Visual Studio" /]

## Writing the code program code

It is left to write **the action** (Action), which **sums the numbers when clicking on the button** [**Calculate**]. We open the file `Controllers\HomeController.cs` and we add the following code into the body of `HomeController` class:

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-1-images/08.Numbers-sum-web-07.png alt="Code" /]

This code implements the action “**calculate**”. It takes two parameters `num1` and `num2` and records them in the objects `ViewBag`, after which **it calculates and records** their sum. The recorded in `ViewBag` values after that **are used from the view**, to be shown in the **three text fields** inside the form for summing number in the web page of the application.

Here is how **the file `HomeController.cs` should look after the change:

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-1-images/08.Numbers-sum-web-08.png alt="Visual Studio" /]

## Testing the application

The application is ready. We can start it with [**Ctrl + F5**] and test whether it works:

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-EN/blob/master/assets/chapter-1-images/08.Numbers-sum-web-09.png alt="Sumator" /]

Does it look scary? **Don't be afraid!** We have a lot more to learn, to reach the level of knowledge and skills to write web-based applications freely like in the example above and much bigger and much more complex ones. If you don't succeed, there is nothing to worry about, keep moving on. After some time you will remeber with a smile how incomprehensible and exsiting your first collision with web programming was. If you have problems with the example above, **watch the video** at the beginning of this chapter. The application is built live there, step by step with a lot of explanations. Or ask in [anchor href=https://softuni.bg/forum]forum of SoftUni[/anchor].

The purpose of both of the above examples (graphical desktop application and web application) is not to teach you, but to make you dive a little deeper into programming, **to enlighten your interest** towards software development and to inspire you to learn hard. **You have a lot to learn yet**, but it's interesting, isn't it?
[/slide]