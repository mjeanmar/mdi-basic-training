---
title: "EXERCISE #1"
parent: R and Shiny
has_children: false
nav_order: 2
---

## {{ page.title }}

Excellent! You are ready to do some first tasks in R and 
(for students working on the MDI Project) to demonstrate to your
mentor that you are ready to move on.

The steps of this excercise are designed to illustrate
the three most fundamental things that R does:

- work with tables of data
- calculate statistics on that data
- make plots of that data

> We are not going to spoonfeed every command to you verbatim! 
> We expect you to immediately start _learning how to learn_ to code, 
> which means you have to read help text, manuals, and use the internet
> to discover things for yourself. When you get stuck, ask!

## Prerequisites

To briefly recap, we expect that you have completed all steps
in the previous sections, and that you now have:

- installed Visual Studio Code and the R Extension (and probably R Studio)
- installed R and verified it is working as expected

## STEP #1 - Load a Data Set

R comes with various data sets that are immediately available 
for use (you don't have to go looking for them). We are going to
use the 'mtcars' data set. So, nothing to actually do here.

## STEP #2 - Examine a Data Table

Myriad data types will come to you the same way that mtcars does,
as a table (i.e., a 'data.frame') with items in rows and measured values in columns. Learn
about the mtcars table using the following commands:

- str
- head
- tail
- colnames
- rownames
- names
- typeof
- class

To learn how to use those commands and what they do, from within an R console type
'?' followed by the name of the command, e.g.,

```
?str
```

Or, alternatively, do a Google search for 'R str' and similar. But READ THE DOCUMENTATION!

## STEP #3 - Calculate Simple Statistics

Now that you know the table's structure, you will be able to 
calculate _aggregate_ statistical values on it. Please 
use the following commands to discover the car type with the
highest and lowest gas mileage (i.e., 'mpg'), and also the average
mileage over all car types.

- max
- min
- mean

What other calculations might you want to make? Play around for a while.

> HINT: completing this step will require you to know how to access the 
> rows and columns of a data.frame. 
> Google this if you're not clear (<https://www.google.com/search?q=r+working+with+data.frames>). 
> You should become familiar with expressions like 'mtcars$mpg' and 'mtcars[1,2]'.


## STEP #4 - Make a Basic Plot

Finally, use the 'plot' function of R to make a simple plot of mileage (mpg)
as a function of engine displacement (disp).  What can you conclude from your plot?

Also, work to make your plot look a bit more professional. Please color the plot points and label the axes with actual words.  There is more you could do, but let's not get crazy for now.

## STEP #5 - Prove Your Success

Email your mentor with the answers to Step #3, and a saved image of your plot
from Step #4. 
