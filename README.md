# Star Classification

The purpose of this project is to classify star's into the following classes:
* Red Dwarf
* Brown Dwarf
* White Dwarf
* Main Sequence
* Super Giants
* Hyper Giants

This is done using different classification algorithms available through the Scikit Learn and TensorFlow Keras libraries.

The models use the following input parameters.
* Absolute Temperature (k)
* Relative Luminosity (L/Lo)
* Relative Radius (R/Ro)
* Absolute Magnitude (Mv)
* Star Color: White, Blue, Red, Yellow, etc.
* Spectral Class (O, B, A, F, K, M)

The Data can be found here: [Kaggle.com](https://www.kaggle.com/datasets/deepu1109/star-dataset)

## Data Preprocessing
The following are data preprocessing steps that were taken:
* Universalizing the case and use of hyphens for the **Star Color** variable
* Creating a one-hot encoding for the the categorical **Star Color** variable
* MinMax regularization of all numeric data

## Exploratory Data Analysis
Appropriate Plots are made to visualize relationships between all variables. 
* When visualizing strictly numeric data, a scatter plot is used
* When visulizing Numeric vs Categorical Data, a bar chart is used
* When visualizing strictly Categorical Data, a table is used

## Machine Learning Algorithms
### Decision Tree
The most optimal Decision Tree classifer used; that is, the Decision Tree classifier with the highest cross validation score averaged between classifications, is the Decision Tree that uses the Gini criterion and is 4 layers deep.

### Neural Network
The most optimal neural network; that is, the neural network with the highest test accuracy, has the following architecture:
* Layer 1: 64 nodes (sigmoid)
* Layer 2: 32 nodes (ReLU)
* Layer 3: Dropout (20% of nodes)
* Layer 4: 16 nodes (ReLU)
* Layer 5: 6 nodes (output layer) (Softmax)
This neural network also utilizes a batch size of 128, a learning rate of 0.05, and categorical cross-entropy loss.

### KNN 
The KNN model worked quite well. Using K=5 neighbhors, the model's metrics were as follows:
* average precision: 0.981
* average recall: 0.977
* average f1 score: 0.987

# Conclusion
There were many different machine learning algorithms that were able to predict star type from input data. These machine learning models could
be used in the assistance of classifying celestial objects by an astronomical observer, human or otherwise. 

### Limitations
* There are only 240 observations in this data set which may have led to added difficulty in model training
* The input data is quite specific and can be difficult to calculate especially for someone with just a telescope, as a result, these models may struggle to be implemented in a commerical setting

### Further Research
Further research could be done to investigate how generative AI models could be used to generate missing data from what someone observes visually strictly with a telescope.
