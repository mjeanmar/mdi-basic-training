---
title: MDI Pipelines
has_children: true
nav_order: 40
---

## {{ page.title }}

You should now have all the basic tools and skills in place
to begin to work with MDI Stage 1 Pipelines.

A **pipeline** is a set of analysis actions applied to some
set of data inputs.

### High level view of MDI pipeline execution

We will guide you to installing
the **mdi** command line utility, or interface (sometimes called
a CLI). The mdi utility is a program subject to the same rules you 
learned for any Linux command. It will have subcommands, take 
options and inputs, and create outputs and messages.  

The primary input to the mdi program is
a is a **job configuration file**, a YAML-format file 
whose purpose is to declare values for the sometimes
long set of options required to describe a data analysis, 
including what pipeline you want to run, the target 
data, analysis parameters, etc.

The mdi program will read your job configuration file and 
either run the requested work synchronously, i.e., in your
terminal window, or asynchronously, by submitting the request
to the job scheduler on your behalf.
