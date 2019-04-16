# Bootcamp at Google Cloud Next 2019: Serverless Machine Learning With Cloud ML
#gcp #cloud

- labs and its resources available til midnight tonight
- lab available via github
- slides are availed on qwiklabs as well (click on my learning)
- this lab is part of free course at coursera: https://www.coursera.org/promo/MLBootcamp
- Bigquery - GCP data warehouse solution
	- can use SQL query
- Deeper neural network: make complicated shapes for decision boundary/threshold vs. just a line
- Tensorflow will take care of gradient descent
- Tensorflow Playground - web tool visualizes models being trained in Tensorflow ([A Neural Network Playground](https://playground.tensorflow.org/))
- Generally should only need 2 layers at most but can have very many neurons within those layers
	- adding more layers = risk overfitting
- softmax layer helps deal with multiple labels
	- ultimately outputs probabilities 
- Datalab - GCP’s hosted Jupyter notebooks
- new instructions: http://bit.ly/2Kf46Vk

## Tensorflow
- Tensorflow 2.0 still alpha so not using it in this lab (using Tensorflow v1)
- tensor = n-dimensional array of data
	- rank 0 = scalar
	- rand 1 = vector/array
	- rank 2 = matrix
	- rank 3 = 3d array e.g. image
	- rank 4 = 4d array e.g. video
- It is an open-source high-performance library for numerical computation that uses directed graphs
- 2 steps
	- build the graph
	- then execute it
- backend runs on C++ but frontend written in python
- python api lets you build and run directed graph
- tensorflow distributes the computation
- refactor estimator models to
	- read out of memory data

## Cloud ML Engine
- interacts with Tensorflow at all layers
- deals with training-serving skew
- performs hyper parameter tuning using statistics (Bayesian optimization)

## Feature Engineering
* represent raw data in a form conducive to ML

## Model Architectures
* DNNs are great for dense, highly correlated data
	* pixel values of images
* wide-and-deep models
	* combine dense and sparse models

## O’reilly book: Data Science on the Google Cloud Platform