---
author: "Geo V L"
date: 2018-05-29
linktitle: How to generate submodules
nomenu:
  main:
    parent: tutorials
next: /tutorials/github-pages-blog
prev: /tutorials/automated-deployments
title: How to generate submodules
tags : [
    "git",
    "development",
]
weight: 10
image: img/writing.jpg
authorAvatar: hugo-logo.png
---

Suppose we have a project named 'flower' with different people working on it. Suppose  some other team already created a repository named 'Rose' which can add as a sub directory under our existing 'flower' repository.

``` 
git submodule add https://github.com/<user>/rose rose
```
At this point, you’ll have a rose folder inside flower, but if you were to check inside that folder, depending on your version of Git, you might see … nothing.
Newer versions of Git will do this automatically, but older versions will require you to explicitly tell Git to download the contents of rose:

```
git submodule update --init --recursive
```
If everything looks good, you can commit this change and you’ll have a rose folder in the flower repository with all the content from the rose repository.
On GitHub, the rose folder icon will have a little indicator showing that it is a submodule

And clicking on the rose folder will take you over to the rose repository.

Now you’ve embedded the rose repository inside the flower repository. You can interact with all the content from rose as if it were a folder inside flower (because it is).

On the command-line, Git commands issued from flower (or any of the other folders) will operate on the “parent repository”, flower, but commands you issue from the rose folder will operate on just the rose repository

```
pwd flower  ##move to flower directory
git log ##will list log of flower repository
cd rose ##change directory to rose
git log ##will list log of rose repository
```

For cloning a git repository with all its submodules clone it with --recursive like the following

```
git clone --recursive <repo> <foldername>
```






#### Reference

* [Git Sub Modules](https://git-scm.com/book/en/v2/Git-Tools-Submodules) 
* [Working with submodules](https://blog.github.com/2016-02-01-working-with-submodules/)