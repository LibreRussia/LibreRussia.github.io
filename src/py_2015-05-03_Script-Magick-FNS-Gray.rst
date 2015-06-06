:title: Краткая инструкция по преобразования сканов для отправки в налоговую (ФНС)
:date: 2015-05-03
:category: Python
:tags: ImageMagick, Python

В соответствии с пунктом 3.3 приказа ФНС России от 09.11.2010 N
ММВ-7-6/535@, изображения для передачи по телекоммуникационным каналам
связи (ТКС) должны иметь:

-  256 градаций серого;
-  разрешение 150-300 DPI (точек на дюйм);
-  глубину цвета 8.


Для быстрого преобразования большого количества изображений [1]_ в соответсвии с требованиями ФНС необходимо.


#. Установть утилиту ``ImageMagick``  `32-бита <http://www.imagemagick.org/download/binaries/ImageMagick-6.9.1-2-Q16-x86-dll.exe>`__    /   `64-бита <http://www.imagemagick.org/download/binaries/ImageMagick-6.9.1-2-Q8-x64-dll.exe>`__
   и интерпритатор языка программирования ``Python``    `32-бита <https://www.python.org/ftp/python/3.4.3/python-3.4.3.msi>`__    /    `64-бита <https://www.python.org/ftp/python/3.4.3/python-3.4.3.amd64.msi>`__;
#. Скачать скрипт    ``magick-fns-gray``\ (`скачать <https://yadi.sk/d/HpdTtZM4gQWmf>`__) и поместить его в папку с изображениями, которые необходимо
   преобразовать;
   
.. figure:: img/2015-05-03_magick-fns-gray/2015-05-03_magick-fns-gray-001.jpg
   :width: 400 px
   :align: center
   :alt:
   
#. Дважды щелкнуть по скрипту левой кнопкой мыши;
#. Дождаться завершения преобразования. Вся информация выводится в
   черном окне.
   
.. figure:: img/2015-05-03_magick-fns-gray/2015-05-03_magick-fns-gray-002.jpg
   :width: 400 px
   :align: center
   :alt:

#. Преобразованные файлы появятся в папке ``magick_out``.

Скрипт кроссплатформенный, работает в ОС Linux, Windows, Mac OS и
других, которые поддерживаются программой ``ImageMagick`` и языком
``Python``.

Материалы по теме.
------------------

-  `ImageMagick: Пакетная обработка изображений с разной
   ориентацией <http://librerussia.blogspot.ru/2014/09/imagemagick.html>`__
-  `ImageMagick: добавление фона к
   изображению <http://librerussia.blogspot.ru/2014/09/imagemagick_30.html>`__
-  `ImageMagick: кадрирование(обрезка)
   изображений <http://librerussia.blogspot.ru/2014/09/imagemagick_29.html>`__
-  `LibreOffice: уменьшение размера документа с помощью пакетной
   обработки
   изображений <http://librerussia.blogspot.ru/2014/12/libreoffice.html>`__

Сайты
-----

-  `Python <https://www.python.org>`__
-  `ImageMagick <http://www.imagemagick.org>`__

--------------


.. [1] Преобразовывать можно от 1 изображения до ..., верхнего ограничения
   нет, все упирается в параметры компьютера. Время обработки также
   зависит от размеров изображений и параметров ПК.
