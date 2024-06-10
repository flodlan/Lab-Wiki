---
layout: default
title: Software
parent: Technical Help
has_children: false
nav_order: 2
---

# Software
- [Programming Languages](#programming-languages)
  - [Python](#python)
  - [MATLAB](#matlab)
  - [R ](#r)


This section will provide you with useful information on resources and tools you can use for programming and analyzing data. The focus will be on providing an overview of important general purpose software that lies at the core of a lot of the analysis and work done by the members of the Predictive Brain Lab. 

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




