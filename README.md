# News_characteristic

<p align="center">
  <img src="https://github.com/docum5/Tweet_classification/blob/main/portfojan2023/workflowtweet.png?raw=true" />
</p>

## Table of Content
  * [The Problem](#the-problem)
  * [Goal](#goal)
  * [Assumption](#assumption)
  * [Dataset](#dataset)
  * [Overview](#overview)
  * [Model_and_architecture](#model_and_architecture)
  * [Evaluation_metrics](#evaluation_metrics)
  * [Conclusions](#conclusions)
  * [Obstacle](#obstacle)
  * [Technologies_Used](#technologies_used)


## The Problem
Since I joined Legal Analytics-Telkom Indonesia as a project-based talent, I got several projects to do, one of which is a News analysis. I asked to Identify the value of news.

Based on BBC Journalistic Guideline, each news has at least one value from several values as follows:
Magnitude, Prominence, Conflict, Proximity, Timeliness, Currency, Unusual, Human Spirit, Magnitude. 


<p align="center">
  <img src="https://github.com/docum5/News_characteristic/blob/main/portfojan2023/newsvalue.png?raw=true" />
</p>



In this Project, I asked to develop a model to identify if the news contains a value for the **human spirit**.

## Goal

**Goal: Predict/detect whether a news item contains issues/information related to the celebration of a specific achievement of humanity**

**Model: Receiving input in the form of news text, news classification, whether it has elements of the human spirit or not**

**Input: Data news**

**Output: “human spirit”: Binary, [“True”, “False”]**
  
## Assumption

The term **human spirit** can refer to the enduring and persistent nature of the human spirit, which enables people to overcome challenges and difficulties.

In news contexts, we can mention the **human spirit** in stories about individuals or groups who have shown extraordinary resilience, courage, or determination in the face of difficult circumstances or have achieved great things despite seemingly insurmountable odds. It can also be used in discussions about a community or society's collective spirit and resilience, particularly in times of crisis or change.

## Dataset
<p align="center">
  <img src="https://github.com/docum5/News_characteristic/blob/main/portfojan2023/datasetnewsvalue.png?raw=truee" />
</p>

Real Data          |  Input 
:-------------------------:|:-------------------------:
![](https://github.com/docum5/News_characteristic/blob/main/portfojan2023/datasetnews1.png?raw=true)   | ![](https://github.com/docum5/News_characteristic/blob/main/portfojan2023/datasetnews2.png?raw=true) 

## Overview
I deploy the model to the API using Fast API.


Homepage          | Get the data by id| Predict  | Search by Content/Category
:-------------------------:|:-------------------------:|:-------------------------:|:-------------------------:
![](https://github.com/docum5/News_characteristic/blob/main/portfojan2023/view1.png?raw=true)   | ![](https://github.com/docum5/News_characteristic/blob/main/portfojan2023/view2.png?raw=true) | ![](https://github.com/docum5/News_characteristic/blob/main/portfojan2023/view3.png?raw=true)| ![](https://github.com/docum5/News_characteristic/blob/main/portfojan2023/view4.png?raw=true) 


**Demo Model**         
:-------------------------:
![](https://github.com/docum5/News_characteristic/blob/main/portfojan2023/apinews.png?raw=true) 



## Model_and_architecture
**IndoBERT Large Model (phase1 - uncased)-indobenchmark/indobert-large-p1**

<p align="center">
  <img src="https://github.com/docum5/Tweet_classification/blob/main/portfojan2023/model.png?raw=true" />
</p>



## Evaluation_metrics

Evaluation Model on Data Testing         | Evaluation Model on Data Eval | Evaluation Matrics
:-------------------------:|:-------------------------:|:-------------------------:
![](https://github.com/docum5/News_characteristic/blob/main/portfojan2023/eval1news.png?raw=true)   | ![](https://github.com/docum5/News_characteristic/blob/main/portfojan2023/eval2news.png?raw=true) | ![](https://github.com/docum5/News_characteristic/blob/main/eval3news.png?raw=true) 

## Conclusions

The analysis results show that using the Indobert Pre-Trained Model in this News analysis case can produce an accuracy of 98% with a True Positive Rate of 88% and a True Negative Rate of 99%.

## Obstacle

* The data used is still classified as imbalance, so it is necessary to add data to the minority class data.

* The need for further understanding of the meaning of **human spirit** so that the resulting output will be by the desired needs

## Technologies_Used


![](https://forthebadge.com/images/badges/made-with-python.svg)

[<img target="_blank" src="https://d3.harvard.edu/platform-digit/wp-content/uploads/sites/2/2022/04/demo-huggingface_optimized-370x200.png" width=170>](https://huggingface.co/) [<img target="_blank" src="https://upload.wikimedia.org/wikipedia/commons/thumb/c/c6/PyTorch_logo_black.svg/2560px-PyTorch_logo_black.svg.png" width=280>](https://pytorch.org/) [<img target="_blank" src="https://upload.wikimedia.org/wikipedia/commons/thumb/f/f4/Elasticsearch_logo.svg/1280px-Elasticsearch_logo.svg.png" width=200>](https://www.elastic.co/) [<img target="_blank" src="https://i.imgur.com/p0Nufjn.jpg" width=100>](https://fastapi.tiangolo.com/)

