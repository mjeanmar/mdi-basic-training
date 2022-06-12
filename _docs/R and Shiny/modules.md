---
title: "Modules"
parent: R and Shiny
has_children: false
nav_order: 60
---

## {{ page.title }}

A principle of good coding is known as DRY,
or, [Don't Repeat Yourself](https://en.wikipedia.org/wiki/Don%27t_repeat_yourself). 
The idea is that when you find yourself
typing essentially the same thing twice, you should partition that code
into some type of reusable function or module. 

Indeed, R Shiny has a means for creating repeated
elements on your app pages called 'modules'.

### Learn the basics

Web pages you will find in the following search will
orient you to what Shiny modules are and why they are crucial
to good app development and used extensively by the MDI.

- <https://www.google.com/search?q=r+shiny+modules>

What you should learn from your reading is:

- a Shiny module creates a single, reusable type of UI element
- like an app itself, a module consists of:
    - a UI function
    - a server function
- a module's server function can return data from the UI elements defined by the module, or any R data object derived from those UI elements, including reactives

{% include figure.html file="R/shiny-modules.png" %}

### A conceptual example

Imagine you have a series of similar 
tables on an app page, each of which allows the user to select one row. The
tables require a common assembly logic but take different data 
sets as input. Finally, imagine that the main app will make a plot based on the rows
the user has selected from the various tables.

Here, the tables are an ideal use case for a module. Instances of that
module would be called several times as, e.g., <code>myModuleUI(id)</code>, 
and its server function, <code>myModuleServer(id)</code>, would return 
information on its selected table row. 

```r
# server.R
row1 <- myModuleServer('id1', data1)
row2 <- myModuleServer('id2', data2)
output$myPlot <- renderPlot({
    x <- doSomething(row1())
    y <- doSomething(row2())
    plot(x, y)
})
```

Note that the value returned by 'myModuleServer' is a _reactive function_
so that the plot updates whenever a selected table row changes.

### Foreshadowing the use of modules in MDI apps

You will learn more about the structure of MDI apps later, 
but for now we'll mention that apps use modules to create
a series of sequential, reusable "steps". The idea is that app step 1
creates an output that can be used by app step 2, etc., 
creating a data flow chain:

appStep1 --> appStep2 --> appStep3

where each appStepN is a Shiny module. Well-designed step modules can 
often be reused, e.g., many apps use a module that defines
the MDI sample assignment grid, with subsequent steps making use
of those assignments.
