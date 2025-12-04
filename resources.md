# Resources

```{contents}
:local:
```

## Docs as Code

### Getting started

This website is created using the Sphinx static site generator. Every page has
a source link that will show you the syntax used to create it. You can also
browse the source in the [github repo](https://github.com/kevinputnam/kevinputnam.github.io). GitHub provides a lot of free
resources that make automating workflows and collaborating a lot easier.

* Issue tracking and Pull request management
* Forking (making a personal copy of a repository)
* GitHub Actions

All of which are the same workflows that both professional and open source
teams use to develop software. And it's all free.

If you do decide to look at the source repository, it might seem pretty overwhelming. The most important thing to know is where to start.

1. `index.md`
2. `conf.py`

These are the only 2 files needed to start building a Sphinx website. 

The `index.md` or `index.rst` is the root page for the hierarchy of the site.
Every other page will link back to it eventually through cascading `toctree`
directives. These look like (markdown):

```` md
```{toctree}
page1
page2
```
````

or like this (reStructuredText):

``` rest
.. toctree::

   page1
   page2
```

`page1` could have it's own `toctree` and so on creating the nested hierarchy
that will ultimately be reflected in the site's table of contents. 

The `conf.py` is a Python file that contains the metadata configuring the theme
and other information required by Sphinx to build the docs. 

At a bare minimum your `conf.py` could look like this:

``` python
project = 'Name of Project'
copyright = '2025, Name of Owner'
author = 'Name of Author'

html_theme = 'name_of_sphinx_theme'

```

The good news is that once Sphinx is installed, it is smart enough to create
all of this automatcally using the `sphinx-quickstart` command. Running it in
the directory where you want to create a new project will start a short
interactive session that prompts you for some basic information and creates a
very basic templated Sphinx project.

``` bash
sphinx-quickstart
```

### Reference

Python
: Popular programming language that must be installed to run Sphinx.

Sphinx
: A static site generator for technical documentation that was created
  to document the Python programming language.

reStructuredText
: A human readable text markup language that is the native markup for Sphinx.
  It is defined by the Docutils project. There are also Sphinx specific
  directives like the `toctree` directive.

Markdown
: Another human readable text markup language that is arguably far more
  popular than reStructuredText. 

Directives
: Define blocks that are handled in a particular way by Sphinx. They can
  also be nested, so you might have an `image` or `codeblock` inside of
  a `note`.

Roles
: Define inline text that is handled in a specific way by Sphinx. They
  cannot be nested. 


```{note}
Sphinx requires the use of the Command Line Interface (CLI).
```

For those that are interested in diving deeper:

* [Installing Python (python.org)](https://wiki.python.org/moin/BeginnersGuide/Download)
* [Installing Sphinx (sphinx-doc)](https://www.sphinx-doc.org/en/master/usage/installation.html)
* [Sphinx Specific reStructuredText (sphinx-doc)](https://www.sphinx-doc.org/en/master/usage/restructuredtext/index.html)
* [restructedText Specification (docutils)](https://docutils.sourceforge.io/docs/ref/rst/restructuredtext.html)
* [reStructuredText Directives (docutils)](https://docutils.sourceforge.io/docs/ref/rst/directives.html)
* [reStructuredText Roles (docutils)](https://docutils.sourceforge.io/docs/ref/rst/roles.html)
* [GitHub Flavored Markdown (github)](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)
* [Sphinx Specific Markdown (Myst)](https://myst-parser.readthedocs.io/en/v0.15.1/sphinx/intro.html)