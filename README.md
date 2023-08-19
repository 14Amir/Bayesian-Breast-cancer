# Bayesian-Breast-cancer
Applying Naive and Gaussian Bayes models on Breast cancer dataset  
Overall steps:  
1- The libraries used are placed together so that the reader can get to know the code as soon as he sees the code.
2- The data has been read with the help of the pandas library.
3- We dropped the first column, which is only for the code of each data and is not used as a feature for recognition and classification.

a)
1- We used CategoricalNB as a non-Gaussian Naive Bayes method.
2- With the help of the cross_val_score function, we divided the training data into 4 parts and each time used one as the evaluation data. Finally, this function determined which of these 4 parts had a better result and returns the corresponding model to our input model.
3- We fitted the model to the training data.
4- Using the score method, we measured the accuracy of the model on the training data.
5- Here we also checked the accuracy rate using the same method as before on the test data.
6- Finally, we used the predict method and saved the labels predicted by the model and displayed them in the confusion matrix along with the labels of the test data that we had already separated.

b)
We repeated the same steps above only by changing the Naive Bayes method to the Gaussian Naive Bayes mode.

Comparison: According to the numbers in the notebook and confusion matrix, we saw that the non-Gaussian model gave better results on our data.

Bonus:
As shown in the CategoricalNB figure taken from the notebook, the data that our model has classified as class 1 (having cancer) are correct with a very high percentage (TP = 74) and the data that our model incorrectly classifies as having cancer That label has given 0, it is almost 0 (FN = 1), so in total, with the recall criterion, this classification can be evaluated as very appropriate in terms of class 1, which is cancer.

For the problem of error imbalance, you can work with other available statistical criteria such as precision, recall and f1-score.
It is also possible to achieve better results by resampling the training data.
