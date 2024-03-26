# deep-learning-challenge

Background
The nonprofit foundation Alphabet Soup wants a tool that can help it select the applicants for funding with the best chance of success in their ventures. With your knowledge of machine learning and neural networks, you’ll use the features in the provided dataset to create a binary classifier that can predict whether applicants will be successful if funded by Alphabet Soup.

From Alphabet Soup’s business team, you have received a CSV containing more than 34,000 organizations that have received funding from Alphabet Soup over the years. Within this dataset are a number of columns that capture metadata about each organization, such as:

EIN and NAME—Identification columns
APPLICATION_TYPE—Alphabet Soup application type
AFFILIATION—Affiliated sector of industry
CLASSIFICATION—Government organization classification
USE_CASE—Use case for funding
ORGANIZATION—Organization type
STATUS—Active status
INCOME_AMT—Income classification
SPECIAL_CONSIDERATIONS—Special considerations for application
ASK_AMT—Funding amount requested
IS_SUCCESSFUL—Was the money used effectively


Overview
1. Create a binary classifier using deep learning neural network for predicting success rate of Alphabet Soup funding applicants.
2. Dataset includes information on 34,000+ organizations with metadata like application type, industry sector, government organization classification, funding use case, income classification, requested funding amount, and effective fund usage status.
3. Preprocess dataset by dropping unnecessary columns, encoding categorical variables, and splitting into training/testing sets.
4. Design, train, and evaluate neural network model to determine loss and accuracy.
5. Optimize model by adjusting input data, adding neurons/hidden layers, using different activation functions, and tuning epochs.
6. Goal: Achieve predictive accuracy >75% and save optimized model as HDF5 file.

Results
Data Preprocessing

What variable(s) are the target(s) for your model?
The target variable(s) for the model is IS_SUCCESSFUL, which serves as the binary classification outcome variable indicating whether a charity donation was successful or not.

What variable(s) are the features for your model?

The feature variables considered for the model include all columns in the DataFrame except for IS_SUCCESSFUL.

What variable(s) should be removed from the input data because they are neither targets nor features?
The EIN was removed 

Compiling, Training, and Evaluating the Model

How many neurons, layers, and activation functions did you select for your neural network model, and why?
	

After experimenting with it, I settled on three hidden layers with node counts of 20, 27, and 3, respectively, as these numbers yielded satisfactory results. For the activation functions, I opted for ReLU for the first layer and sigmoid for the next two layers because they were more suitable for the task. Similarly, I chose sigmoid for the output layer to ensure the output was in binary format.

Were you able to achieve the target model performance?

I was at 77%
What steps did you take in your attempts to increase model performance?

I added back in name from the 1st set and did the same steps that was used for the other fields and this did improve my results 

Summary 

In summary, the deep learning model implemented using TensorFlow and Keras achieved a predictive accuracy of 77% in classifying the success of Alphabet Soup-funded organizations based on their features. The model underwent various optimization attempts, such as dropping columns, binning categorical variables, adding hidden layers and neurons, and experimenting with different activation functions, among other adjustments. Although the desired predictive accuracy of 75% was attained, it required considerable optimization efforts to reach that level.

One suggestion for addressing this classification challenge would be to explore alternative models like Random Forest Classifier or Support Vector Machine (SVM). These models have demonstrated effectiveness in binary classification tasks and might achieve higher accuracy without extensive optimization efforts. Moreover, they can handle both numerical and categorical variables effectively, along with managing outliers and imbalanced datasets, which could be present in this dataset. Hence, exploring these alternative models could offer a potential solution to improving the classification accuracy.
