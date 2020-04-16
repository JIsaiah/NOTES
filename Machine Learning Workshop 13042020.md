*Machine Learning Notes*
<h1>(WHEN VIEWING IN GITHUB, ALWAYS CHOOSE "Raw" TO PREVENT FORMATTING!!)</h1>
<h6>(Best viewed in Visual Studio Code)</h6>

Machine Learning is the ability of the computer to learn independently without given explicit programming. AI uses parameters while ML does not. AI learns through human input and ML. Machine Learning can be divided into three sub-groups, Supervised Learning, Unsupervised Learning and Reinforcement Learning.

An algorithm is the way the computer learns, just like the way humans learn from brain input.

_Supervised Learning:_
This uses input data to work out a 'target variable'. It uses all previous data to predict an answer by comparing the data. The more information given, the easier it is to predict a more accurate answer. The accuracy improves with more data.

Supervised Learning is broken down into two types:
Regression: This is when the target variable is numeric. (e.g. 1, 2, 5.4, 9,007)

Classification: This is when the target variable is a category/classification. The parameters must first be set by someone. (e.g. true/false, retweets/likes/reports, inbox/spam/social)

_Unsupervised Learning:_
This uses input data to find hidden patterns or groupings in data. It looks at the data to make clusters of data and find which clusters are relevent to its cause.

_Reinforcement Learning:_
A learning method that trains algorithms using a reward and punishment system, where the algorithm interacts with its environment to find out what gets it rewarded and what gets it punished.

**K-Nearest Neighbors (KNN)**
The unknown value becomes the value of its neighbor (The closest values near it).
The drawback is that there might be outliers that change the shape of the decision function line.

There are three types of distance movements: (VSCode no pics so go google)
_Euclidean Distance_
_Manhattan Distance_
_Chebyshev Distance_

**PYTHON DATA SCIENCE WORKFLOW**
e.g. # Import packages
        import numpy as np
        import pandas as pd
        from sklearn.model_selection import train_test_split, GridSearchCV
        from sklearn.pipeline import Pipeline
        from sklearn.compose import ColumnTransformer
        from sklearn.neighbors import KNeighborsClassifier
        from sklearn.impute import SimpleImputer
        from sklearn.preprocessing import OneHotEncoder, MinMaxScaler

     # Import data and drop columns
        df = pd.read_csv("data/titanic.csv", index_col="PassengerId")
        df.drop(columns=["Name", "Ticket", "Age", "Cabin"], inplace=True)

     # Dataset Splitting
        X = df.drop(columns='Survived')
        y = df.Survived
        X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2, stratify=y, random_state=42)
        X_train.shape, X_test.shape, y_train.shape, y_test.shape

     # Preprocessor
        numerical_pipeline = Pipeline([
            ("imputer", SimpleImputer(strategy='mean')),
            ("scaler", MinMaxScaler())
        ])

        categorical_pipeline = Pipeline([
            ("imputer", SimpleImputer(strategy='most_frequent')),
            ("onehot", OneHotEncoder())
        ])

        preprocessor = ColumnTransformer([
            ('numeric', numerical_pipeline, ["SibSp", "Parch", "Fare"]),
            ('categoric', categorical_pipeline, ["Pclass", "Sex", "Embarked"]),
        ])

     # Pipeline
        pipeline = Pipeline([
            ("prep", preprocessor),
            ("algo", KNeighborsClassifier())
        ])

     # Hyper Parameter Tuning
        parameter = {
            "algo__n_neighbors": np.arange(1, 51, 2),
            "algo__weights": ['uniform', 'distance'],
            "algo__p": [1, 2]
        }
        model = GridSearchCV(pipeline, param_grid=parameter, cv=3, n_jobs=-1, verbose=1)
        model.fit(X_train, y_train)

     # Evaluation
        print(model.best_params_)
        print(model.score(X_train, y_train), model.best_score_, model.score(X_test, y_test))