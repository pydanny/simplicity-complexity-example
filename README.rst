=============================
simplicity-complexity-example
=============================
:date: July 19, 2013
:author: Daniel Greenfeld
:version: 1.0
:description: An example of using Simplicity to populate the data in a Complexity generated site. 

Clone this and use it with the Complexity static site generator. Try it out:

.. code-block:: bash

    $ pip install simplicity
    $ pip install complexity
    $ git clone git@github.com:pydanny/simplicity-complexity-example.git my_project
    $ cd my_project
    $ simplicity README.rst > project/json/README.json
    $ complexity project www

Open http://127.0.0.1:9090/

What the @#$% just happened?!?
================================

1. You installed:

    * simplicity_: Converts ReStructuredText into JSON.
    * complexity_: A refreshingly simple static site generator, for those who like to work in HTML.

2. You cloned these files to your local machine and went inside them.

3. You used simplicity_ to convert this README.rst file to JSON.

4. You used complexity_ to generate a static HTML site in a new 'www' folder.


.. _simplicity: https://github.com/pydanny/simplicity
.. _complexity: https://github.com/audreyr/complexity

