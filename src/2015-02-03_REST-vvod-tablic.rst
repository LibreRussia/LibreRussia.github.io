:title: reStructuredText (ReST): Быстрый способ ввода таблиц
:date: 2015-02-03
:category: Разметка
:tags: reStructuredText, markdown, pandoc, html, docutils


Когда дело касается больших таблиц, то их не очень удобно набирать
вручную. Так как мне приходится работать в основном над переносом текста
из LibreOffice (odf, doc, docx и т.д.), то я нашел быстрый, легкий и
удобный способ с использованием CSV-таблиц и LibreOffice.

Напомню, что CSV таблицы в reStructuredText вводятся следующим образом:

::

    .. csv-table:: CSV-таблица
       :header: "Treat", "Quantity", "Description"
       :widths: 15, 10, 30

       "Albatross", 2.99, "On a stick!"
       "Crunchy Frog", 1.49, "If we took the bones out, it wouldn't be
       crunchy, now would it?"
       "Gannet Ripple", 1.99, "On a stick!"

Все достаточно просто. Строки вводятся на новых строках, а столбцы
разделяются запятыми. Внутреннее содержимое ячеек лучше брать в кавычки.

Результат:

.. figure:: img/2015-02-03_rest-tables/2015-02-03_rst-tables-001.png
       :width: 350 px
       :align: center
       :alt:

В LibreOffice Writer есть функция преобразования текста разделенного
запятыми (на самом деле разделитель может быть любой) в таблицу и
наоборот, преобразование таблицы в текст разделенный запятыми.

Таким образом, при составлении ReST файла я беру шапку таблицы:

::

    .. csv-table:: CSV-таблица
       :header: "Treat", "Quantity", "Description"
       :widths: 15, 10, 30

А само содержимое набираю в LibreOffice, как это обычно делается в
подобных программах.

.. figure:: img/2015-02-03_rest-tables/2015-02-03_rst-tables-002.png
       :width: 350 px
       :align: center
       :alt:

Далее выделяю таблицу и перехожу в *Таблица > Преобразовать > Таблицу в
текст*. Откроется диалог, в котором я устанавливаю в качестве
разделителя запятую.

.. figure:: img/2015-02-03_rest-tables/2015-02-03_rst-tables-003.png
       :width: 350 px
       :align: center
       :alt:

Получившийся материал копирую в ReST файл.

.. figure:: img/2015-02-03_rest-tables/2015-02-03_rst-tables-004.png
       :width: 350 px
       :align: center
       :alt:

::

    "Albatross", 2.99, "On a stick!"
    "Crunchy Frog", 1.49, "If we took the bones out, it wouldn't be crunchy, now would it?"
    "Gannet Ripple", 1.99, "On a stick!"

**ПРИМЕЧАНИЕ!** В *Сервис > Параметры автозамены* на вкладке
*Национальные* рекомендую отключить преобразование кавычек.

.. figure:: img/2015-02-03_rest-tables/2015-02-03_rst-tables-005.png
       :width: 350 px
       :align: center
       :alt: