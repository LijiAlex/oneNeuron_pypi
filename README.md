# oneNeuron_pypi
one-Neuron-pypi-LijiAlex

# Description
A package to implement the functionality of a Perceptron

## Package description
* oneNeuron.perceptron [A Perceptron class]
* utils.all_utils.createModel [Creates a perceptron model]
* utils.all_utils.prepare_data [Prepares a pandas data frame from numpy array data]
* utils.all_utils.save_model [Saves the perceptron model created]
* utils.all_utils.save_plot [Saves the plot of the input vs output]

## Installation
pip install one-Neuron-pypi-LijiAlex

## How to import the Package

``` python
from oneNeuron.perceptron import perceptron
from utils.all_utils import createModel
```

## Sample code to create an AND model

``` python
from utils.all_utils import createModel

def main(data, eta, epoch, file_name, plot_name):
    createModel(data, eta, epoch, file_name, plot_name)    

if __name__ == '__main__': ##entry point
    AND = {
        "x1": [0,0,1,1],
        "x2": [0,1,0,1],
        "y": [0, 0, 0, 1]
    } #data

    ETA = 0.3 # learning rate between 0 and 1 (assume)
    EPOCHS = 10
    
    try:
        main(data=AND, eta=ETA, epoch=EPOCHS, file_name="and.model", plot_name="and.png")
    except Exception as e:
        raise e # raise exception in terminal
```
### Tips to create other models
* Copy the sample code for AND.
* Replace data with desired data.
* Give appropriate value for data,file_name and plot_name while calling main.

### Sample Project using the package
https://github.com/LijiAlex/oneNeuron

### What works
AND, OR, NOT, NOT, NAND

### What doesn't work
XOR, XNOR
