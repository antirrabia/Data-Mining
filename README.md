# DataMining-_-
All my work about my passion. Here 



## List of my DataSets and ipynbd


\# | Description | Link | Testing
--- | --- | --- | ---
`Titanic` | <p>I wrote my own functions to create new features and code them using domain knowledge.</p> <p> After having all the features coded, I use `IterativeImputer` and `KNNImputer` I tried different parameters for `imputation_order` and `n_neighbors` </p> <p> I created a main `Pipeline` and a `GridSearchCV` to tune hyperparameters. </p>|  <a href="https://nbviewer.jupyter.org/github/antirrabia/DataMining-_-/blob/main/notebooks/Titanic_01.ipynb"><img src="icons/nb.svg" width="20px" align="top" title="View code"></a> | 
... | <p>  I improved and turned my functions into transformers using `FunctionTransformer` which I then used in `FeatureUnion` </p> <p> This time I wanted to try `SimpleImpute` and the strategies of `mean`, `median`, `constant`, `most_frequent` for numeric features and `most_frequent` for categorical features. </p> | <a href="https://nbviewer.jupyter.org/github/antirrabia/DataMining-_-/blob/main/notebooks/Titanic_02.ipynb"><img src="icons/nb.svg" width="20px" align="top" title="View code"></a> | .. |