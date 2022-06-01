---
title: Terminal Commands
parent: Linux Basics
grand_parent: HPC Servers
has_children: false
nav_order: 20
---

## {{ page.title }}

Commands are utility programs available on a Linux system,
executed in a terminal window, or a command "shell". 

### Command shells

A "shell" is a program that controls an an intance of a user's interaction 
with the Linux operation system. When you open a terminal window, you are placed
into an interactive shell and given a command "prompt", shown as a **$** symbol:

```bash
# the shell, waiting for you to type a command at the prompt
wilma@server $
```

Most Linux servers today use the "bash" shell:

- <https://www.google.com/search?q=linux+bash+shell>

We don't need to say more about that - for now, just know the name "bash". 
The details of differences between shells is only important to advanced users.

### Command syntax

A common structure of many bash commands is:

```
command [subcommand] [options] <target> ...
```

where:
- square brackets, [ ], means "optional, not always present"
- angled brackets, <>, means "required, must be present"
- an ellipis, '...', means "more of the same", e.g., multiple targets



### Getting command help

Here are three ways to get help on Linux commands. 

- **man COMMAND** = open the command's complete manual page
- **COMMAND -h** or **COMMAND --help** = briefer help information
- searching for 'Linux COMMAND' on the internet 

Invoke these help methods frequently!
You will _not_ remember everything about every command, so read, read, 
read the documentation. Don't spend time memorizing commands - 
when you need them, check a command
list for what you want to do, read the help, and go. 


### Command options

Nearly every shell command has many options to modify its behavior 
when you call it. A typical format might be:

```
command --example 222 -y
```

where:
- '--example' is longhand notation for an option being assigned value 222
- '-y' is shorthand notation for a yes/no flag, i.e., it takes no value and is set to false if not present on the options list

Typically you can choose whether to use short or longhand notation.
