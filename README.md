You must decompress Data1 and Data2.
This script was created with the "jupyter notebook".

Preprocessing only filled the missing data. 
This is because the value of RMSE dropped when it attempted to normalize.

XGBoost was used for modeling. 
The original purpose is "Classification", 
but it has been shown that rounding up to the appropriate reference value by performing a "Regressor" has been more efficient.

The rounding reference value was found through the iterative statement.

"RandomizedSearchCV" was used to select the parameters of the model.

The combination of XGBoost and Lightgbm was "Blending." Then, it did better.

The reason why XGBoost was used as a model was because the "EDA" result data did not follow the Gaussian normal distribution, 
and the difference between variables was so great that it could benefit from the tree.

What I felt from this was that I tried to use the "Imputation" module in the data preprocessing process, 
but I regret that I created it myself because of environmental issues. 
I also believe that more sophisticated normalization should have allowed 
the distribution of data to follow a more Gaussian normal distribution. 

Finally, when choosing a model, it was necessary to use more "Regressor" models to determine which would perform best. 
"Ridge" and "Elastic Net" were used, but the performance was poor.
