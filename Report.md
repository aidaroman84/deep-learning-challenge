# deep-learning-challenge
## Overview of the analysis
The primary objective of this analysis is to develop a binary classifier model using neural network techniques that can accurately predict the success of funding applicants for Alphabet Soup, a nonprofit foundation. This foundation has historically supported over 34,000 organizations, providing them with financial aid to kickstart or sustain their ventures. However, not all investments yield the intended outcomes, making it crucial for Alphabet Soup to optimize their funding process to ensure that resources are allocated to entities with the highest likelihood of success.

## Results
### Data Preprocessing
* #### What variable(s) are the target(s) for your model?
     
     The target variable for the model is IS_SUCCESSFUL. This variable is a binary indicator representing whether the 
     funding provided to an organization by Alphabet Soup was used effectively
     
* #### What variable(s) are the features for your model?  
     - APPLICATION_TYPE: The type of application submitted by the organization.  
     - AFFILIATION: The affiliated sector of industry for the organization.  
     - CLASSIFICATION: The government classification of the organization.  
     - USE_CASE: The intended use case for the funding.  
     - ORGANIZATION: The type of organization (e.g., nonprofit, corporation).  
     - STATUS: The active status of the organization.  
     - INCOME_AMT: The income classification for the organization, indicating its financial scale.  
     - SPECIAL_CONSIDERATIONS: Indicates if there are any special considerations for the application.  
     - ASK_AMT: The amount of funding requested by the organization.

* #### What variable(s) should be removed from the input data because they are neither targets nor features?
     
     The variables "EIN" and "NAME" are primarily for identification and administrative tracking by Alphabet Soup and do 
     not contribute to understanding or predicting the effectiveness of the funding provided to the organizations. 
     Removing these variables helps streamline the dataset for analysis, ensuring the model focuses on relevant features 
     that impact the outcome of interest, which is the success of the funded projects.

### Compiling, Training, and Evaluating the Model  
* #### How many neurons, layers, and activation functions did you select for your neural network model, and why?
     For my original neural network model, the configuration chosen includes:
     - 3 Layers Total: 2 Hidden Layers and 1 Output Layer
     - Neurons: First Hidden Layer: 80 neurons, Second Hidden Layer: 30 neurons, Output Layer: 1 neuron
     - Activation Functions: Hidden Layers: ReLU (Rectified Linear Unit) and Output Layer: Sigmoid
      
     ![Original_model](https://github.com/aidaroman84/deep-learning-challenge/blob/main/Images/Original_model.png)

     The choice of 80 neurons for the first hidden layer is intended to provide the model with ample capacity to process and learn from the input 
     features, enabling the identification of a wide range of patterns and relationships in the data. Reducing the number of neurons to 30 in the second 
     hidden layer helps in refining the abstraction of features learned by the first layer, concentrating on the most pertinent information for making 
     the final prediction. ReLU is chosen for its efficiency and effectiveness in adding non-linearity to the model, allowing it to learn complex 
     patterns.
    
     The sigmoid function is used in the output layer for its ability to map the output to a probability score between 0 and 1.
    
     The choices of the number of layers, neurons, and activation functions are designed to create a network that is complex enough to capture the 
     necessary patterns in the data for accurate predictions while remaining computationally feasible and understandable.
    
* #### Were you able to achieve the target model performance?
 
     Based on the results of my original neural network model, which achieved an accuracy of approximately 72.51%, the target model performance of 75% 
     accuracy was not achieved.

     ![Original_result](https://github.com/aidaroman84/deep-learning-challenge/blob/main/Images/Original_result.png)

* #### What steps did you take in your attempts to increase model performance?
  1. Increasing the Number of Neurons and Epochs:

      ![Opt_1](https://github.com/aidaroman84/deep-learning-challenge/blob/main/Images/Opt_1.png)
     
     By increasing the number of neurons in the second hidden layer, we have increased the model's capacity. This means the model has a 
     greater potential to capture and learn from the complexities in the dataset, capturing more intricate dependencies that could influence the 
     prediction of successful funding applications.
     
     Increasing the Number of Epochs allowed the model more iterations over the training dataset to learn the patterns. Training for more epochs can 
     lead to better model performance as it gives the model more opportunities to adjust its weights and biases to minimize the loss function. However, 
     it's important to find a balance as increasing epochs excessively can lead to overfitting.

     ![Opt_1_result](https://github.com/aidaroman84/deep-learning-challenge/blob/main/Images/Opt_1_result.png)

     Based on the result of my first optimization attempt, the model achieved an accuracy of approximately 72.55%. This shows a slight improvement in 
     accuracy (from 72.51% to 72.55%) compared to the original model. However, the target model performance of 75% accuracy was still not achieved.

  2. Adding more layers to the model:
     
     ![Opt_2](https://github.com/aidaroman84/deep-learning-challenge/blob/main/Images/Opt_2.png)

     Adding an extra hidden layer increases the depth of the neural network. This can enhance the model's ability to learn more complex and abstract 
     features from the input data. With each additional layer, the network can create more sophisticated representations of the data, which is 
     beneficial for capturing the nuances in complex datasets.

     ![Opt_2_result](https://github.com/aidaroman84/deep-learning-challenge/blob/main/Images/Opt_2_result.png)

     After implementing the second optimization step, the model achieved an accuracy of approximately 72.52% which is still below the target 
     performance of 75% accuracy.

  3. Using a different activation function (tanh for the second layer):

     ![Opt_3](https://github.com/aidaroman84/deep-learning-challenge/blob/main/Images/Opt_3.png)

     The switch to tanh for the second hidden layer could lead to different learning dynamics due to the nature of the tanh function. It might enable 
     the model to better handle data that benefits from having both positive and negative activations normalized around zero.

     ![Opt_3_result](https://github.com/aidaroman84/deep-learning-challenge/blob/main/Images/Opt_3_result.png)

     After implementing the third optimization step, which involved changing the activation function of the second hidden layer to tanh, the model 
     achieved an accuracy of approximately 72.49% which indicates that accuracy remains relatively stable and still below the target of 75%.

## Summary
The optimization attempts to improve the neural network model's performance in predicting the success of funding applications for Alphabet Soup resulted in a series of iterative modifications, each aimed at enhancing model accuracy and loss metrics. Each optimization attempt led to marginal improvements in either loss or accuracy, but none succeeded in achieving the target model performance of 75% accuracy. The accuracy of the model remained relatively stable across all optimizations, hovering around the 72.5% mark. This stability suggests a potential plateau in performance given the current feature set and model complexity. Loss metrics showed slight variations with each optimization attempt, indicating some impact from the adjustments. However, these changes in loss did not translate into substantial gains in accuracy.

Exploring other machine learning models, including decision trees, random forests, or gradient boosting machines, might offer better performance on this particular dataset. Additionally, ensemble methods that combine predictions from multiple models could also enhance accuracy.
The Random Forest Classifier offers a powerful, flexible, and relatively easy-to-implement solution for classification problems. Its ability to handle a variety of data types, along with its robustness against overfitting and capability to rank feature importance, makes it an excellent candidate for predicting the success of funding applications for Alphabet Soup. By carefully tuning its hyperparameters and evaluating its performance across multiple metrics, could be developed a highly effective model for assisting the nonprofit foundation in its decision-making process.


 

    
