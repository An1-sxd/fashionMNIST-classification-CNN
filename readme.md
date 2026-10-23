# Fashion-MNIST Classifier with PyTorch

A convolutional neural network for classifying Fashion-MNIST clothing images with PyTorch.

## Project overview

The notebook:

1. Downloads the Fashion-MNIST dataset into a local `./data/FashionMNIST` directory.
2. Applies data augmentation to the training set using a small random affine transformation.
3. Normalizes all images using the Fashion-MNIST mean and standard deviation used in the notebook.
4. Splits the training data into training and validation subsets.
5. Trains a CNN with batch normalization.
6. Evaluates the best validation checkpoint on the test set using loss, accuracy, F1 scores, and a confusion matrix.

## Model

The model contains:

- Two convolutional layers with ELU activations and max pooling.
- `BatchNorm2d` after each convolution.
- A fully connected layer with `BatchNorm1d` and ReLU.
- A final linear layer for the 10 Fashion-MNIST classes.

## Results

The current notebook run reports:

- Test loss: **0.2291**
- Accuracy: **91.61%**
- Macro F1: **0.9158**
- Micro F1: **0.9161**
- Weighted F1: **0.9158**

Results can vary slightly depending on the PyTorch version, hardware, and random state.

## Requirements

- Python 3.10+
- PyTorch
- TorchVision
- TorchMetrics
- NumPy
- Matplotlib
- Jupyter Notebook or JupyterLab

Install the Python dependencies with:

```bash
pip install torch torchvision torchmetrics numpy matplotlib jupyter
```

## Running the notebook

From this directory, start Jupyter:

```bash
jupyter notebook
```

Open `notebook.ipynb` and run the cells from top to bottom. The Fashion-MNIST files are downloaded automatically to `./data/FashionMNIST`.

No Google Drive mount or personal account configuration is required.