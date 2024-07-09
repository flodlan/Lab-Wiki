---
layout: default
title: Neuro-AI Resources
parent: Neuro-AI
nav_order: 1
---

# Neuro-AI Resources
This page will try to highlight resources that can be very helpful if you are trying to get up to speed in the field of NeuroAI. Some of them might be more focused on the AI side of things while others will be directly tailored towards the combination of both.

Before going through any work on NeuroAI, we recommend trying to understand why this field exists and the goals associated with it. These two papers provide a great summary of the aims of this type of work:
- [Cognitive Computational Neuroscience](https://www.nature.com/articles/s41593-018-0210-5)
- [The Neuroconnectionist Research Programme](https://www.nature.com/articles/s41583-023-00705-w)

#### Before Starting
The resources mentioned here assume that you have neuroscience knowledge and programming knowledge. It is very unlikely that you will not know about neuroscience, however, if for some reason your background is purely a Machine Learning one, check out this resource:
* [Neuroscience for Machine Learners](https://neuro4ml.github.io/)

Additionally, if your programming knowledge is not as strong as you wish, check out the [Programming Section]({% link documents/technical-help/software/programming_languages.md %}) of the wiki and focus on Python.

The resources you should know before starting to work with NeuroAI are the following:
- Python Programming
    - Specifically, try to learn about [Object Oriented Programming](https://www.datacamp.com/tutorial/python-oop-tutorial)
- Linear Alegbra (check the [Stats & Maths]({% link documents/technical-help/maths-and-stats/maths-and-stats.md %}) section)
- Trying to properly understand Regression models in Machine Learning - [link](https://www.codecademy.com/learn/machine-learning-introduction-with-regression)

### Starting Point (Software)
When working with NeuroAI, you will most likely be exclusively working with Python. While there are other programming languages that you might be able to use, we recommend sticking to Python.
Within Python, there are three packages that you will need to know relatively well to be able to do NeuroAI projects, these are:

- [PyTorch](https://pytorch.org/) or [Tensor Flow](https://www.tensorflow.org/) -- Package for Neuroscience related tools
    - [Tutorial for Pytorch](https://app.datacamp.com/learn/courses/introduction-to-deep-learning-with-pytorch?utm_source=google&utm_medium=paid_search&utm_campaignid=654038607&utm_adgroupid=149047152950&utm_device=c&utm_keyword=python+pytorch&utm_matchtype=p&utm_network=g&utm_adpostion=&utm_creative=680154148299&utm_targetid=kwd-868783079006&utm_loc_interest_ms=&utm_loc_physical_ms=9197724&utm_content=tech~python~pytorch&utm_campaign=220808_1-sea~tech~python_2-b2c_3-row-p1_4-prc_5-na_6-na_7-le_8-pdsh-go_9-nb-e_10-na_11-na&gad_source=1&gclid=Cj0KCQjwv7O0BhDwARIsAC0sjWP8WfTQky-DAW5EqP5erNHIfLQr92moCXG8uiD7vF-tjPbe20OfZUkaAg_6EALw_wcB)
    - [Tutorial for TensorFlow](https://www.tensorflow.org/tutorials)
- [SciKit Learn](https://scikit-learn.org/stable/) -- Package for Machine Learning tools (also relevant outside of NeuroAI)
    - [SciKit Learn Tutorial (Machine Learning)](https://app.datacamp.com/learn/courses/supervised-learning-with-scikit-learn?utm_source=google&utm_medium=paid_search&utm_campaignid=898687156&utm_adgroupid=150708303240&utm_device=c&utm_keyword=&utm_matchtype=&utm_network=g&utm_adpostion=&utm_creative=661527087971&utm_targetid=dsa-2220136287253&utm_loc_interest_ms=&utm_loc_physical_ms=9197724&utm_content=dsa~generic~courses~python&utm_campaign=220808_1-sea~dsa~generic_2-b2c_3-row-p1_4-prc_5-na_6-na_7-le_8-pdsh-go_9-nb-e_10-na_11-na&gad_source=1&gclid=Cj0KCQjwv7O0BhDwARIsAC0sjWOoCkqWE9Aoz-riVDBBL1Pkf2dz41N8sprctzwdF9rlqKFOgzya0yQaArOyEALw_wcB)
- **EXTRA** [Pandas](https://pandas.pydata.org/) -- Package to work with Data Frames (particularly useful if you want to use Large Language Models)
    - [Pandas Tutorial](https://www.datacamp.com/tutorial/pandas)     

All of these packages include the functions that you will be using when working on this type of work. Additionally, being proficient on them will allow you to more easily understand the code of other researchers. 
PyTorch and Tensor Flow are quite similar and in principle you should not have to learn both. We recommend reading about them online and deciding which one suits your needs. In general, PyTorch is the preferred option (at the current moment, this might change)

### Courses 

#### NEUROMATCH
Neuromatch is a collective effort by many researchers around the world to create an online summer school that provides people from all over the world with the possibility of learning about Neuroscience and AI. Even more amazing, the organizers provide all their materials for free (lectures and tutorials) for everyone to use. These are an invaluable source to learn about NeuroAI in a thorough fashion. 
While we recommend attending the summer school (if possible), you are definitely encouraged to try out these different courses yourself. 

{: .note}
> They are intended to be a two/three-week summer school. Hence, you might want to take that into consideration.

- [Deep Learning Course](https://deeplearning.neuromatch.io/tutorials/intro.html)
- [Computational Neuroscience Course](https://compneuro.neuromatch.io/tutorials/intro.html)
- [NeuroAI Course](https://neuroai.neuromatch.io/tutorials/intro.html)

These materials, due to their interactive nature, will get you up to speed in your programming as well as conceptual skills!

#### NEURO-AI SUMMER SCHOOL

Recently, a summer school took place at the Univeristy of Amsterdam. Some of our lab members were able to attend such school in which they had to work through four-hour long interactive JupyterNotebooks in the afternoons. These cover a broad range of topics within the field of NeuroAI. 

This [link](https://drive.google.com/drive/folders/1l5hHjxTCVIORzgUiHHfxSlcUGUeIX22H?usp=drive_link) contains a folder with the different notebooks. 
If you are new to JupyterNotebook you can open the different files using Google Colab (they were intended to be used there)

{: .note}
> These are learning materials, which means that some of them will not contain the answers for the different exercises. Hence, we recommend doing these courses if you are already comfortable with programming

We recommend enrolling in the summer school, which most likely will be taking place every summer after now. 

The topics covered are the following:

- Convolutional Neural Networks (PyTorch and Convolutions)
- Encoding Models
- RSA, Geometry, Reweighting, and Variation Paritioning.
- Reconstruction with Linear Regression and GANs
- Transfer Learning and Functional Units
- Using LLMs as a Platform for Behavioral Research
- Reinforcement learning in the brain, from classical conditioning to deep RL
- Cognitive maps: from hippocampal formation to prefrontal cortex


