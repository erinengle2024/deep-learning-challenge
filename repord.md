# Overview of the Analysis
The purpose of this analysis is to create a binary classifier using a deep learning neural network to predict whether applicants funded by Alphabet Soup will be successful. The dataset contains metadata on over 34,000 organizations that have received funding, which will be used to build and train the model.

# Results
### Data Preprocessing

- Target Variable: The target variable for the model is IS_SUCCESSFUL, indicating whether the funding was used effectively.
- Feature Variables: The feature variables for the model include APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS, and ASK_AMT.
- Removed Variables: The variables EIN and NAME were removed as they are identification columns and do not contribute to the predictive capability of the model, and are not relevant to predicting success.


## Compiling, Training, and Evaluating the Model

### Model Architecture:
* Initial Model:
  - The initial model had two hidden layers with 80 and 30 neurons, respectively, both using the ReLU activation function. The output layer used the sigmoid activation function.
* Dropout Model:
  -  Added dropout layers to the initial model to prevent overfitting, with a dropout rate of 0.2.
* Complex Model:
  - Increased the complexity by adding more neurons and an additional hidden layer, with layer sizes of 128, 64, and 32 neurons, and added dropout layers.

### Results of Model Evaluations:

* Original Model:
  - Loss: 0.5675
  - Accuracy: 0.7254
* Attempt 1 - Initial Model:
  - Loss: 0.5608
  - Accuracy: 0.7244
* Attempt 2 - Dropout Model:
  - Loss: 0.5528
  - Accuracy: 0.7268
* Attempt 3 - Complex Model:
  - Loss: 0.5591
  - Accuracy: 0.7244

### Steps Taken to Increase Model Performance:

- Initial Model:
  - Created a simple neural network with two hidden layers.
- Dropout Model:
   - Added dropout layers to prevent overfitting.
- Complex Model:
  - Increased the number of neurons and added an additional hidden layer for greater complexity.
 
  ![image](https://github.com/erinengle2024/deep-learning-challenge/assets/158017994/ecdcf8e5-0886-47e1-83a3-8903b02dd066)
  ![image](https://github.com/erinengle2024/deep-learning-challenge/assets/158017994/8c6f3315-573a-42d2-b5eb-568b1464a4c0)

  ![image](https://github.com/erinengle2024/deep-learning-challenge/assets/158017994/4606fe3a-b164-401c-a751-b64b87bf3c97)
  ![image](https://github.com/erinengle2024/deep-learning-challenge/assets/158017994/10acf19f-ba58-4fd6-83e1-7860ff16151c)

  ![image](https://github.com/erinengle2024/deep-learning-challenge/assets/158017994/a6dbeefc-a08f-4aaa-9431-15ba29a3b4a4)
  ![image](https://github.com/erinengle2024/deep-learning-challenge/assets/158017994/407530d3-96a8-4102-b60b-41b111ecfaee)






## Summary
The deep learning model achieved an accuracy of approximately 72.7% after optimization attempts. The best-performing model was the one with added dropout layers, achieving a loss of 0.5528 and an accuracy of 72.68%.

## Recommendations for Further Improvement:

* Hyperparameter Tuning:
  - Perform hyperparameter tuning using techniques like grid search or random search to find the optimal parameters.
* Feature Engineering:
  - Explore additional feature engineering techniques to create more meaningful features from the existing data.
* Ensemble Methods:
  -  Consider using ensemble methods, such as combining multiple models, to improve predictive performance.
* Alternative Models:
  - Experiment with other classification models, such as decision trees, random forests, or gradient boosting machines, to see if they offer better performance.

By implementing these recommendations, there is potential to further enhance the model's predictive accuracy and better assist Alphabet Soup in selecting successful funding applicants.
