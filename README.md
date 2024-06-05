# deep_learning_challenge

Analysis Report on the Neural Network Model:

* Overview of model: Created a deep learning model for Alphabet Soup.

* Tools used:

* Actions performed:
  * Preprocess the Data using Pandas and scikit-learn’s StandardScaler() and identified the mandatory varaiables:
    * target variable: Is_successful
    * feature variable for my model: Remaining attributes besides EIN and Name
  * Data Preprocessing:
    * Drop the EIN and NAME columns
    * For columns that have more than 10 unique values, aggregated values into groups to narrow down the number of unique data attributes
    * Used pd.get_dummies() to encode categorical variables.
    * Splited the preprocessed data into a features array, X, and a target array, y, and used the train_test_split function to split the data into training and testing datasets
    * Scaled the training and testing features datasets by creating a StandardScaler instance, fitting it to the training data, then using the transform function.
    * Designed a neural network model to create a binary classification model that predicted if an Alphabet Soup-funded organization will be successful based on the features in the dataset and calculate the binary classification model’s loss and accuracy.
    * Compiled the model, trained the model using training data, and evaluated the Model using testing data to determine the loss and accuracy
 * Performance of initial model:
    * <img width="679" alt="image" src="https://github.com/Tianyueli/deep_learning_challenge/assets/42381263/9d404d85-9aac-43ba-8891-31d1f9e022ae">

    * Exported the model 
 * Optimize the Model:
    * Used TensorFlow, and Kerastuner to adjust the input data to ensure that no variables or outliers are causing confusion in the model
    * Dropping more columns: Status and Special_Consideration
    * Added 10 more neurons to a both 2nd hidden layer
    * Add an additional hidden layer with Sigmoid activation function.
Use different activation functions for the hidden layers.
    * Increased the number of epochs to the training regimen to 100
* Improved model performance to 0.7301 (73.01%) accuracy:
  <img width="668" alt="image" src="https://github.com/Tianyueli/deep_learning_challenge/assets/42381263/ef884ba8-6f61-4a7d-b78e-fefce31a4455">


* Optimization of model:
Attempt 1: Best Accuracy so far: 0.7359663844108582
<img width="834" alt="image" src="https://github.com/Tianyueli/deep_learning_challenge/assets/42381263/dc8e3fe2-bccb-4a99-a644-6603e7c3aa56">

* Glossory:
  * EIN and NAME—Identification columns
  * APPLICATION_TYPE—Alphabet Soup application type
  * AFFILIATION—Affiliated sector of industry
  * CLASSIFICATION—Government organization classification
  * USE_CASE—Use case for funding
  * ORGANIZATION—Organization type
  * STATUS—Active status
  * INCOME_AMT—Income classification
  * SPECIAL_CONSIDERATIONS—Special considerations for application
  * ASK_AMT—Funding amount requested
  * IS_SUCCESSFUL—Was the money used effectively
 

The report should contain the following:
Overview of the analysis: Explain the purpose of this analysis.
Results: Using bulleted lists and images to support your answers, address the following questions:
Data Preprocessing
What variable(s) are the target(s) for your model?
What variable(s) are the features for your model?
What variable(s) should be removed from the input data because they are neither targets nor features?
Compiling, Training, and Evaluating the Model
How many neurons, layers, and activation functions did you select for your neural network model, and why?
Were you able to achieve the target model performance?
What steps did you take in your attempts to increase model performance?
Summary: Summarize the overall results of the deep learning model. Include a recommendation for how a different model could solve this classification problem, and then explain your recommendation.
