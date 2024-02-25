# deep-learning-challenge
## 1. Overview of the analysis
The primary objective of this analysis is to develop a binary classifier model using neural network techniques that can accurately predict the success of funding applicants for Alphabet Soup, a nonprofit foundation. This foundation has historically supported over 34,000 organizations, providing them with financial aid to kickstart or sustain their ventures. However, not all investments yield the intended outcomes, making it crucial for Alphabet Soup to optimize their funding process to ensure that resources are allocated to entities with the highest likelihood of success.

## 2. Results
 * Data Preprocessing
   - What variable(s) are the target(s) for your model?
     
     The target variable for the model is IS_SUCCESSFUL. This variable is a binary indicator representing whether the 
     funding provided to an organization by Alphabet Soup was used effectively
     
   - What variable(s) are the features for your model?  
     - APPLICATION_TYPE: The type of application submitted by the organization.  
     - AFFILIATION: The affiliated sector of industry for the organization.  
     - CLASSIFICATION: The government classification of the organization.  
     - USE_CASE: The intended use case for the funding.  
     - ORGANIZATION: The type of organization (e.g., nonprofit, corporation).  
     - STATUS: The active status of the organization.  
     - INCOME_AMT: The income classification for the organization, indicating its financial scale.  
     - SPECIAL_CONSIDERATIONS: Indicates if there are any special considerations for the application.  
     - ASK_AMT: The amount of funding requested by the organization.

   - What variable(s) should be removed from the input data because they are neither targets nor features?
     
     The variables "EIN" and "NAME" are primarily for identification and administrative tracking by Alphabet Soup and do 
     not contribute to understanding or predicting the effectiveness of the funding provided to the organizations. 
     Removing these variables helps streamline the dataset for analysis, ensuring the model focuses on relevant features 
     that impact the outcome of interest, which is the success of the funded projects.

* Compiling, Training, and Evaluating the Model  
  - How many neurons, layers, and activation functions did you select for your neural network model, and why?  
