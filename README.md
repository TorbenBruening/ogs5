[![Tag](https://img.shields.io/github/tag/ufz/ogs5.svg?style=flat-square)](https://github.com/ufz/ogs5/releases)
[![BSD License (modified)](http://img.shields.io/badge/license-BSD-blue.svg?style=flat-square)](https://github.com/ufz/ogs5/blob/master/LICENSE.txt)
[![Travis](https://img.shields.io/travis/ufz/ogs5.svg?style=flat-square)](https://travis-ci.org/ufz/ogs5)
[![Shippable](https://api.shippable.com/projects/553ff718edd7f2c052d6b180/badge?branchName=develop)](https://app.shippable.com/projects/553ff718edd7f2c052d6b180/builds/latest)

# OGS-5 #

- General homepage: http://www.opengeosys.org
- Wiki: https://svn.ufz.de/ogs

## Quickstart ##

``` bash
cd [source-directory]
mkdir build
cd build
cmake ..
```

Open the Visual Studio solution which was created in the build-directory or just type `make` on Linux.

# Using Git and GitHub #

Following ["A successful Git branching model"](http://nvie.com/posts/a-successful-git-branching-model/), we suggest to have the following two main branches
- ***master*** - the main branch where the source code of HEAD always reflects the latest official codes (i.e. trunk in SVN repository)
- ***development*** - the main branch where the source code of HEAD always reflects a state with the latest delivered development changes for the next release.

To implement new features, every developer
1. forks this repository to have their own (your repository is still private)
2. makes a branch from master or development branch, and implement their stuff
3. pushes the local branch to its GitHub repository
4. makes a pull request from its GitHub repository to development branch in the `envinf/ogs5-trunk` repository

Once the development branch is ready to release a new version (this can also be done by one of the OGS core developers)
1. merge the development branch into master
2. push all new commits in master to the SVN repository using `git svn dcommit`

