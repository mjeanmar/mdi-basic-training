---
title: "R Shiny"
parent: R and Shiny
has_children: false
nav_order: 30
---

## {{ page.title }}

As noted above, MDI Stage 2 Apps make extensive use of R. 
A main reason is to exploit the R Shiny framework for creating interactive 
data visualization tools (another is to make use of tools developed by the 
[Bioconductor](https://www.bioconductor.org/) project).

### What is R Shiny?

Like nearly everything in R, Shiny is an R package that you must install and attach. 
Specifically, the Shiny package exposes a set of resources that allow you to 
run a web server on any computer, which is:
- a [single-page application](https://www.google.com/search?q=single+page+application) (SPA)
- **reactive**, i.e., it updates its contents in response to user actions
- capable of executing any R command that you might do manually or in a script

{% include figure.html file="R/hello-world.png" border=true %}

Have you ever gotten tired of manually re-trying to make just the right plot? 
R Shiny allows you to update your plot (and more) quickly and repeatedly by interacting 
with a web page. Enabling the development of such tools is a major goal of the MDI. 
Shiny encourages a "separation of activities" where developers make tools to create 
useful R outputs and users interact with those tools to analyze and display their data.

### Learn the basics

Please make use of the internet for learning the basics of R Shiny and hows its apps are structured.

- <https://www.google.com/search?q=r+shiny+basics>

Pay attention to one critical distinction from the work you've already done in R 
(or many other scripting languages) and Shiny code. In most languages, 
scripts are executed "from the top down", i.e., executing the first line, then the second, etc. 
Shiny scripts are _read_ from the top down, but they do not _execute_ in an ordered sequence. 
This is obvious if you think about it - many parts of your code won't execute until the user
does something on the web page. 

Thus, many code elements in Shiny are _reactive_. When the script is first read, 
it declares the existence and functionality of each element, but those elements won't 
execute until the user does something to make them execute. This takes some getting used to! 

### Install R Shiny

Shiny is installed like any R package. Eventually, the MDI applications framework will 
do this for you, but for learning the basics, you'll want to install it on your computer 
from within an R console:

```r
install.packages('shiny')
library(shiny)
runExample("01_hello")
```

It's a big package, it may take a few minutes. If you see the Hello Shiny app, you're good to go!

> For this section, you might find it easier to work in R Studio, although everything is also readily accomplished in VS Code. 

## Create an account on shinyapps.io

Shiny is very powerful by itself because you can run a web tool on your own computer, 
which acts as both the server and the client. However, you will want to share your apps with the world, 
a major goal of the MDI. Ultimately, we will do this in a different way, but for the purposes of 
quickly sharing small apps as you learn, we will make use of **shinyapps.io**.

shinyapps.io is a web service that will _host_ your web applications on a secure, public server 
for anyone in the world to use. To do this, you need a free account and to deploy your code on the server.

Please use the following link to establish your account on shinyapps.io. You can 
and should use your GitHub account to log in to shinyapps.io - it should be obvious. 

<https://www.shinyapps.io/>
