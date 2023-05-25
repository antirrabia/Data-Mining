# Machine Learning Repository for High-Performing Classification and Regression Models
Welcome to my GitHub repository dedicated to developing state-of-the-art supervised machine learning algorithms for classification and regression tasks. My primary focus is on achieving excellent scores in Kaggle.com competitions, where I strive to push the boundaries of model performance. 

Join me on this exciting journey of developing high-performing classification and regression models. Let's unlock the full potential of supervised learning and make our mark in the Kaggle.com competitions. Happy coding and may our models achieve excellence!

---

### Classification

> **Titanic** - A Classification problem on this data set. I have tried some best practices. I developed 3 models of increasing complexity.
**Skills:** Data wrangling and cleaning | Feature engineering | Model training and evaluation | Hyperparameter tuning | Ensemble learning | **Accomplishments:** Developed my own functions to create new features using domain knowledge. | Used IterativeImputer and KNNImputer to impute missing values. | Tuned hyperparameters using GridSearchCV. | Improved my functions into transformers using FunctionTransformer. | Used SimpleImpute with different strategies for numeric and categorical features. | Improved my own transformers and included the Cabin feature.
 - [Basic](https://nbviewer.jupyter.org/github/antirrabia/DataMining-_-/blob/main/notebooks/Titanic_01.ipynb) - wrote my own functions to create new features and code them using domain knowledge. After having all the features coded, I use `IterativeImputer` and `KNNImputer`. I tried different parameters for `imputation_order` and `n_neighbors`. I created a main `Pipeline` and a `GridSearchCV` to tune hyper-parameters. 
 - [02](https://nbviewer.jupyter.org/github/antirrabia/DataMining-_-/blob/main/notebooks/Titanic_02.ipynb) - I improved and turned my functions into transformers using `FunctionTransformer` which I then used in `FeatureUnion` . This time I wanted to try `SimpleImpute` and the strategies of `mean`, `median`, `constant`, `most_frequent` for numeric features and `most_frequent` for categorical features. 
 - [03](https://nbviewer.jupyter.org/github/antirrabia/DataMining-_-/blob/main/notebooks/Titanic_03.ipynb) - I improved my own transformers. This time, I included and coded the `Cabin` feature, which I didn't use in the previous 2 procedures. I use `IterativeImputer` and `KNNImputer`. I tried different parameters for `imputation_order` and `n_neighbors` .  


### Regression

---

> **House Prices** - A regression problem. 

[Final Version](https://nbviewer.jupyter.org/github/antirrabia/DataMining-_-/blob/main/notebooks/HousePrices.ipynb) 

 **General Info** <br />  - Every step in the process is a `function`, (e.g. Imputation, Reducing Cardinality). <br /> - Create custom `transformers`, so I can impute `nan` values in a Pipeline. <br /> - I preserved  columns name, when I encode Ordinal and Nominal variables, by using  the `category_encoders` library <br /> <br /> **Outliers:** <br /> - I remove them by Domain knowledge, <br /> - Applying IsolationForest<br /> - Analyzing Residuals (e.g. > than 3 standard deviation) <br /> <br /> **Categorical features**:   <br /> - To reduce the number of dimensions that OneHotEncoder will produce: <br /> - I collapse the less frequent categories into a single category ‘Others’ or <br /> - I create **clusters** using `KMeans` algorithm from `scikit-learn` <br /> - To encode an **Ordinal** variable, I created a dictionary that maps each category to the corresponding order. I then pass it to the OrdinalEncoder instance.<br /> - To encode **Nominal** variables, I used OneHotEncoder from `category_encoders`<br /> - **Ordinal Cyclical variables**: I calculated the SIN and COS components of them.       <br /> <br /> **Numerical Features**: <br /> - I treated Skewness(> 0.7) of numerical variables with Yeo-Johnson technique in the `PowerTransformer` to make them more Gaussian Like.<br /> - Scaling Variables using RobustScaler, because of outliers.   <br /> <br /> **Feature Selection**: <br /> - By using `mutual_info_regressio` model <br /> - Drop features with mutual info = 0.    <br /> <br /> **Feature Engineering**: <br /> - By domain knowledge (e.g combine different measurements of the land)<br /> - Create Polynomial interaction features from the top 20 features with highest mutual information <br /> <br />  **Feature Importance:**  <br /> - I used the feature importance from XGBoost in SelectFromModel to filter out most important feature  <br /> <br />  **Data Sets**: <br />  - I used 80% of the Training set as training set and the remaining 20% as validation set  <br /> <br /> **Modeling**: <br /> I tune the hyperparameters **manually** or by **GridSearchCV**, **RandomizedSearchCV** for the following algorithms. <br/> - **TheilSenRegressor, HuberRegressor, RANSACRegressor, Ridge, ElasticNet, ElasticNetCV, LinearRegression, XGBRegressor, catboost.CatBoostRegressor** <br />    - Next I used them in a **StackingRegressor**  and a **LinearRegression** as a **Meta** model.  <br /> 

