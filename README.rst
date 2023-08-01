Template for the Read the Docs tutorial
=======================================

This GitHub template includes fictional Python library
with some basic Sphinx docs.

Read the tutorial here:

https://docs.readthedocs.io/en/stable/tutorial/

1) pip install --upgrade --no-cache-dir pip setuptools
2) pip install --upgrade --no-cache-dir pillow mock==1.0.1 alabaster==0.7.13 commonmark==0.9.1 recommonmark==0.5.0 sphinx sphinx-rtd-theme readthedocs-sphinx-ext<2.3
3) python -m sphinx -T -E -b html -d _build/doctrees -D language=vi . _build/html
