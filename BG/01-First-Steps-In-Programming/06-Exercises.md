[slide]
# Упражнения: първи стъпки в коденето

Добре дошли в упражненията. Сега ще напишем няколко конзолни програми, с които ще направим още няколко първи стъпки в програмирането, след което ще покажем как можем да програмираме нещо по-сложно - програми с графичен и уеб потребителски интерфейс.
[/slide]

[slide]
# Задача: конзолна програма “Expression”

Да се напише конзолна C# програма, която **пресмята** и **отпечатва** стойността на следния числен израз:

<p align="center"> (3522 + 52353) * 23 - (2336 * 501 + 23432 - 6743) * 3 </p>

[code-task title='Print out Hello World' executionStrategy='csharp-dot-net-core-code' requiresInput]
    [code-editor language=csharp]
        Console.WriteLine(...);
    [/code-editor]

    [code-task title='Print out Hello World' executionStrategy='csharp-dot-net-core-code' requiresInput-description]
        Забележка: **не е разрешено да се пресметне стойността предварително** (например с Windows Calculator).
    [/task-description]
[/task]

Забележка: **не е разрешено да се пресметне стойността предварително** (например с Windows Calculator).

## Насоки и подсказки

Правим **нов C# конзолен проект** с име "**Expression**".	Намираме метода **``static void Main(string[] args)``** и **влизаме в неговото тяло** между **`{`** и **`}`**. След това трябва да **напишем кода**, който да изчисли горния числен израз и да отпечата на конзолата стойността му. Подаваме горния числен израз в скобите на командата **``Console.WriteLine(…)``**:

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-BG/blob/master/assets/chapter-1-images/02.Expression-01.png alt="Expression" /]

Стартираме програмата с [**Ctrl+F5**] и проверяваме дали резултатът е същия като на картинката:

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-BG/blob/master/assets/chapter-1-images/02.Expression-02.png alt="Expression" /]

## Тестване в Judge системата

Тествайте решението си тук: [anchor href=https://judge.softuni.bg/Contests/Practice/Index/503#1]https://judge.softuni.bg/Contests/Practice/Index/503#1[/anchor]


[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-BG/blob/master/assets/chapter-1-images/02.Expression-03.png alt="Expression" /]
[/slide]

[slide]
# Задача: числата от 1 до 20

Да се напише C# конзолна програма, която **отпечатва числата от 1 до 20** на отделни редове на конзолата.

[code-task title='Print out Hello World' executionStrategy='csharp-dot-net-core-code' requiresInput]
    [code-editor language=csharp]
    [/code-editor]

    [code-task title='Print out Hello World' executionStrategy='csharp-dot-net-core-code' requiresInput-description]
        Опитайте да въведете грешно число, например "hello". Ще получите съобщение за грешка по време на изпълнение (exception). Това е нормално. По-късно ще разберем как можем да прихващаме такива грешки и да караме потребителят да въвежда число наново.
    [/task-description]
[/code-task]

## Насоки и подсказки

Създаваме **конзолно C# приложение** с име "**Nums1To20**":
[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-BG/blob/master/assets/chapter-1-images/03.Numbers-1-to-20-01.png alt="Numbers 1 to 20" /]

В **`static void Main()`** метода пишем 20 команди **``Console.WriteLine(…)``**, всяка на отделен ред, за да отпечатаме числата от 1 до 20 едно след друго. По-досетливите от вас, сигурно се питат дали няма по-умен начин. Спокойно, има, но за него по-късно.

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-BG/blob/master/assets/chapter-1-images/03.Numbers-1-to-20-02.png alt="Numbers 1 to 20" /]

Сега **стартираме програмата** и поверяваме дали резултатът е какъвто се очаква да бъде:

```
1
2
…
20
```

## Тестване в Judge системата

Тествайте решението си тук: [anchor href=https://judge.softuni.bg/Contests/Practice/Index/503#2]https://judge.softuni.bg/Contests/Practice/Index/503#2[/anchor].

Сега помислете дали може да напишем програмата по **по-умен начин**, така че да не повтаряме 20 пъти една и съща команда. Потърсете в Интернет информация за "**[anchor href=https://www.google.bg/search?q=for+loop+C%23&oq=for+loop+C%23]for loop C#[/anchor]**".
[/slide]

[slide]
# Задача: триъгълник от 55 звездички

Да се напише C# конзолна програма, която **отпечатва триъгълник от 55 звездички**, разположени на 10 реда:

```
*
**
***
****
*****
******
*******
********
*********
**********
```

[code-task title='Print out Hello World' executionStrategy='csharp-dot-net-core-code' requiresInput]
    [code-editor language=csharp]
        Console.WriteLine("*");
        Console.WriteLine("**");
        …
    [/code-editor]

    [code-task title='Print out Hello World' executionStrategy='csharp-dot-net-core-code' requiresInput-description]
        Опитайте да **подобрите решението**, така че да няма много повтарящи се команди. Може ли това да стане с **`for`** цикъл. Успяхте ли да намерите умно решение (например с цикъл) на предната задача? При тази задача може да се ползва нещо подобно, но малко по-сложно (два цикъла един в друг). Ако не успеете, няма проблем, ще учим цикли след няколко глави и ще си спомните за тази задача тогава.
    [/task-description]
[/task]

## Насоки и подсказки

Създаваме **ново конзолно C# приложение** с име "**TriangleOf55Stars**". В него трябва да напишем код, който печата триъгълника от звездички, например чрез 10 команди, като посочените по-долу:

```csharp
Console.WriteLine("*");
Console.WriteLine("**");
…
```

## Тестване в Judge системата

Тествайте решението си тук: [anchor href=https://judge.softuni.bg/Contests/Practice/Index/503#3]https://judge.softuni.bg/Contests/Practice/Index/503#3[/anchor].

Опитайте да **подобрите решението**, така че да няма много повтарящи се команди. Може ли това да стане с **`for`** цикъл. Успяхте ли да намерите умно решение (например с цикъл) на предната задача? При тази задача може да се ползва нещо подобно, но малко по-сложно (два цикъла един в друг). Ако не успеете, няма проблем, ще учим цикли след няколко глави и ще си спомните за тази задача тогава.
[/slide]

[slide]
# Задача: лице на правоъгълник

Да се напише C# програма, която **прочита** от конзолата **две числа a и b**, **пресмята** и **отпечатва** лицето на правоъгълник със страни **a** и **b**.

[code-task title='Print out Hello World' executionStrategy='csharp-dot-net-core-code' requiresInput]
    [code-editor language=csharp]
        var a = decimal.Parse(Console.ReadLine());
        var b = decimal.Parse(Console.ReadLine());

        // TODO: Calculate and print the area
    [/code-editor]

    [code-task title='Print out Hello World' executionStrategy='csharp-dot-net-core-code' requiresInput-description]
        Допишете програмата, за да пресмята лицето на правоъгълника и да го отпечата. Използвайте познатата ни вече команда **`Console.WriteLine()`** и й подайте в скобите произведението на числата **a** и **b**. В програмирането умножението се извършва с оператора **`*`**.
    [/task-description]
[/task]

## Примерен вход и изход

| a | b | area |
| :---: | :---: | :---: |
| 2 | 7 |  14  |
| 7 | 8 |  56  |
| 12 | 5 |  60  |

## Насоки и подсказки

Правим нова **конзолна C# програма**. За да **прочетем двете числа**, използваме следните две команди:

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-BG/blob/master/assets/chapter-1-images/05.Rectangle-area-01.png alt="Rectangle Area" /]

Остава да се допише програмата по-горе, за да пресмята лицето на правоъгълника и да го отпечата. Използвайте познатата ни вече команда **`Console.WriteLine()`** и й подайте в скобите произведението на числата **a** и **b**. В програмирането умножението се извършва с оператора **`*`**.

## Тествайте решението си

Тествайте решението си с няколко примера. Трябва да получите резултат, подобен на този (въвеждаме 2 и 7 като вход и програмата отпечатва като резултат 14 - тяхното произведение):

```
2
7
14
```

## Тестване в Judge системата

Тествайте решението си тук: [anchor href=https://judge.softuni.bg/Contests/Practice/Index/503#4]https://judge.softuni.bg/Contests/Practice/Index/503#4[/anchor].
[/slide]

[slide]
# \* Задача: квадрат от звездички

Да се напише C# конзолна програма, която **прочита** от конзолата **цяло положително число N** и **отпечатва** на конзолата **квадрат от N звездички**, като в примерите по-долу.

[code-task title='Print out Hello World' executionStrategy='csharp-dot-net-core-code' requiresInput]
    [code-editor language=csharp]
        var n = int.Parse(Console.ReadLine());

        // TODO: Draw square
    [/code-editor]

    [code-task title='Print out Hello World' executionStrategy='csharp-dot-net-core-code' requiresInput-description]
         Да се допише програмата, за да отпечатва квадрат, съставен от звездички. Може да се наложи да се използват **`for`** цикли. Потърсете информация в Интернет.
    [/task-description]
[/task]

## Примерен вход и изход

| Вход  |    Изход   	| Вход  |    Изход   	| Вход  |    Изход   	|
|-----|-----------|-----|-----------|-----|----------|
|  3  	|<code>\*\*\*</code><br><code>\*&nbsp;\*</code><br><code>\*\*\*</code>|  4  |<code>\*\*\*\*</code><br><code>\*&nbsp;&nbsp;\*</code><br><code>\*&nbsp;&nbsp;\*</code><br><code>\*\*\*\*</code>| 5  	|<code>\*\*\*\*\*</code><br><code>\*&nbsp;&nbsp;&nbsp;\*</code><br><code>\*&nbsp;&nbsp;&nbsp;\*</code><br><code>\*&nbsp;&nbsp;&nbsp;\*</code><br><code>\*\*\*\*\*</code>|

## Насоки и подсказки

Правим нова **конзолна C# програма**. За да прочетем числото N (2 ≤ N ≤100), използваме следния код:

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-BG/blob/master/assets/chapter-1-images/06.Square-of-stars-01.png alt="Square of stars" /]

Да се допише програмата по-горе, за да отпечатва квадрат, съставен от звездички. Може да се наложи да се използват **`for`** цикли. Потърсете информация в Интернет.

**Внимание**: тази задача е по-трудна от останалите и нарочно е дадена сега и е обозначена със звездичка, за да ви провокира да потърсите информация в Интернет. Това е едно от най-важните умения, което трябва да развивате докато учите програмирането: **да търсите информация в Интернет**. Това ще правите всеки ден, ако работите като програмисти, така че не се плашете, а се опитайте. Ако имате трудности, можете да потърсите помощ и в СофтУни форума: [anchor href=https://softuni.bg/forum]https://softuni.bg/forum[/anchor].

## Тестване в Judge системата

Тествайте решението си тук: [anchor href=https://judge.softuni.bg/Contests/Practice/Index/503#5]https://judge.softuni.bg/Contests/Practice/Index/503#5[/anchor].
[/slide]
