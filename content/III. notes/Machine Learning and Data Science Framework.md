---
title: Machine Learning and Data Science Framework
draft: false
tags:
---
> Come back to this lesson when you feel lost or overwhelmed! 
## Machine Learning Framework 
![[Pasted image 20240319223559.png]]
### 1) Problem definition: What are we trying to solve? 
- Align the problem with a machine learning problem 
- Remember: not all problems need a machine learning solution 
- Types of machine learning 
	- Supervised learning
		- Classification 
		- Regression 
	- Unsupervised learning 
		- Clustering 
	- Transfer learning
		- Uses past ML and builds on it 
	- Reinforcement learning (out of the scope of this course)
		- Uses reward and punishment to learn 
### 2) Data: What kind of dat do we have? 
- Types 
	- Structured: Excel, CSV 
	- Unstructured: Photos, images, audio, emails, etc. 
	- Static: Data that doesn't change over time 
	- Streaming: Data that changes over time 
### 3) Evaluation: What does success mean to us? 
- Important because you can keep "improving" the model but you need a tangible end goal that you can measure your success against 
- Different types of metrics 
	- Classification: Accuracy, precision, recall
	- Regression: Mean absolute error (MAE), mean squared error (MSE), root mean squared error (RMSE)
	- Recommendation: Precision at K
### 4) Features: What do we already know about the data? 
- Examples of data features: weight, heart rate, chest pain 
- Types of features 
	- Numerical 
	- Categorical 
	- Derived 
- It's important that MOST of your data has the feature for it to be useful 
### 5) Modeling: Based on our problem and data, what model should we use?
#### 3 sets 
- Split your data into three different sets: 
	- training set (70%-80%)
	- validation set (10%-15%)
	- testing set (10%-15%)
#### Choosing and training a model  
- Know how to choose the appropriate model for the data 
- Goal: minimize time between experiments 
- Don't be afraid to try things but start small and add complexity as you go 
#### Tuning a model 
- Usually done on the validation set 
- Goal: improve the results to match our end goal 
- Remember that it can take time 
#### Comparing models 
- How will out model perform in the real world? 
- Watch out for under-fitting and over-fitting 
- Make sure you're comparing apples to apples 
	- You use the same training set
	- What's the "cost" of increased accuracy 
### 6) Experimentation: How can we improve? What can we do next? 