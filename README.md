# Deep Learning Model

<img src="https://github.com/user-attachments/assets/939d2914-ea1d-415b-ac7a-eb6ecd477cea" alt="image" width="150"/>

## Overview of the Analysis

The primary objective of this analysis is to develop a predictive model using machine learning techniques to determine whether an organization funded by Alphabet Soup will be successful. Leveraging the charity_data.csv dataset, we aimed to preprocess the data, identify the most significant features, and build various machine learning models capable of achieving a predictive accuracy exceeding 75%. By comparing different models and optimizing their hyperparameters, we seek to identify the most effective approach for this classification task.

**Results**
**Data Preprocessing**

**Target Variable:**

The target variable for the model is IS_SUCCESSFUL, a binary indicator (0 or 1) representing whether a project received funding.

**Feature Variables:**
- **Features utilized in the model include:**
- APPLICATION_TYPE: The type of application submitted.
- AFFILIATION: The affiliation of the applicant.
- USE_CASE: The intended use of the funds.
- Various numerical features (e.g., FUNDING_AMOUNT).

**Variables to Remove:**

Non-informative variables, such as EIN (Employer Identification Number) and NAME (project name), were removed from the input data as they do not contribute to the predictive capabilities of the model.

**Compiling, Training, and Evaluating the Model**

Neurons, Layers, and Activation Functions:

**The neural network architecture includes:**

**Option 1: 2 Hidden Layers:**

- Layer 1: 200 neurons with LeakyReLU activation
- Layer 2: 150 neurons with LeakyReLU activation
- Output Layer: 1 neuron with a sigmoid activation function for binary classification.
- **Accuracy score: 71.79%**

**Option 2:4 Hidden Layers**

- Layer 1: 300 neurons with LeakyReLU activation
- Layer 2: 150 neurons with LeakyReLU activation
- Layer 3: 100 neurons with LeakyReLU activation
- Layer 4: 50 neurons with LeakyReLU activation
- Output Layer: 1 neuron with a sigmoid activation function for binary classification.
- Rationale: This architecture facilitates complex pattern recognition and accommodates non-linear relationships among features, which is critical for the classification task.
- **Accuracy score: 72%**

**Achieving Target Performance:**
The model achieved an accuracy of approximately 72%, indicating a reasonable performance level. However, the results may require further improvement to meet desired benchmarks in precision and recall.

**Models Tried to Optimize Performance:**
- **Standard Neural Network:** The initial model was built using the architecture described above.
- **Grid Search for Hyperparameter Tuning: A grid search was conducted to identify the best combination of hyperparameters, including learning rates and batch sizes.
- **XGBoost:** An attempt was made to use the XGBoost algorithm, a powerful gradient boosting technique, to assess its performance compared to the neural network.
- **Random Forest**: This ensemble model was tested for its capability to handle the classification task effectively and to compare results with the neural network model.
- **Support Vector Machine (SVM)**: SVM was also evaluated for its effectiveness in distinguishing between successful and unsuccessful projects.

![image](https://github.com/user-attachments/assets/791a0864-0723-484b-91ea-4f474781e71a)

![image](https://github.com/user-attachments/assets/fabe3e8e-359a-4772-8fc7-84a846127cd9)

**Steps to Increase Model Performance:**
- **Hyperparameter Tuning:** Experimented with different learning rates, batch sizes, and the number of training epochs.
- **Regularization Techniques:** Implemented dropout layers to mitigate overfitting.
- **Feature Engineering**: Analyzed feature importance and transformed features to optimize model input.
- **Callbacks**: Employed early stopping and learning rate reduction strategies during training to enhance efficiency and performance.

**Summary**
The deep learning model successfully classifies project funding statuses within the Alphabet Soup dataset, achieving a 72% accuracy rate. While this is a solid foundation, enhancing model performance is a priority.

**Recommendations for Alternative Models:**

Consider sticking with Ensemble Models: Given the trials with models like XGBoost and Random Forest, these techniques could yield improved results, especially with tabular data where feature interactions are significant.

- Justification:
Ensemble methods like XGBoost and Random Forest typically offer greater accuracy and can be less sensitive to overfitting, providing a more robust solution for this classification problem.

![image](https://github.com/user-attachments/assets/d1990815-7645-4771-b112-88f777d32d83)

- The model was fairly accurate overall, correctly classifying about 72% of projects.
- It did better at identifying funded projects (Class 1) with a recall of 79%, while it struggled more with projects that did not receive funding (Class 0), only identifying 64% correctly.
- The balance between precision and recall indicates that while the model is generally reliable, there is room for improvement, especially in identifying non-funded projects correctly.

Exploring these alternative models could enhance the predictive capabilities for the funding classification problem in the Alphabet Soup dataset.

**References**
IRS. Tax Exempt Organization Search Bulk Data Downloads. https://www.irs.gov/Links to an external site.
