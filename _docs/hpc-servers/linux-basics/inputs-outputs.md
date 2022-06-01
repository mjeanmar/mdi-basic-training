---
title: Inputs and Outputs
parent: Linux Basics
grand_parent: HPC Servers
has_children: false
nav_order: 50
---

## {{ page.title }}

You want to give your programs interesting data to work on - 
called "inputs" - and to create files with their results - called "outputs".
You'll also need to know if there were problems with program execution,
called "errors". 

### Standard data streams

There are three standard "streams" that correspond to the data flow needs above.

- **STDIN** = where a program gets its input
- **STDOUT** = where a program writes its output
- **STDERR** = where a program reports its errors

"STD" means "standard". The rest is obvious.

### Inputs

Programs often get their input from a file provided as a target, e.g.:

```bash
command [options] <INPUT_FILE>
```

A "connection" is established to INPUT_FILE that becomes STDIN for the command.
Otherwise, it will take its input from a data stream - see below.

### Outputs

Unless otherwise specified, programs write their output to STDOUT.
In an interactive shell, STDOUT is your terminal window, i.e.,
the program will print its results for you to see.

```bash
echo abc123
abc123
```

Otherwise, you can "redirect" STDOUT to some other output, like a file - see below.

### Errors

Some of the output from a program is not considered
to be its primary results, but is ancillary information about the state of the 
program and what it is doing. Such "messages" are often a report of warnings or errors
encountered during execution, but could be anything the program wants to tell you.
Messages are written to the third standard stream called STDERR.

In a terminal window, STDERR is merged into STDOUT, i.e., you also see those messages
printed to your screen. Otherwise, you can again redirect STDERR to some other output.

### Streams and pipes

A critical feature of Linux and efficient data
analysis is that data can be "piped" from one program to another 
in a "stream". You do not always write the output from one program
to a file, only for that file to be read by the next program. 
Instead you send the first program's output directly to the second 
program's input.

Such data streams are established using the pipe character, i.e., **|**, as follows:

```bash
command1 <INPUT_FILE> | command2
```

In the sequence above:
- command1 reads INPUT_FILE
- command1 does something to the data
- command1 sends its results to command2
- command2 does something else to the results from command1
- command2 print its results to STDOUT

The reason to do this, as opposed to writing interim files, is that
it is MUCH faster. Writing to disk is the slowest thing a computer does.
Programs that must do a lot of disk read/writes are referred to as "I/O bound",
where "I/O" means "input/output".

### Redirecting STDOUT to a file

Many times you don't want the final results on your screen, you
want them written to a file. That last piece is established using a 
redirect of STDOUT using the **>** symbol, as follows:

```bash
# overwrite OUTPUT_FILE
command1 <INPUT_FILE> | command2 > OUTPUT_FILE
```

The last bit says "assign STDOUT to OUTPUT_FILE". Our stream now:

- prints command2 results to OUTPUT_FILE, overwriting any existing file
- prints any informative messages to STDERR, i.e., to your screen - only the results of command2 go to the file as written

If we used **>>** instead of just **>**, the output would now be appended to
the end of OUTPUT_FILE, if the file already existed.

```bash
# append to OUTPUT_FILE
command1 <INPUT_FILE> | command2 >> OUTPUT_FILE
```
