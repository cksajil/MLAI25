- Regularization
	- Recap
		- L1 (Lasso), L2 (Ridge), Elasticnet
		- Random Forest
	- Keras regularization

- Dropout
	- Dropout concept
	- Dropout paper-diagram
	- Working during training and testing time

- Callbacks
	- Early Stopping
	- Model Checkpoint
	- Learning Rate Scheduler
	- TensorBoard
	- Custom History

- Activity 1: Apply MNIST classification using DNN and construct the following table with error rates computed. Share your table via discord
```
------------------------------
Model 			  |	Error rate
------------------------------
DNN+L1            |           |
DNN+L2            |           |
DNN+Dropout(0.2)  |           |
```

- Activity 2: Write a custom earlystopper callback which stops model training if either of the following happens. validation accuracy>0.95 or validation loss<0.1

- Activity 3: Modify model checkpoint example so that each model is saved as separate files with file name "dnn_model_val_acc_dd.keras" where dd is validation accuracy in percentage. Only save model if validation accuracy improves from one iteration to next.