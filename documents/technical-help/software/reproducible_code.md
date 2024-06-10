---
layout: default
title: Reproducible (and Efficient) Coding
parent: Software
grand_parent: Technical Help
nav_order: 2
---

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

