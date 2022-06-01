---
title: Linux Commands
parent: HPC Servers
has_children: false
nav_order: 30
---

## {{ page.title }}

New users will not have much or any prior experience
interacting with computers at the command line, but it is 
an essential skill in data analysis. Be confident, countless
people have mastered it without much effort.

Unsurprisingly, the internet has abundant guides to the
essential Linux commands:

- <https://www.google.com/search?q=basic+linux+commands>
- <https://www.google.com/search?q=linux+command+cheat+sheet>

### File system basics

Like any computer, files are stored in a tree of directories, or folders.
This is how a complete _path_ to a file is written:

```
/home/wilma/data/file.txt
```

where:
- the first '/' points to the root of the tree
- '/home/wilma' is Wilma's "home" directory
- '/home/wilma/data' is the directory, or dirname, of the file
- 'file.txt' is the name of the file itself, called its basename

### Linux command summary



### Getting command help

Here are three ways to get help on Linux commands. 

- **man COMMAND** = open the command's complete manual page
- **COMMAND -h** or **COMMAND --help** = briefer help information
- searching for 'Linux COMMAND' on the internet 

Invoke these help methods frequently!
You will _not_ remember everything about every command, so read, read, 
read the documentation. Don't spend a lot of
time memorizing commands - when you need them, check a command
list for what you want to do, read the help, and go. 

### Command syntax

A common structure of many terminal commands is:

```
command [subcommand] [options] <target> ...
```

where:
- square brackets, [], means "optional, not always present"
- angled brackets, <>, means "required, must be present"
- an ellipis, '...', means "more of the same", e.g., multiple targets

### Command options

Nearly every terminal command has many options to modify its behavior 
when you call it. A typical format might be:

```
command --example 222 -y
```

where:
- '--example' is longhand notation for an option with a value (222)
- '-y' is shorthand notation for a yes/no flag

Typically you can choose whether to use short or longhand notation.

### Environment variables

In addition to command options, Linux servers offer another common means 
of accessing data that is used extensively by the MDI, called
environment variables.

An **environment variable** is a value present in the environment
of the 'shell' where a command is executed.

Here are a few important environment variables:

PATH
HOME
PWD
USER

You can set and access your own environment variables as follows:

```bash
export MY_VAR=abc
echo $MY_VAR
echo ${MY_VAR}
```

Notice that:
- it is common practice to use uppercase variable names with
'_' separators for environment variables
- you _set_ a variable _without_ the $ symbol
- you _read_ a variable _with_ the $ symbol, or as ${MY_VAR}
- 'export' makes the variable accessible to all commands you may call
