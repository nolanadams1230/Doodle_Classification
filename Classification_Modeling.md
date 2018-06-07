# Classification Modeling

[Jupyter Notebook](http://nbviewer.jupyter.org/github/nolanadams1230/Doodle_Classification/blob/master/notebooks/Classification%20Models%20-%20Doodles.ipynb)

[Github](https://github.com/nolanadams1230/Doodle_Classification/blob/master/notebooks/Classification%20Models%20-%20Doodles.ipynb)

By simply randomly guessing, one should be able to reach ~10% accuracy (since there are only ten class labels). A machine learning algorithm will need to obtain > 10% accuracy in order to demonstrate that it has in fact “learned” something (or found an underlying pattern in the data).

For all the models, except the Convolutional Neural Network and the Transfer Learning model (VGG16), we used GridSearchCV to tune the most important hyper-parameters.

## K-Nearest Neighbors

To start, I modeled the data with the k-Nearest Neighbor (k-NN) classifier, which is arguably the most simple, easy to understand machine learning algorithm. The k-NN algorithm classifies unknown data points by finding the most common class among the k-closest examples. Each data point in the k closest examples casts a vote and the category with the most votes is chosen.

Using GridsearchCV and the elbow-method to tune the *k-neighbors* parameter we found that 3 neighbors seems like the best choice to avoid overfitting. The main advantage of the KNN algorithm is that it performs well with multi-modal classes because the basis of its decision is based on a small neighborhood of similar objects. This is why its results were fairly high with 80%. The main disadvantage is the computational cost are very high and the results take far too long. Also this classifier would not be ideal if we wanted to make predictions on the fly, since k-NN classifier trains the data fast but then makes predictions very slow.

## Random Forest
Random forests is an ensemble model which means that it uses the results from many different models to calculate a label. For our model we tuned *n_estimators* which is the number of trees you built before taking the maximum voting or averages of predictions. Higher number of trees give you better performance but makes your code slower. Using the elbow method again, show us **80 estimators** was a good choice since the number of estimators above 80 did not improve the model enough to be worth the extra computational requirements.

We then tuned the *max_features* parameters, which are the maximum number of features Random Forest is allowed to try in individual tree.
