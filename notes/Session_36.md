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
- SGD with Momentum
- Nesterov Accelerated Gradient (NAG)
- Adagrad 
- RMSProp
- Adam (Adaptive Moment Estimation)

Batch Normalization

Sequential and Functional API
Weight Initialization Methods
Regularization
Data Loader in Keras

Activities
1. Impliment different loss functions without ML/DL libraries
2. Apply different optimizers for a computationally demanding task and compare loss curves
3. Data Loader example
4. Impliment a neural network in Keras using both sequential and functional APIs

