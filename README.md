# Predicting Network attacks/intrusion detection using Neural Nets

## Summary

This is part of a project for Artificial Intelligent Class at California State University, Sacramento

There are many types of connections that can happen simultaneously in a network. It is crucial to have a system that can effectively detect attacks, spy, malwares while maintaining the normal connections. This project uses a small dataset of several types of connection, and attempt on detecting abnormal connections or prevent attacks.  

## Implementation
1. **Dataset**: The small dataset can be viewed in the file "network_intrusion_data.csv"

2. **Data Preprocessing**: I attempted to solve this problem in 2 different ways: binary classification and multi-class classification. In binary classification, I only differentiate between "good" and "bad" connections, while in multi-class problem, there are a total of 23 different outcomes for the types of connections. There are a lots of duplicate/redundant records in the data, so removing them helped my models train better and achieved more accurate results.

3. **Model**: The models used in this project include: CNN, fully-connected NN, SVM, Logistic Regression, KNN, and Gaussian Naive Bayes. The data is split into training and testing set. I also use EarlyStopping and ModelCheckPoint to save the best model and avoid overfitting. The main framework of this project is Tensorflow and Keras. The F-1 Score and Confusion matrix of each model were used to compare the performances of all the models. 

## Result:
All the models performed very well on the test data. However, as we take a closer look at the multi-class classification problem, the data is unevenly distributed and biased toward 2 types of connections, which made the prediction over the other 21 types of connections inaccurate. If the data is more evenly distributed, we can see different performances on all the models. 
