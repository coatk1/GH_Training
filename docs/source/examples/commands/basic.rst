=====
Basic
=====

.. sidebar:: Labels

    GitHub labels are a way to identify a type of issue or pull request.

Searching
=========
Search GH_Training in GitHub.

Create an issue
===============
* Go to issues
* Select First Issue
* Name-test in headers
* Fill in template
* Click labels and select another label
* Click projects and select project
* Click milestone and select class 1

Clone Repo
==========

::

    git clone git@github.com:coatk1/GH_Training.git

Then navigate to that repo.

::

    cd GH_Training

Git Commands
============

Pull from Remote
----------------

::

    git pull origin

Check Branch
------------

::

    git branch

Create a feature branch
-----------------------

::

    git checkout -b coatk1/first-issue

Make an edit
------------

Edit examples/class_list.md

Check Status
------------

::

    git status

Add file to stage
-----------------

::

    git add -A

Make a commit
-------------

::

    git commit -m "adding coatk1"

Push commit to feature branch
-----------------------------

::

    git push origin coatk1/first-issue

Check tag
---------

::

    git tag

Add tag
-------

Go up one in version.

E.g.

    If tag is 0.1.0, then you add 0.2.0.

::

    git tag -a 0.1.0 -m "coatk1 version"

Push tag
--------

::

    git push origin --tags

Submit a Pull Request
=====================
On GitHub you show see your branch.

Click open pull request.

* Name-test in headers
* Fill in template
* Click labels and select another label
* Click projects and select project
* Click milestone and select class 1

Click create pull request.
