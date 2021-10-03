---
title: Exercise
parent: Code Collaboration
has_children: false
nav_order: 4
---

## {{ page.title }}

Excellent! You are ready to engage in a bit of code collaoration!
When you are done, you will see the following values update with your changes:

> {{ site.data.status.number_of_people }} people have successfully completed this Excercise
as of {{ site.data.status.most_recent_date }}.

## Prerequisites

To briefly recap, we expect that you have completed all the steps
in the previous sections, and that you now have:

- installed Visual Studio Code
- created a GitHub account
- logged into GitHub from within VS Code

## STEP #1 - Fork This Repository

As mentioned, MDI Basic Training is a public GitHub repository.
Your first step is to fork it into your GitHub account:

- go to: <https://github.com/MiDataInt/mdi-basic-training>
- find and click "Fork" in the upper right corner

That's it! You now have your own complete copy of this web page.

## STEP #2 - Clone Your Fork Using VS Code

Your fork of the repo is currently only on GitHub. You need
to have a copy on your local computer so that you can edit it.
To do this:

- go to your fork on GitHub
- click the big green "Code" button
- copy the link, i.e., https://github.com/<YOUR_USER>/mdi-basic-training.git
- open VS Code
- if you have a file or folder open, use 'File' to close it
- see: <https://code.visualstudio.com/docs/editor/github#_cloning-a-repository>
    - click the Source Control icon in the left sidebar
    - click Clone Repository
    - paste in the link you copied above
    - pick a folder where your clone will be stored

You will now have a local copy of your fork, ready to edit in VS Code.

## STEP #3 - Edit a File in Your Clone

First, take a minute to browse around the folders of this Basic Training
repository. For example, can you find the file that has the text for this page?

Then find the file **_data/status.yml**.  Read the comments in the file
to begin to understand how YAML files work (more on this later). 

Finally, edit the file by incrementing 'number_of_people' up by one (the 
new person is you!) and changing 'most_recent_date' to today's date. These are the changes you will now send back up the chain. Save the file.

## STEP #4 - Push the Changes to Your Fork on GitHub

The changes you just made are currently only found on your local
computer. To get them onto GitHub:

- click the Source Control icon in the leftmost sidebar
- find the "+" symbol for your Changes
- click the "+" symbol, which will _add_, or _stage_, your changes
- type a short message in the text box, e.g. "increment status.yml"
- find and click the checkmark icon, which will _commit_ your changes
- click the "..." icon and find and click "Push", which will push your changes to your fork of the repository on GitHub

To summarize, you just went through three basic actions in Git:
- "add", i.e., stage, code changes for commiting
- "commit" changes, with a short, descriptive message
- "push" changes from your local computer to GitHub

## STEP #5 - Make a Pull Request on GitHub

The changes you just made are now on GitHub, but only in your fork.
You are free to use them there however you'd like (e.g., you could
run your own version of this web page with the changes).

However, we really want to see your new change incorporated into the
definitive MDI repository. To do that you need to make a "Pull Request",
which mean you will ask the MDI maintainters to pull the change from your
fork into the main repo.

- go to your fork of the Basic Training repository on GitHub
- verify that you see the evidence of your recent commit
- find and click the "Contribute" button
- click the big green button labeled "Open Pull Request".

Note: you can also make the Pull Request from within VS Code; try to find
where you would do this.

## STEP #6 - Wait for Your Changes to Be Accepted

Once an MDI maintainer reviews and merges your changes into the 
definitive repository, you will see evidence of them by reloading this web page:

https://midataint.github.io/mdi-basic-training/
