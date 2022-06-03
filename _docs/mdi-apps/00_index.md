---
title: MDI Apps
has_children: true
nav_order: 60
---

## {{ page.title }}

You now have the basic tools and skills in place
to begin to work with MDI Stage 1 Apps, where
an **app** is a single R Shiny web application for interactive
data analysis.

### High-level view of app configuration

The MDI apps framework is an R Shiny app. When the 
web page is first loaded, it calls Shiny with sufficient information
to load the UI with an entirely generic interface ready to support
data upload and/or app selection.

A specific MDI app is a set of instructions for how to 
dynamically populate that initial framework with an 
integrated set of tabs and widgets toward some purpose 
in interactive data analysis. 

Page filling does not replace the framework, it adds to it.
As a result, when you write an MDI app you will pay very little
attention to the typical UI and server functions - the framework
does that for you. You will spend your effort writing the
code for the specific tools you wish to add to your pages.
The majority of that will be adding and constructing appStep modules.
