# Git Workflow

In this chapter, we'll delve into the fundamental concepts of version control and explore the basic Git workflow. Understanding these concepts is crucial for effectively managing your project's codebase and collaborating with others.

Version control systems, such as Git, provide a structured approach to tracking changes in your codebase. Before we dive into the Git workflow, let's grasp some key ideas:

Git operates with a local repository on your machine. You can work on it, make changes, and commit those changes. Until you use the `git push` command, all your changes are stored locally. (More on this in [Remote Repositories](07_Remote%20Repositories.md).)
Now, let's explore the basic Git workflow using an example.

## An Example Workflow

Imagine you're working on a project called "my-project," and you want to use Git to track the changes you make. Follow these steps to get started:

1. Navigate to the directory where you intend to create your project, and initialize a new Git repository using the `git init` command. This command will create a `.git` directory in the current working directory, housing all the necessary files for version control.

```bash
$ mkdir my-project
$ cd my-project
$ git init
```

2. After initializing the repository, make changes to the project files. You can use the `git status` command to see the changes made in the working directory.

```bash
$ git status 
On branch main

No commits yet

nothing to commit (create/copy files and use "git add" to track)
```

This command will show you the current status of your project, including any untracked files.
Create some files in the project directory and use the `git status` command again to see the changes.

3. To include your changes in the next commit, use the `git add` command to add them to the staging area. This step prepares your changes for the commit.

```bash
$ git add file1.txt file2.txt file3.txt
```

4. Check the status again with `git status` to confirm that your changes are now in the staging area.

```bash
$ git status On branch master

No commits yet

Changes to be committed: (use "git rm --cached <file>..." to unstage) 
new file: file1.txt 
new file: file2.txt 
new file: file3.txt
```
You'll see the changes listed under "Changes to be committed."

5. Finally, commit your changes using the `git commit` command. Be sure to provide a meaningful commit message describing the changes made.

```bash
$ git commit --message "Initial commit"
```

6. To view the commit history, you can use the `git log` command:

```bash
$ git log
commit 9a5c1a5b5f5b5a5c5c5b5f5a5c5a5b5a5b5f5c5b5a5c5a5b5a5b5f5c5b5a5c
Author: Nico Harms <nico.harms@awi.com>
Date: Mon Jan 29 11:00:00 2024 +0100

 Initial commit

```

This command displays a list of commits along with their unique identifiers and commit messages.

7. For a more visual representation of the commit history and branches, you can use the following command:

```bash
git log --all --graph --oneline
```

This command shows a graphical representation of the commit history, including all branches and commits. It can be extremely useful in understanding the project's history and identifying issues.

By following these steps, you've successfully created a Git repository, made your initial commit, and explored some essential Git commands. Remember that Git offers a powerful set of tools for managing your codebase, tracking changes, and collaborating with others.


8. Additionally, you can use the `git diff` command to see the differences between the working directory and the latest commit, and the `git show` command to see the details of a specific commit.

```bash
$ git diff 
$ git show 9a5c1a5b5f5b5a5c5c5b5f5a5c5a5b5a5b5f5c5b5a5c5a5b5a5b5f5c5b5a5c
```
