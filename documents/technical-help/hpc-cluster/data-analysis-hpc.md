---
layout: default
title: Data Analysis in HPC Cluster
parent: HPC Cluster
grand_parent: Technical Help
nav_order: 4
---
## Data Analysis Software

To run the different options of software in the cluster, a tool called **Environment Modules** is used. This allows you to see all the different programs already installed in the cluster as well as their different versions. From there, you can load the one you need and use it accordingly. On this [page](https://hpc.dccn.nl/docs/cluster_howto/software-modules.html), you can find more information on how to check and load software in the cluster. If you want to get a more hands-on approach, check [this set of exercises](https://hpc.dccn.nl/docs/cluster_howto/exercise_env_modules/exercise.html) before diving in with your own work. 

Certain applications are widely used and do not require any loading to connect to the cluster. **Utility scripts** are provided to integrate with job submissions to the Torque cluster. These applications are MATLAB, R and Jupyter Notebooks. For more information on what these are and how to use them see [here](https://hpc.dccn.nl/docs/cluster_howto/software-scripts.html). 

The HPC Wiki also contains **more information on how to effectively use MATLAB, R, and Python on the cluster**. These pages are relevant on how to create environments, use specific versions, and understand the features that have been hand-crafted by the TG to make your analysis pipelines as smooth as possible:
-	[MATLAB](https://hpc.dccn.nl/docs/cluster_howto/exercise_matlab/exercise.html)
-	[R](https://hpc.dccn.nl/docs/cluster_howto/exercise_R/index.html)
-	[Python](https://hpc.dccn.nl/docs/cluster_howto/exercise_python/exercise.html)

### Using Integrated Development Environments on the Cluster 
There are two [integrated development environments](https://en.wikipedia.org/wiki/Integrated_development_environment) (IDE) that you can use for coding and have specific ways of connecting them to the cluster. In some cases, this means you might be able to run the program from your laptop by using the integrated terminal in the app to connect to the cluster. 

The two options currently available are:
1.	[PyCharm](https://www.jetbrains.com/pycharm/promo/?source=google&medium=cpc&campaign=EMEA_en_NL_PyCharm_Branded&term=pycharm&content=536947779960&gad_source=1&gclid=Cj0KCQjwir2xBhC_ARIsAMTXk87pzxVhYu3tYfZEoAgH9AZW1PFA66677IDr6HewFsqER9U3XWnXC5QaAohZEALw_wcB) – an IDE for Python project. You can find more information about the IDE and how to use it in the cluster [here](https://hpc.dccn.nl/docs/cluster_howto/ide-pycharm.html). 
Our lab member Maartje Koot created a small tutorial on setting up PyCharm Pro to Run Jupyter Notebooks in the cluster. You can find that [here](./Notebooks_in_PyCharm_on_Cluster_KOOT.pdf). 

2.	[VSCode](https://code.visualstudio.com/) -- is a cross-platform source-code editor made by Microsoft. It is great for laptops that do not have a lot of memory/RAM as it is a very light app. [This page](https://hpc.dccn.nl/docs/cluster_howto/ide-vscode.html) contains information on connecting your local VSCode to the cluster server.
The developers of VSCode also have official documentation on how to do this [here](https://code.visualstudio.com/docs/remote/tunneling). 

## Data Analysis in Parallel 

This section can be thought of as a _tips and tricks_ for a specific situation: you have collected data from **multiple subjects** and you want to perform an **analysis** on each subject’s data independently. Using some of the resources above, especially knowledge of bash, you can run all these analyses in parallel and avoid running each one of them script-by-script. 

This [section](https://hpc.dccn.nl/docs/cluster_howto/exercise_da/exercise.html#exercise-da) of the HPC cluster WIKI has a small exercise in Python, R and MATLAB to see **how you can do this in each of these software options.**
