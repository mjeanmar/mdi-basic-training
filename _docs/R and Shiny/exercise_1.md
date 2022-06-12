---
title: "EXERCISE #1"
parent: R and Shiny
has_children: false
nav_order: 20
---

## {{ page.title }}

Excellent! You are ready to do some first tasks in R and 
(for students working on the MDI Project) to demonstrate to your
mentor that you are ready to move on.

This exercise is designed to illustrate
the three most fundamental things that R does:

- work with tables of data
- calculate statistics on that data
- make plots of that data

### Prerequisites

To recap, we expect that you have completed all steps
in the previous sections, and that you now have:

- installed Visual Studio Code and the R Extension (and probably R Studio)
- installed R and verified it is working as expected

### STEP #1 - Load a data set

R comes with various data sets that are immediately available 
for use (you don't have to go looking for them). We are going to
use the 'mtcars' data set. So, nothing to actually do here.

### STEP #2 - Examine a data table

Myriad data types will come to you as mtcars does,
as a table (i.e., a 'data.frame') with items in rows and measured values 
in columns. Learn about the mtcars table using the following commands:

- str
- head
- tail
- colnames
- rownames
- names
- typeof
- class

As one first example:

```r
> head(mtcars[1:3, ])
               mpg cyl disp  hp drat    wt  qsec vs am gear carb
Mazda RX4     21.0   6  160 110 3.90 2.620 16.46  0  1    4    4
Mazda RX4 Wag 21.0   6  160 110 3.90 2.875 17.02  0  1    4    4
Datsun 710    22.8   4  108  93 3.85 2.320 18.61  1  1    4    1
```

To learn how to use those commands and what they do, from within an R console type
'?' followed by the name of the command, e.g.,

```
?str
```

Or, alternatively, do a Google search for 'R str' and similar. You will find
that they are all commands to help you understand the structure and content
of a data object.

### STEP #3 - Calculate simple statistics

Now that you know the table's structure, you will be able to 
calculate _aggregate_ statistical values on it. Please 
use the following commands to discover the car type with the
highest and lowest gas mileage (i.e., 'mpg'), and also the average
mileage over all car types.

- max
- min
- mean

What other calculations might you want to make about automobiles? 
Play around for a while.

> HINT: completing this step requires you to know how to access the 
> rows and columns of a data.frame object. 
> Google this if you're not clear (<https://www.google.com/search?q=r+working+with+data.frames>). 
> You must become familiar with expressions like 'mtcars$mpg' and 'mtcars[1, 2]'.

### STEP #4 - Make a basic plot

Finally, use the 'plot' function of R to make a simple plot of mileage (mpg)
as a function of engine displacement (disp).  What can you conclude from your plot?

Also, work to make your plot look a bit more professional. 
Please color the plot points and label the axes with actual words.  

### STEP #5 - Write your code into a script

Up to this point, you  were probably working mainly in an R console. 
That is great and very important but the MDI will rely heavily on R scripts.
A 'script' is nothing more than a set of the same commands you might execute manually 
written down into a file to allow them to be executed automatically from a single call 
to the script. Read more if you need to:

- <https://www.google.com/search?q=r+scripts>

So, open up your code editor and write a series of commands that will do many or all
of the steps above. Run the script to make sure it does what you want.

### STEP #6 - Demonstrate Your success

Email your mentor with the answers to Step #3, a saved image of your plot
from Step #4, and your script file from Step #5.
