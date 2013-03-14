Optimizing Software Occlusion Culling
=====================================

This is a conversion of the blog series from Fabian Giesen into
ReStructuredText so that it can be published in ePub and PDF
formats.

The `original material`_ can be found on his `blog`_.

Building
--------

Before building this documentation, you will need a copy of Sphinx installed.
The easiest way to do this is to get it from the `Python Package Index
<http://pypi.python.org/pypi/Sphinx>`_ or to use ``easy_install``::

    sudo easy_install -U Sphinx

Building the documentation is easy on a system with ``make``::

    make html

If you are on Windows, there is a ``make.bat`` as well::

    make.bat html

The generated documentation will be in ``build/html``.

You can build other formats as well. Run ``make`` or ``make.bat`` without
arguments to see which formats are available.

TODO
----

* Code blocks all need to be fixed.
* Tables need to be converted to ReStructuredText syntax.

.. _original material: http://fgiesen.wordpress.com/2013/02/17/optimizing-sw-occlusion-culling-index/
.. _blog: http://fgiesen.wordpress.com/
