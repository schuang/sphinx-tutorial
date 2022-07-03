======================
Code listing
======================


Syntax highlighting
----------------------------

Some of the useful code-listing features are:

- syntax highlighting
- line numbering
- line highlighting (emphasis)
- including external files.

Highlighting of programming languages are supported by `Pygments <http://pygments.org/docs/>`_.

Pygments has a collection of syntax highlighting styles:

.. code-block:: python

    from pygments.styles import get_all_styles
    print(list(get_all_styles()))

['default', 'emacs', 'friendly', 'colorful', 'autumn', 'murphy', 'manni', 'monokai', 'perldoc', 'pastie', 'borland', 'trac', 'native', 'fruity', 'bw', 'vim', 'vs', 'tango', 'rrt', 'xcode', 'igor', 'paraiso-light', 'paraiso-dark', 'lovelace', 'algol', 'algol_nu', 'arduino', 'rainbow_dash', 'abap']


For example, in ```conf.py```:

.. code-block:: python

    pygments_style = 'emacs'


Examples
----------------------------------------

Inlined listing
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

The code listing is embedded in the text:

Bash:

.. code-block:: bash

    export PATH=$HOME/bin:$PATH
    for i in `seq 1 10`; do
       echo $i
       echo $LD_LIBRARY_PATH
    done


C language (also with line emphasis):

.. code-block:: c
   :linenos:
   :emphasize-lines: 1,3

    #include <stdio.h>

    int static hello(int *i)
    {
       double *x;
       return 0;
    }

    for (int i=0; i<10; i++) {
      printf("i = %d\n", i);
    } 


Including external file(s)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

The code is in an external file, e.g. ```foo.py```:


.. literalinclude:: code1.py
   :language: python
   :linenos:

Code listing without highlighting:

.. literalinclude:: code1.py
   :language: none


