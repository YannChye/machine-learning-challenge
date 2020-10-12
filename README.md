# machine-learning-challenge

Completed machine learning (week 20) homework for Monash University Data Analytics Boot Camp.

Goal is to create a machine learning model capable of classifying candidate exoplanets from the [NASA Kepler space telescope dataset](https://www.kaggle.com/nasa/kepler-exoplanet-search-results). 

**Dataset was first cleaned to**
1. remove null values 
2. remove unneccessary columns
3. scale the dataset

**Two models were used**
1. (random forest)[https://github.com/YannChye/machine-learning-challenge/blob/main/starter_code/model_1_rf.ipynb]
2. (k-nearest neighbour)[https://github.com/YannChye/machine-learning-challenge/blob/main/starter_code/model_2_knn.ipynb]

**Models were tuned with**
* feature selection based on 
    * feature importance
    * mutual info classifier
* GridSearchCV

**Performance of final model**
|                | Random Forest  | k-nearest neighbour  |
| -------------- |------------:| ---------:|
| Training r2 Score | 0.895     | 1.0       |
| Testing r2 Score  | 0.903     | 0.867   |

### Conclusion
The random forest model is superior for classifiying candidate exoplanet, with a higher r2 score. Nevertheless, it may be likely that the random forest model is overfitting, particularly as the depth of the forest (7) is comparatively large in relation to the number of features (11). Potential options to explore include limitng the forest depth, increasing the sample, or running cross-validation.
