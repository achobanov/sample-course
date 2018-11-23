[slide]
# Как да напишем конзолна програма?

Нека преминем през **стъпките за създаване и изпълнение на компютърна програма**, която чете и пише своите данни от и на текстова конзола (прозорец за въвеждане и извеждане на текст). Такива програми се наричат "**конзолни**". Преди това, обаче, трябва първо да си **инсталираме и подготвим средата за разработка**, в която ще пишем и изпълняваме C# програмите от тази книга и упражненията към нея.
[/slide]

[slide]
# Среда за разработка (IDE)

Както вече стана дума, за да програмираме ни е нужна **среда за разработка** - **Integrated Development Environment** (IDE). Това е всъщност редактор за програми, в който пишем програмния код и можем да го компилираме и изпълняваме, да виждаме грешките, да ги поправяме и да стартираме програмата отново.
- За програмиране на C# използваме средата **Visual Studio** за операционната система Windows и **MonoDevelop** или **Raider** за Linux или Mac OS X.
- Ако програмираме на Java, подходящи са средите **IntelliJ IDEA**, **Eclipse** или **NetBeans**.
- Ако ще пишем на Python, можем да използваме средата **PyCharm**.
[/slide]

[slide]
# Инсталация на Visual Studio Community

Започваме с инсталацията на интегрираната среда **Microsoft Visual Studio Community** (версия 2017, актуална към юни 2017 г.).

**Community** версията на Visual Studio (VS) се разпространява безплатно от Microsoft и може да бъде изтеглена от: [anchor href=https://www.visualstudio.com/vs/community]https://www.visualstudio.com/vs/community[/anchor]. Инсталацията е типичната за Windows с [**Next**], [**Next**] и [**Finish**], но е важно да включим компонентите за "**Desktop Development**" и "**ASP.NET**". Не е необходимо да променяме останалите настройки за инсталация.

В следващите редове подробно са описани подробно **стъпките за инсталация на Visual Studio** (версия Community 2017). След като свалим инсталационния файл и го стартираме, се появява следният екран:

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-BG/blob/master/assets/chapter-1-images/00.visual-studio-1.png alt="Visual Studio Image" /]

Натискаме бутона [**Continue**], след което ще видим прозореца долу:

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-BG/blob/master/assets/chapter-1-images/00.visual-studio-2.png alt="Visual Studio Image" /]

Зарежда се прозорец с инсталационния панел на Visual Studio:

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-BG/blob/master/assets/chapter-1-images/00.visual-studio-3.png alt="Visual Studio Image" /]

Слагаме отметка на [**Universal Windows Platform development**], [**.NET desktop development**] и [**ASP.NET and web development**], след което натискаме бутона [**Install**]. Общо взето това е всичко.

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-BG/blob/master/assets/chapter-1-images/00.visual-studio-4.png alt="Visual Studio Image" /]

Започва инсталацията на Visual Studio и ще се появи екран като този по-долу:

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-BG/blob/master/assets/chapter-1-images/00.visual-studio-5.png alt="Visual Studio Image" /]

След като Visual Studio се инсталира, ще се появи информативен екран и трябва да натиснем бутона [**Launch**], за да го стартираме:

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-BG/blob/master/assets/chapter-1-images/00.visual-studio-6.png alt="Visual Studio Image" /]

След **старта на VS** излиза екран като този по-долу. От него можем да изберем дали да влезем с Microsoft профила си във Visual Studio. За момента избираме да работим без да сме се логнали с Microsoft акаунта си, затова избираме опцията [**Not now, maybe later.**]. На по-късен етап, ако имате такъв акаунт, можете да се логнете, а ако нямате и срещате затруднения със създаването му, винаги можете да пишете във форума на SoftUni: [anchor href=https://softuni.bg/forum]https://softuni.bg/forum[/anchor]


[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-BG/blob/master/assets/chapter-1-images/00.visual-studio-7.png alt="Visual Studio Image" /]

Следващата стъпка е да изберем **цветовата тема**, с която да се визуализира Visual Studio. Тук изборът е изцяло според предпочитанията на потребителя, като няма значение коя опция ще бъде избрана.

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-BG/blob/master/assets/chapter-1-images/00.visual-studio-8.png alt="Visual Studio Image" /]

Натискаме бутона [**Start Visual Studio**] и се зарежда в началния изглед на Visual Studio Community:

[image src=https://github.com/SoftUni/Programming-Basics-Book-CSharp-BG/blob/master/assets/chapter-1-images/00.visual-studio-9.png alt="Visual Studio Image" /]

Това е всичко. Готови сме за работа с Visual Studio.

# По-стари версии на Visual Studio

Можем да използваме и по-стари версии на Visual Studio (например версия 2015 или 2013 или дори 2010 или 2005), но **не е препоръчително**, тъй като в тях не се съдържат някои от по-новите възможности за разработка и не всички примери от книгата ще тръгнат.
[/slide]

[slide]
# Онлайн среди за разработка

Съществуват и **алтернативни среди за разработка онлайн**, директно във вашия уеб браузър. Тези среди не са много удобни, но ако нямате друга възможност, може да стартирате обучението си с тях и да си качите Visual Studio по-късно. Ето някои линкове:
* За езика C# сайтът **.NET Fiddle** позволява писане на код и изпълнението му онлайн: [anchor href=https://dotnetfiddle.net]https://dotnetfiddle.net[/anchor].
* За Java можем да използваме следното онлайн Java IDE: [anchor href=https://www.compilejava.net]https://www.compilejava.net[/anchor].
* За JavaScript можем да пишем JS код директно в конзолата на даден браузър с натискане на **[F12]**.
[/slide]

[slide]
# Проектни решения и проекти във Visual Studio

Преди да започнем да работим с Visual Studio е нужно да се запознаем с понятията **Visual Studio Solution** и **Visual Studio Project**, които са неизменна част от него.

**Visual Studio Project** представлява "проектът", върху който работим. В началото това ще са нашите конзолни програми, които ще се научим да пишем с помощта на настоящата книга, ресурсите към нея и в курса Programming Basics в SoftUni. При по-задълбочено изучаване и с времето и практиката, тези проекти ще преминат в апликации, уеб приложения и други разработки. Проектът във VS **логически групира множество файлове**, изграждащи дадено приложение или компонент. Един **C# проект** съдържа един или няколко **C# сорс файла**, конфигурационни файлове и други ресурси. Във всеки C# сорс файл има една или повече **дефиниции на типове** (класове или други дефиниции). В **класовете** има **методи** (действия), а те се състоят от **поредици от команди**. Изглежда сложно, но при големи проекти такава структура е много удобна и позволява добра организация на работните файлове.

**Visual Studio Solution** представлява контейнер (работно решение), в който **логически са обединени няколко проекта**. Целта на обединението на тези VS Projects е да има възможност кода от който и да е от проектите, да си взаимодейства с кода на останалите VS проекти, за да може приложението или уеб сайта да работи коректно. Когато софтуерният продукт или услуга, който разработваме е голям, той се изгражда като **VS Solution**, а този Solution се разделя на **проекти** (VS Projects) и във всеки проект има **папки със сорс файлове**. Такава йерархична организация е много удобна при по-сериозни проекти (да кажем над 50 000 реда код).

За **малки проекти** VS Solutions и VS Projects повече **усложняват работата**, отколкото помагат, но се свиква бързо.
[/slide]
