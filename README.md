# pl-object-detection_moc_ppc64
pl-objectdetection
================================

.. image:: https://badge.fury.io/py/objectdetection.svg
    :target: https://badge.fury.io/py/objectdetection

.. image:: https://travis-ci.org/FNNDSC/objectdetection.svg?branch=master
    :target: https://travis-ci.org/FNNDSC/objectdetection

.. image:: https://img.shields.io/badge/python-3.5%2B-blue.svg
    :target: https://badge.fury.io/py/pl-objectdetection

.. contents:: Table of Contents


Abstract
--------

An app to ...


Synopsis
--------

.. code::

    python objectdetection.py                                           \
        [-v <level>] [--verbosity <level>]                          \
        [--version]                                                 \
        [--man]                                                     \
        [--meta]                                                    \
        <inputDir>
        <outputDir> 

Description
-----------

``objectdetection.py`` is a ChRIS-based application that...

Agruments
---------

.. code::

    [-v <level>] [--verbosity <level>]
    Verbosity level for app. Not used currently.

    [--version]
    If specified, print version number. 
    
    [--man]
    If specified, print (this) man page.

    [--meta]
    If specified, print plugin meta data.


Run
----


Using ``docker run``
~~~~~~~~~~~~~~~~~~~~

To run using ``docker``, be sure to assign an "input" directory to ``/incoming`` and an output directory to ``/outgoing``. *Make sure that the* ``$(pwd)/out`` *directory is world writable!*

Now, prefix all calls with 

.. code:: bash

    docker run --rm -v $(pwd)/out:/outgoing                             \
            fnndsc/pl-objectdetection objectdetection.py                        \

Thus, getting inline help is:

.. code:: bash

    mkdir in out && chmod 777 out
    docker run --rm -v $(pwd)/in:/incoming -v $(pwd)/out:/outgoing      \
            fnndsc/pl-objectdetection objectdetection.py                        \
            --man                                                       \
            /incoming /outgoing

Examples
--------




