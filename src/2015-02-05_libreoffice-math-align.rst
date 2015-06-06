:title: LibreOffice Math: Выравнивание многострочных выражений (формул) Impress
:date: 2015-02-05
:category: LibreOffice
:tags: Руководства, LibreOffice, Math

Казалось, что тема с Math исчерпана полностью. Но все же нашелся один
неучтенный момент.

По умолчанию выражения в многострочных формулах выравниваются по центру.
В русскоязычной литературе принято выравнивать выражения по левому краю.
Делается это с помощью команды ``alignl``. Все хорошо, но вот загвоздка:

::

    left lbrace alignl 
    stack  {
    x = 9 - y
    # 
    2  over   {9-y} - 2 over y = {x-1} over 10
    } right none

.. figure:: /home/dmitry/Docs/LibreRussia/librerussia.github.io/img/2015-02-05_lo-math-align/2015-02-05_lo-math-align-001.png
       :width: 300 px
       :align: center
       :alt:

Во второй строке, абсолютно все выражения тоже выравниваются по левому
краю, в том числе знаменатели и числители дробей. Что некрасиво.

Самым первым в голову приходит то, что нужном ставить команду
выравнивания для каждого выражения в отдельности. Но на деле, можно
обойтись всего одной дополнительной командой ``alignc``.

::

    left lbrace alignl 
    stack  {
    x = 9 - y
    # 
    alignc {2  over   {9-y} - 2 over y = {x-1} over 10}
    } right none

.. figure:: /home/dmitry/Docs/LibreRussia/librerussia.github.io/img/2015-02-05_lo-math-align/2015-02-05_lo-math-align-002.png
       :width: 300 px
       :align: center
       :alt:

Обратите внимание, я взял в фигурные скобки (имеются ввиду служебные
символы) всю вторую строку и добавил перед ней команду ``alignc``.

Дополнительно
-------------

На данный момент компонент Math обладает самой полной русскоязычной
документацией, в отличии от других компонентов (это временно).
Напоминаю, по Math есть целых два руководства:

-  `Краткое руководство по LibreOffice
   Math <http://libreoffice.readthedocs.org/ru/latest/math.html>`__
   (официальное)
-  `Руководство по LibreOffice
   Math <http://librerussia.blogspot.ru/2014/10/libreoffice-math.html>`__
   (авторское)

Читать рекомендую оба. В кратком официальном руководстве более детально
рассматриваются основы работы с Math и есть несколько примеров ввода
формул, которых нет в авторском руководстве. Авторское руководство
содержит больше примеров и рассматривает некоторые вопросы более
подробно.

Пока руки не доходят объединить весь материал в единое полное
руководство. Но, думаю, что после завершения работы над `Кратким
руководством по LibreOffice <http://libreoffice.readthedocs.org>`__
возьмусь за это дело.

Статьи
~~~~~~

-  `LibreOffice Math: Каталог. Создание нестандартного набора
   символов <http://librerussia.blogspot.ru/2014/11/libreoffice-math_19.html>`__
-  `Как поставить дополнительный пробел? (Пробелы и
   табуляция) <http://librerussia.blogspot.ru/2014/11/libreoffice-math_96.html>`__
-  `LibreOffice Math: Работа над
   ошибками <http://librerussia.blogspot.ru/2014/11/libreoffice-math_17.html>`__
-  `Пример ввода сложной формулы в LibreOffice
   Math <http://librerussia.blogspot.ru/2014/11/libreoffice-math.html>`__
-  `LibreOffice Math: Пример ввода формул
   (#1) <http://librerussia.blogspot.ru/2014/09/libreoffice-math-1.html>`__

Также несколько интересных примеров можно найти на странице ЧаВо в
официальной Вики The Document Foundation:

-  `Часто задаваемые вопросы ― LibreOffice
   Math <https://wiki.documentfoundation.org/Faq/Math/ru>`__