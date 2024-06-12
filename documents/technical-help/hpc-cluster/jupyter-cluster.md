---
layout: default
title: Running Jupyter/iPython Notebooks Remotely
nav_exclude: true
---

# Step-by-Step to Run Jupyter/iPython Notebooks in the Cluster

## Step 1: Create SSH tunnel and start VNC server
If you don't have a VNC server already, you must start one. You can see more information on how to do this in the [HPC Cluster Access page]({% link documents/technical-help/hpc-cluster/hpc-cluster-access.md %})

## Step 2: Connect to your VNC server

Once we have a server running, we will SSH to the access node.
In a new terminal we would type:

`ssh -L 59[portnumber]:[accessnode]:59[portnumber] username@ssh.dccn.nl -p 10990`

we can now open a VNC window via a VNC viewer.

## Step 3: Submit an Interactive Job

If you want to do resource-intensive analysis, such as neuroimaging data, you should start an interactive job on the torque cluster and work from there, instead of running the notebook on the access nodes.

To do this, run these commands in your terminal in the VNC client on the cluster:

`qsub -I -l walltime=72:00:00,mem=3gb`

Currently the maximum time is 72 hours (3 days). Memory can be as much as you need. Remember that you should be mindful of the resources you request from the cluster. 

## Step 4 (Optional): Activate your Virtual Environment
By default your notebook will run in the default python environment. If you have a virtual environment, be sure to start it now (from the same terminal on the cluster):

`source activate [environment_name]`

## Step 5: Start the Notebook
Still in the terminal on the cluster, go to a directory of interest:

`cd /projects/dir_of_interest/`

{: .note}
> This directory will be the root of the jupyter kernel, meaning that from the notebook you won't be able to access any notebooks or view files in 'higher' directories than this. Typically you would therefore want to use the root of your project folder.

In that directory, launch the notebook:

`jupyter-notebook --ip=$(hostname -f) --no-browser --port=8888`

This will generate some lines and a token, looking something like this:

![jupyer-cluster-output](./jupyer-cluster.png)

Copy the token (i.e. the string after "token=") and remember the name of the compute node (dccn-c012 in this example), and the port (8888 in this example).

## Step 6: Connect to Compute Node

On your local machine, open a new terminal and SSH into the compute node where your interactive job is running:

`ssh -L 8888:dccn-c012.dccn.nl:8888 michei@ssh.fcdonders.nl -p 10990`

Here 8888 is the port of your jupyter notebook and dccn-c012 is the compute node your job is running.

{: .note}
> If you want to reconnect later, assuming the interactive job is still running, all previous steps can be skipped and you can go to step 7) directly.

{: .important}
> If you are working on your desktop from WITHIN DCCN, this step is not necessary and you can just open your browser (from windows so not on a virtual desktop) and enter [compute name]:[port] in the browser url bar, e.g. https://dccn-c012.dccn.nl:8888

## Step 7: Open your Browser and Go to the Notebook
On your remote computer, open a browser of interest and for URL type in:

`localhost:8888`

The first time you do this, you will be asked for a password, this is the token from step 5.
