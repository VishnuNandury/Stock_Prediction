# Stock_Prediction
Deep Learning models to predict Open and Close Prices of a stock and comparison between model with sentiment data and model without sentiment data

# Data pre-proccessing
We have two types of data, News and Charts.

The News data is used to generate Sentiment (VADER_Sentiment) and is merged with Charts data which will be given as input to the model.
we can select input features and target variables accordingly

# CNN-LSTM:
In this method, we will gather the sentiment/pre-processed data from the feature engineering process and use that as input to the CNN-LSTM implementation.
1. CNN Block:-
This is used first to extract short-term patterns or trends and features of the data and also remove the noise and unrelated patterns across the data.
The convolution and pooling layers both perform smoothing on the data by only keeping the important features across various filters.
2. LSTM Block:-
This block is used for the actual modeling of the sequential stock market data since it can learn long-term dependencies which is effective for this form of sequential data.
We use Bi-directional LSTM cells to process sequences forward and backward, preserving past and future dependencies.
3. Dense Layer:-
Finally, we use a fully connected dense layer that flattens the outputs before the final classification layer.
Training the model can be done with a ‘ReLU’ activation function and optimizers such as ‘Adam’ or ‘RMSprop’ with Mean Square Error (MSE) as Perfomance Metric.

# .ipynb Files
The .ipynb files contain the model training and prediction for Amazon and Apple data respectively.
The predictions are for the stock open and close price with and without sentiment data on Train, Validation and Testing data.

# Results
We see that the model which has sentiment data performs better i.e. Lower MSE, than the model without sentiment data.

