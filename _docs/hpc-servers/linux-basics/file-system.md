---
title: File System
parent: Linux Basics
grand_parent: HPC Servers
has_children: false
nav_order: 10
---

## {{ page.title }}

Files on a Linux server are stored in a tree of directories, 
also called folders. This is how a complete _path_ to a file is written:

```
/home/wilma/data/file.txt
```

where:
- the first '/' points to the root of the tree
- '/home/wilma' is Wilma's "home" directory (see below)
- '/home/wilma/data' is the directory, or dirname, of the file
- 'file.txt' is the name of the file itself, called its basename
- '.txt' is the "extension" of the file that tells you what kind of file it is

### Special-case paths and symbols

Certain file paths on Linux
have special purposes, sometimes with shortcut symbols.
Many are only important for system administrators,
but you need to know you have a home directory for your use:

```bash
/home/<your_username>
```

that can be accessed with the following universal shortcut without
needing to know the actual path:

```bash
~
```

Another shortcut to know about refers to the parent of the 
current working directory, i.e., "move up one level on the directory tree":

```bash
..
```

whereas, the following refers to the current working directory itself:

```bash
.
```

### File access permissions

On a shared server, you don't want just anybody reading
your files! Linux servers use a "owner/group/other" + "read/write/execute"
method for determining who can do what to a given file or directory.

The kinds of people being granted permissions, in order of precedence, are:

- **owner** a.k.a. 'user' = generally the person who created the file
- **group** = the name of a group of users to which a person belongs
- **other** = everyone who is not 'user' or someone in 'group'

The kinds of permissions being granted are:

- **read** = view the contents of a directory or file
- **write** = create or modify  a directory or file
- **execute** = run a program or move into a directory

The following shows a common way this information is communicated:

```bash
drwxrw-r-- userName groupName myDirectory
-rwxrw-r-- userName groupName myFile
```

which is split apart and explained as follows:

```bash
# d=directory owner group other  owner group       directory
  d           rwx   rw-   r--    wilma flintstones myDirectory

# -=file      owner group other  owner group       file
  -           rwx   rw-   r--    wilma flintstones myFile
```

Thus, the two lines refer to one directory and one file, respectively.
Each grants read+write+execute permissions to the owner, who is 'wilma', 
only read+write to people in the 'flintstones' group, and only read to everyone else.
