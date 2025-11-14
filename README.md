# Comp 376

[Link to catalog](https://www.franklin.edu/catalog#/courses/B1cu0-Rv6)

## Course Overview

The course is twelve weeks, broken into two halves.
Each half consists of four weeks of lecture, followed by two weeks to work on a project.
Lecture weeks have 


## Grading and Assignments

* **8 Homeworks Assignments**: 75 points each
* **Mid Semester Project**: 200 points
* **Final Project**: 200 points
* **Total**: 1000 points

There are no timed exams or quizes.

## Textbook

This course will use this textbook

https://www.oreilly.com/library/view/ai-engineering/9781098166298/

Which students can access online for free. The textbook is not used extensively.

### Projects

Students are given two weeks to complete a simple project, culminating in a deployed machine learning application.
They are permitted to work alone or in teams.
There are provided milestones for each week.
Class time during project weeks will be open Q&A with the instructor.
There will not be homework due during project weeks.

## Lecture and Homework Materials

Lecture materials and homework assignments are on Google colab notebooks.
Links to the notebooks are included below.


## Schedule

Week | Topic
-----|-----
1    | Intro to Cloud Computing and Production Python
2    | MLFlow for Experiment Tracking
3    | MLFlow for Model Deployment
4    | Feature Engineering
5    | Mid-Semester Project 1
6    | Mid-Semester Project 2
7    | Introduction to Large Language Models
8    | Prompt Engineering
9    | LLM Based Agents
10   | MLFlow for Generative AI Model Tracking
11   | End of Semester Project 1
12   | End of Semester Project 2


# Module Breakdown

Below is a breakdown of each module and unit.
Learning outcomes are explained.
Example homework problems are included for some units here, but do not include that in Canvas.
The actual homework assignment will be posted in the provided link.

## Week 1: Intro to Cloud Computing and Production Python

**Learning Outcomes**

* Students can explain what we mean by cloud coumpting.
* Students are able to log into a cloud environment and execute basic commands.
* Studentc can run install Python modules and run scripts on the cloud.
* Students can explain the pros/cons of working in Jupyter notebooks vs. in Python scripts or executable modules.
* Students can explain dependency managenment with `pip` and `requirements.txt`. 
* Students understand the need for virtual environments and can create new venvs using different tools
    - `vevv`
    - `poetry`
    - `uv`
* Students can create Python scripts executable from the command line, with arguments. (Optional: use the Click library).

**Reading and Preparation**

* [Real Python](https://realpython.com/if-name-main-python/)
* [Lecture Notebook](https://colab.research.google.com/drive/1uo4N9Smcc9xbq4VLSj7jXyga5a0bXfOt?usp=sharing)

**Optional Resources**

* [Click](https://click.palletsprojects.com/en/stable/)
* [venv](https://packaging.python.org/en/latest/guides/installing-using-pip-and-virtual-environments/)
* [Poetry](https://python-poetry.org/)
* [uv](https://docs.astral.sh/uv/)

### Homework

* [Homework Notebook](https://colab.research.google.com/drive/1lVLh7GMNuMIte9JBtw441G3YW5tl-15_?usp=sharing)


#### Example Questions

1. (Short answer). 
Give and example of a situation where a Jupyter notebook is preferable to a Python script. Give another example where a script is preferable. Explain why in each case.
2. (Short answer). Explain the purpose of `if __name__ == '__main__'` in a Python program.
3. (Short answer). Explain why we need something like `requirements.txt` to manage our dependencies.
4. (Coding). Take the given jupyter notebook file and translate it into an executable Python script.
Make sure to allow the user to provide command line arguments for hyperparameter values of the trained model.

Example use:

```bash
$ python train_model.py --data data.csv --regularization 3.0 --output model.pkl
```
**Purpose**

To make sure that students understand the importance of creating executable scripts for use in a production environment as opposed to an expermentation/analysis environment.

**Overview**

* Students will have a `comp_376` virtual environment which they will be able to use for the remainder of the semester.
* Students will have set up their remote compute linux machine.

## Week 2:  MLFLow for Experiment Tracking

**Learning Outcomes**

* Students are able to explain the importance of using tools like MLFlow to track traditional machine learning model training.
* Students can install MLFlow and run an MLFlow tracking server locally.
* Students can integrate with a remote MLFLow tracking server.
* Students are able to integrate MLFlow code into an existing training script.

**Reading and Preparation**

* [MLFlow experments documentation](https://mlflow.org/docs/latest/ml/)
* [Lecture Notebook](https://colab.research.google.com/drive/1I98RzYVY-_DJfD7nTVQZ_8wUrP92WLTL?usp=sharing)

**Optional Resources**

* [MLFlow Tracking Docs](https://mlflow.org/docs/latest/ml/tracking/)

### Homework 

* [Homework Notebook](https://colab.research.google.com/drive/1XAYgm-OWRpsoEiskkD8et_c16pyo22vI?usp=sharing)

#### Example Questions

1. (Short answer). Explain what MLFlow is and how we can use it for model tracking.
2. (Coding). Take a given Python script which trains a model. Edit the script to inforporate MLFlow experiment tracking.
3. (Coding). Update the script from question 2. to track additional metrics and a plot artifact.

**Purpose**

To teach the students the importance of an organized experiment tracking workflow.

**Overview**

Students will have access to the MLFlow tracking server.

## Week 3:  MLFLow for model deployment and tracking

**Learning Outcomes**

* Students are able to explain the difference between model metrics (e.g. accuracy, mean square error, etc.) and business key performance indecators (KPIs) such as customer conversion rate.
* Students can explain two things  which impact an overall model:
    - Version of the code used to train
    - Dataset used to train the model 
* Students can explain data drift and can track data drift in two ways.
    - Track drift in the input features using unsupervised methods
    - Track actual model performance once true values are ovserved.
* Students can explain selection bias as it pertains to model training and model evaluation.
* Students are able to "deploy" a model to a MLFLow web server and make predictions.
* Students can track model performance over time (simulated).

**Reading and Preparation**

* [MLFlow Model Registry Docs](https://mlflow.org/docs/latest/ml/model-registry/)
* [Lecture Notebook](https://colab.research.google.com/drive/10-VCXrG_DaJLBfj4nIP9qd71PHk30Cfg?usp=sharing)

### Homework

* [Homework Notebook](https://colab.research.google.com/drive/1NAMEW3VeODC652kzgcgtlMvHPKETpiPk?usp=sharing)

**Purpose**

To introduce students to the process of deploying predictve models to a production environment.

**Overview**

Students will have successfully deployed a basic model using thier MLFLow tracking server web UI.

## Week 4: Feature Engineering

**Learning Outcomes**

* Students can describe the process of feature engineering
* Students can explain the difference between raw input data and a model's features.
* Students can explain two different ways to pre-process inputs for a model and the pros/cons
    - Pre-computed
    - At prediction time
* Students can explain the importance of repeatability between feature generation for training and live prediction.

**Reading and Preparation**

[Lecture Notebook](https://colab.research.google.com/drive/1r_RxHtArz2YFZsoxkBUtsKKSK_spL2id?usp=sharing)

### Homework

[Homework Nokebook](https://colab.research.google.com/drive/1hDutry6exvpXUZLf6xelYw20wtY6uKXo?usp=sharing)
 
## Weeks 5 & 6: Mid Semester Project

These weeks will be focused on the first big project.
Students can work alone or in small teams (<=3) to complete the project.
There will be required milestones each week which the professor will check in on.
There are no lectures or homeworks and regularly scheduled class time will be reserved for
Q&A time with the professor to help the students overcome any issues.

* [Mid Semester Project Notebook](https://colab.research.google.com/drive/1dqHLQcYG-uKYB-zusu06L9QYpzdID_Zf?usp=sharing)

**Purpose**

Simulate the experience of working on a real model deployment task, similar to what you would do as a
professional data scientist or machine learning engineer.

**Overview**

Students will be provided access to a database (SQLite) which contains some generated data
They will need to create an end-to-end machine learning application which can
* Preprocess the data into input features
* Combine features and targets to make training datasets
* Train a model to predict the required target - track model metrics on MLFLow
* Deploy this trained model to their cloud infrastructure
* Interpret model predictions for business use case

At the end, the instuctor will use their deployed model to make predictions using data the students did
not have access to.

## Week 7: Introduction to Large Language Models

**Learning Outcomes**

* Students can explain what a large language model is
* Students can describe what a foundation model is and the general process of creating one
    - In addition, students can explain why we typically do not create our own foundation models
* Students understand what a token is and why they are important for LLM applications
* Students are able to connect with free LLM apis to send queries
* Students can derermine when a LLM is useful for solving problems vs. traditional ML solutions

**Reading and Preparation**

* Textbook Chapter 2: Understanding Foundation Models
* [Lecture Notebook](https://colab.research.google.com/drive/1y8DnXt2wapfF6UPWZTyawYXu5cpAyTgY?usp=sharing)

**Optional Resources**

[Youtube: Large Language Models explained breifly](https://www.youtube.com/watch?v=LPZh9BOjkQs&t=9s)

## Week 8: Prompt Engineering

**Learning Outcomes**

* Students can explain what prompt engineering is
* Students can describe the aspects of a good prompt
* Students can describe ways they can improve 

**Reading and Preparation**

* Textbook Chapter 5: Prompt Engineering
* [Lecture Notebook](https://colab.research.google.com/drive/1V1RchAzwIL2WPjPHXCkcfagGTbcK0lda?usp=sharing)

### Homework Description

* [Homework Notebook](https://colab.research.google.com/drive/1_kFp760Ff5J8M_OPza6yX3Z2o9bT2uK4?usp=sharing)

**Purpose**

Give students the experience of writing good prompts for use in LLM based applications.

**Overview**

Students will create prompts for LLMs. This will serve as a foundation for agents in the following week.

## Week 9: LLM Based Agents

**Learning Outcomes**

* Students can explain what an AI agent is and what we might use one for
* Students can create simple AI agent tools
* Students can design good prompts for LLMs to allow it to work with tools they designed

**Reading and Preparation**

* [Lecture Notebook](https://colab.research.google.com/drive/12j3LbikAgFUw7JrvvvG2n23gJPmucGxq?usp=sharing)

**Optional Resources**

### Homework Description

* [Homework Notebook](https://colab.research.google.com/drive/1rP9wkYIVe1PMvalQ5mTbvIXAP02JprwI?usp=sharing)

#### Example Problems

1. (Short Answer). What is an AI agent? When should you consider using one?
2. (Short Answer). What are some downsides of working with AI agents as opposed to traditional software solutions?
3. (Short Answer). What do we mean by a "tool" in the context of AI agents?
4. (Coding). Read a csv file which contains a table of children and their favorite foods.
Using an LLM from hugging face, create a tool which allows the agent to answer questions about favorite foods.
Fill in the missing functionality in the given python script.

(Use provided template python script file).

```
fav_foods.csv

name,category,favorite
Charlie,pizza,pepperoni
Charlie,icecream,strawberry
Jessica,pizza,cheese
...
```
Example use:
```

> What is Charlie's favorite flavor of icecream?  

Charlie like strawberry icecream.
```

**Purpose**

Give students the experience of creating an LLM, tool based agent.

**Overview**

## Week 10: MLFlow Generative AI Model Tracking

**Learning Outcomes**

* Students are able to use MLFlow's GenAI platform to develop and iterate on AI agents.
* Students can leverage their previous experience of MLFlow deployment to deploy their agents.

**Reading and Preparation**

* [MLFlow GenAI Documentation](https://mlflow.org/docs/latest/genai/)
* [Lecture Notebook](https://colab.research.google.com/drive/1Dm6c_ZxLa7U7IdEQdqEYwS3ahPN9rZAb?usp=sharing)

**Optional Resources**

### Homework Description

* [Homework Notebook](https://colab.research.google.com/drive/1q-PrXYJDBVUnkfB15b6lvY-JLYRIGCWH?usp=sharing)

**Purpose**

Give students the skills necessary to work with an machine learning tracking platform for agent deployment.

**Overview**

## Week 11 & 12: Final Project with AI Agents

Similar to the the mid-semester project, this project will simulate the working in a machine engieering team.

**Learning Outcomes**

* Students will work in teams of 2-4 to create an end-to-end system leveraging AI agents.
* Class time will function similarly to a real DS team meeting in a company.
* Students will breakout into Zoom rooms to discuss their role and responsibilties.
* The professor will hop from room to room to make sure that things are going smoothly

**Reading and Preparation**

* [Final Project Notebook](https://colab.research.google.com/drive/1KRTlm6bOLswT9An42SNdAtC1RmA1wTrX?usp=sharing)
* [TextWorld](https://github.com/microsoft/TextWorld/tree/main)

**Optional Resources**

### Project Description

Your goal is to create an LLM agent which plays a simple text-based adventure game.
We will use the Microsoft TextWorld framework for the game.
Your model should be albe to interact with the game, use tools, and hopefully solve the game and reach the end.
The LLM will be run locally, or via a free API.

Week 1 milestones:

* Students have created their code repository on github
* Students have set up an MLFlow tracking server to keep track of their model's progress
* Students have started working on tools and iterated.

Week 2 milestones:

* The agent is now able to play through the game
* Students can keep track of play sessions

**Purpose**

Give students the experience of developing an end-to-end, LLM bases, agent application.

**Overview**
