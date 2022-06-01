---
title: YAML Files
parent: MDI Pipelines
has_children: false
nav_order: 10
---

## {{ page.title }}

As you work with data, you will increasingly recognize
the need to store it in a structured, reproducible way,
known as a file format. There are a great many file formats
for different kinds of data.

Here, we need to understand **YAML**, which
stands for Yet Another Markup Language. YAML files always
have the file extension **.yml**.  They are designed to store
any kind of data that can be described as:

- **name:value pairs**, like Wilma:redhead
- **lists of values**, like Fred, Wilma, Barney, Betty

in a format that is easy to both write and read.

### Learn the basics

We won't give a complete description of the YAML 
file format specifications, it is abundantly covered on
the internet:

- <https://www.google.com/search?q=YAML+basics>

### YAML features needed for the MDI

Fortunately, the MDI requires you to understand only a small
subset of all that YAML files can do, which can be summarized as:

- use a colon, ":", to separate name:value pairs
- use a hyphen, "-", to enumerate items on a list
- you can make lists of named items, named lists, etc.
- use fixed indent widths to indicate the level of nesting on an organizational tree

Thus, we get data structures like:

```yml
Flintstones:
    People:
        - Fred
        - Wilma
    Pets:
        - name: Dino
          species: dinosaur
Rubbles:
    People:
        - Barney
        - Betty
```

We aren't going to say any more than that. The beauty of YAML
is that is it extremely intuitive, you will naturally understand how
to read and write it. 

Just remember, you must used a fixed indent width,
choose either 2 or 4 spaces per your preference and stick with it.
