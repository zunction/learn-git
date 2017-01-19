# Branching

## What is branching?
If you think what we did in [Basics](https://github.com/zunction/learn-git/blob/master/BASICS.md) is all what Git is all about, then you are so wrong :joy:. Here is where we shall learn about the main selling point of Git, which is its version control capabilities. What do I mean by version control? Suppose you are working on writing `mycode.py` and you are very pleased with it. But after reading some papers or from some other references, you decide that you want to implement your code in a more efficient manner, then perhaps you will make a copy of `mycode.py` and rename it `mycode1.py`, after which for anything new you add to your code you will have `mycode2.py`, `mycode3.py`, ... Eventually you will forget what changes are made to which versions and you become frustrated, either from **having too many versions of your file** or **deleting the wrong version and emptying you recycling bin** :scream: That's why we have branches, each branch to contain a particular version of your work.

### How to create a branch

For any repository that is created, the default branch is called `master`. By typing `git branch`, it shows you all the available (local) branches in that repository. Thus if there are no other branches, then you see `* master` which means that there is only one branch `master` and the `*` means that you are currently on that branch.

```git
$ git branch
* master
```
 To create a branch, say with branch name `v1.1` you type
 ```git
 $ git branch v1.1
 $ git branch
 * master
   v1.1  
 ```
there is nothing printed or prompted when creating a branch, but when you `git branch` again, you will see
```git
$ git branch
* master
  v1.1  
```
which shows your available branches `master` and `v1.1` with you currently on the branch `master`. To switch to your newly created branch just

```git
$ git checkout v1.1
M	BRANCHING.md
Switched to branch 'v1.1'
```

and once you are on branch `v1.1` you are free to make any wild or irreversible changes without any worries; should you work on branch `v1.1` be messed up beyond repair, you always have the good and working version `master` to fall back to.

Below is a chunk of text about Git and you would like to create a version of this file without it. In the raw `.md` file, this chunk of text starts and ends with `---`. By using the branching technique that we learnt above, create a new branch `v1.1` (or any branch name that you like) and remove this chunk of text (including the `---`).
---

The Git feature that really makes it stand apart from nearly every other SCM out there is its branching model.

Git allows and encourages you to have multiple local branches that can be entirely independent of each other. The creation, merging, and deletion of those lines of development takes seconds.

This means that you can do things like:

Frictionless Context Switching. Create a branch to try out an idea, commit a few times, switch back to where you branched from, apply a patch, switch back to where you are experimenting, and merge it in.
Role-Based Codelines. Have a branch that always contains only what goes to production, another that you merge work into for testing, and several smaller ones for day to day work.
Feature Based Workflow. Create new branches for each new feature you're working on so you can seamlessly switch back and forth between them, then delete each branch when that feature gets merged into your main line.
Disposable Experimentation. Create a branch to experiment in, realize it's not going to work, and just delete it - abandoning the work—with nobody else ever seeing it (even if you've pushed other branches in the meantime).
---

Hint: Remember to `add` and `commit` for the changes to take place (locally)!


To be continued...
