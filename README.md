# Kaggle_Titanic
Reader's level = Novice level in the Data Science field, and Machine Learning models.

The aim of this work is for me to understand better the methods used for Data Science. <br>

This analysis is the continuation of my previous work. It is an iterated process. <br>

The topic here is a Classification task. This is because I need to classify who died or who survived from the Titanic csv files. <br>

I selected the following models for the analysis: <br>
* Logistic Regression, a basic model.
* RandomForestClassifier
* AdaBoostClassifier
* BaggingClassifier

I learned how to: <BR>
* create a pipeline, test the pipeline to see if it works as expected <br>
* create Ensemble methods <br>
* run Classification Performance metrics <br>
* create k-fold Cross Validation Score <br>
* create Correlations, Scatter Matrix to check which column/feature to use for modelling <br>
* use Simple Imputer method to fill in unknown / not available values in a column / feature <br>

Using the outcomes, I submitted the predicted classification to the Kaggle competition to know how the relevant model works in a real world. <br> 
    
The public scores of the following model in the Kaggle´s Titanic Competition: <br>

+ Pipeline using Logistic Regression without Scaling (`StandardScaler()`) = 0.76555
+ Pipeline using Logistic Regression with Scaling (`StandardScaler()`) = 0.76315
+ Pipeline using Random Forest Classifier with Scaling (`StandardScaler()`) = 0.73205
+ AdaBoostClassifier with LogisticRegression = 0.76555 <br>
+ AdaBoostClassifier with RandomForestClassifier = 0.74162 <br>
+ BaggingClassifier with LogisticRegression = 0.62200 <br>
+ BaggingClassifier with RandomForestClassifier = 0.62200 <br>

Benchmark is 0.76555. This Public score came from submitting a csv file that predicted ALL females survived in the Titanic csv files. <br>
 > The idea is most survivors were females based on the given training dataset. Hence the benchmark represents some sort of extreme extrapolation of the idea. <br>
        
So far with the existing inputs, Logistic Regression model seems the best model for this classification problem. Both Pipeline using Logistic Regression without Scaling (`StandardScaler()`) and AdaBoostClassifier with LogisticRegression produce the same Public score. The score is on par with the Benchmark. If I were to continue with the analysis I would go with Logistic Regression model, and enhance the model by fine tuning it. In the _next steps section_ I listed what I would do. <br>     
    
I found that Bagging Classifier model does not fare well in labelling passengers who survived or died the Titanic csv files. Random Forest Classifier model in general is weaker than the Logistic Regression model, which is a less complex model than the former. It seems that the simple Logistic Regression is a winner here based on my selection of models for this analysis. This does not mean it is the best model for this classification task. If time permits, I would want to include additional models such as KNN Classifier, and Support Vector Machines in the Pipeline, AdaBoost Classifier, and Bagging Classifier, and observe for example their Accuracies, roc_auc_scores, and Public scores. <br> 

What are my next steps? <br>
* I did not focus on Feature Engineering so I am curious how this works in my next project. <br>
* I want to play around Stacking method. This could be implemented in next iterated analysis or on a new project. <br>
* I can enhance the exisiting models by fine tuning their hyperparameters. <br>
    > Hyperparameters are machine learning paramaters in a model that are set/configured BEFORE the model is FITTED onto a training dataset, i.e. `model.fit(X,)`. <br>
        
    > Examples of Hyperparameters: 
    * Learning Rate
    * Number of Epochs
    
        > Note on Parameters of a model: These are for example coefficients and intercept. Here the linear model is y = a + bX, b = coefficient and a = intercept of the linear model. <br>
    
* I chose RandomForestClassifier and LogisticRegression as the basic models. I think RandomForestClassifier is not a basic model because it is an Ensemble model, so I could have had instead use a KNN Classifier. <br>
    > I would use the KNN Classifier in the next project. <br>
* Beside the KNN Classifier model, I also can extend the current selection of models to include Support Vector Machines model as an example. <br>
* I want to play with Autism dataset. A new project. <br>
