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

# Distributable Files
The following distributable files can be created as described below.
```
    easyvector.tar.gz       Tarball containing package, documentation, and 
                            README.dist.md, CHANGELOG.dist.md, and makefile.dist
                            (renamed without .dist)
    easyvector.zip          Zip file containing package, documentation, and 
                            README.dist.md, CHANGELOG.dist.md, and makefile.dist
                            (renamed without .dist)
```
Each distributable file contains the following:
```
    makefile                GNU makefile to simplify building and installation
                            on linux
    README.md               This file.
    README.dist.md          The readme file to be disributed with the package
    CHANGELOG.md            List of changes
    CHANGELOG.dist.md       The change log file to be disributed with the 
                            package
    exam-random.ins         The installer file
    exam-random.dtx         The package code and documentation
    exam-random.pdf         The package user manual
```
## Building
### Linux / max
1. `make` to generate the package
### Windows or if make doesn't work

Instructions that might help can be for windows can be found at 
[this post on StackExchange]
(https://tex.stackexchange.com/questions/369921/loading-packages-with-ins-and-dtx-files).
1. Run `latex` on exam-random.ins
1. Run `latex` of some form (e.g. `xelatex`) on `exam-random.dtx`
1. Run `makeindex -s gind.ist -o exam-random.ind exam-random.idx`
1. Run `makeindex -s gglo.ist -o $(pkgname).gls $(pkgname).glo`
1. Run `latex` of some form (e.g. `xelatex`) on `exam-random.dtx` to create the 
index
1. Run `latex` of some form (e.g. `xelatex`) on `exam-random.dtx` to get the 
right links and labels.

## Creating distributions

### Linux / max
To create a disribution on linux (or mac?)
1. Build the package as described above.
1. `make dist` to generate the distributable tarball and zip file

### Windows or if make doesn't work
1. Build the package as described above.
1. Create a directory named `exam-random`
1. Copy `exam-random.ins`, `exam-random.dtx`, `exam-random.pdf`, and 
`CHANGELOG.md` into the directory
1. Copy `README.dist.md` into the directory as `README.md`
1. Copy `makefile.dist` into the directory as `makefile`
1. Create a `.zip` file from the directory.

# Installation
## Linux (and mac?)
### For a single project
1. Build the package as described above.
1. Copy the `exam-random.sty` into your project where your `.tex` files are 
located.
### for all users and projects
1. Build the package as described above.
1. `make localinstall` to generate the package.


## Windows or if the above doesn't work for linux/max
1. Build the package as described above.
1. Instructions that might help can be for windows can be found at 
[this post on StackExchange]
(https://tex.stackexchange.com/questions/369921/loading-packages-with-ins-and-dtx-files).
1. Figure out where your LaTeX local packages are installed.
1. Create a directory named `exam-random` in that location.
1. Copy `exam-random.sty` into the new directory.
1. Figure out where your LaTeX local package documentation is installed.
1. Create a directory named `exam-random` in that location.
1. Copy `exam-random.pdf` into the new directory.
1. Run `texhash` or the equivalent to let latex know the package is there.

# Uninstallation

## Linux (and mac?)
1. `sudo make localuninstall`

## Windows or if the above doesn't work for linux/max
1. Figure out where your LaTeX local packages are installed.
1. Delete the directory named `exam-random` in that location.
1. Figure out where your LaTeX local package documentation is installed.
1. Delete the directory named `exam-random` in that location.
1. Run `texhash` or the equivalent to let LaTeX know the package is gone.

