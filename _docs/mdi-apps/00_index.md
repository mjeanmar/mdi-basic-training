---
title: MDI Apps
has_children: true
nav_order: 60
---

## {{ page.title }}

You now have the tools and skills in place
to begin to work with MDI Stage 1 Apps, where
an **app** is a single R Shiny web application for interactive
data analysis.

### High-level view of app configuration

The MDI apps framework is itself an R Shiny app. When the 
web page is first loaded, it calls Shiny with sufficient information
to load the UI with a launcher interface ready to support
data upload and/or app selection.

A specific MDI app is a set of instructions for how to 
populate that initial framework with an 
integrated set of tabs and widgets toward some purpose 
in interactive data analysis. 

Page filling with an app does not _replace_ the framework, it _adds to it_.
As a result, when you write an MDI app you will not care about
the typical app-level UI and server functions - 
the framework does that for you. 
You will spend your effort writing
code for the specific tools you wish to add to your pages,
mostly by
[constructing appStep modules](/mdi-apps-framework/docs/appSteps/00_appSteps.html)
and widget modules. You can see why it is important that you
understand the 
[R and Shiny : Modules](/mdi-basic-training/docs/R%20and%20Shiny/modules/)
section above.
