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

