:title: Конвертация HTML в reStructuredText и наоборот
:date: 2015-06-06 
:category: Разметка
:tags: reStructuredText, markdown, pandoc, html, docutils


Конвертация HTML в reStructuredText:

.. code-block:: bash

    pandoc --from=html --to=rst --output=README.rst README.html

Конвертация reStructuredText в HTML:

.. code-block:: bash

    pandoc --from=rst --to=html --output=README.html README.rst


**Автоматизация с помощью Python**

.. code-block:: python

    import os
    
    fr_format = 'html'     # Из какого формата
    to_format = 'rst'      # В какой формат
    
    def convert(fr_format, to_format, file):
      out_file = '{0}.{1}'.format(file, to_format)
      command = 'pandoc --from={0} --to={1} --output={2} {3}'.format(fr_format, to_format, out_file, file)
      os.popen(command)
    
Ссылки
------

* `HTML to reStructuredText in Python using Pandoc <http://www.johnpaulett.com/2009/10/15/html-to-restructured-text-in-python-using-pandoc/>`_
* `Try pandoc! <http://pandoc.org/try/>`_

