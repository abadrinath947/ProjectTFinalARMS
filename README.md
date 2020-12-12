# Keras/Apache Spark 
_*Team ARMS*_

## Overview

Through this assignment, we strive to introduce the basics of creating, training, and testing neural networks in Keras and well as utilizing the powers of Apache Spark. We start off by providing simple problems with lots of prewritten code to exemplify how various Keras functions and classes while probing the student to somewhat conceptually understand them. After this, we move on to more free flow tasks like implementing high-performing models from scratch or debugging existing code to really test and grow the students ability to apply the concepts they have learned.

## How to Navigate this Repository

The the notes and slide deck can be found under 'Documentation'. Obviously, the homework requires moderate levels of comprehension of the notes and slides to begin. For homework, there are two directories, 'Problems' which contains the problems/tasks that are given to the student and 'Solution' which contains possible answers to the coding and conceptual questions. The order in which we expect students to complete this is as following (with intended time written adjacently):

* 'Problem 1 - Pythagorean Distance' (45 minutes)
* 'Problem 2 - MNIST Classification Walkthrough' (1.5 hours)
* 'Task 1' (1.5 hours)
* 'Task 2' (1.5 hours)
* 'Task 3' (1.5 hours)
* 'Problem 3 - Apache Spark Walkthrough' (45 minutes)
* 'Task 4' (1.5 hours)

The naming is such that the "problems" are far more guided with more skeleton code while "tasks" are more freeform with a few hints of what to try. The solutions for the tasks, especially task 1, are just one in many that work. As long as the student achieves the desired level of accuracy or effort, any implementation is acceptable. 

Finally, the quiz to check comprehension is located under the 'Quiz' directory with solutions in 'Solution'. 

## Environments

All of these problems require a fair amount of computation and memory so, while a few of them can be run on DataHub, we suggest uploading Problem 1-2 and Task 1-3 to Google Collab and running it on there (using the file upload feature to upload the required datasets). For Problem 3 and Task 4, the main library that is explored in pyspark. Installation of this library locally or on Google Collab can be fairly involved so we decided instead to use Kaggle instead. Both problems have links to their respective Kaggle notebooks. The student should be able to just use the Kaggle "copy and edit" function and easily start coding without having to download any additional libraries or datasets. 

## Objective 1: Introduction to Keras

By far the most common use of Keras is to create sequential models, the simplest of which is the multi-layer perceptron (MLP). Unfortunately, there are quite a few aspects of Keras that must be understood before being able to implement your own MLP. The lecture covers all of these (initiating a sequential model, creating an input layer, adding hidden layers, and so on), however, its one thing to see it in lecture and another to be able to interact with the code. That is the goal of 'Problem 1 - Pythagorean Distance.' Without modification, it contains the full code to create training data for the pythagorean distance problem, feed it into a neural network (albiet not a very good one), and test the results. The questions in this assignment are largely conceptual and have the students play around with parameters of the model to see how they affect performance. Additionally, the last question serves as a "hype-deflating" one, questioning whether neural networks are effective, especially with a problem as simple as this one.

## Objective 2: Image Classification

After somewhat showing that neural network regression works, we try to apply Keras to a more relevant process. Especially in the last decade, one of the flagship applications of ML has been to classify images. The MNIST dataset, a collection of handwritten digits 0-9, is our selection of what to explore for this application because it's a problem thats relatively easy to solve, doesn't require a whole lot of preprocessing, and has fairly low dimensionality. The exploration starts in 'Problem 2 - MNIST Classification Walkthrough.' We begin by exploring the data a little bit: since this is, in fact, an image problem, the first step is to visualize the inputs to get a sense for what they look like. After that, we want to do some basic preprocessing to make sure our neural network will work effectively. We then start testing how well students have understood the concepts from the previous problem by asking them to implement an MLP for MNIST classification (which doesn't perform too great, but also doesn't do terrible). Since the "flatten" layer is new, that is provided in the skeleton code. Now, since the student understands the challenge at hand and is motivated to find a better solution, we introduce the idea of convolutional neural networks. These are fairly involved in syntax so a lot of the code is provided. Finally, data generators are introduced but not explored in much detail.

With all this knowledge at hand, we then transition to a much more hands on exercise, 'Task 1.' In this one, we provide various hints for how to improve the accuracy of the model, but then let the student free to explore their own ideas. Here, we also link to the Keras documentation so that they get a sense of what its like to read about and implement new features from any ML libraries they might encounter online. Although the task is fairly difficult, completing is should feel very eye-opening and rewarding.


## Objective 3: Exploring and Debugging Keras Models

Especially when working in large-scale projects, the skill of being able to look through models and get a sense of how they work and how to improve them is crucial. As a result, we propose two tasks that allow the student to both explore, understand, and debug Keras models that may even be slightly difficult to understand. The student's ability to make sense out of seemingly difficult-looking or challenging networks is one of the more important skills in applying this machine learning framework in the real world.

Therefore, to wrap up Keras development, in 'Task 2' we provide a pre-implemented model for a fairly basic input/output relationship which seems to not perform particularly well. The student, using all the information gained in the previous parts about the strengths/weaknesses of neural networks, can experiment around with the code until they find out how to tweak it to signficantly improve its accuracy. Its intentional that the generated dataset is fairly large to make sure the student is reserved in how many changes they attempt: in projects with terabytes of training data, experimentation must be smart to assure time is not wasted. 

Finally, in 'Task 3', we allow the student to explore a seemingly complex Keras model that is adapted from the U-Net architecture convolutional neural network (CNN). This provides a good opportunity for this student to parse the innerworkings and technical details of such a network without understanding the motivations behind its creation. We ask the student to explore the network and ask some generic questions regarding convolutional neural networks as well. One of the more important tools introduced in this task is to diagram a pre-written model, which is important within the machine learning community as a visualization tool as well as a great way to understand networks.

## Objective 4: Spark Introduction

Another very powerful tool that will be introduced this week is Apache Spark which allows for a lot of parrallized computation. Although the underlying data structure behind it behaves similarly to a pandas dataframe, the commands are fairly niche and students are likely to have never seen many of them before. That's why we start off the journey with a very segmented 'Problem 3 - Apache Spark Walkthrough.' In this, each subtask has a simple 1-3 line solution, but you might have to refer to the notes or pyspark documentation to figure it out. It starts off with some basic data processing and then goes on to implementing a linear regression model. 

Then, as the student is more familiar with Spark, in 'Task 4' they can begin to explore a little more, trying different regression techniques or applying feature engineering/scaling skills from previous weeks in the Spark framework to improve the performance of the model from Problem 3.
