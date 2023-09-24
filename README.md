# deep-learning-challenge

Overview

The purpose of this analysis was to create a machine learning neural network to predict which applicants to select for funding that have the best chance of success in their ventures.

Results

Data Preprocessing:
- The target variable is the "IS_SUCCESSFUL" column which stores the information regarding whether the fundraising for the venture was used effectively.
- The other variables provided, except the name and id columns, are the features for the model.
- Since the name and id columns are neither features nor targets, they should be removed from the input data.

Compiling, Training, and Evaluating the Model:
- For the initial model, I chose 2 hidden layers, both with 'relu' activation function. The first layer had 7 neurons, while the second had 5. There was an output layer with single output and 'sigmoid' activation function because this is a classification problem.
- In the initial model, an accuracy of 72% was achieved - this fell short of the target performance (75% accuracy)
- In the preprocessing, we replaced more "application types" and "classifications" with the other category to reduce the number of dummies. We also changed the number of nodes to 9 for the first hidden layer and 4 for the second hidden layer. This however, reduced our accuracy. Keeping the preprocessing from before, we added another hidden layer while also changing the number of neurons in the previous layers. Now hidden layer 1 had 7 nodes, hidden layer 2 had 4 nodes and hidden layer 3 also had 4 nodes. This still left us short of our desired accuracy threshold. Finally for the last attempt, we looked at the correlation values of features with our target columns. We found that "STATUS" column was very poorly correlated to the target. Upon further analysis, we noted that STATUS had two unique values but the second value ("0") occured only 5 times compared to 34394 for "1". This column was dropped. Keeping the same architecture as the previous optimization attempt, a new model was fitted. The accuracy still did not reach the target.

Summary:
In summary, our machine learning neural network model did not achieve the target accuracy of 75%. More exploratory data analysis is needed to determine the optimum application types and classifications.
