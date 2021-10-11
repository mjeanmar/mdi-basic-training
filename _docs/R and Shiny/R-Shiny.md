---
title: "R Shiny"
parent: R and Shiny
has_children: false
nav_order: 3
---

## {{ page.title }}

As noted above, MDI Stage 2 Apps make extensive use of 
R. The main reason is to exploit the R Shiny framework for creating interactive data visualization tools (other reasons are to make use of
the tools developed by the 
[Bioconductor](https://www.bioconductor.org/)
project).

## What is R Shiny?

Like nearly everything in R, Shiny is an R package that you must install and attach. Specifically, the Shiny
package exposes a large set of resources that allow you to run a web server
on any computer, which is:
- a [single-page application](https://www.google.com/search?q=single+page+application) (SPA)
- **reactive**, i.e., it updates its contents in response to user actions
- capable of executing any R command that you might do manually or in a script

Have you ever gotten tired of manually re-trying things to make just the right plot? R Shiny allows you to update your plot (and a lot more) quickly and repeatedly by interacting with a web page. Enabling the development of such tools is a major goal of the MDI. Thus, Shiny encourages a "separation of activities" where developers make tools to create useful R outputs in a general sense, and user interact with those tools to deeply analyze and represent their data in a specific way.

## Learn the Basics

Let's once again make use of the internet for learning about the basics of R Shiny and hows its apps are structured.

<https://www.google.com/search?q=r+shiny+basics>

As you read, pay attention to one critical distinction from the work you've already done in R (or many other scripting languages) and Shiny code. In most scripting languages, scripts are executed "from the top down", i.e., executing the first line, then the second, etc. Shiny scripts are _read_ from the top down, but they do not _execute_ in a time sequence. This is obvious if you think about it, since many parts of your code won't execute until the user actually does something on the web page. 

Thus, many code elements in Shiny are _reactive_. When the script is first read, it declares the existence and functionality of each element, but those elements won't execute until the user does something to make them execute. This takes some getting used to! Otherwise, Shiny code is pretty much like all R code.

## Install R Shiny

As noted above, R Shiny is an R package, so it is installed just like any package. Eventually, the MDI applications framework will do this for you, but for learing the basics, you'll want to install it on your computer from within an R console:

```
install.packages('shiny')
library(shiny)
runExample("01_hello")
```

It's a big package, it may take a few minutes. If you see the Hello Shiny app, you're good to go!

By the way, for this section, you might find it easier to work in R Studio, although everything is also readily accomplished in VS Code. 

## Create an Account on shinyapps.io

Shiny is very powerful by itself because you can run a web tool on your own computer, which acts as both the server and the client. However, you will quickly want to share your apps with the world, which is a major goal of the MDI. Ultimately, the MDI will do this in a different way, but for the purposes of quickly sharing small apps as you learn, we will make use of **shinyapps.io**.

shinyapps.io is a web service that will help you _host_ your web applications on a secure, public server for anyone in the world to use. To do this, you need a free account and to upload and deploy your code on the server.

Please use the following link to establish your account on shinyapps.io. Importantly, you can and should simply use your new GitHub account to log in to shinyapps.io - it should be obvious. 

<https://www.shinyapps.io/>
