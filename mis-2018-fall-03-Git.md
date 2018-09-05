# IMSE 4410 Fall 2018 - Module 1

*IMSE 4410/7410 Management Information Systems Design (MIS)*

Material Copyright 2017, 2018 by Timothy Middelkoop. Sourcecode licensed under the Apache License, Version 2.0. Documentation licensed under CC by SA 3.0.

## Topic 3 - Development Process and Community

### Git and Revision Control

Git Workflow

### Git Workflow
A git workflow takes changes in an editor and provides a mechanism to create publishable "work" in the form of a "Work Package" in project management speak.  We can see this as a "stack" as follows.

1. Community Repository (gitlab.missouri.edu)
2. Staging Repository (topic branches, maintainers)
3. Machine/Local repository
4. project index or staging area
5. project local filesystem
6. editor (unsaved changes)

Moving up and down this stack is accomplished by a series of git commands (presented in class and below).  Between 1 and 2 is also social.

### Git Workflow Hands-On

Below is the workflow to edit and commit a file.  This is just an example, please be sure to replace many of the example values with actual values that pertain to your environment.

For a new system or repository (if you only configure locally) update your name and email to ensure the commit information is correct.  Optionally set your preferred editor (nano in this case).
```
git config --global user.name "First Last"
git config --global user.email pawprint@missouri.edu
git config --global core.editor nano
```

Clone your project into a folder
```
git clone git@gitlab.missouri.edu:middelkoopt/welcome.git
cd welcome
```

At many of the steps throughout the process run the following to see what is going on and your changes.
```
git status
git diff
git diff -r HEAD
```

Edit the ReadMe.md file.
```
nano ReadMe.md
```

Save and exit.  Now view the changes and add the changes to the index.
```
git diff
git add ReadMe.md
```

This is where you would change other files.  When done commit.  First view what is "staged" in the index with

```
git status
```

Then see what your "commit" will be 

```
git diff -r HEAD
```

From this determine a good description (not "changes and updates") and commit the changes.

```
git commit -m "Fix spelling"
```

Now the changes are in the local repository and ready to be "published" to gitlabs (vcs.rnet.missouri.edu).  View the commit in the logs (press 'q' to exit)

```
git log
```

And push to the remote with the following:

```
git push origin master
```

Also verify that the changes have been pushed and there are no more changes.  The last commit is also printed.  This is what is "proof" of your work, and should be submitted to the Homework assignment along with your repository URL.

```
git status
git rev-parse HEAD
```

### Homework
Using the hands-on instructions and the documentation complete the following homework:

Homework 1-3-1: Git
  1. Edit the file "ReadMe.md" or other file in your class repository (`git@gitlab.missouri.edu:$PAWPRINT/mis-$PAWPRINT-$FIRST-$LAST.git`) cloned on `clark.rnet.missouri.edu`.
  2. Commit those changes and push them to `gitlab.missouri.edu`
  3. Run `git log` and paste the last commit/revision/hash or the output of `git rev-parse HEAD` into the assignment along with your repository URL to receive a grade for example:
	```
	1a9c8bc7e3011f563d2370c35f592fc6c987bab4
	git@gitlab.missouri.edu:middelkoopt/welcome.git
	```

Homework 1-3-2: Git Assignments
  1. If you have not already done so create a git repository on
     `gitlab.missouri.edu` and share it with the instructors and TA.
  2. Ensure that in the commit log the "Author:" line contains your
     full name and email address and fix if need be.
  3. Clean up your repository (removing any extra test files etc.) and commit the changes.
  4. Create a folder called `homework-1-3` in the project and create a
     file called `homework-1-3-shell.txt` that contains the *text* of
     the commands and results (including the prompt) of the following:
	 1. Create a file called `fruit.txt` in the `homework-1-3` folder
        with a number of fruit names, one on each line.
	 2. Display this file to the console/screen (hint `cat`).
	 3. Count the number of fruit in this file using a pipe (`|`).
	 4. Sort the fruit into a second file named `fruit-sorted.txt`
        (hint: redirection).
	 5. Show the changes to `fruit.txt` and `fruit-sorted.txt` that
        you are about to commit and then commit these files to the
        repository.
	 6. What is the **commit** id of the previous step.
	 7. Commit the *text* of the commands and results (including the
        prompt) of the previous steps stored in the
        `homework-1-3-shell.txt` file.
  6. Push all the commits to the `gitlab.missouri.edu` repository and submit the most
     recent (HEAD) commit-id and the `gitlab.missouri.edu` repository URL to the course
     assignment 'Homework 1-3'.

### Reading
Read Chapter 9 of the text.  Read the introduction material of the references and as much as you wish.
* ISBB Chapter 9 - People https://bus206.pressbooks.com/chapter/chapter-people/

### References
* Pro Git book https://git-scm.com/book/en/v2
* Software Carpentry - Git http://swcarpentry.github.io/git-novice/
* GitLabs Markdown https://docs.gitlab.com/ee/user/markdown.html
