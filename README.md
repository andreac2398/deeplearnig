# deeplearnig
Overview of the Analysis

The purpose of this analysis was to develop a deep learning model to help the nonprofit foundation, Alphabet Soup, identify applicants with the highest likelihood of success if funded. The dataset provided contains metadata on over 34,000 organizations that have received funding in the past. By leveraging this data, we aimed to create a binary classifier to predict whether an applicant will be successful, thus aiding Alphabet Soup in making more informed funding decisions.

Results

Data Preprocessing
Target Variable(s):

IS_SUCCESSFUL: This is the target variable, indicating whether the funding was used effectively.
Feature Variable(s):

The features include all other columns in the dataset after dropping the target variable and irrelevant columns. These features include:

APPLICATION_TYPE
AFFILIATION
CLASSIFICATION
USE_CASE
ORGANIZATION
STATUS
INCOME_AMT
SPECIAL_CONSIDERATIONS
ASK_AMT

And any other encoded categorical variables derived from these.
Removed Variable(s):

EIN and NAME: These columns were removed as they are identification variables and do not contribute to the prediction of success.
Compiling, Training, and Evaluating the Model
Neurons, Layers, and Activation Functions:

Neurons:
Layer 1: 32 neurons
Layer 2: 16 neurons
Layer 3: 8 neurons

Layers:
The model consists of three hidden layers followed by a dropout layer to prevent overfitting, and finally, an output layer.
Activation Functions:
ReLU (relu) activation function was used for all hidden layers to introduce non-linearity.
Sigmoid activation function was used in the output layer for binary classification.
Why these choices?

The number of neurons and layers was chosen to balance complexity with overfitting. ReLU is commonly used for hidden layers due to its effectiveness in deep learning models, and the sigmoid function is suitable for binary classification tasks.

Model Performance:

The initial model was trained with these parameters, and after evaluating it on the test data, the accuracy achieved was .73.
Steps to Increase Model

Performance:

Increased the number of neurons in each layer.
Added a third hidden layer to increase the model's capacity to learn complex patterns.
Implemented a dropout layer with a 0.2 dropout rate to reduce the risk of overfitting.
Increased the number of epochs to 150 to allow the model more time to learn the underlying patterns in the data.

Summary

The deep learning model developed was able to achieve .78 accuracy on the test set, which excende the 75%. While the model showed decent performance, there are potential improvements that could be made:

Alternative Model Recommendation:

Random Forest Classifier: A Random Forest could be explored as it is highly effective in handling a large number of features and can provide insights into feature importance.

Gradient Boosting Machines (GBM): Techniques like XGBoost or LightGBM could be effective in this scenario due to their ability to handle large datasets and their superior performance in binary classification tasks.

Why?
These ensemble methods often outperform neural networks in structured data scenarios like this one, especially when there is a mix of categorical and numerical features.

In conclusion, while the deep learning model provided a good starting point, experimenting with different machine learning models such as Random Forests or Gradient Boosting Machines could yield even better predictive performance for Alphabet Soup's funding decisions.