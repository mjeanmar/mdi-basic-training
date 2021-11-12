---
title: "Modules"
parent: R and Shiny
has_children: false
nav_order: 6
---

## {{ page.title }}

A commonly cited principle of good coding is known as DRY,
or, [Don't Repeat Yourself](https://en.wikipedia.org/wiki/Don%27t_repeat_yourself). 
The idea is that when you find yourself
typing essentially the same thing twice, you should partition that code
into some type of reusable function or module. 

Indeed, R Shiny has a means for creating repeated
elements on your app pages called 'modules'.

## Learn the Basics

Web pages you will find in the following search will help
orient you to what Shiny modules are and why they are crucial
to good app development and used extensively by the MDI.

<https://www.google.com/search?q=r+shiny+modules>

What you should learn from your reading is:

- a Shiny module will create a single, reusable type of UI element
- like an app itself, or other Shiny UI elements, a module consists of:
    - a UI function
    - a server function
- a module's server function can return data from the UI elements defined by the module, or any R data object derived from those UI elements, including reactive elements


