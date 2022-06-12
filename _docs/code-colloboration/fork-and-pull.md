---
title: Fork & Pull
parent: Code Collaboration
has_children: false
nav_order: 30
---

## {{ page.title }}

There are various collaboration models that a project can use
for developers to work together on code. A project will
declare its model and stick with it. The MDI uses the 
model known as "Fork & Pull" or the "Forking Workflow".

### Open source code projects

Understanding the Fork & Pull collaboration model requires a basic
understanding of Open Source software, which means that the 
code for a project is publicly available for others to see and use,
according to license grants beyond the scope of this tutorial. 

- <https://en.wikipedia.org/wiki/Open-source_software>

On GitHub, this means that a developer
has set the status of a code repository to "Public". 
For example, the content for this Basic Training web site
is a public repo distributed under the CC BY-NC 4.0 license.

- <https://github.com/MiDataInt/mdi-basic-training>

### Learn the basics

As always, there are many internet resources to help you understand
forking and pulling into a git code repository.

- <https://www.google.com/search?q=git+fork+and+pull>

The concepts you want to understand are that:

- Project maintainers control the code in the "definitive" repository
- Code developers:
    - fork a copy of the repo to their own GitHub account
    - clone their fork of the code to their local computer
    - edit code toward some purpose
    - push their changes to their fork, in their own GitHub account
    - make a "pull request" to the project maintainers to have their code incorporated into the definitive repository

{% include figure.html file="git/fork-and-pull.png" width="400px" %}

The next Exercise will walk you through these steps.
