# Git commands cheatsheet: the most useful git commands

## 1. Navigate to your git project folder


Use `cd` to move between folders. E.g:


```
cd workspace
cd bdl02_sachs_git_cheatsheet
```

## 2. Check the status of the project

I can use this **anytime** to inspect my project.

- `git status` 

With `git status` I can see if some changes happened and if some files are ready to be committed. It gives me an overview of the project at that specific moment in line.


- `git log`
- `git diff`

## 3. Initializing a git project

If any `git` command that we run that we run gives the following output:

> fatal: not a git repository (or any of the parent directories): .git

It means we are not in a git project.

In such case we can:

1. make sure we are in the right folder (and navigate to it if necessary)
2. initialize git

To initialize git, run

```
 git init
```

This command create an empty Git repo.
From now on we can make changes to our files and permanently save those changes.
