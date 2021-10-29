---
title: "Remote_Server"
parent: Working_Notes
has_children: false
nav_order: 1
---

## {{ page.title }}


## Stage 1 pipelines

Because Stage 1 pipelines entail handling of large files
and computationally intensive data analysis steps,
in general they are executed on a remote HPC server.
As a result, it is usually best to develop pipeline
code within such a server environment.

Instructions below will help set up an optimal environment
for developing Stage 1 pipelines on the Michigan Great Lakes
server cluster. Small modifications would allow you to use
any other Linux server in a similar fashion.

### Get a Great Lakes account and login

Pending.

### Editing code on the server

The code development tools that are available in a command line terminal 
of the type accessible by SSH are much less versatile as compared 
to VS Code. Fortunately, VS Code is designed to allow you to edit
and develop code remotely.  Complete descriptions can be found here:

<https://code.visualstudio.com/docs/remote/remote-overview>

First, install the VS Code extension **Remote - SSH**, by Microsoft,
if you did not do that earlier.

Because Great Lakes uses interactive two-factor authentication, you should 
set Remote-SSH to allow you to always see the login prompts:
- click the Extensions icon on the left sidebar of VS Code
- click "Remote - SSH" on the list
- click the gear icon
- select "Extension Settings"
- at the top, search for "login"
- make sure "Remote.SSH: Show Login Terminal" is clicked
- close the above tabs

Next, add your Great Lakes account to Remote-SSH.
- click the "Remote Explorer" icon on the left sidebar of VS Code
- click "+" to add a remote ssh target
- type or paste "ssh YOUR_USER_NAME@greatlakes-ts.umich.edu"
- hit Enter

To start working in VS Code on Great Lakes
- click the "Connect to Host" icon next to your new greatlakes SSH listing
- in the new window, at the top you will be asked to select "Linux" as the server type
- complete the two-factor authentication process as prompted in the terminal window
- wait for potentially several minutes as VS Code is set up on Great Lakes

If successful, at the bottom left of the window you should see a green
status bar that tells you that you are successfully connected to Great Lakes.
You may now proceed to use VS Code exactly as before, but now you are
working on Great Lakes, with access to its file tree, command line, etc.

As a last step, you will want to repeat the MDI installation on Great Lakes.
