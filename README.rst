Avocado Test Framework
======================

Avocado is a test framework that is built on the experience accumulated with
`autotest <http://autotest.github.io/>`__, while improving on its weaknesses
and shortcomings.

The main goal of the Avocado project is to provide a set of smart tools for
automated testing and continuous integration. Among them, we can highlight:

- A powerful test runner;
- A multiplexer that allows tests to be run with different sets of variables;
- Test APIs for test writers;
- A database for results, with a web interface;
- A scheduler for setting up a test grid.

An `extensive set of slides about avocado
<https://docs.google.com/presentation/d/1PLyOcmoYooWGAe-rS2gtjmrZ0B9J22FbfpNlQY8fIUE>`__,
including details about its architecture, main features and status is available
in google-drive.

Using avocado
-------------

The most straightforward way of `using` avocado is to install packages
available for your distro:

1) Fedora

   To use the latest version of avocado, or to use it while it's not officially
   packaged in Fedora yet, you should use `Avocado's copr repository
   <http://copr.fedoraproject.org/coprs/lmr/Autotest/>`__.

Once you install it, you can start exploring it by checking the output of
``avocado --help`` and the test runner man-page, accessible via ``man avocado``.

If you want to `develop` avocado, or run it directly from the git repository,
you have a couple of options:

1) The avocado test runner was designed to run in tree, for rapid development
   prototypes. Just use::

    $ scripts/avocado --help

2) Installing avocado in the system is also an option, although remember that
   distutils has no ``uninstall`` functionality::

    $ sudo python setup.py install
    $ avocado --help

Documentation
-------------

Avocado comes with in tree documentation about the most advanced features and
its API. It can be built with ``sphinx``, but a publicly available build of
the latest master branch documentation and releases can be seen on `read the
docs <https://readthedocs.org/>`__:

http://avocado-framework.readthedocs.org/

If you want to build the documentation yourself:

1) Make sure you have the package ``python-sphinx`` installed. For Fedora::

    $ sudo yum install python-sphinx

2) For Mint/Ubuntu/Debian::

    $ sudo apt-get install python-sphinx

3) Optionally, you can install the read the docs theme, that will make your
   in-tree documentation look just like the online version::

    $ sudo pip install sphinx_rtd_theme

4) Build the docs::

    $ make -C docs html

5) Once done, point your browser to::

    $ [your-browser] docs/build/html/index.html

