# Neural_Network_Charity_Analysis


# Overview of the Project

Beks has come a long way since her first day at that boot camp five years ago—and since earlier this week, when she started learning about neural networks! Now, she is finally ready to put her skills to work to help the foundation predict where to make investments.
With your knowledge of machine learning and neural networks, you’ll use the features in the provided dataset to help Beks create a binary classifier that is capable of predicting whether applicants will be successful if funded by Alphabet Soup.
From Alphabet Soup’s business team, Beks received a CSV containing more than 34,000 organizations that have received funding from Alphabet Soup over the years. Within this dataset are a number of columns that capture metadata about each organization, such as the following:

•	EIN and NAME—Identification columns

•	APPLICATION_TYPE—Alphabet Soup application type

•	AFFILIATION—Affiliated sector of industry

•	CLASSIFICATION—Government organization classification

•	USE_CASE—Use case for funding

•	ORGANIZATION—Organization type

•	STATUS—Active status

•	INCOME_AMT—Income classification

•	SPECIAL_CONSIDERATIONS—Special consideration for application

•	ASK_AMT—Funding amount requested

•	IS_SUCCESSFUL—Was the money used effectively




# Overview of the Analysis


The goal of the project was to create and train deep learning models in order to predict whether applicants will be successful if funded by the charity organization ‘Alphabet Soup’.

# Results

Data Preprocessing:

The original dataset contained the following columns: 



![Data Set](https://user-images.githubusercontent.com/101373142/180109382-b254c0ea-29df-4a28-937e-5bbc74a4c0bd.png)



•	The columns:  ‘EIN’ and ‘Name’ were dropped because they don not provide any value to the analysis

•	The ‘IS_SUCCESSFUL’ column is considered as target

•	The remaining columns were used as features for the model


Compiling, Training, and Evaluating the Model

The first model was created with two hidden layers. The first has 80 neurons and the second layer has 80 neurons. The Relu Activation Function was used on both layers.  The Sigmoid Activation Function was used on the Output layer.  This model predicts a target with an accuracy of:  0.731 



![Evaluate model](https://user-images.githubusercontent.com/101373142/180109492-b0d6452c-1d41-46a5-8c9c-51e0195af596.png)


In an attempt to achieve 75% accuracy, the number of neurons in the second layer were increased to 80, resulting in no change.  The accuracy of the model did not increase or decrease. It remained at: 0.731



![Test model 1](https://user-images.githubusercontent.com/101373142/180109543-cd493473-4383-4dee-85bb-4e225ea8b66d.png)


The activation function for the hidden layers was then changed to Tanh, resulting to a slight increased accuracy of: 0.732 


![Test model 2](https://user-images.githubusercontent.com/101373142/180109583-2b76a113-5124-4dc9-a245-2916fa8774aa.png)


Next, the bucketing technique was used for the asked amount (column ASK_AMT)



![Applications](https://user-images.githubusercontent.com/101373142/180109626-c25123fa-e658-40db-b7ed-a45cad241e50.png)


For this model the initial parameters were used resulting in an accuracy of: 0.729 


![Test model 3](https://user-images.githubusercontent.com/101373142/180109669-ca8f0045-8fd5-4722-aefd-070455b32c44.png)



# Summary


The goal of 75% accuracy for the model was not met.  Removing the ‘application type’ and ‘classification’ columns may improve accuracy in the future.  These features may delay the response/accuracy. Also, increasing the number of neurons seems inadequate.  Changes such as this should possibly be done prior in a preprocessed dataset.

