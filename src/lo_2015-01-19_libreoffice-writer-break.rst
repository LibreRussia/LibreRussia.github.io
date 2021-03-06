:title: Writer: Изменение ориентации отдельных страниц
:date: 2015-01-19
:category: LibreOffice
:tags: LibreOffice, Writer

Writer: Изменение ориентации отдельных страниц
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Обычно для всего документа задается единая ориентация страниц. Но в
некоторых случаях требуется сделать одну или несколько страниц иной
ориентации.

Предлагаю несколько способов сделать это. В качестве исходного условия
принимаем ситуацию, когда среди портретноориентированных страниц надо
вставить две страницы альбомной ориентации.


.. figure:: /home/dmitry/Docs/LibreRussia/librerussia.github.io/img/lo_2015-01-19_libreoffice-writer-break/lo_2015-01-19_libreoffice-writer-break.001.png
    :width: 350 px
    :align: center
    :alt:


Попутно статья отвечает на следующие вопросы:

-  Как сделать, чтобы заголовок начинался с новой страницы
-  Как изменить нумерацию страниц
-  Как вставить разрыв
-  Как удалить разрыв

Ручной способ
-------------

Чтобы изменить ориентацию страницы, надо сначала вставить *Разрыв
страницы* и задать следуемый за ним стиль страницы.

#. Открываем документ и устанавливаем курсор мыши на странице за
   текстом. Т.е. если у нас имеется некоторый текст, то курсор должен
   располагаться за ним, иначе часть текста после курсора перескочит на
   следующую страницу.
#. Так как нам надо **вставить** разрыв, следовательно идем на вкладку
   *«Вставка → Разрыв»*.
#. Откроется диалог «Вставить разрыв», в котором устанавливаем маркер
   напротив *«Разрыв страниц»*, а в списке *«Стиль»* выбираем
   *«Альбомный»*. Нажимаем *«ОК»*.


.. figure:: /home/dmitry/Docs/LibreRussia/librerussia.github.io/img/lo_2015-01-19_libreoffice-writer-break/lo_2015-01-19_libreoffice-writer-break.002.png
    :width: 250 px
    :align: center
    :alt:


Альбомная страница вставлена. Разрыв обозначается синей полосой над
страницей. Теперь нажмем сочетание клавиш ``Ctrl+Enter`` на клавиатуре.
У нас появится еще одна альбомная страница. Вместо сочетания клавиш
можно было ещё раз выполнить вставку разрыва.

Чтобы после альбомных страниц снова шли страницы с портретной
ориентацией, повторяем шаги 1-3, но только в списке *«Стиль»* выбираем
*«Базовый»* (или тот, который вы создали).

Ничего сложного нет. Но стоит иметь ввиду, если вы изменяли параметры
страницы вне стиля (т.е. просто через диалог *«Формат → Страница»*), то
скорее всего, после вставки стиля *«Базовый»* у вас будут идти страницы
с другими параметрами.

Чтобы избежать этого, лучше заранее создать нужный вам стиль страницы
или изменить уже существующий стиль страницы под свои требования. О том
что такое стили и как с ними работать можно прочитать
`здесь <http://librerussia.blogspot.ru/2014/11/LibreOffice-Styles-000.html>`__.

Ложный путь
~~~~~~~~~~~

На многих форумах и блогах дают ошибочное решение этого вопроса. Там
предлагается открыть диалог параметров страницы *«Формат → Страница»* и
на вкладке *«Управление»* выбрать *«Следующий стиль»*.


.. figure:: /home/dmitry/Docs/LibreRussia/librerussia.github.io/img/lo_2015-01-19_libreoffice-writer-break/lo_2015-01-19_libreoffice-writer-break.003.png
    :width: 350 px
    :align: center
    :alt:


Такой подход приводит к путанице. Это совсем другая функция. Допустим, у
вас имеется страница со стилем *«Базовый»* и это основной стиль всех
страниц в вашем документе. За каждой страницей со стилем *«Базовый»*
автоматически следует страница с таким же стилем. Если вы зададите ему
*«Следующий стиль»*, например, *«Альбомный»*, то у вас начнется
чередование страниц. Каждый раз после страницы со стилем *«Базовый»*
будет автоматически следовать страница со стилем *«Альбомный»*. Как
только после альбомной странице вы вставите базовую страницу, после
базовой снова пойдет альбомная и так будет происходить каждый раз.

Поэтому не стоит так делать. Для нарушения нормального хода страниц и
используется разрыв страницы, так как обычно требуется вставить только
одну-две отличные от остальных страницы.

Расширение Pager
----------------

Есть удобное расширение Pager (http://myooo.ru/content/view/106/99/),
которое служит для быстрой вставки страниц. В том числе, с его помощью
можно быстро изменить ориентацию отдельных страниц.

Параметры страницы
------------------

В LibreOffice все построено на стилях. Даже если вы явно их не
применяете, то вы все равно пользуетесь стилями. Любая страница имеет
свой стиль. В стандартном шаблоне по умолчанию используется страница со
стилем *«Базовый»*.

Если вы просто идете во вкладку *«Формат → Страница»* и изменяете там
параметры страницы, вы не изменяете сам стиль. Вы вносите изменения
только для конкретной страницы. Поэтому, если вам требуется изменить
параметры страницы, меняйте стиль страницы.

Подробнее о стилях написано:

-  `Руководство по стилям
   LibreOffice <http://librerussia.blogspot.ru/2014/11/LibreOffice-Styles-000.html>`__
-  `Краткое руководство по
   LibreOffice <http://libreoffice.readthedocs.org/ru/latest/Using-Styles-and-Templates.html>`__

Не ленитесь изучать стили. В МС Офис тоже все строится на стилях.
Большие документы невозможно грамотно оформлять без их использования.

Заголовок с новой страницы
--------------------------

С помощью разрыва страницы можно, например, сделать чтобы все заголовки
глав автоматически начинались с новой страницы.

Для этого в стиле заголовка на вкладке *«Положение на странице»*
необходимо задать *«Разрывы»*. Можно не указывать конкретный стиль
страницы, тогда будет применен стиль страницы используемый во всем
документе.


.. figure:: /home/dmitry/Docs/LibreRussia/librerussia.github.io/img/lo_2015-01-19_libreoffice-writer-break/lo_2015-01-19_libreoffice-writer-break.004.png
    :width: 350 px
    :align: center
    :alt:


Изменить нумерацию страниц
--------------------------

С помощью разрыва и стилей страниц можно изменить нумерацию следующей
страницы, например, за 3-й страницей сразу может следовать 8-я. Для
этого также используется диалог вставки разрыва.


.. figure:: /home/dmitry/Docs/LibreRussia/librerussia.github.io/img/lo_2015-01-19_libreoffice-writer-break/lo_2015-01-19_libreoffice-writer-break.005.png
    :width: 250 px
    :align: center
    :alt:


Удаление разрыва
----------------

Для удаления разрыва, достаточно установить курсор перед разрывом и
нажать клавишу ``Backspace`` на клавиатуре.

И снова о логике
----------------

Снова хочу порассуждать о логике. Я не устаю твердить о том, что
интерфейс LibreOffice очень логичен. Но иногда логика требует
определенных знаний.

Вполне логично пытаться сменить ориентацию страницы с помощью диалога
*«Параметры страницы»* (*«Формат → Страница»*). Но с его помощью нельзя
добиться желаемого результата, так как он изменяет параметры для всех
страниц в документе.

Программы не умеют читать мысли людей. Вполне удобно, что за портретной
страницей автоматически следует тоже портретная страница. Ведь в
большинстве случаев отдельный документ оформляется в едином стиле. Было
бы крайне неудобно каждый раз указывать программе какая страница должна
следовать. Но даже на этот случай придуман механизм с *«Разрывом
страниц»*.

Однако разрыв страницы является параметром абзаца. Эту логику не все
могут проследить. Дело в том, что такие программы, как LibreOffice,
оперирую абзацами. Абзац первичен, без абзаца нет страницы. Ни в
LibreOffice, ни в МС Офис невозможно создать абсолютно пустую страницу.
Всегда на новой странице будет находиться мигающий курсор и будет
автоматически сделана пустая строка. Да, пустая строка это тоже абзац.

Программы, которые используются для создания полиграфической продукции
(Scribus, Inkscape, CorelDraw, Illustrator и подобные) наоборот
оперируют страницами. Для них первична страница, на которой можно
размещать изображения, текстовые блоки и т.д.

Поэтому в LibreOffice разрыв страницы является атрибутом абзаца.
Взгляните на картинку ниже.


.. figure:: /home/dmitry/Docs/LibreRussia/librerussia.github.io/img/lo_2015-01-19_libreoffice-writer-break/lo_2015-01-19_libreoffice-writer-break.006.png
    :width: 350 px
    :align: center
    :alt:


Синими метками отмечены абзацы. Делая разрыв страницы, мы как-бы говорим
программе, что следующий абзац должен начинаться с новой страницы.

Так что, логика по прежнему присутствует, но для её понимания нужно
знание базовых основ.

Разрывы в Microsoft Office
~~~~~~~~~~~~~~~~~~~~~~~~~~

В Microsoft Office разрыв страницы является спецсимволом. Вставляется из
меню *«Вставка → Разрыв»* или вставкой спецсимвола с кодом 012.

В Libre/Open Office разрыв страницы является свойством абзаца.

Дополнительные ссылки
---------------------

-  `Руководство по стилям
   LibreOffice <http://librerussia.blogspot.ru/2014/11/LibreOffice-Styles-000.html>`__
-  `Краткое руководство по
   LibreOffice <http://libreoffice.readthedocs.org/ru/latest/Using-Styles-and-Templates.html>`__
-  `Справка LibreOffice: Вставка и удаление разрывов
   страниц <https://help.libreoffice.org/Writer/Inserting_and_Deleting_Page_Breaks/ru>`__


