---
title: EXERCISE #1
parent: MDI Pipelines
has_children: false
nav_order: 20
---

## {{ page.title }}

In this exercise you will learn how to _use_ an MDI pipeline,
specifically, the MDI demo pipeline in this tool suite:

- <https://github.com/MiDataInt/demo-mdi-tools>

### STEP #1 - Install the MDI demo tool suite

First, create and switch to a directory where you would like to do this work.
It could be anything, but we recommend **~/mdi-exercises**.

Then, please follow these instructions to clone the repository 
and install the tool suite, being sure to follow 
**Quick Start 1: suite-centric installation**.

- <https://github.com/MiDataInt/demo-mdi-tools#quick-start-1-suite-centric-installation>

For this exercise, you only need to install Stage 1 Pipelines (not Stage 2 apps).

### STEP #2 - Write a job configuration file

To run the demo pipeline, you need to create a job configuration file,
with the instructions for what to do. 

First, you need a place to store your job file. It should NOT
be in the mdi-demo-tools folder, since you don't want job files, or your
pipeline output, to be part of the repository. We recommend creating
folder **~/mdi-exercises/job-files**.

Then, use the MDI's template function to get a structure of the required
job configuration file. Assuming you used the paths above, try:

```bash
cd ~/mdi-exercises/job-files
alias run-demo=~/mdi-exercises/demo-mdi-tools/run # for convenience...

run-demo demo template --help
run-demo demo template > exercise_1.yml
```

Then, edit the job file, changing \_REQUIRED\_ to real values.

```bash
nano exercise_1.yml
```

Start simple.  As you get comfortable, read these instructions to 
increase the complexity of your job file:

- <https://midataint.github.io/mdi/docs/job_config_files.html>

### STEP #3 - Run the demo pipeline synchronously

Let's see if your job file works!  First, let's try a test run 
in the terminal window.

```bash
run-demo demo exercise_1.yml --dry-run
```

Notice that we set option --dry-run on the command line. This means
the pipeline will only be tested, but not executed. Always do this first!

You may get an error message if you didn't create your output directory, 
didn't construct your job file correctly, etc.  

```bash
!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!
'--output-dir' does not exist or is not a directory
    /home/user/mdi-exercises/output
!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!
```

You need to fix it
until --dry-run displays a YAML format report of the action(s) the pipeline will take,
with no reported errors.

```yml
---
pipeline: demo-mdi-tools/demo:v1.0.0
# content removed for brevity
    singularity:
        image: oras://ghcr.io/MiDataInt/demo-mdi-tools/demo:v1.0
        level: pipeline
...
```

Then, repeat the call above, omitting --dry-run so that the pipeline will execute fully.
You will be asked to confirm download of the Singularity container that contains
the software to run the pipeline. Say yes.

### STEP #4 - Run the demo pipeline asynchronously

Because the demo pipeline is very simple, it was fine to run it on the login node.
But let's practice submitting it to the job scheduler.

```bash
run-demo submit --dry-run exercise_1.yml --account SLURM_ACCOUNT
```

Think about the report you are seeing, then repeat with --dry-run omitted to queue the jobs.
For this to work, you will have to have a Slurm account that you provide
to the submit command using the --account option. Use help commands to explore this, e.g.:

```bash
run-demo demo do --help
```

Use commands like the following to monitor your pipeline's execution:

```bash
run-demo exercise_1.yml status
run-demo exercise_1.yml report
```

### STEP #5 - Visualize your data in an MDI app

If you succeeded to this point, you should find a file like this:

```bash
ls -l ~/mdi-exercises/output/do/*.zip
-rw-rw-r-- 1 user user 2769 Jun  2 11:57 /home/user/mdi-exercises/output/do/do.demo.do.mdi.package.zip
```

Please download that data package to your desktop or laptop computer.
Then, upload it into the demo Stage 2 App you will find here:

- <https://mdi-demo.wilsonte-umich.io/>
- access key = **mdi-demo**

Play around in the app to see if it reflects your expectation of the demo
pipeline and the job configuration file you wrote.
