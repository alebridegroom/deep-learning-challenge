# deep-learning-challenge

## Data Preprocessing
* What variable(s) are the target(s) for your model? What variable(s) are the features for your model? What variable(s) should be removed from the input data because they are neither targets nor features?

  The target variable used was "IS_SUCCESSFUL" with 1 being consideres yes and 0 being no.  EIN and NAMED were dropped in the first run through and then the data was split into test and training.  CLASSIFICATION and APPLICATION_TYPE were columns that were binned in the first round due to there being many unique values in those columns and to compile the model faster.  These columns had more than 10 unique values and binned and picked out a cutoff point for these into the category "other".  For the second round of doing this, NAME was added back as a feature and also binned.  After binning all categorial data was converted to categorical data using 'pd.get_dummies'.

  

## Compiling, Training, and Evaluating the Model
* How many neurons, layers, and activation functions did you select for your neural network model, and why?

  Three layers in total were used for the neural network model.  The activations that were used were relu and sigmoid for the output layer. "The hidden layers perform nonlinear transformations of the inputs entered into the network" - (https://deepai.org/machine-learning-glossary-and-terms/hidden-layer-machine-learning#:~:text=In%20neural%20networks%2C%20a%20hidden,inputs%20entered%20into%20the%20network.). 

  ![Screenshot 2023-10-16 at 12 40 37 PM](https://github.com/alebridegroom/deep-learning-challenge/assets/91504694/cfd58dea-5779-44ce-bfe3-8ab9a94e1f29)

* Were you able to achieve the target model performance?

  The first attemp I got 73.79% accuracy using 50 epochs with the total parameters being 6561.
  ![Screenshot 2023-10-16 at 12 49 27 PM](https://github.com/alebridegroom/deep-learning-challenge/assets/91504694/94b36863-479b-4e70-af60-9f86e4b49534)

  For the second attempt I got 75.99% accuracy with 9041 parameters.

  ![Screenshot 2023-10-16 at 12 54 27 PM](https://github.com/alebridegroom/deep-learning-challenge/assets/91504694/74376c5a-b26c-4857-951c-ac73c24d9145)


* What steps did you take in your attempts to increase model performance?

  The steps I took was adding back NAME to the features and binning for unique values greater than 100.

## Summary: 
 Overall, keeping NAME as a feature, made the accuracy.  The name column must have some signigance to the data set.  For increasing the accuracy I could have increased the epoch's or changed the attributes of the hidden layers, but ended getting the target accuracy which was 75%.  Binning was important to do, cause the program could take a long time to run without the binning. 
