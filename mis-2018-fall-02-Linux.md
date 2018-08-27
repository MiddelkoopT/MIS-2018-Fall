# IMSE 4410 Fall 2018 - Module 1

*IMSE 4410/7410 Management Information Systems Design (MIS)*

Material Copyright 2017, 2018 by Timothy Middelkoop. Sourcecode licensed under the Apache License, Version 2.0. Documentation licensed under CC by SA 3.0.

## Topic 2 - Computational Systems

And in the beginning there was git. `git init`

### Git

We will first create a `gitlab.missouri.edu` repository and clone it.

Go to Mizzou's Gitlabs server at https://gitlab.missouri.edu and login using your Pawprint (SSO) and password (use the default LDAP method).

Create a new private project called `mis-login-First-Last` where login is your pawprint, for example I would be `mis-middelkoopt-Timothy-Middelkoop`.

Make sure your gitlabs project visibility is set to private. To make it priviate navigate to Settings -> Sharing and Visibility -> Project Visibility -> Private.

Share this project with myself `@middelkoopt`, Dr. Srinivas `@srinivassh` and the TA `@nzqpc` with the access "Reporter".

Create a ssh key by logging into `clark.rnet.missouri.edu` and running the following (make sure to create a strong passphrase):

```
$ cd ~
$ ssh-keygen
$ cat .ssh/id_rsa.pub
```

Copy the public key shown by the `cat .ssh/id_rsa.pub` command, it should look similar to this:

```
ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABAQDuSqEsyPw9gULRil72VHCrpw/+dmKpcPp50rr7YypK95T4US7eiwOqX0VJANKde77MjAy7+rgbjNJDbO6V3VLSJxOlUWS4Vj7wBF1j/u7EUnjdp2mMMHA2zu7sIwbjp+tjt44MYxK1P/RbB1sXwwIOUvxOZjG1uKsO/Xze6GX3l2pxkb+aDiZ+i8JZdnwC9+0ZFwUVBhcXO90IHapz1rppTFO9K1LRJtj/aiSOcD2E0mphLLDD7Z5l9EDK0tijYz/fB2F0lUFlF1isjKAGkW+Uq5CzsMDtfXWG5skaEKMf2ujMDGEenHZ3662tN2XfVc/I6NOGFGZ9QH+jLmV7JhCl middelkoopt@tc-m610-login-node623
```

Go back to gitlabs and add your public ssh-key to your account as follows (the Avatar/Account button is on the top right of the page):

```
"Avatar" -> Settings -> ssh-keys -> Key: paste public key
```

Now go to "Project" website and copy the git URL by doing the following (the "Hamburger" is the icon with three lines on the top left of the page).

"Hamburger" -> Projects -> Your Projects -> select the project to
clone (in this case mis-$USER-$NAME) -> home -> click the clipboard
icon next to the URL, make sure SSH is selected not HTTP.

Now go to your class folder on `clark.rnet.missouri.edu` and clone the repository
```
git clone git@gitlab.missouri.edu:middelkoopt/welcome.git
```
where `git@gitlab.missouri.edu:middelkoopt/welcome.git` is the pasted from the step before.

### Editing Files

### Homework

1. Homework 1-2: Gitlabs
    1. Create a repository on https://gitlab.missouri.edu called mis-pawprint-first-last as described in the Hands-On section.
    2. Assign "Reporter" permissions to `@middelkoopt`, `@srinivassh` and `@nzqpc` to the project
    3. Create a `ReadMe.md` file and commit it to the repository (note the upper/lower case and spelling).
    4. Clone the repository on `clark.rnet.missouri.edu`
    5. Bonus: Modify the `ReadMe.md` on `clark.rnet.missouri.edu` and push it back to `gitlab.missouri.edu`.
	  6. Run `git log` and paste the last commit/revision/hash or the output of `git rev-parse HEAD` into the assignment to receive a grade.

### References
* Software Carpentry: Linux Shell (http://swcarpentry.github.io/shell-novice/) sections 1-3
* Pro Git book https://git-scm.com/book/en/v2
* Software Carpentry - Git http://swcarpentry.github.io/git-novice/
* GitLabs Markdown https://docs.gitlab.com/ee/user/markdown.html


