---
layout: default
title: HPC Cluster Access
parent: HPC Cluster
grand_parent: Technical Help
nav_order: 1
---

## Cluster Access

The system that connects multiple computers together is what we call **the cluster**. You can access it using any computer in the DCCN building or through your personal laptop.


{: .note }
> To connect to the cluster you need to be connected to the DCCN network through your eduVPN account (if you need help to do this, you can [contact the TG](https://intranet.donders.ru.nl/index.php?id=helpdesk)).

When you are connected to the cluster, you are not directly accessing the high-performance computers. Instead, you access what is called **access nodes** that allow you to “talk” to the HPC and send in your work. These **access nodes** are called **mentat001, mentat002, mentat003, mentat004, mentat005, mentat006.**

**Important**: 
-	The access nodes are **NOT** a computer cluster, but they are linked to it. 
-	You are **NOT** allowed to run heavy computations on them. 
-	They have very limited memory/RAM (only 4gb)

There are two ways of accessing one of the access nodes: a **command line interface (CLI)** and a **graphical user interface (GUI)**. From the CLI you will use a terminal (shell) to navigate the access nodes and communicate with the HPC. From the GUI you will see a graphic desktop window (running on [LINUX](https://en.wikipedia.org/wiki/Linux) software) on your computer which you can navigate and use the terminal there to send your commands. 

### Command Line Access (CLI)
The command line access allows you to connect with one of the access nodes using a terminal interface (i.e., you will be using the **access node** computer only by typing in commands in the terminal).  From there you can access all of your user data present in the DCCN cluster as well as send your analysis to the HPC. 

To effectively use the terminal, you will have to learn how to navigate it using certain commands (using LINUX). If you are not familiar with this, check [here](#linux) for resources to learn how to do it.

#### How to Connect to the CLI?

For **Windows users** see the instructions [here](https://hpc.dccn.nl/docs/cluster_howto/access-internal.html#ssh-login-with-putty).

_Tips and Tricks_
-	You can use any of the `mentat00x` servers. There is not a rationale for picking one over another.
-	The configuration on the HPC WIKI is exactly how the screen in your computer should look like 
-	When you are logging in with your username and password, you will not see the password being typed. However, it is there, so once you finish, simply click enter (this is the DCCN account in which the username is composed of the three first letters of your name and surname)

For **MacBook users**

The HPC wiki does not contain information on how to do it. For this operating system (OS), you will **not** be making use of PUTTY. 

These are the steps:
-	Open the terminal of your computer (`cmd+spacebar` and type in `terminal`)
-	In the terminal you will directly type:
`ssh username@mentat00x.dccn.nl` (e.g., ssh pauort@mentat003.dccn.nl)
-	You will be prompted to insert your password (your typing will not be appearing, but it is being typed).
-	Done! You will see a message that says you have effectively connected to the server on your terminal. 

### Virtual Network Computing (VNC)
The VNC allows you to connect with one of the **access nodes** using a graphical user interface (GUI). This means you will see a desktop window pop-up that allows you to use the access node as if it were your own desktop (e.g., run apps, open folders, etc.). Within that LINUX desktop, you can open a terminal and use it to communicate with the HPC. 

The **general two stages to set up the VNC** are the following:
1.	Start the VNCserver (in the remote system (_i.e.,_ access node))
2.	Use a VNCviewer client (on your personal desktop) to connect to a (remote) VNCserver

The step-by-step to connect to the VNC for both Windows and MacBook users are essentially identical. You can find the detailed steps with illustrations on this [page](https://hpc.dccn.nl/docs/cluster_howto/access-internal.html#vnc-for-graphic-desktop). 

_Tips and Tricks_
-	The first time you start a VNC server, it will prompt you to enter a password. This is a **new password unique for when you use the VNC** (not related to any of your other DCCN accounts). This password is needed so other users don't join your session. 
-	In step 2, when you select a host. Go for the first option as this is the recommendation given by the system.
-	Remember to always write down the VNC server associated with a display endpoint – `mentat00x.dccn.nl:xx` (you want to keep track of the numbers in the spaces occupied by the x’s here). This is so you can tell your computer to which serve to connect once you set up the GUI.  
-	For MacBook users, you will need to download the Tiger VNC Viewer. You can do that [here](https://tigervnc.org/). Click on the GitHub release page, then on the sourceforge website and download the latest version. 
