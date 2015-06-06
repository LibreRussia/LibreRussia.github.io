:title: Конвертация reStructuredText в Markdown и наоборот
:date: 2015-06-04 08:25 
:category: Разметка
:tags: reStructuredText, markdown, pandoc, docutils


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
