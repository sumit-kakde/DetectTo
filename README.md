# DetectTo
DetectTo is a model which can be used by Radiologist to diagnose tumor. DetectTo is designed to classify tumors as benign (0) or malignant (1) based on input data that represents various attributes of the tumors. Here's a brief overview of the steps involved:

## Data Preparation

The initial step involves data loading and preparation. We use a dataset stored in a CSV file named `cancer.csv`. The dataset is read using the pandas library, and data is split into attributes (features) and the target variable (diagnosis: 0 for benign, 1 for malignant). We also split the data into a training set and a testing set using the `train_test_split` function.

## Model Architecture

The model is built using TensorFlow and Keras. It's a neural network with the following architecture:

- Input Layer: A dense layer with 256 neurons, accepting input data with the same shape as the number of features in the training data. The activation function used is 'sigmoid'.

- Hidden Layer: Another dense layer with 256 neurons and a 'sigmoid' activation function.

- Output Layer: A dense layer with 1 neuron and a 'sigmoid' activation function. This layer provides the binary classification output.

## Model Compilation

We compile the model with the following settings:

- Optimizer: Adam optimizer is used to fine-tune the model weights during training.

- Loss Function: The model uses the 'binary_crossentropy' loss function, suitable for binary classification problems.

- Metrics: The primary metric used for model evaluation is accuracy, which measures how accurately the model classifies tumors.

## Model Training

The model is trained with the training data for a specified number of epochs (in this case, 1000). During training, the model learns to make accurate predictions based on the input data and minimizes the loss.

## Model Evaluation

After training, we evaluate the model's performance using the testing data. The evaluation provides insights into how well the model classifies tumors by computing metrics such as loss and accuracy.

The results show that the model achieves high accuracy, making it effective for tumor classification.

**Note:** This README provides an overview of the model's purpose and architecture in simple, concise language. Detailed documentation, including code comments and additional explanations, is available in the provided code.

Please refer to the code for more technical details and any additional steps, such as data preprocessing, that may be required for the model's successful operation.
