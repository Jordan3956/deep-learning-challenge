# deep-learning-challenge

Overview
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


Analysis
To preprocess the data for the neural network model, I started by uploading the starter file to Google Colab and followed the provided instructions. I read in the 'charity_data.csv' into a Pandas DataFrame and identified the target and feature variables, ultimately dropping the 'EIN' and 'NAME' columns. I then determined the number of unique values for each column and applied binning to "rare" categorical variables. Using pd.get_dummies(), I encoded categorical variables and split the preprocessed data into features (X) and target (y) arrays, utilizing the train_test_split function. Next, I scaled the training and testing feature datasets using the StandardScaler. Moving on to Step 2, I designed a binary classification neural network model with TensorFlow and Keras, considering the appropriate number of inputs, nodes, and layers. I created hidden layers with suitable activation functions and an output layer. After compiling and training the model, I evaluated its performance on the test data, calculating loss and accuracy. Additionally, I implemented a callback to save the model's weights every five epochs and exported the results to an HDF5 file named 'AlphabetSoupCharity.h5.'

For Step 3, I aimed to optimize the model's predictive accuracy beyond 75%. I experimented with various strategies, such as adjusting input data, modifying binning, adding more neurons or hidden layers, and exploring different activation functions and epoch counts. Despite making at least three optimization attempts, there was no strict requirement to achieve the target performance. To document the optimization process, I created a new Google Colab file named 'AlphabetSoupCharity_Optimization.ipynb.' I imported dependencies, read in 'charity_data.csv,' preprocessed the data, and designed a neural network model with adjustments for optimization. Finally, I saved and exported the optimized results to an HDF5 file named 'AlphabetSoupCharity_Optimization.h5.'

Results
![Screen Shot 2023-12-01 at 11 11 47 PM](https://github.com/Jordan3956/deep-learning-challenge/assets/136666362/57d96e38-3c85-4124-9449-af92bd9be5d1)
![Screen Shot 2023-12-01 at 11 11 29 PM](https://github.com/Jordan3956/deep-learning-challenge/assets/136666362/128c2371-fefc-4957-9322-abc65fa1967f)


