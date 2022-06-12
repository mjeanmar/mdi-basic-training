---
title: Branching
parent: Code Collaboration
has_children: false
nav_order: 50
---

## {{ page.title }}

Congratulations! You now have all the 
basic skills and tools in place to work on a collaborative code
project like the MDI. 

There is one more wrinkle we need to introduce to improve the
way you work in the Fork & Pull model. Specifically, Git (and
thus GitHub) can actually have multiple running versions of a codebase
within a single repository. These versions are called "branches".

{% include figure.html file="git/branching.png" %}

### Learn the basics

Once again, please use the many available internet resources to learn 
more about Git branching.

- <https://www.google.com/search?q=git+branch+basics>

### Improving our exercise

All MDI repositories have a definitive branch called 'main'.
When you are ready to begin work on some aspect of the code,
the best practice is to declare, and "checkout", a new branch
that is derived from 'main'. That way, you can edit without 
affecting the state of the definitive code, even in your local
version of the repository. 

If we had done it the best possible way, you would have
created a new branch prior to editing the Basic Training repo.
We won't make you repeat the Exercise, but
please find the ways within VS Code, or in Git Bash, that you
can switch to a new branch.

### Contributing to the MDI Basic Training documentation

You are now fully ready to help us write these
Basic Training pages. If there
are things you'd like to see incorporated, you should:

- Create a new branch in your local repository with a short, helpful name
- Add or edit content as needed
- Go through the 'add', 'commit', 'push' and 'pull request' steps as in the Exercise

It is also good to create an Issue on GitHub
to let people know what you think needs to be improved, and so work can
be associated with specific people. 

- <https://www.google.com/search?q=github+issues>
