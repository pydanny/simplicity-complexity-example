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

BOOM!

What the @#$% just happened?!?
================================

1. You installed:

    * simplicity_: Converts ReStructuredText into JSON.
    * complexity_: A refreshingly simple static site generator, for those who like to work in HTML.

.. code-block:: bash

    $ pip install simplicity
    $ pip install complexity

2. You cloned these files to your local machine and went inside them.

.. code-block:: bash

    $ git clone git@github.com:pydanny/simplicity-complexity-example.git my_project
    $ cd my_project


3. You used simplicity_ to convert this README.rst file to JSON.

.. code-block:: bash

    $ simplicity README.rst > project/json/README.json

4. You used complexity_ to generate a static HTML site in a new 'www' folder.

.. code-block:: bash

    $ complexity project www

5. You viewed the generated static site which was served by complexity_'s built-in HTTP server:

    $ open http://127.0.0.1:9090

And?
====

Take a look at https://github.com/pydanny/simplicity-complexity-example/blob/master/project/templates/index.html

.. code-block:: jinja2

    {% extends "base.html" %}

    {% block title %}Home{% endblock %}

    {% block content %}
    <div class="row">
        <div class="span12">
            <h1>{{ README.0.title }}</h1>
            <p>Created: {{ README.0.date }}</p>
            <p>Author: {{ README.0.author }}</p>
            <p>Version: {{ README.0.version }}</p>
            <p>Version: {{ README.0.description }}</p>

        </div>
    </div>
    {% endblock %}

Complexity_ used Jinja2 to render the data elements in that module with the README.json module you just created from this file using simplicity_.

Easy as that.



.. _simplicity: https://github.com/pydanny/simplicity
.. _complexity: https://github.com/audreyr/complexity


