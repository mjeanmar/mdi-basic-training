---
title: VS Code
parent: Remote Access
grand_parent: HPC Servers
has_children: false
nav_order: 20
---

## Work remotely using VS Code

The code editing tools available in a command line terminal 
of the type accessible by SSH, or via Open OnDemand, 
are less versatile than a dedicated IDE, which
more readily supports things like version control, parallel
editing of multiple files, syntax checking, code testing, and more. 

Fortunately, VS Code lets you edit and develop code remotely. 
Complete descriptions can be found here:

- <https://code.visualstudio.com/docs/remote/remote-overview>

### Install and configure Remote - SSH

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

### Set up Great Lakes (or your HPC server) access in VS Code

Next, add your Great Lakes account to Remote-SSH.

- click the "Remote Explorer" icon on the left sidebar of VS Code
- click "+" to add a remote ssh target
- type or paste "ssh YOUR_USER_NAME@greatlakes.arc-ts.umich.edu"
- hit Enter

### Connect to the server 

To start working in VS Code on Great Lakes:

- click the "Connect to Host" icon next to your new greatlakes SSH listing
- in the new window, at the top you will be asked to select "Linux" as the server type
- complete the two-factor authentication process as prompted in the terminal window
- wait for potentially several minutes as VS Code is set up on Great Lakes

If successful, at the bottom left of the window you should see a green
status bar that tells you that you are successfully connected to Great Lakes.
You may now proceed to use VS Code exactly as before, but now you are
working on Great Lakes, not your own computer.

{% include figure.html file="hpc/vscode-remote.png" %}

### File browsing and editing

File access doesn't require any further explanation - it works more or less
the same as if you were accessing local files.

### Command line terminal

Click **View >> Terminal** to open a terminal window on the server.

Alternatively, right-click on a folder in the file tree and
select "Open in Integrated Terminal" to go straight there. 

Among other useful features is the ability to split terminals - 
it is common to have multiple terminals open at the same time under active use.
