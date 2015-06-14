:title: Python 3: Работа с zip архивами. Модуль ZipFile
:date: 2015-06-14
:category: Python
:tags: Python, ZipFile, zip


**Импорт модуля ZipFile:**

.. code-block:: python

    import zipfile


**Работа с zip архивами:**

.. code-block:: python

    ZipFile(filename [, mode [, compression [, allowZip64]]])

``filename`` - имя файла zip архива.

``mode``:

* ``r`` - файл будет открыт для чтения;
* ``w`` - если файл существует, то он будет уничтожен и вместо него будет создан новый файл;
* ``a`` - существующий файл будет открыт в режиме добавления в конец.

``compression`` определяет метод сжатия, который должен использоваться при записи в архив. Он принимает одно из значений: ``ZIP_STORED`` или ``ZIP_DEFLATED``. По умолчанию используется значение ``ZIP_STORED``. Последний аргумент 

``allowZip64`` позволяет разрешить использование расширений ``ZIP64``, которые дают возможность создавать архивы размером больше 2 гигабайт. По умолчанию равен False.

Итак, давайте откроем наш ранее созданный архив для чтения:

**Является ли файл zip архивом:**

.. code-block:: python

   zipfile.is_zipfile('xml_healer.zip')
   True

**Чтение архива:**

.. code-block:: python

    z = zipfile.ZipFile('xml_healer.zip', 'r')


**Просмотр содержимого:**

.. code-block:: python

    z.printdir()

**Извлечение содержимого:**

.. code-block:: python

    z.extract('file') # Извлечь файл из архива
    
    z.extractall()    # Извлечь все файлы

**Запись содержимого:**

.. code-block:: python

    with zipfile.ZipFile('spam.zip', 'w') as myzip:
        myzip.write('file')

.. code-block:: python

    z = zipfile.ZipFile('spam.zip', 'w')
    z.write('file')
    z.close()


Для записи всех файлов в директории можно воспользоваться функцией ``os.walk``:

.. code-block:: python 

    import zipfile
    import os
    
    z = zipfile.ZipFile('spam.zip', 'w')        # Создание нового архива
    for root, dirs, files in os.walk('folder'): # Список всех файлов и папок в директории folder
    for file in files:
       z.write(os.path.join(root,file))         # Создание относительных путей и запись файлов в архив
       
    z.close()
      

**Закрытие архива:**

.. code-block:: python    

    z.close()

Ссылки:
-------

* `13.5. zipfile — Work with ZIP archives <https://docs.python.org/3.3/library/zipfile.html?highlight=zipfile#module-zipfile>`_
* `Работаем с zip архивами в Python <http://sayakhov.com/blog/post/6/>`_
* `Python - Добавление файлов в архив. Создание копий директорий  <http://www.cyberforum.ru/python/thread1268498.html>`_



