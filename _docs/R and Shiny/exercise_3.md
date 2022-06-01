---
title: "EXERCISE #3"
parent: R and Shiny
has_children: false
nav_order: 70
---

## {{ page.title }}

Let's turn your prior app into something more complete
by incorporating layout and modules.

## Prerequisites

Please by sure you have completed **Exercise #2** in this section.
You should have a functioning, interactive app for plotting values
from the 'mtcars' object as a scatterplot.

## STEP #1 - Build a module for selecting the plot axis data columns

In Exercise #2, your code likely made two different calls to an input
such as 'selectInput', which helped the user select two data columns
from 'mtcars' for the x- and y-axis. 

Your next goal is to make a Shiny module to encapsulate
that selectInput. Your module's **UI function should display a selectInput**
with the columns from mtcars, and its 
**server function should return the current value of that selectInput** as a reactive. 

That module alone is overly simplistic, but
it should help you understand the basics of module assembly that you can
build on as your apps grow in complexity.

To get you started, here is the basic anatomy of a module's two functions:

```r
# module ui function, in myModule_ui.R

myModuleUI <- function(id, ...) {
    ns <- NS(id) # initialize the module's namespace
    xxxxInput(ns('inputName')) # add Shiny UI elements in that namespace
}
```

```r
# module server function, in myModule_server.R

myModuleServer <- function(id, ...) {
    moduleServer(id, function(input, output, session) {

        # add Shiny server actions here: observe, render, etc.

        reactive(input$inputName) # the module's return value
})}
```

## STEP #2 - Add additional UI elements to your module

To make it more obvious how modules help build code fast, in addition
to the selectInput itself, also have your module display the <code>range()</code>
of values from the selected mtcars data column, immediately below the selectInput.

Now you only have to add the range output once, to the module -
you are no longer repeating yourself!

## STEP #3 - Create a helpful layout for your app page

Most likely, your app currently has both inputs above the plot.  Let's help
the user by placing the x-axis selectInput below the x-axis, and the y-axis 
selectInput to the left of the y-axis. Your final page should have this layout:

|  |  |
| :-----------: | :-----------: |
| y-axis selector | plot                   |
|                 | x-axis selector        |
|  |  |

>Use the <code>fluidRow()</code> and <code>column()</code>
>functions to achieve this, making use of the Bootstrap-style 'width' argument.

## STEP #4 - Demonstrate your success

Re-upload your app to shinyapps.io and email your mentor when ready!
