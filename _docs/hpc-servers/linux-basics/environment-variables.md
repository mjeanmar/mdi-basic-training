---
title: Environment Variables
parent: Linux Basics
grand_parent: HPC Servers
has_children: false
nav_order: 40
---

## {{ page.title }}

In addition to command options, Linux servers offer another means 
of sharing information values that is used extensively by the MDI, called
environment variables.

An **environment variable** is a value present in the shell 
where a command is executed.

### Some common environment variables

Here are a few environment variables to know - these are all
set by the system and ready to use. There will certainly be others set also.

| Variable Name | Description | 
|---------------|-------------| 
{% for variable in site.data.linux.variables %}| {{ variable.name }} | {{ variable.description }} | 
{% endfor %}

### Using environment variables

You can set and access your own environment variables, or modify
existing variables, as follows:

```bash
MY_VAR=abc
echo $MY_VAR
echo ${MY_VAR}
```

Notice that:
- it is common practice to use uppercase variable names with
'_' separators for environment variables
- you _set_ a variable _without_ the leading \$ symbol
- you _read_ a variable _with_ the leading \$ symbol, or as ${MY_VAR}

### Environment variable scope

When you run a program on a Linux server, the program is started
in it's own instance of the command shell. That "subshell" may or may
not have access to the environment variables in the shell
that called the program.

By default, a variable set in a shell is _not_ passed to its
subshells. Thus, in our example above, MY_VAR is _not_ set in the
shell that runs a child program.

We often want our variables to pass into the programs we call.
We sometimes do that by using the environment variable to set a
program's options:

```bash
MY_VAR=abc
command --option $MY_VAR
```

But for the program to read the environment variable itself, we must **export**
the variable into the subshell, as follows:

```bash
export MY_VAR=abc
command
```
