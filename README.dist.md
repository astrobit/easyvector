# easyvector
A LaTeX package typesetting vector data in a easy to use way.

# License
Copyright (C) 2020 by Brian W. Mulligan <bwmulligan@astronaos.com>
-----------------------------------------------------------

This file may be distributed and/or modified under the conditions of
the LaTeX Project Public License, either version 1.3c of this license
or (at your option) any later version. The latest version of this
license is in:

http://www.latex-project.org/lppl.txt

and version 1.3c or later is part of all distributions of LaTeX
version 2006/05/20 or later.

# Dependencies
  - the `amsmath` package for latex

# Build Dependencies
- some LaTeX distribution.
- `hyperref` package for LaTeX

# Files
```
    makefile                GNU makefile to simplify building and installation 
                            on linux
    README.md               This file.
    CHANGELOG.md            List of changes
    easyvector.ins          The installer file
    easyvector.dtx          The package code and documentation
    easyvector.pdf          The package user manual
```

# Building the Package
## Linux / Mac using make and xelatex
1. `make`

## Otherwise
1. Run `latex` on `exam-random.ins` to create the `.sty` file. e.g. 
`latex exam-random.ins`.
1. The following steps apply only if you want the documentation (recommended).
  1. Run `latex` on `exam-random.dtx` to create the `.pdf` file. e.g. 
`xelatex exam-random.pdf`.
  1. Run `makeindex` to create the index, e.g. 
`makeindex -s gind.ist -o exam-random.ind exam-random.idx`.
  1. Run `makeindex` to create the change log, e.g. 
`makeindex -s gglo.ist -o exam-random.gls exam-random.glo`.
  1. Run `latex` on `exam-random.dtx` to create the `.pdf` file with index and 
change log. e.g. `xelatex exam-random.pdf`.
  1. Run `latex` on `exam-random.dtx` to get the labels sorted out. e.g. 
`xelatex exam-random.pdf`.

Instructions that might help can be for windows can be found at 
[this post on StackExchange]
(https://tex.stackexchange.com/questions/369921/loading-packages-with-ins-and-dtx-files).

# Installation
First build the project as described above.

## For a single project
1. Copy the `exam-random.sty` into your project where your `.tex` files are
 located.

## for all users and projects
### Linux / Mac using make and xelatex
1. `make localinstall`

### Otherwise
Instructions that might help can be for windows can be found at 
[this post on StackExchange]
(https://tex.stackexchange.com/questions/369921/loading-packages-with-ins-and-dtx-files).
1. Figure out where your LaTeX local packages are installed.
1. Create a directory named `exam-random` in that location.
1. Copy the `.sty` file into the directory you just created.
1. Figure out where your LaTeX local package documentation is installed.
1. Create a directory named `exam-random` in that location.
1. Copy the `.pdf` file into the directory you just created.
1. Run `texhash` or the equivalent to let LaTeX know the package is there.


# Uninstallation

### Linux / Mac using make
1. `make localuninstall`
### Otherwise
1. Figure out where your LaTeX local packages are installed.
1. Delete the directory named `exam-random` in that location.
1. Figure out where your LaTeX local package documentation is installed.
1. Delete the directory named `exam-random` in that location.
1. Run `texhash` or the equivalent to let LaTeX know the package is gone.

