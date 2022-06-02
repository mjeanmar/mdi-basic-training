---
title: YAML Files
parent: MDI Pipelines
has_children: false
nav_order: 10
---

## {{ page.title }}

As you work with data, you will recognize
the need to store it in a structured, reproducible way,
known as a file format. There are a great many file formats
for different kinds of data.

Here, we need to understand **YAML**, which
stands for Yet Another Markup Language. YAML files
have the file extension **.yml**.  They are designed to store
any kind of data that can be described as:

- **name:value pairs**, like Wilma:redhead
- **lists of values**, like Fred, Wilma, Barney, Betty

in a format that is easy to both read and write.

### Learn the basics

We won't give a complete description of the YAML 
format specifications, which are abundantly covered on
the internet:

- <https://www.google.com/search?q=YAML+basics>

### YAML features needed for the MDI

Fortunately, the MDI requires only a small
subset of all that YAML files can do, which can be summarized as:

- use a colon, ":", to separate name:value pairs
- use a hyphen, "-", to enumerate items on a list
- you can make named lists, lists of name:value dictionaries, etc.
- use fixed-width indentation to indicate the level of nesting on an organizational tree

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

That's all we're going to say! YAML is extremely intuitive, 
you will naturally understand how to read and write it. 

Just remember to choose a fixed-width indentation,
either 2 or 4 spaces per your preference, and stick with it.
