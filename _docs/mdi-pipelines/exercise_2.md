---
title: "EXERCISE #2"
parent: MDI Pipelines
has_children: false
nav_order: 30
---

## {{ page.title }}

In this exercise you will begin to learn how to _develop_ an MDI pipeline,
specifically, by changing the MDI demo pipeline.

### Prerequisites

You should have already completed Exercise #1, so that you 
have the mdi-demo-tools suite installed and running the demo
pipeline from your own job configuration file.

### STEP #1 - Change the 'demo do' functionality

This is an easy exercise to explain - we want you
to edit the code of the 'do' action of the 'demo' pipeline
to change what it does. The following will get you started.

```bash
DEMO_DIR=~/mdi-exercises/demo-mdi-tools/mdi/suites/definitive/demo-mdi-tools/pipelines/demo

ls -l $DEMO_DIR # the demo pipeline's directory
ls -l $DEMO_DIR/do # the do action's directory

cat $DEMO_DIR/do/Workflow.sh

nano $DEMO_DIR/do/Workflow.sh
# etc.
```

Your goal is to edit Workflow.sh, or a script that it calls, 
to do something the pipeline action doesn't already do.

Don't try to make it do complicated work, stick to simple system tasks for now.
The idea is to get you exploring the file structure of a pipeline
so you can see where code gets written.

### STEP #2 - Re-run the pipeline with your codes changes

```bash
cd ~/mdi-exercises/job-files
alias run-demo=~/mdi-exercises/demo-mdi-tools/run # for convenience...

run-demo demo exercise_1.yml --dry-run
run-demo demo exercise_1.yml
```

Hopefully, your modified pipeline works! If not, read and deal with
any errors.
