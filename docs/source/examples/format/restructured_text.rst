================
reStructuredText
================
GitHub also uses reStructuredText(.rst) files because it is easy-to-read, easy-to-write syntax for formatting plain text.

.. note::

    GitHub pages are in reStructuredText format.

Inline
------

:: 

    *italic*
    **bold**
    ``*``

*italic*

**bold**

``*``

Headings
--------

::

    *****
    Title
    *****

    subtitle
    ########

    subsubtitle
    **********************
    and so on

* ``#`` with overline, for parts
* ``*`` with overline, for chapters
* ``=``, for sections
* ``-``, for subsections
* ``^``, for subsubsections
* ``“``, for paragraphs

Links
-----

External
++++++++

::

    `<http://www.python.org/>`_

`<http://www.python.org/>`_

::

    `Python <http://www.python.org/>`_

`Python <http://www.python.org/>`_

Implicit Links to Titles
++++++++++++++++++++++++

::

    `Internal and External links`_

Explicit Links
++++++++++++++

::

    .. _rst_tutorial:

::

    :ref:`rst_tutorial`

List and Bullets
----------------

::

    * This is a bulleted list.
    * It has two items, the second
      item uses two lines. (note the indentation)

    1. This is a numbered list.
    2. It has two items too.

    #. This is a numbered list.
    #. It has two items too.

* This is a bulleted list.
* It has two items, the second
  item uses two lines. (note the indentation)

1. This is a numbered list.
2. It has two items too.

#. This is a numbered list.
#. It has two items too.

::

    -a            command-line option "a"
    -b file       options can have arguments
                  and long descriptions
    --long        options can be long also
    --input=file  long options can also have
                  arguments
    /V            DOS/VMS-style options too

-a            command-line option "a"
-b file       options can have arguments
              and long descriptions
--long        options can be long also
--input=file  long options can also have
              arguments
/V            DOS/VMS-style options too

Directives
----------

::

    .. code-block:: html
        :linenos:

        <h1>code block example</h1>

.. code-block:: html
    :linenos:

    <h1>code block example</h1>

Code and Literal Blocks
-----------------------

::

    This is a simple example:
    ::

        import math
        print 'import done'

This is a simple example::

    import math
    print 'import done'

Tables
------

::

    +------------+------------+-----------+
    | Header 1   | Header 2   | Header 3  |
    +============+============+===========+
    | body row 1 | column 2   | column 3  |
    +------------+------------+-----------+
    | body row 2 | Cells may span columns.|
    +------------+------------+-----------+
    | body row 3 | Cells may  | - Cells   |
    +------------+ span rows. | - contain |
    | body row 4 |            | - blocks. |
    +------------+------------+-----------+

+------------+------------+-----------+
| Header 1   | Header 2   | Header 3  |
+============+============+===========+
| body row 1 | column 2   | column 3  |
+------------+------------+-----------+
| body row 2 | Cells may span columns.|
+------------+------------+-----------+
| body row 3 | Cells may  | - Cells   |
+------------+ span rows. | - contain |
| body row 4 |            | - blocks. |
+------------+------------+-----------+

::

    =====  =====  ======
       Inputs     Output
    ------------  ------
      A      B    A or B
    =====  =====  ======
    False  False  False
    True   False  True
    =====  =====  ======

=====  =====  ======
   Inputs     Output
------------  ------
  A      B    A or B
=====  =====  ======
False  False  False
True   False  True
=====  =====  ======

Csv-table Directive
-------------------

::

    .. csv-table:: a title
       :header: "name", "firstname", "age"
       :widths: 20, 20, 10

       "Smith", "John", 40
       "Smith", "John, Junior", 20

.. csv-table:: a title
   :header: "name", "firstname", "age"
   :widths: 20, 20, 10

   "Smith", "John", 40
   "Smith", "John, Junior", 20
   
Include other RST files
-----------------------

::

    .. toctree::
        :maxdepth: 2
        :numbered:
        :titlesonly:
        :glob:
        :hidden:

        intro.rst
        chapter1.rst
        chapter2.rst

* **maxdepth** is used to indicates the depth of the tree.
* **numbered** adds relevant section numbers.
* **titlesonly** adds only the main title of each document
* **glob** can be used to indicate that * and ? characters are used to indicate patterns.
* **hidden** hides the toctree. It can be used to include files that do not need to be shown

Images
------

::

    .. image:: stars.jpg
        :width: 200px
        :align: center
        :height: 100px
        :alt: alternate text
        
Boxes
-----

See also

::

    .. seealso:: This is a simple **see also** note.

.. seealso:: This is a simple **see also** note.

Note

::

    .. note::  This is a **note** box.

.. note::  This is a **note** box.

Warning

::

    .. warning:: note the space between the directive and the text

.. warning:: note the space between the directive and the text

Todo

::

    .. todo:: todo requires an extension

.. todo:: todo requires an extension

Topic

::

    .. topic:: Your Topic Title

        Subsequent indented lines comprise
        the body of the topic, and are
        interpreted as body elements.
        
.. topic:: Your Topic Title

    Subsequent indented lines comprise
    the body of the topic, and are
    interpreted as body elements.

Sidebar

::

    .. sidebar:: Sidebar Title
        :subtitle: Optional Sidebar Subtitle

        Subsequent indented lines comprise
        the body of the sidebar, and are
        interpreted as body elements.

.. sidebar:: Sidebar Title
    :subtitle: Optional Sidebar Subtitle

    Subsequent indented lines comprise
    the body of the sidebar, and are
    interpreted as body elements.

Other
-----

Footnotes

::

    Some text that requires a footnote [#f1]_ .

    .. rubric:: Footnotes

    .. [#f1] Text of the first footnote.

Some text that requires a footnote [#f1]_ .

.. rubric:: Footnotes

.. [#f1] Text of the first footnote.

Credits
-------
https://thomas-cokelaer.info/tutorials/sphinx/rest_syntax.html

https://github.com/ralsina/rst-cheatsheet/blob/master/rst-cheatsheet.rst