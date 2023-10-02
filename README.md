### Recipe Ingredients Prediction

This project focuses on predicting the ingredients of a recipe based on its name. The dataset used is the Recipe Ingredients Dataset from Kaggle, which comprises 39,774 recipes and 20,000 ingredients. The dataset is divided into two files: 'train.json' and 'test.json'. The 'train.json' file contains 39,774 recipes and is used for training the model, while the 'test.json' file contains 9,944 recipes.

However, the 'test.json' file does not include labels for validation. To overcome this, we utilized the 'train.json' file and performed a data split. Specifically, 10% of the 'train' set was reserved for testing, while the remaining 90% was used for training the model.

If anyone has the tags for the 'Test.json' file, I would be very grateful if they could share them with me. Even if not, we can compare the 'test.json' outputs of our model.

### Results

The model was trained using the following parameters:

Total number of epochs: 25
EarlyStop was used with a patience of 5 epochs.

| Model | Activation (hidden layer) Function | Activation (output layer) Function | Optimizer | Epochs | Accuracy |
| ----- | ---------------------------------- | ---------------------------------- | --------- | ------ | -------- |
| GRU   | tanh                               | Sigmoid                            | Adam      | 17     | 0.673    |
| GRU   | tanh                               | Sigmoid                            | RMSprop   | 19     | 0.681    |
| GRU   | tanh                               | Softmax                            | Adam      | 15     | 0.666    |
| GRU   | tanh                               | Softmax                            | RMSprop   | 21     | 0.683    |
| LSTM  | tanh                               | Sigmoid                            | Adam      | 12     | 0.655    |
| LSTM  | tanh                               | Sigmoid                            | RMSprop   | 25     | 0.68     |
| LSTM  | tanh                               | Softmax                            | Adam      | 14     | 0.631    |
| LSTM  | tanh                               | Softmax                            | RMSprop   | 21     | 0.69     |
