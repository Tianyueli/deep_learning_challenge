# deep_learning_challenge

Analysis Report on the Neural Network Model:

* Overview of model: Created a deep learning model for Alphabet Soup.

* Tools used:

* Actions performed:
  * Preprocess the Data using Pandas and scikit-learn’s StandardScaler() and identified the mandatory varaiables:
    * Target variable: Is_successful
    * Feature variable for my model: Remaining attributes besides EIN and Name
  * Data Preprocessing:
    * Dropped the EIN and NAME columns
    * For columns that have more than 10 unique values, aggregated values into groups to narrow down the number of unique data attributes
    * Used pd.get_dummies() to encode categorical variables.
    * Split the preprocessed data into a features array, X, and a target array, y, and used the train_test_split function to split the data into training and testing datasets
    * Scaled the training and testing features datasets by creating a StandardScaler instance, fitting it to the training data, then using the transform function.
    * Designed a neural network model to create a binary classification model that predicted if an Alphabet Soup-funded organization would be successful based on the features in the dataset and calculated the binary classification model’s loss and accuracy.
    * Compiled the model, trained the model using training data, and evaluated the model using testing data to determine the loss and accuracy


 * Performance of the model:
   * Initial model:
   * Result: calculated 72.758% accuracy of correctly predicting the success of an Alphabet Soup-funded organization
    * <img width="679" alt="image" src="https://github.com/Tianyueli/deep_learning_challenge/assets/42381263/9d404d85-9aac-43ba-8891-31d1f9e022ae">

   * Optimize the Model:
    * Used TensorFlow and Kerastuner to adjust the input data to ensure that no variables or outliers are confusing the model
    * We are Dropping two more columns, Status and Special_Consideration because these variables were neither targets nor prominent features within the input data.

    * Added ten more neurons to both 2nd hidden layer
    * Add a hidden layer with a Sigmoid activation function.
Use different activation functions for the hidden layers.
    * Increased the number of epochs in the training regimen to 100
  * Result: Improved model performance to 0.7301 (73.01%) accuracy:
    * <img width="668" alt="image" src="https://github.com/Tianyueli/deep_learning_challenge/assets/42381263/ef884ba8-6f61-4a7d-b78e-fefce31a4455">


  * Optimization of model:
Attempt 1: Best Accuracy so far: 0.7359663844108582
    * <img width="834" alt="image" src="https://github.com/Tianyueli/deep_learning_challenge/assets/42381263/dc8e3fe2-bccb-4a99-a644-6603e7c3aa56">

* Summary:
  * Via several attempts, the final model could not achieve the 75% accuracy score; however, inched closely towards the positive directly with the various optimization methods.
  * The final model achieved approximately 73.6% accuracy using a deep learning model.
  * For future analysis, a heat map or PCA method can be generated in the data preprocessing phase to help further narrow down the key factors required to fit the classification neural network model properly.

* Glossary:
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

* Reference:
IRS. Tax Exempt Organization Search Bulk Data Downloads. https://www.irs.gov/ Links to an external site.
