# 22b2157_SOC_PROJECT ID 24
Model Architecture:
• Libraries Used: numpy, pandas, sklearn (for MinMaxScaler), matplotlib.pyplot, tensorflow.keras.

• Data Source: CSV file named AAPL.csv of APPLE downloaded from Yahoo finance

Model Architecture:
o Input Layer: LSTM with 50 units, return sequences

o Dropout Layer: Dropout rate of 20% to prevent overfitting

o Hidden Layer: LSTM with 50 units

o Dropout Layer: Dropout rate of 20%

o Output Layer: Dense layer with 25 units followed by another Dense layer with 1 unit (for regression).

o Optimizer: Adam optimizer

o Loss Function: Mean Squared Error (MSE).

Data Loading and Preprocessing:
• The data is loaded from AAPL.csv and the 'Date' column is converted to a datetime index.

• Only the 'Close' prices are selected for prediction.

• Data is scaled using MinMaxScaler to normalize values between 0 and 1. Training Configuration:

• Sequence Length: 20 (for creating sequences).

• Number of Epochs: 1 (for demonstration purposes; typically, more epochs are used for training).

• Batch Size: 1 (one sequence at a time due to constraints).

Model Training:
• The model is trained on the scaled training data (X_train, y_train) for 1 epoch.

• Batch size is set to 1 for demonstration; adjust for efficiency based on hardware and model constraints. Prediction and Evaluation:

• Prediction: Predictions are made for future stock prices using the last 20 data points.

• Evaluation Metrics: Mean Squared Error (MSE), Root Mean Squared Error (RMSE), Mean Absolute Error (MAE) are calculated for model performance evaluation.

Visualization:
• Predicted prices are plotted against actual prices to visualize the model's performance.

• Future predictions (1 week, 1 fortnight, and 1 month) are overlaid but I couldn’t find the reason why i can’t predict 1week,1 fortnight predictions.

Conclusion:
• The LSTM model demonstrates the ability to predict future stock prices based on historical data.

• I tried to predict 1 week, 1 fortnight but I couldn’t find the reason why I am not able to predict them.

• Further optimization can be achieved by tuning hyperparameters such as batch size, number of epochs, and model architecture.

• Hardware considerations (like GPU utilization) could enhance training and prediction efficiency.
