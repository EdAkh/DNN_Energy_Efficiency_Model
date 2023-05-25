# Deep Neural Network For Energy Efficiency Prediction Model 

## Introduction 📚

This project is about using a deep neural network to predict the heating load and cooling load of buildings. The data set used is from UCI (https://archive.ics.uci.edu/ml/datasets/energy+efficiency#) and is based on a Ecotect simulation of twelve different building, by playing with eight parameters (Relative Compactness, Surface Area, Wall Area, Roof Area, Overall Height, Orientation, Glazing Area, Glazing Area Distribution) they obtained 768 different shapes of building which have two outcomes (Heating Load and Cooling Load).
 
## Objective 🎯 
The goal is to train a  deep neural network capable of predict the heating load and cooling load of buildings.

## Model 🤖
We developed a Sequential model using TensorFlow, which comprises eight inputs. The model architecture consists of two hidden layers, each containing 128 nodes, two nodes for each outcomes. The diagram below visually represents this configuration:
![nn(1)](https://github.com/EdAkh/DNN_Energy_Efficiency_Model/assets/98283423/68a81897-b999-4568-9baa-aaa1711e5fbc)
To facilitate information flow within the network, we employed the Rectified Linear Unit (ReLU) activation function in the hidden layers. This activation function ensures that neurons are activated when the input has a positive value and deactivated when it is negative.

For the output layer, we utilized a linear activation function. This choice is particularly suitable for linear regression tasks, as it allows the model to predict continuous values.
![actfunc (2)](https://github.com/EdAkh/RNN_Energy_Efficiency_Model/assets/98283423/be17f847-6c9c-4feb-8f90-832ec35a1dc6)

## Metrics 📊
To assess the performance of our model, we employed the mean squared error (MSE) as the loss function, which is commonly used for regression problems. Additionally, we used the R-Squared metric to measure accuracy.
![RegularizationTwoLossFunctions](https://github.com/EdAkh/RNN_Energy_Efficiency_Model/assets/98283423/b516d605-ff56-4b22-a7c5-92e1ecfb2a0c)


After obtaining the predicted values, we divided them into two parts: y1 for the heating load and y2 for the cooling load. For each of these subsets, we applied linear regression using the scikit-learn library. To visualize the fit of our data points to the regression line, we plotted the results.
![image|500x500](https://github.com/EdAkh/RNN_Energy_Efficiency_Model/assets/98283423/2e414e1b-98f5-4632-b372-6a3e7c5e9a2d)

