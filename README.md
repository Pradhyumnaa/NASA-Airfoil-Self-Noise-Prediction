# NASA Airfoil Self-Noise Prediction
 Prediction Model for NASA Airfoil Self-Noise

 The source of the dataset is: https://www.kaggle.com/datasets/fedesoriano/airfoil-selfnoise-dataset

 # Method

 So it will be difficult to pinpoint the prediction to one number so I have made use of the IQR to create a range for which the predictions can fall under. Using the IQR over the Standard Deviation because the SSPL column does not follow a normal distribution, but a negative skewed distribution. The IQR is 9.80449999999999 (close to 10) but since Decibels follow a logarithmic ratio, a 10 db increase means the sound is 10 times lounder. For this, I'm setting the acceptable range to be ActualValue+-0.5IQR.

 # Statistics of 10 Runs:

Values that fall within the acceptable range (Out of 100 Test Cases): 87, 80, 90, 84, 83, 86, 83, 87, 84, 86
Standard Deviation, σ: 2.6457513110646
Mean, μ: 85
