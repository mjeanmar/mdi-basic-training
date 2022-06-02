---
title: EXERCISE
parent: Linux Basics
grand_parent: HPC Servers
has_children: false
nav_order: 70
---

## {{ page.title }}

We've covered a lot of ground to get you going on Linux!
Let's show that you are ready to work at the command line.

As always, we are going to tell you what
to do, but not exactly how to do it. Use the documentation
here and elsewhere to find the commands you need.

> Hint: you can use any text editor for steps below. We suggest **nano**
if you do it from the command line. Otherwise, you can edit the file
in VS Code.

### Prerequisites

To recap, we expect that you have completed all steps
in the previous sections, and that you now have:

- a valid account on an HPC server, like Great Lakes
- an ability to log in and open a remote terminal window on that server

### STEP #1 - Basic directory and file manipulations

Please do the following:

- navigate to your home directory
- create a new subdirectory called "basic-training"
- change to that subdirectory
- create and edit a new file called "exercise.txt"
- write "Linux rocks!" in the file.
- save the file
- print the contents of the file to the command terminal window

### STEP #2 - Use scripts and environment variables

Working from within your basic training directory:

- write a script called "whoami.sh"
- edit "whoami.sh" so that it writes the **name of the server host** and **your username** to a new file, called "whoami.txt"
- run your new script
- print the contents of whoami.txt to the command terminal window

### STEP #3 - Send your results

Prove to your mentor that you've done these things by copy-pasting the 
contents of your terminal window, with:

- a long-form listing of the contents of the basic-training directory
- the output of each step above
