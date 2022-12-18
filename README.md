# Neural_Network_Charity_Analysis
## Overview of Project
1. Compare differences between traditional machine learning classification, regression models, and neural network models.
2. Describe the perceptron model utilized, and its components.
3. Implement neural network models using TensorFlow.
4. Explain how different neural network structures change algorithm performance.
5. Preprocess and construct datasets for neural network models.
6. Compare the differences between neural network models and deep neural networks.
7. Implement deep neural network models using TensorFlow.
8. Save trained TensorFlow models for later use.

###Purpose
Alphabet Soup is looking to predict where to make investments. While using machine learning and neural networks to apply features on a provided dataset, we are able to create a binary classifier capable of predicting whether applicants will be successful if funded by Alphabet Soup. The initial file has 34,000 organizations and columns that capture metadata about each organization from past successful fundings.

## Results and Analysis
### Results
Data Preprocessing:
1. What variable(s) are considered the target(s) for your model?
Based on the data, analyzing to see if the target is marked as successful in the DataFrame, indicating it has been successfully funded by Alphabet Soup.

2. What variable(s) are considered to be the features for your model?
The IS_SUCCESSFUL column is the feature for this dataset.

3. What variable(s) are neither targets nor features, and should be removed from the input data?
The EIN and NAME columns are neither targets nor features, and should be removed from the input data. 

Compiling, Training, and Evaluating the Model: 
4. How many neurons, layers, and activation functions did you select for your neural network model, and why?
In the optimized model, layer 1 began with 120 neurons with a relu activation. For layer 2, it dropped to 80 neurons and relu activation continued. From there, the sigmoid activation was the better fit for layers 3 (40 neurons) and layer 4 (20 neurons).

![image](https://user-images.githubusercontent.com/109991916/208312738-7be4cbfb-a0b4-469d-9355-d536e49345c0.png)

5. Were you able to achieve the target model performance?
The target for the model was 75%, but the best the model could produce was 42.0%.

![image](https://user-images.githubusercontent.com/109991916/208313058-d4692314-5062-4421-8945-635015490755.png)

6. What steps did you take to try and increase model performance?
Columns were reviewed and the STATUS and SPECIAL_CONSIDERATIONS columns were dropped as well as increasing the neuron and layer count. Other activations were tried such as tanh, but the model produced went from 40% to 68% accuracy. The relu activation at the early layers and sigmoid activation at the latter provided the most accurate results.

## Summary
The relu and sigmoid activations yielded a 42.0% accuracy, using various number of neurons and layers. The next step should be to utilize the random forest classifier as it is not easily influenced by outliers.
