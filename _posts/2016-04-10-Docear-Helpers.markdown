---
layout: default
github: https://github.com/schlichtanders/docear_helpers
keywords: latex, mindmap, docear, python
description: Commandline helper functionalities to simplify working with Docear.
---

docear_helpers currently encompass the following utilities. I especially
recommend ``init`` and ``autorename``.

- init : initialize the current directory as a docear project. A references.bib
    file is created if not existent, where all latex references are stored.

- move : move / rename docear projects to another directory

- autorename : rename all pdf files according to their meta-data in
  references.bib (concerns all pdfs listed in the given docear project).
  This means that you can rename a "id034789234.pdf" file to
  "AuthorName(Year)PaperTitle.pdf" by one command, without breaking anything

- open_user_settings : opens the user.settings file in the default text editor
