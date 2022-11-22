# Git

## Overview

What is Git?
Git is a command line tool for version control and teamwork. It's distributed (it has the ability to work across multiple machines).

## Concepts

### Repository

A folder that is under version control. The history of all changes is recorded. You can keep multiple versions of your data at the same time.

-   the thing that makes a repository a repository is the '.git' folder
-   `git init` is the command you use to create a new repository in a folder

### Staging && Commits

A commit is a point in time. A checkpoint. One version of your data.

-   You have the stage changes before you can commit them (mark them as included in the next checkpoint/commit).
-   You can stage changes with the `git add .` command
-   You can commit staged changes with the `git commit` command
-   If you don't want to use the default git editor (normally VIM), you can use the -m flag like `git commit -m "this is my commit message"`
-   `git reset` will reset the staging
-   `git reset --hard` will restore everything to the state of the current commit (which gets rid of all changes since then)

### Branches & Checking out

A branch is a pointer. It's a name that points at a commit.

-   You can checkout specific commits by using the command `git checkout $COMMIT_HASH`
-   You can checkout branches with `git checkout $BRANCH_NAME`. This does two things: it takes you to the commit that the branch is currently pointing at, and makes the branch pointer follow you when you make new commits.
-   You can create new branches that will start off pointed at where you currently are by using the command `git branch $NEW_BRANCH_NAME`
-   To see all available branches, type `git branch` or `git branch -a`

### Status & Log

-   You can type `git status` to see what's going on/where things are at.
-   You can type `git log` to see the history of the timeline your currently on. Use the `--graph` flag for a graph version of the timeline that visually shows the relationships between commits.

### Local vs. Remote

You have a local version of a repository on your machine. The remote server (Github) has a version on it's machine(s), and they may not be the same.
