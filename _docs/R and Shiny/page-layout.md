---
title: "Page Layout"
parent: R and Shiny
has_children: false
nav_order: 5
---

## {{ page.title }}

At this point, your first R Shiny app should be up and functioning, but there is 
a chance it is still rough in appearance and inefficient in its coding. The
next sections will introduce two important concepts to improve your apps: 
**page layout** and **modular coding**.

## The Importance of Layout

Let's make two points about web page layout. First, it is very important to 
the usability of your app. Second, you can bet (like most things) you are 
not the first person to want to do it well. Accordingly, Shiny and the MDI 
try to use proven solutions when they exist. 

Enter Bootstrap.

## About Bootstrap

Briefly, Bootstrap is a web
framework directed at responsive, mobile-first development that is ideal
for web apps. You can learn about it at the link below if you'd like,
but don't spend _too_ much time learning Bootstrap!  What you need to know
is that R Shiny uses Bootstrap internally, and so we have to follow
its basic structures.

<https://www.google.com/search?q=what+is+bootstrap+web>

## Bootstrap (and thus Shiny) Grid-Based Layout

The most important thing to know about Bootstrap's contributions
to R Shiny is a specific way to assemble pages on a grid-based
system of rows and columns.  Learn more here:

<https://www.google.com/search?q=bootstrap+grid+layout>

Before you continue, be sure you understand the following concepts:

- a page, or a container on a page, is divided into _rows_
- each row is divided into _columns_
- each row has exactly 12 equal-width column divisions (never more, never less)
- an individual column in a row can claim 1 to 12 of the available divisions
- the exact width of each column will scale to the size of the user's viewport

Thus, you can specify the row and column(s) where you want your element 
to appear and trust that the size of the element will scale properly
as the user changes the size of their web window. Web developers call that
a "responsive" page.

## Shiny Layout UI Functions

Now we need to make the grid layout happen in Shiny.
See the following to learn how:

<https://www.google.com/search?q=R+Shiny+grid+layout>

The most important Shiny functions you need to learn, which are
used heavily throughout MDI apps, are:

- fluidRow()
- column()

## The shinydashboard Page Layout

The grid system can be applied to any 
container on a page. The last layout detail we will introduce is 
how to structure the _overall_ app page.  

You have seen many web sites that have menu bars at the
top, the side, or both. The MDI web page mixes a bit of both 
in a common layout known as a 'dashboard'
using the R package 'shinydashboard'.

<https://rstudio.github.io/shinydashboard/>

Take a look through the demos in the link above for the basic idea.
Importantly, you will not need to worry about the page layout,
the MDI framework does that for you.

What you mostly want to add from shinydashboard is its
nice functions to create boxes and other container elements, 
thus, pay attention to the new functions:

- **box()**
- tabBox()
- infoBox()
- valueBox()
