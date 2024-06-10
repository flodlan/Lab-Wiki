---
layout: default
title: Software
parent: Technical Help
has_children: false
nav_order: 2
---

# Software

This section will provide you with useful information on resources and tools you can use for programming and analyzing data. The focus will be on providing an overview of important general purpose software that lies at the core of a lot of the analysis and work done by the members of the Predictive Brain Lab. 

- [Programming Languages](#programming-languages)
  - [Python](#python)
  - [MATLAB](#matlab)
  - [R ](#r)
- [Reproducible (and Efficient) Coding](#reproducible-and-efficient-coding)
  - [GitHub](#github)
  - [The Unix Shell](#the-unix-shell)
  - [Writing Code](#writing-code)
- [Reference Management Tools](#reference-management-tools)
  - [Zotero](#zotero)
- [Taking Notes and Writing Papers](#taking-notes-and-writing-papers)

## Programming Languages
### Python
Python is a general-purpose, open-source programming language known for its simple syntax, easy readability, and efficient commands. It has become the standard in most technical fields, including deep learning, due to its advanced capabilities. 

For researchers, Python simplifies complex tasks like visualizations, machine learning, and statistical analysis, often requiring only a few lines of code with the right package. 

Additionally, learning Python is easy, especially for those already proficient in another programming language.

#### Starting with Python 

If you have never seen or used Python, we will provide you with useful resources to get you up to speed. This will avoid you getting stuck or learning bad coding practices. Once you are familiar with data types, looping, functions, modules and especially `numpy`, you should be ready to 'hit the streets'.

Interactive resources online are one of the best ways of learning Python as they teach you with a hands-on approach.  However, some of these require you to pay, which is not always ideal. Hence, we will highlight both payed and free resources for you.

* [DataCamp](https://app.datacamp.com/) - Amazing resource full of tutorials and lectures that provide a comprehensive understanding of Python as well as specialized courses that might be useful for you as a researcher.

{: .note }
> Some people in the lab have free access to DataCamp. You can ask around to see whether they can provide you with this free access. 

* [Codecademy](https://www.codecademy.com/learn) - Very similar to Data Camp with the difference that some of their courses are given for free.

* [Lab in Cognition and Perception (Todd Gureckis)](https://teaching.gureckislab.org/spring24/labincp/intro.html) - A nice resource tailored to learning Python from scratch and applying it to neuroscience. If you are just looking to purely learn Python, this is NOT the resource for you as it also include theoretical information about the brain.

* [Python Data Science Handbook](https://jakevdp.github.io/PythonDataScienceHandbook/) - This digital book is a detailed and amazing resource created by Jake VanderPlas. It provides very comprehensive explanations that will ensure a strong programming foundation.

* Learn Python 3 The Hard Way (Zed Shaw) - This book is a perfect introductory text that, despite its name, will get you up to speed in no time.

{: .note }
> You can find the PDF for the book online by typing the title + PDF

* [Introduction to Programming in Python](https://www.ru.nl/en/education/education-for-professionals/overview/introduction-to-programming-in-python-rss0002-closed) - The Radboud University offers a **five-day introduction to Programming in Python course** designed for social scientists - with zero experience in programming - who would like to conduct data collection, analysis, and modelling with Python.

##### Not a Beginner?
* [Python for Neuroscientists (Tomas Knappen)](https://github.com/tknapen/python_workshop-Basel/tree/master) - This series of Python tutorials is directed towards neuroscientists and can serve to refresh your knowledge of some Python commands. 

* [Python Research Masters Course (Lukas Snoek)](https://lukas-snoek.com/introPy/index.html) - This is a course designed by Lukas Snoek for Research Masters students from the University of Amsterdam that assumes basic knowledge of programming languagues. It is directed towards behavioral sciences and includes a module of programming in [Psychopy](https://www.psychopy.org/)


#### How to use Python?
As with any other programming language, you can only really learn it by using it. Therefore, by far the easiest way to learn Python is to choose a new project and plan up front to do this entire project (or at least a part of it, like all fMRI-analysis) in Python - and stick with it.  

We recommend to postpone your learning until you will start using Python for your work. Even when you use some of the resources highlighted above, all the time might be wasted if you do not use the things you have learned consistently. 

#### Python's Organization
Python is not an all-in-one product. At its core it is a programming language, which comes in different versions (Python 2 and 3). There are different distributions, which contain the pure language in addition to a lot of packages (these are like toolboxes for different needs you might have). Becase Python is open source and not centrally planned, these different distributions might have different ways of updating and maintaining them. 

Additionally, Python does not come with a programming environment. This means you need to make use of a interactive development environment (IDE) or a code editor to use it. 

All these options can be overwhelming to a beginner. Hence, we always recommend reading a little bit about Python before starting. You can see [here](https://github.com/swc-pyclub/pystarters/tree/master/topic_1_interactive_python) for an  easy introduction. 

In general, our recommendations are:

* Install Python with [Anaconda](https://www.anaconda.com/) as a distribution
* Use virtual environments to maintain dependencies.
* Use conda to manage packages — or pip but only use pip *in a virtual environment*.
* Use one of the following IDEs for programming:
  * [PyCharm](https://www.jetbrains.com/pycharm/?source=google&medium=cpc&campaign=EMEA_en_NL_PyCharm_Branded&term=pycharm&content=698987581422&gad_source=1&gclid=CjwKCAjwvIWzBhAlEiwAHHWgvTa8eQkxFxhaniSEJ8J9yk2YYQOQKSi1kvFbF1WoaJJhEzuRS7ocHRoCOh0QAvD_BwE) - Great tool and widely used. Not the default if your laptop has low RAM Memory.
  * [VSCode](https://code.visualstudio.com/) - Easy to use, can be used in the cluster directly, suitable for laptops with limited memory.
  * [Jupyter notebooks or JupyterLab](https://jupyter.org/) - Not the first recommendation, but you might already be familiar with them 

### MATLAB
Matlab is a programming platform and language that was specifically developed to perform computational mathematics (Matlab stands for Matrix Laboratory). It is tailored specifically for scientists and engineers and has relatively simple syntax. Unlike Python and R, Matlab is paid software, which means a specialized team provides constant updates to the program. On the downside, its prices make it less accessible for the general public. 

It used to be the golden standard in neuroscience for a number of years and still is in a lot of places. In general, this is the default programming language at the DCCN given that toolboxes to analyze neuroimaging data ([FieldTrip](https://www.fieldtriptoolbox.org/)) and present experimental designs ([PyschToolbox](http://psychtoolbox.org/)) were developed at the Donders Institute using Matlab. This means, direct support is available at the DCCN in case you have questions while using this program. Additionally, everyone working at the DCCN gets a free suscription, making it appealing as a first choice (you can ask the [Technical Group](https://intranet.donders.ru.nl/index.php?id=helpdesk) for help to install it in your computer) 

#### Starting with MATLAB

Being a payed software, the MATLAB creators have great tutorials and documentation on their software online. 

* [MATLAB Tutorials](https://nl.mathworks.com/support/learn-with-matlab-tutorials.html)

Besides their tutorials, there are not a lot of courses online available to learn how to use MATLAB in an interactive way. However, we will provide some resources below that can help you get up to speed with it:

* [MATLAB: A Practical Introduction to Programming and Problem Solving](https://www.sciencedirect.com/science/article/pii/B9780128045251099918). This book starts from learning the basics of programming to how to use the powerful capabilities of MATLAB for scientific analysis. 
* [MATLAB for Brain and Cognitive Scientists](https://mitpress.mit.edu/9780262035828/) - This book teaches brain scientists how to program in MATLAB, with a focus on applications most commonly used in neuroscience and psychology. The advantage of this resource over others is that it provides not only beginner level information, but goes all the way to advanced.


### R 
R is a programming language and platform for **statistical computing and data visualization**. It is the preferred software for statisticians and some lab members use it for their statistical analysis. 

Similarly to Python, the core R language is the augmented by a variety of extension packages (something like toolboxes) that allows you to do specific analysis. In addition, it is open-source and free software, which makes it readily available and easy to understand. 

We would not recommend learning R as your **first and only** programming language during your time in the lab as you most likely will have to make use of some of the other two programming languages mentioned above (_e.g.,_ for creating experiment scripts). However, it is a very powerful tool that in a lot of occassions can do more than what you would expect it, especially for data wrangling and visualizations. 

The program R works with an interpreter that looks very similar to the terminal in your computer. To effectively use R, we recommend making use of [RStudio](https://posit.co/download/rstudio-desktop/), which makes it look like other IDEs. 

R also contains [RMarkdown](https://rmarkdown.rstudio.com/), which is a format for writing reproducible, dynamic reports with R (similar to Jupyter Notebooks for Python). It allows you to turn your analyses into high quality documents, reports, presentations and dashboards. This means you can write and keep an always up-to-date manuscript in there (using [LATEX](https://www.latex-project.org/)) or HTML-Presentations.

#### Starting with R

One of the main contributors to the programming language R, [Hadley Wickham](https://hadley.nz/), has created a very useful and interactive book to teach you to do data science with R. It goes through how to use it, look at structures, transform and visualize them. 

* [R for Data Science (2e) - Wickham ](https://r4ds.hadley.nz/)

There is a different way of doing R called the tidy way. This is super useful for organizing your data, reproducibility and doing your statistical analysis. While the resource above contains some information on how to use this 'tidyverse', the following book is **focused** on learning how to use R in a tidy way.

* [Statistical Inference via Data Science: A ModernDive into R and the Tidyverse (2024)](https://moderndive.com/index.html)

Besides the two books previously mentioned, you can learn R through a variety of interactive tutorials online. 

* [DataCamp](https://app.datacamp.com/learn/courses?technologies=1) - This resource contains a large range of courses to learn to use R, from the most beginner friendly to very advanced analysis.

* [Codecademy](https://www.codecademy.com/learn/learn-r) - Similar to DataCamp, this resource contains tutorials with interactive exercises to learn how to code using R. 

The two resources mentioned above require you to have a paid suscription, however, there are also other free options online

* [SWIRL](https://swirlstats.com/) - an R package that teaches you how to use the programming language interactively. You have to install the package and it has instructions that walk you through the most important information to use R.

* [Programming in Psychological Science with R (Michael Nunez and Hannes Rosenbusch)](https://github.com/mdnunez/PIPS_course?tab=readme-ov-file) - This is a four week course that introduces master's students of the University of Amsterdam to the usage of R and Python. It should be beginner friendly and prepare you for the type of usage you will most likely need in your time at the PBL lab.

If none of these materials seem to suit your needs, the Radboud University offers summer courses to learn how to use R:

* [Introduction to Data Science with R and Rstudio](https://www.ru.nl/en/education/education-for-professionals/overview/introduction-to-data-science-with-r-and-rstudio-rss301-confirmed)
* [Introduction into R](https://www.ru.nl/en/education/education-for-professionals/overview/introduction-into-r-rss209-confirmed)
* Crash Course in R – A Gentle Introduction (https://www.ru.nl/en/education/education-for-professionals/overview/crash-course-in-r-a-gentle-introduction-rss0006-confirmed)


## Reproducible (and Efficient) Coding 
### GitHub
#### What is Github?
Git is a software that allows you to do version control of your scripts and files in detail. What version control does is that each time you modify your code, it saves a version of how the code looked like before that modification. In this way, it allows you to go back to how your files looked like before certain changes happened (similar to how Google Docs works). Another advantage of Git, is that is makes it easier to work together on projects and conduct new ideas independently. Once again, similar to Google Docs, Git allows you to collaborate with other people in a specific project indicating what each person has contributed to that work. 

**Importantly, Git and Github are not the same thing.** Github, which is based on Git, is an online (cloud) platform that makes working together easier. It provides you with a direct way of sharing your projects online with colleagues and the outside world. 

##### Why would I use Github?

Github has many advantages at the individual but also at the group level:
- It allows you to keep the code and files for your project organized (without having a billion files names `project_X_V1`, `project_X_V2`, `project_X_V2_good`, etc...)
- It allows you to have a place in which you can go back to previous code in case something breaks in a very easy way
- Straightforward way to share your projects online with colleagues and the outside world
- It allows you to find, develop and publish analysis scripts and research software. Other developers and researchers can then use and adapt these in turn (_e.g.,_ you might find specific toolboxes or code that provide you with information on how to perform certain analysis)

{: .important }
> You might be discouraged to use GitHub thinking that everyone will be able to see your code. However, you can make all your code PRIVATE! and only share it with others once you are satisfied.

#### Github sounds amazing. How do I start?
Luckily, there are a lot of resources online to start using Github. 

First and foremost:
* [How to Install Git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)

Tutorials:

- [Github's Tutorials](https://docs.github.com/en/get-started) - The obvious first option to mention is Github's own documentation website. They have very clear explanations and tutorials on how to use Github efficiently.

- [Data Camp](https://tinyurl.com/4dz84h6y) - DataCamp has a great interactive tutorial on what GitHub is and how to use it. It also includes a module on shell scripting, which means you would be killing two birds with one stone!

- [Software Carpentry Git Novice](https://swcarpentry.github.io/git-novice/) - Great resource to get up to speed on using Git. Recommended by many data scientists as one of the best ways of learning Git. 

- [Donders Institute Agenda](https://www.ru.nl/en/donders-institute/agenda) - The Donders organizes different workshops throughout the year in which they often include introductions to Github. The next one will occur at the Graduate Day of the Donders Institute. We recommend keeping an eye in the agenda linked above. 


### The Unix Shell
At some point during your time as a researcher you will have to interact with the command line interface (CLI; this is the termianl in your computer). Either for running jobs on the cluster, using Github or creating environments in Python. While you do not need to be proficient in the CLI to succesfully do your work, it is a great skill to have that will surely make your work more efficient. 

We will highlight some resources that you might find useful to learn how to interact with the shell (terminal) of your computer:

* [Software Carpentry](https://swcarpentry.github.io/shell-novice/) - They provide very useful hands-on tutorials to learn shell scripting. They are highly recommended by data scientists.

* [Data Camps](https://app.datacamp.com/learn/courses/introduction-to-shell) - They have interactive tutorials full of exercises to master the basics of the shell. Highly recommended by some of our lab members.

* [HPC Wiki Tutorials](https://hpc.dccn.nl/docs/linux/index.html) - The people from the TG that maintain the HPC Cluster from the Donders, created a introductory tutorial on how to use Linux and the shell terminal. This should provide you with basic information on shell that can be applied to other situations besides using the cluster. The advantage is that by doing this tutorial you will have all the necessary shell scriptings skills for running jobs on the cluster. 

### Writing Code

Code is often written without annotations, modularity, and generality, leading to scripts with hard-coded parameters that are difficult to reproduce or adapt. Poor organization and ignoring coding conventions increase the likelihood of bugs and make debugging harder. This can result in numerous questions if you share your code or difficulties understanding your past work.

Fortunately, resources are available to improve your coding practices, enhancing reproducibility for both the scientific community (which as part of the Donders you are commited to) and yourself. Here are a few to get you started:

* [The Good Research Code Handbook by Patrick Mineault](https://goodresearch.dev/index.html) - Handbook created by [Patrick Mineault](https://xcorr.net/about/) with a series of coding principles that should improve the way your organize your data

* [Lightweight guidelines for code and data sharing by Sam Gersham](https://gershmanlab.com/docs/Sharing.pdf) - A series of concise guidelines that should already help you organize your code and data more efficiently. 


## Reference Management Tools 
### Zotero

[Zotero](https://www.zotero.org/) is a bibliography management tool that enables easy importing of citations (to papers etc.) from online sources, automatically grabs the PDF for stuff you import, and integrates with Word (or BibTeX) to manage bibliographies in your own papers. 

Installing Zotero and the corresponding browser connector on your computer is relatively straightforward and information about this can be easily found [online](https://www.zotero.org/). 

Already good on its own, Zotero really shines when you (1) instruct it to store PDFs of papers somewhere in your OneDrive Donders folder and (2) use the ZotFile plugin to automatically rename and move new attachments. Incidentally, this also means you will never run out of Zotero account storage (which can fill up very quickly with PDF attachments), since your files are all stored inside OneDrive. This page will explain how to setup Zotero in such an optimal fashion. 

{: .note }
>You will need to do all these steps exactly once on every machine on which you wish to use Zotero.

There are other reference tools besides Zotero (_e.g.,_ Mendeley), but we recommend sticking to this one.

#### Zotero and One Drive: Your Library in the Cloud

**Step 1: Instruct Zotero to store PDFs in Dropbox**
1. Open Zotero.
2. Edit -> Preferences -> Advanced -> Files and Folders
3. At 'Base directory', choose a folder that lives inside your OneDrive (you might need to create it first), e.g. "C:\Users\eelspa\OneDrive (Personal)\Zotero PDF" in my case.
4. It's recommended to leave 'Data Directory Location' untouched! Storing the actual Zotero database inside OneDrive can lead to problems, so just leave it in some local folder only (the default is fine).
5. Press OK.

**Step 2: Install Zotfile**
1. Head to http://zotfile.com/ and click the 'Download' link.
2. In Zotero, go to Tools -> Add-ons.
3. Click the gear (⚙) icon at the top right -> Install add-on from file…
4. Select the .xpi file you just downloaded from the Zotfile website.
5. Zotfile will be installed into Zotero. You may need to restart Zotero now.

**Step 3: Setup Zotfile to integrate with your OneDrive PDF folder**
1. Inside Zotero, go to Tools -> ZotFile Preferences.
2. On the tab 'General settings', section 'Location of Files', make sure 'Custom Location' is selected and have it point to the same OneDrive PDF folder you selected in step 1.3 above.

**Step 4: BONUS! Nice filenames**
1. While still in ZotFile Preferences, head to tab 'Renaming rules', make sure 'Use Zotero to Rename' is unchecked.
2. Enter the following to get sensible filenames, similar to what we're all used to in e.g. APA-compliant bibliographies:

![Zotero_One_Drive](./zotero_onedrive.png)

**Step 5: Test it out!**
Make sure Zotero is running.
Head to any journal article on the web in your browser and click the "Save to Zotero" button. It should now be added to your library, the PDF should be downloaded automatically, stored in the folder you selected, and renamed according to the rules you defined in step 4.
OneDrive will take care of syncing the new file to the cloud, so you have access to your full-text library wherever you go!

## Taking Notes and Writing Papers

The resources that will be highlighted here are software options that should make note-taking and writing easier. 

### Note-Taking
If you are looking for a transition to an app that allows you to keep notes in a similar fashion as handwritten ones. You can look at:
- [Notion](https://www.notion.so/) - It is a productivity and note-taking application that provides you with a highly customizable space for planning and writing. While the free suscription should be enough for individual project, it is paid software
- [Obsidian](https://obsidian.md/) - Similar to Notion, it is a note taking app that allows you to have your documents easily accesible and organize them in an intuitive manner. It is free for personal use

### Writing Papers

There are a wide range of software options that you can be using for writing scientific papers. Here, we are only providing tips that might make this process easier for you.

The Donders Institute provides all of its employees with the basic Office365 package. This means that you will automatically have access to a suscription of [Microsoft Word](https://intranet.donders.ru.nl/index.php?id=computerservices) to edit any text document. This text editor can be enhanced by linking your Zotero resource manager to it so it automatically keeps track of your references and automatically generates a reference table. 

#### Alternative
LaTeX is a document preparation system used for the communication and publication of scientific documents. It provides a consistent formatting style that can be used to create complex documents with ease (such as scientific papers). The main advantages of LaTeX is the way it handles formatting (to look professional and follow your specifications) as well as adding equations (if your paper contains a lot of equations, we highly recommend it). Additionally, you can link your Zotero to it, making it equally nice for bibliography handling as Microsoft Word. 

[Overleaf](https://es.overleaf.com/) is an online LaTeX editor that's easy to use. No installation, real-time collaboration, version control, hundreds of LaTeX templates, and more. It expans on using LaTeX and provides extra features that make it more attractive. In specific, allowing for collaborations means it has the functionality of Google Documents with the addition of all the features that make LaTeX special. 

The downside: learning to write in LaTeX will take some effort. However, as with a lot of things in science, it eventually ends up saving you time. If you try and see that this is not for you, we always recommend sticking to the software that works best for your personal working style. 

Here we attach a LaTeX tutorial in case you want to give it a go:

* [LaTeX Tutorial](https://www.overleaf.com/learn/latex/Learn_LaTeX_in_30_minutes)






