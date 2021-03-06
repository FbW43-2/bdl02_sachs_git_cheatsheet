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

Messages given by `git status`:
- >working tree clean

This means that no change happened in our project since our last `git commit`

- > nothing to commit

This means that no `git add` has happened yet, so there is nothing to commit.

- > changes not staged for commit

This means that we need to use `git add` to prepare some changes to be committed.

- `git log`

This command shows the commit log.

- `git diff`

Shows what changes have been done since the last `git add`.
- Lines marked in **red** are lines that were removed.
- Lines marked in **green** are lines that been added.



## 3. Initializing a git project

If any `git` command that we run that we run gives the following output:

> fatal: not a git repository (or any of the parent directories): .git

It means **we are not in a git project**.

In such case we can:

1. make sure we are in the right folder (and navigate to it if necessary)
2. initialize git

To initialize git, run

```
 git init
```

This command create an empty Git repo.
From now on we can make changes to our files and permanently save those changes.

## 4. Save changes

1. `git add .` (or `git add -A`)

`git add` tells Git that you want to include the latest changes in the next commit. However, changes ar not actually recorded until you run `git commit`.

2. `git commit -m "meaningful message here"`

A commit is the Git equivalent of a "save". Commits can be thought as a snapshot of our project at a given time.

You can also **quick commit** by using `git commit -am`

3. `git push` 

This command send the committed changes to the server. It is used to upload local repository content to a remote repository. 

## 5. Branching

1. `git branch`

List all of the branches in your repository. This is synonymous with git branch --list.

2. `get branch name`

Create a new branch called name. This does not check out the new branch.

3. `git branch -d`

Delete the specified branch. This is a “safe” operation in that Git prevents you from deleting the branch if it has unmerged changes.

4. `git branch -D`

Force delete the specified branch, even if it has unmerged changes. This is the command to use if you want to permanently throw away all of the commits associated with a particular line of development.

5. `git branch -m`

Rename the current branch to .

6. `git branch -a`

List all remote branches. 


## 6. Merging

### Assuming:
- we are on a separate branch. Note: it can be checked by running git 

- `branch -l`

- we have added and committed all our changes

we are now ready to merge our changes back to the main branch (which is usually master). It's time to:

1) Move to branch that you want to merge your changes on.

	- `git checkout master`
	
	after checking out on master, its always good practice to pull the latest changes from the origin with:
	- `git pull`
	
2) Merge the changes from the source branch (the one where we committed our changes on) with:

-	`git merge my-username/source-branch`

3) Save our changes to the server

 - `git push`