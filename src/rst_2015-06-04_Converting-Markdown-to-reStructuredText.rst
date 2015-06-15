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

**Автоматизация с помощью Python**

.. code-block:: python

    import os
    
    fr_format = 'md'     # Из какого формата
    to_format = 'rst'      # В какой формат
    
    def convert(fr_format, to_format, file):
      out_file = '{0}.{1}'.format(file, to_format)
      command = 'pandoc --from={0} --to={1} --output={2} {3}'.format(fr_format, to_format, out_file, file)
      os.popen(command)
   
Или с помощью модуля ``pypandoc``:

.. code-block:: python

    import pypandoc

    output = pypandoc.convert('somefile.md', 'rst', outputfile="somefile.rst")
 
Ссылки
------

* `Converting Markdown to reStructuredText <http://bfroehle.com/2013/04/26/converting-md-to-rst/>`_
* `Try pandoc! <http://pandoc.org/try/>`_
* `pypandoc 0.9.8 <https://pypi.python.org/pypi/pypandoc/>`_