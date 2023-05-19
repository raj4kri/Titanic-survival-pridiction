# Titanic-survival-pridiction
whole process of creating a machine learning model on the famous Titanic dataset, which is used by many people all over the world. It provides information on the fate of passengers on the Titanic, summarized according to economic status (class), sex, age and survival.



step 1: Importing the Libraries
step 2: Getting the Data
step 3: Data Exploration/Analysis
        The training-set has 891 examples and 11 features + the target variable (survived). 2 of the features are floats, 
        5 are integers and 5 are objects.
        ![image](https://github.com/raj4kri/Titanic-survival-pridiction/assets/100435391/4d6db332-5b33-49f9-b8d0-e4d38ebff379)
        
        that 38% out of the training-set survived the Titanic. We can also see that the passenger ages range from 0.4 to 80. On top of that we can already detect             some features, that contain missing values, like the ‘Age’ feature.
        
        First of all, that we need to convert a lot of features into numeric ones later on, so that the machine learning algorithms can process them. Furthermore, we         can see that the features have widely different ranges, that we will need to convert into roughly the same scale. We can also spot some more features, that           contain missing values (NaN = not a number), that wee need to deal with.
        
        The Embarked feature has only 2 missing values, which can easily be filled. It will be much more tricky, to deal with the ‘Age’ feature, which has 177                missing values. The ‘Cabin’ feature needs further investigation, but it looks like that we might want to drop it from the dataset, since 77 % of it are             missing.
         it would make sense if everything except ‘PassengerId’, ‘Ticket’ and ‘Name’ would be correlated with a high survival rate.
         
         You can see that men have a high probability of survival when they are between 18 and 30 years old, which is also a little bit true for women but not fully. For women the survival chances are higher between 14 and 40.

For men the probability of survival is very low between the age of 5 and 18, but that isn’t true for women. Another thing to note is that infants also have a little bit higher probability of survival.

Since there seem to be certain ages, which have increased odds of survival and because I want every feature to be roughly on the same scale, I will create age groups later on.

Since there seem to be certain ages, which have increased odds of survival and because I want every feature to be roughly on the same scale.


step 4: Data Preprocessing

        drop ‘PassengerId’ from the train set, because it does not contribute to a persons survival probability.
        
        Age:
        Now we can tackle the issue with the age features missing values. I will create an array that contains random numbers, which are computed based on the             mean  age value in regards to the standard deviation and is_null.
        
        Since the Embarked feature has only 2 missing values, we will just fill these with the most common one.
        
        Fare:
        Converting “Fare” from float to int64, using the “astype()” function pandas
        
        Name:
        We will use the Name feature to extract the Titles from the Name, so that we can build a new feature out of that
        
        Convert ‘Sex’ feature into numeric.
        
        Embarked:
        Since the Ticket attribute has 681 unique tickets, it will be a bit tricky to convert them into useful categories. So we will drop it from the dataset
        Convert ‘Embarked’ feature into numeric.
       
       
step 5:Building Machine Learning Models

        Now we will train several Machine Learning models and compare their results. Note that because the dataset does not provide labels for their testing-set,         we need to use the predictions on the training set to compare the algorithms with each other
        
        Stochastic Gradient Descent (SGD):
        
        Random Forest:
        
        K Nearest Neighbor:
        
        Perceptron
        
        Linear Support Vector Machine
        
        Decision Tree







       
