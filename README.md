# git-populate

## Contents

-  [Description](#description)
-  [Requirements](#requirements)
-  [Installation](#installation)
   -  [System-Level Install](#system-level-install)
   -  [User-Level Install](#user-level-install)
-  [Usage](#usage)
   -  [Configuration Files](#configuration-files)
   -  [Template Files](#template-files)
-  [Versioning](#versioning)
-  [Copyright and License](#copyright-and-license)
   -  [The MIT License](#the-mit-license)


---
## Description

Bash script to pre-populate a new repo with common meta files

[TOP](#contents)

---
## Requirements

The only requirement for this package is a [Bash](https://www.gnu.org/software/bash/) shell.

[TOP](#contents)

---
## Installation

Execute the "install" script. The files are installed in either the system-level directories, if executed as root, or the user-level directories.

### System-Level Install

A system-level install will be in:

-  `$XDG_DATA_DIRS/chindraba/git-populate/` and
-  `$XDG_CONFIG_DIRS/chindraba/git-populate/` and
-  `/usr/local/bin/` will have a symlink to the `git-populate` script

### User-Level Install

A user-level install will be in:

-  `$XDG_DATA_HOME/chindraba/git-populate/` and
-  `$XDG_CONFIG_HOME/chindraba/git-populate/` and
-  `$HOME/bin/` will have a symlink to the `git-populate` script

As a convenience, if installed as root, the user-level directories will be created, and left empty.

[TOP](#contents)

---
## Usage

While in the repo root directory, execute `git-populate` or `git populate`.

### Configuration Files

The configuration file `git-populate.conf` will be searched for as:

-  `$XDG_CONFIG_DIRS/chindraba/git-populate/git-populate.conf`
   -  Global common and default settings
-  `$XDG_CONFIG_HOME/chindraba/git-populate/git-populate.conf`
   -  Per-user common and default settings
-  `$PWD/git-populate.conf`
   -  Per-repo data and default setting overrides

The configuration file found at each level will be loaded. Global settings will be overridden by per-user settings which are, in turn, overridden with per-repo settings.

### Template Files

Template files used for building the new meta files are loaded from:

-  `$PWD/`
   -  Per-repo templates
-  `$XDG_DATA_HOME/chindraba/git-populate/`
   -  Per-user templates
-  `$XDG_DATA_DIRS/chindraba/git-populate/`
   -  Global templates

The first template found will be used, local first, global last.

[TOP](#contents)

---
## Versioning

The **git-populate** project uses Semantic Versioning v2.0.0.

[Semantic Versioning](https://semver.org/spec/v2.0.0.html) was created by [Tom Preston-Werner](http://tom.preston-werner.com/), inventor of Gravatars and cofounder of GitHub.

Version numbers take the form X.Y.Z where X is the major version, Y is the minor version and Z is the patch version. The meaning of the different levels are:

* Major version increases indicates that there is some kind of change in the API (how this program works as seen by the user) or the program features which is incompatible with previous version

* Minor version increases indicates that there is some kind of change in the API (how this program works as seen by the user) or the program features which might be new, while still being compatible with all other versions of the same major version

* Patch version increases indicate that there is some internal change, bug fixes, changes in logic, or other internal changes which do not create any incompatible changes within the same major version, and which do not add any features to the program operations or functionality

[TOP](#contents)

---
## Copyright and License

The MIT license applies to all the code within this repository.

Copyright © 2020  Chindraba (Ronald Lamoreaux)

   <[projects@chindraba.work](mailto:projects@chindraba.work?subject=Project%20git-populate)>

- All Rights Reserved

### The MIT License

    Permission is hereby granted, free of charge, to any person
    obtaining a copy of this software and associated documentation
    files (the "Software"), to deal in the Software without restriction,
    including without limitation the rights to use, copy, modify, merge,
    publish, distribute, sublicense, and/or sell copies of the Software,
    and to permit persons to whom the Software is furnished to do so,
    subject to the following conditions:

    The above copyright notice and this permission notice shall be
    included in all copies or substantial portions of the Software

    THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND,
    EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF
    MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGE-
    MENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE
    FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF
    CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION
    WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

[TOP](#contents)
