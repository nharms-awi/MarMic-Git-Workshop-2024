# Git Workflow

There are many various conventions on how to work with git. Usually participants or repository maintainers agree upon a workflow. This workflow defines how to work with branches, how to merge them, and how to handle releases. But how you work locally is usually the same for all workflows.
You have a local repository on your machine. You can work on it and commit changes. You can also create branches and merge them. Until you use the `git push` command, all your changes are only stored locally. Mor on this in [Remote Repositories](07_Remote%20Repositories.md). Lets have a look at the basic workflow.

## An first example
Let's say you're working on a project called "my-project" and you want to use Git to track the changes you make to the project.

First, navigate to the directory where you want to create the project and initialize a new Git repository using the `git init` command. This will create a new `.git` directory in the current working directory, which contains all the necessary files for the version control system.

```bash
$ cd my-project
$ git init
```

Now let's say you've made some changes to the files in the project. Use the `git status` command to see the changes that have been made in the working directory.

```bash
$ git status On branch master

No commits yet

Untracked files: (use "git add <file>..." to include in what will be committed)

file1.txt 
file2.txt 
file3.txt

nothing added to commit but untracked files present (use "git add" to track)
```

To include the changes in the next commit, use the `git add` command to add the changes to the staging area.

```bash
$ git add file1.txt file2.txt file3.txt
```

Now use the `git status` command again to see the changes that have been added to the staging area.

```bash
$ git status On branch master

No commits yet

Changes to be committed: (use "git rm --cached <file>..." to unstage) 
new file: file1.txt 
new file: file2.txt 
new file: file3.txt
```

Finally, use the `git commit` command to create a new commit with the changes in the staging area.

```bash
$ git commit -m "Initial commit"
```

You can use `git log` command to see all the commits made in the project.

```bash
$ git log
commit 9a5c1a5b5f5b5a5c5c5b5f5a5c5a5b5a5b5f5c5b5a5c5a5b5a5b5f5c5b5a5c
Author: Nico Harms <nico.harms@awi.com>
Date: Mon May 10 11:00:00 2021 +0100

 Initial commit

```

Another useful command when working with branches is `git log --all --graph --oneline`. This command shows a graphical representation of the commit history, including all branches and commits.

The `--all` flag shows commits from all branches and not just the current one. The `--graph` flag displays the commits in a visually pleasing format that allows for a quick overview of the branching and merging in the repository. And the `--oneline` flag shows the commits in a compact format, displaying only the first line of the commit message and the commit hash.

This command can be very helpful in understanding the history of a repository and keeping track of what changes were made and when. It also allows you to quickly identify merge conflicts and find the source of bugs.

You can also add `--decorate` to show the branches and tags, and `--color` to colorize the output.

By using these commands, you've created a new Git repository and made your first commit. This example project illustrates the basic Git commands and how they can be used to track changes to a project.

You can continue to make changes to the files in the project and use the `git add` and `git commit` commands to track the changes. It is also a good practice to use a meaningful message to describe the changes you've made in your commit.

Additionally, you can use the `git diff` command to see the differences between the working directory and the latest commit, and the `git show` command to see the details of a specific commit.

```bash
$ git diff 
$ git show 9a5c1a5b5f5b5a5c5c5b5f5a5c5a5b5a5b5f5c5b5a5c5a5b5a5b5f5c5b5a5c
```
