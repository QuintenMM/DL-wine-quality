# Deep learing with wine dataset
## Overview 
In this challenge the goal was to get a working deep learning program running with the wine dataset that was given. Using the various ingreedients we wanted to predict what the quality of the wine would be. 

Dataset: 
| Features           | format         |
|-------------------|----------------------------------------------|
| fixed acidity | float64 | 
|  volatile acidity | float64 | 
|  citric acid | float64 | 
|  residual sugar | float64 | 
|  chlorides  | float64 | 
|  free sulfur dioxide |float64 |  
|  total sulfur dioxide |float64 |  
|  density | float64 | 
|  pH | float64 | 
|  sulphates | float64 | 
|  alcohol | float64 | 
| quality (score between 0 and 10) | int | 



# version one 
First stepp taken in this assignment was understanding the data and use it without any pre-processing. The goal was to understand all the steps that have to be taken to get to our goal. This was quickley done and after that we understand what we're working with. 

Our first model had an accurcey score of 32% which is really bad. As you can see below the graps also don't look like they're supposed to.

# version two
Determining what the quality is out of a possible score of 10 might be a biy much for our model, so I made it easier. If the quality is above a 6 it counts as a good wine and if not it's a bad wine.

Secondley I looked at the features to see if there was anything that could be used. A deep dive into the features revealed that "Free sulfur dioxide" had a high correlation in comparison to the other features, so I removed it.

With these changes I tried againg. Model accuracy score changed to 73%. This is a big improvement over the other score.

After checking the graps it's clear that it's much better at predicting the right anwser but still it's not what we want yet.

The confussion matrix gives a better vieuw of what is going on. It's obvious that the model is overfitting and thinks all the wine is bad.

# Version Three
For this version I tried adding normalising, scaling, feature engeneering. These all had little to no effect and the problem of overfitting remained.Feature engeineering did't really work because relations between features is very low.

There is also a descrepetency between the "good", and "bad" wines. there is a relation of 5:1 foor bad wines. To solve this I tried donw/upsampling but this also had no effect. This tells me that the relation of good and bad isn't the problem but the little relation between the features.

With these changes the model had a small improvement and accuracy 79%. But as you can tell the model stil has an overfitting problemem.






