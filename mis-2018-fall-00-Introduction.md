# IMSE 4410 Fall 2018 - Module 1

*IMSE 4410/7410 Management Information Systems Design (MIS)*

Material Copyright 2017, 2018 by Timothy Middelkoop. Sourcecode licensed under the Apache License, Version 2.0. Documentation licensed under CC by SA 3.0.

## Introduction to MIS 

So you want to be an Engineer. You need to use, understand, and be
comfortable with information technology.  This is the course for that.

### Outline 
 * Welcome and personal introduction
 * Motivation for the class (information technology and computational engineering)
 * Module outline
 * Hands on with secure shell (ssh).

### Hands on
 * Use a secure shell client and connect to `clark.rnet.missouri.edu` using your pawprint login (SSO) and password.  You must use all lower case for your username and do not include the `@` or anything after it.
 * The following ssh clients are recommended: 
   * MobaXterm (https://missouri.app.box.com/rcss-mobaxterm) for Windows, 
   * Putty (https://the.earth.li/~sgtatham/putty/latest/w32/putty.exe ) for Windows, 
   * or hterm, the Chrome browser “Secure Shell” extension for Windows, Mac, and Chromebooks (https://chrome.google.com/webstore/detail/secure-shell/pnhechapfaindjhompbnflcldabbghjo).
   * Mac users can use the built-in terminal by launching it from Spotlight by hitting `Command + Spacebar` and typing `Terminal` and then return.  To connect to the teaching cluster enter the command `ssh pawprint@clark.rnet.missouri.edu` where `pawprint` is your login (SSO) and enter your password when prompted.

### Reading
 * ISBB Chapter 1 - Introduction (https://bus206.pressbooks.com/chapter/chapter-1/)

### Discussion 
 * What does IT mean to you?
 * What about technology things would you like to know about?

Information Technology (IT), and by extension Management Information
Systems (MIS), is the **physical**, **computational**, and **software**,
infrastructure built by **teams**, to manage **information**.

IT needs **physical** infrastructure consisting of
 * power, 
 * cooling,
 * and space,

to supports the fundamental **computational** resources 
 * compute,
 * storage, and
 * networking.

From these resources a **software** system is built through
 * provisioning (physical and logical), 
 * configuration,
 * software (Operating System, libraries, applications), and
 * security.

This infrastructure is used to **manage information** (data) through 
 * business process,
 * data,
 * policy, and
 * security.

All this is all brought together by **teams** with 
 * people,
 * process, and
 * community.

** Security a fundamental property of systems and applications.

### Homework
Homework 1-0: Using Secure Shell
 1. Connect to clark.rnet.missouri.edu with your pawprint (SSO) and pawprint password and run the following commands and copy and paste the session (as text).
    1. `hostname`
    1. `whoami |sum`
