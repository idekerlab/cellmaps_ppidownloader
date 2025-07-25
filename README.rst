================================
Cell Maps for AI PPI Downloader
================================
The Cell Maps PPI Downloader is part of the Cell Mapping Toolkit

.. image:: https://img.shields.io/pypi/v/cellmaps_ppidownloader.svg
        :target: https://pypi.python.org/pypi/cellmaps_ppidownloader

.. image:: https://app.travis-ci.com/idekerlab/cellmaps_ppidownloader.svg?branch=main
    :target: https://app.travis-ci.com/idekerlab/cellmaps_ppidownloader

.. image:: https://readthedocs.org/projects/cellmaps-ppidownloader/badge/?version=latest
        :target: https://cellmaps-ppidownloader.readthedocs.io/en/latest/?badge=latest
        :alt: Documentation Status

.. image:: https://zenodo.org/badge/636892648.svg
        :target: https://zenodo.org/doi/10.5281/zenodo.10607408
        :alt: Zenodo DOI badge


Downloads protein-protein interaction data


* Free software: MIT license
* Documentation: https://cellmaps-ppidownloader.readthedocs.io.

Dependencies
------------

* `cellmaps_utils <https://pypi.org/project/cellmaps-utils>`__
* `requests <https://pypi.org/project/requests>`__
* `mygene <https://pypi.org/project/mygene>`__
* `tqdm <https://pypi.org/project/tqdm>`__

Compatibility
-------------

* Python 3.8+

Installation
------------

.. code-block::

   git clone https://github.com/idekerlab/cellmaps_ppidownloader
   cd cellmaps_ppidownloader
   pip install -r requirements_dev.txt
   make dist
   pip install dist/cellmaps_ppidownloader*whl


Run **make** command with no arguments to see other build/deploy options including creation of Docker image

.. code-block::

   make

Output:

.. code-block::

   clean                remove all build, test, coverage and Python artifacts
   clean-build          remove build artifacts
   clean-pyc            remove Python file artifacts
   clean-test           remove test and coverage artifacts
   lint                 check style with flake8
   test                 run tests quickly with the default Python
   test-all             run tests on every Python version with tox
   coverage             check code coverage quickly with the default Python
   docs                 generate Sphinx HTML documentation, including API docs
   servedocs            compile the docs watching for changes
   testrelease          package and upload a TEST release
   release              package and upload a release
   dist                 builds source and wheel package
   install              install the package to the active Python's site-packages
   dockerbuild          build docker image and store in local repository
   dockerpush           push image to dockerhub

Before running tests, please install ``pip install -r requirements_dev.txt``.


Needed files
------------

* bait list file: TSV file of baits used for AP-MS experiments
* edge list file: TSV file of edges for protein interaction network
* provenance: file containing provenance information about input files in JSON format (see sample provenance file in examples folder)


Usage
-----

For information invoke :code:`cellmaps_ppidownloadercmd.py -h`

**Example usage**

.. code-block::

   cellmaps_ppidownloadercmd.py ./cellmaps_ppidownloader_outdir --edgelist examples/edgelist.tsv --baitlist examples/baitlist.tsv --provenance examples/provenance.json


Via Docker
~~~~~~~~~~~~~~~~~~~~~~

**Example usage**

.. code-block::

   Coming soon...

Cite
-------

If you find this tool useful, please cite:

Lenkiewicz, J., Churas, C., Hu, M., Qian, G., Jain, M., Levinson, M. A., ... & Schaffer, L. V. (2025). Cell Mapping Toolkit: An end-to-end pipeline for mapping subcellular organization. Bioinformatics, 41(6), btaf205.

Credits
-------

This package was created with Cookiecutter_ and the `audreyr/cookiecutter-pypackage`_ project template.

.. _Cookiecutter: https://github.com/audreyr/cookiecutter
.. _`audreyr/cookiecutter-pypackage`: https://github.com/audreyr/cookiecutter-pypackage
.. _NDEx: http://www.ndexbio.org
