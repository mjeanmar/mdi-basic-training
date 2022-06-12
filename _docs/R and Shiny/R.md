---
title: R
parent: R and Shiny
has_children: false
nav_order: 10
---

## {{ page.title }}

The MDI, especially its Stage 2 Apps, makes extensive use of 
the statistical scripting language called **R**. You will
need R to access many things the MDI offers.

### Install R

You will find everything you need to install R here:

- <https://www.r-project.org/>

We recommend that you install the most recent, up-to-date
version of R. Note that you can have multiple R versions
installed simultaneously on the same computer.

Once you have it installed, open an R console and paste in the command:

```
plot(1:10)
```

If you see a simple plot, you're ready to proceed.

{% include figure.html file="R/first-plot.png" %}

### Install an R-compatible IDE

As noted above, we encourage all MDI code development to be done in 
VS Code. If you didn't do it before, please install the VS Code extension:

- **R**, by REditorSupport

To take advantage of R syntax checking in VS Code, open an R console 
and install the 'languageserver' package using this command:

```
install.packages("languageserver")
```

You may also wish to install **R Studio** on your computer. 
R Studio is an IDE specifically geared toward working in R. You should 
go ahead and install it, since it is very common and 
a useful tool to have (as your work on the MDI grows, you may see why
VS Code is a more versatile IDE for working on a large project that uses
more languages and tools than just R). 

- <https://www.rstudio.com/>

### Learn the basics

There are many resources on the internet to introduce you to the basic
concepts of R. Take a look through the ones you find most useful:

- <https://www.google.com/search?q=r+basics>

> Understanding R at a deep level is a _very_ large task!
> For now, just get your feet wet. 
