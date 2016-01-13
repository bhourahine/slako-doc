# README #

### What is this repository for? ###

This repository is for a draft standard for the Slater-Koster data required by the [DFTB](http://www.dftb.org) method

* This document covers versions 1.0 - 1.5 of the standard for the *slako* data
* v1.0
    * Original format for the data
* v1.1 
    * The [DFTB+](http://www.dftb-plus.info/) extended format for *f* electron data
* v1.15
    * The excited state extended data fields in the [mio-1-1](http://www.dftb.org/parameters/download/mio/mio-1-1/) and onsite corrected linear response data.
* v1.5
    * The transitional standard to include extra data inside the SK files that was previously user supplied to the code parsing these files.

### How do I get set up? ###

The spec is written in [reStructuredText](http://docutils.sourceforge.net/rst.html), the [sphinx](http://www.sphinx-doc.org/) generator can produce various document formats from this data.

### Contribution guidelines ###

The current version of the document is always in the master branch, and we follow Vincent Driessen's [master/develop](http://nvie.com/posts/a-successful-git-branching-model/) structure. See the [notes](https://bitbucket.org/dftbplus/fortyxima/src/a5fd8ea501528457db9f26d24bfc332fa0c597d1/doc/devel/guide/gitworkflow.rst?at=develop&fileviewer=file-view-default) on workflow with this structure.

### Who do I talk to? ###

* Initial document version from Ben Hourahine (benjamin.hourahine@strath.ac.uk)