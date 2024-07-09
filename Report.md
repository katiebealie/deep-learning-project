# deep-learning-project

# Overview
The purpose of this project is to create a binary classifier that can predict the likelihood that a particular applicant for funding from Alphabet Soup will be successful or not. Diverse machine learning methodds will be used to train and assess the model. The overall objective is to optimize the model so that it becomes at least 75% accurate.

# Results
## Data Preprocessing
The data was split with the IS_SUCCESSFUL column being the target variable, the EIN and NAME columns being dropped, and the rest of the columns used as feature columns. Binning was implemented for the APPLICATION_TYPE and CLASSIFICATION columns to avoid overfitting and outlier influence. The data was then split into features and targets, and training and testing, and scaled for uniformity.

## Compiling, Training, and Evaluating the Model
Model 1 contained 3 layers: input (80 neurons), second (30 neurons), and output (1 neuron). relu activation function was used for the input and second layers, and sigmoid for the output layer. Model was trained for roughly 100 epochs and achieved 74% accuracy intraining and 72% in testing.

Model 2 contained 2 added layers to the above setup: 2 dropout layers with a rate of 0.5, activation function changed to tanh in the input and second layers. Model achieved 74.1% for the training set and 72% for the testing set.

Model 3 used hyperparameter tuning. Used Keras to identify the optimal hyperparameters, which include using the tanh activation function, setting 41 neurons for the input layer, and assigning 13, 5, and 4 units for the subsequent layers. As a result, the model achieved 73.3% accuracy.

Model 4: removed the STATUS column, applied binning to the ASK AMT during preprocessing. Histogram analysis was used to determine bin parameters. Dropout layers with a dropout rate of 0.5 and an activation function of tanh were kept. Optimal number of epochs was determined by early stopping function and monitoring the val_accuracy metric to be 8 epochs. Final model achieved 73.3% accuracy.


# Conclusion
These models were unsuccessful in reaching the 75% accuracy threshold, and thus as they are, I would not recommend their use. However, in the future, using the Random Forest Classifier and experimenting with preprocessing might yield better results. Additionally, different activation functions could be tried, as well as adjusting the number of layers and neurons and changing the dropout layer might also lead to better optimization. All in all, these models are a good start to achieving the desired optimization.
