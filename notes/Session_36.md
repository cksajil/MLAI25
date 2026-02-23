## Comparison between Performance Metrics and Loss Function

### Performance Metrics
#### Classification
- Accuracy
- TP, TN, FP, FN (confusion matrix)
- Precision
- Recall
- F1-score
- ROC
- AUC

#### Regression
- Mean Absolute Error (MAE): Average absolute difference between actual and predicted values.
- Mean Squared Error (MSE): Average squared difference.
  $$L_{\text{MSE}} = \frac{1}{N} \sum_{i=1}^N \left( y_i - \hat{y}_i \right)^2$$
- Root Mean Squared Error (RMSE): Square root of MSE.
- R-squared (Δ²): Proportion of variance explained by the model.
- Mean Absolute Percentage Error (MAPE): Percentage-based error.

#### Loss Functions in DL
- Mean Squared Error
- Mean Absolute Error
  $$L_{\text{MAE}} = \frac{1}{N} \sum_{i=1}^N \left| y_i - \hat{y}_i \right|$$

- Binary Cross-Entropy (Log Loss)
  $$L_{\text{BCE}} = - \frac{1}{N} \sum_{i=1}^N \left[ y_i \log(\hat{y}_i) + (1-y_i) \log(1 - \hat{y}_i) \right]$$

- Categorical Cross-Entropy
  $$L_{\text{CCE}} = - \sum_{c=1}^C y_c \log(\hat{y}_c)$$
- Sparse Categorical Cross-Entropy


- Dice Loss 
- IoU Loss (segmentation task)

### Optimizers

- Gradient Descent (GD)
	- Stochastic GD (SGD) — updates after each example (fast but noisy)
	- Batch GD — uses all data (slow for large datasets)
	- Mini-batch GD — updates after small batches (most common)
- SGD with Momentum (Adds a velocity term to dampen oscillations and accelerate in relevant directions)
- Nesterov Accelerated Gradient (NAG) (Looks ahead before computing the gradient for faster convergence)
- Adagrad (larger updates for infrequent parameters, smaller for frequent one)
- RMSProp (fixes Adagrad’s shrinking learning rate problem by using an exponential moving average of squared gradients)
- Adam (Adaptive Moment Estimation) (Combines momentum and RMSProp ideas)



- Batch Normalization
- Sequential and Functional API
- Weight Initialization Methods
- Regularization
- Data Loader in Keras

Visualizing Neural Network (Summary & Plot Model)
Sequential and Functional API

Batch Normalization
Weight Initialization Methods
Regularization
Data Loader in Keras

GPU Access
	- GPU usage in Google Colab
	- GPU usage in Kaggle
Kaggle
	- Code Version Control in Kaggle
	- Data Version Control in Kaggle

Activities
1. Performance metric/Loss function activity
- Write functions to compute MSE, RMSE, MAE using numpy only
- Generate 100 random numbers for both y and yhat
- compute MSE, RMSE, MAE using library and custom functions and verify if both are same
2. Do a similar excercise for Binary Cross-Entropy (here y and yhat is allowed to have only 0 or 1 as value)
3. Apply different optimizers (e.g Adam, RMSProp, Adagrad) for a deep learning task and compare loss curves (give different colors)
4. Data Loader example
5. Impliment a neural network in Keras using both sequential and functional APIs

