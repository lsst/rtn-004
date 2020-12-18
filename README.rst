.. image:: https://img.shields.io/badge/rtn--004-lsst.io-brightgreen.svg
   :target: https://rtn-004.lsst.io
.. image:: https://github.com/rubin-observatory/rtn-004/workflows/CI/badge.svg
   :target: https://github.com/rubin-observatory/rtn-004/actions/

########################################################
Guidelines for Community Participation in Data Preview 0
########################################################

RTN-004
=======

This document provides an overview of the goals and policies for community participation in the Rubin Observatory pre-operations Data Preview 0 (DP0).

Links
=====

- Live drafts: https://rtn-004.lsst.io
- GitHub: https://github.com/rubin-observatory/rtn-004

Build
=====

This repository includes lsst-texmf_ as a Git submodule.
Clone this repository::

    git clone --recurse-submodules https://github.com/rubin-observatory/rtn-004

Compile the PDF::

    make

Clean built files::

    make clean


Extract milestones
------------------

A table of the relevant milestones and their dates is extracted from Jira into the ``milestones.tex`` file, which is committed as part of this repository.
To update the milestones table in ``milestones.tex``::

    make milestones.tex


Updating acronyms
-----------------

A table of the technote's acronyms and their definitions are maintained in the ``acronyms.tex`` file, which is committed as part of this repository.
To update the acronyms table in ``acronyms.tex``::

    make acronyms.tex

*Note: this command requires that this repository was cloned as a submodule.*

The acronyms discovery code scans the LaTeX source for probable acronyms.
You can ensure that certain strings aren't treated as acronyms by adding them to the `skipacronyms.txt <./skipacronyms.txt>`_ file.

The lsst-texmf_ repository centrally maintains definitions for LSST acronyms.
You can also add new acronym definitions, or override the definitions of acronyms, by editing the `myacronyms.txt <./myacronyms.txt>`_ file.

Updating lsst-texmf
-------------------

`lsst-texmf`_ includes BibTeX files, the ``lsstdoc`` class file, and acronym definitions, among other essential tooling for LSST's LaTeX documentation projects.
To update to a newer version of `lsst-texmf`_, you can update the submodule in this repository::

   git submodule update --init --recursive

Commit, then push, the updated submodule.

.. _lsst-texmf: https://github.com/lsst/lsst-texmf
