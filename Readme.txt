This is a README file for the Practical Application #2 submission for the UC Berkeley Professional Certificate in ML and AI. 
Author: Akshat Kharaya 

This file contains summary of findings from the data analysis and model development for used car prices and the link to the supporting Jupyter notebook. 

Summary of findings:
(A) Data
1. The dataset contains some not useful columns due to high missing rate. Decision was to drop these, e.g., cylinders, VIN, drive, size. Also removed rows with missing data. 
2. Histogram of price reflected a wide range of prices. Decision was to remove outliers outside the 5th-95th percentile range. Similar treatment was performed on odometer to remove the ones above 95th percentile.
3. Boxplot of price vs year showed an interesting relationship 

(B) Model
1. RMSE of the best model based on the hyperparameter search is 9205.26
2. The selected features along with the interpretation of the coefficients is as follows:
* Transmission = "Other": This has a positive effect on the car price. If the transmission is Other, the price of the car increases by $5,606 on average.
* Type = SUV: This has a negative effect on the price. For this car type, the price of the car reduces by $1,157 on average.
* Type = Hatchback: This has a negative effect on the price. For this car type, the price of the car reduces by $1,233 on average.
* Type = Pickup: This has a positive effect on the price. For this car type, the price of the car increases by $5,146 on average.
* Type = Sedan: This has a negative effect on the price. For this car type, the price of the car reduces by $6,161 on average.
* Type = Truck: This has a positive effect on the price. For this car type, the price of the car increases by $2,056 on average.
* Year: As the year of the car increases, the price increases. The effect of 1 year newer is $615 on average.
* Odometer: As the odometer of the car increases, the price decreases. The effect of every additional 10,000 miles is $497 price reduction on average. 

(C) Business recommendation 
We need to understand the business objective related to fine tuning the inventory to deliver a robust recommendation. To elaborate further:
* If the business model is oriented to optimize commission in dollars per car (which is a % of car price), then the used car dealership should focus on Pickup and Truck car types because of the positive relationship with price on average for regular cars (i.e., year >= 1990). Dealer should also look for newer cars with less mileage (i.e., odometer reading) based on the model. 
* If the business model is such that moving inventory is important, then instead of the price, we should look at number of days car held on inventory. 

Link to Jupyter notebook: https://github.com/akshatkharaya/UCB_MLAI_Module11/blob/main/prompt_II_AkshatKharaya.ipynb