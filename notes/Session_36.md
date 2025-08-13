Comparison between Performance Metrics and Loss Function

Performance Metric
Classification
	- Accuracy
	- TP, TN, FP, FN (confusion matrix)
	- Precision
	- Recall
	- F1-score
	- ROC
	- AUC

Regression
	- Mean Absolute Error (MAE): Average absolute difference between actual and predicted values.
	- Mean Squared Error (MSE): Average squared difference.
	- Root Mean Squared Error (RMSE): Square root of MSE.
	- R-squared (Δ²): Proportion of variance explained by the model.
	- Mean Absolute Percentage Error (MAPE): Percentage-based error.

Loss Functions in DL
- Mean Squared Error
- Mean Absolute Error

- Binary Cross-Entropy (Log Loss)
- Categorical Cross-Entropy 
- Sparse Categorical Cross-Entropy

- Dice Loss 
- IoU Loss (segmentation task)

Optimizers
- Gradient Descent (GD)
	- Stochastic GD (SGD) — updates after each example (fast but noisy)
	- Batch GD — uses all data (slow for large datasets)
	- Mini-batch GD — updates after small batches (most common)
- SGD with Momentum (Adds a velocity term to dampen oscillations and accelerate in relevant directions)
- Nesterov Accelerated Gradient (NAG) (Looks ahead before computing the gradient for faster convergence)
- Adagrad (larger updates for infrequent parameters, smaller for frequent one)
- RMSProp (fixes Adagrad’s shrinking learning rate problem by using an exponential moving average of squared gradients)
- Adam (Adaptive Moment Estimation) (Combines momentum and RMSProp ideas)

Batch Normalization

Sequential and Functional API
Weight Initialization Methods
Regularization
Data Loader in Keras

Activities
1. Performance metric/Loss function activity
	a. Write functions to compute MSE, RMSE, MAE using numpy only
	b. Generate 100 random numbers for both y and yhat
	c. compute MSE, RMSE, MAE using library and custom functions and verify if both are same
2. Do a similar excercise for Binary Cross-Entropy (here y and yhat is allowed to have only 0 or 1 as value)


3. Apply different optimizers for a computationally demanding task and compare loss curves
4. Data Loader example
5. Impliment a neural network in Keras using both sequential and functional APIs

