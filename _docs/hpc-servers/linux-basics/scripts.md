---
title: Shell Scripts
parent: Linux Basics
grand_parent: HPC Servers
has_children: false
nav_order: 60
---

## {{ page.title }}

You type shell commands at the command line when you want
to see the results of one command, or stream, immediately. 

Other times, you want to defer execution of a more complex 
sequence of commands, which is accomplished by writing 
them into a script. 
A **script** is a text file with a set 
of commands that you could have typed at the command line.
The lines of the script will be executed one by one, in order.

By convention, shell script files always end with the extension ".sh".

### Executing a script

The two ways to execute, or "call", a script depend on whether or not
it has the "execute" permission set.

The following will work to run any script. It tells
the bash shell - which is a program - to run the script:

```bash
bash SCRIPT_FILE.sh
```

The following will only work if the execute permission is set on SCRIPT_FILE.sh:

```bash
./SCRIPT_FILE.sh
```

In the latter example, we are using the "." symbol to 
mean "the current directory" and then naming the file we want 
to run as a program, i.e., we are providing a path to the program to the
Linux operating system. If that file is not considered "executable",
as determined from its "x" permission, the system will throw an error.

### Script comments

Not all lines in a script are executed. Any line starting with the **#**
character is considered a comment that is ignored by the script intepreter.

```bash
# a comment, not executed
command
```

### The shebang line

One comment line of a script - the first one - is special and goes by the
name of "shebang". That line starts with the characters **#!** and tells the
Linux operating system what program should run the script.

Thus, this script:

```bash
# myScript.sh

#!/bin/bash
echo abc123
```

will be run by bash when called as follows:

```bash
./myScript.sh
```

### Other script directives

Notice that the shebang line starts with **#**, which is the comment character.
Thus, the first character "#", says "I'm a comment", whereas the second character, 
"!", says "I'm a SPECIAL comment!"

You will see that pattern of special comments - which we call **directives** - 
elsewhere, e.g., to communicate information to a cluster job scheduler.

