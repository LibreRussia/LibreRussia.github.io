:title: Конвертация reStructuredText в Markdown и наоборот
:date: 04.06.2015 03:25:37
:category: Разметка
:tags: reStructuredText, Markdown, pandoc


Конвертация Markdown в reStructuredText:

.. code-block:: bash

    pandoc --from=markdown --to=rst --output=README.rst README.md

Конвертация reStructuredText в Markdown:

.. code-block:: bash

    pandoc --from=rst --to=markdown --output=README.md README.rst
    
Ссылки
------

* `Converting Markdown to reStructuredText <http://bfroehle.com/2013/04/26/converting-md-to-rst/>`_
* `Try pandoc! <http://pandoc.org/try/>`_
