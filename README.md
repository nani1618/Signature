# Signature Verification using Convolutional Neural Networks

This project aims to develop a Convolutional Neural Network (CNN) model to verify the authenticity of signatures, classifying them as genuine or forged. The model is trained on the CEDAR dataset, which contains images of both genuine and forged signatures.

## Dataset

The CEDAR dataset is used for training and evaluation. It contains a collection of handwritten signatures, including both genuine and forged samples. The dataset is split into training and validation sets, with 80% of the data used for training and the remaining 20% for validation.

## Preprocessing

The dataset is preprocessed by resizing the images to 64x64 pixels and applying data augmentation techniques such as shearing, zooming, and horizontal flipping to the training set. The images are also normalized by rescaling the pixel values between 0 and 1.

## Model Architecture

The CNN model consists of the following layers:

1. Convolutional Layer (32 filters, 3x3 kernel)
2. Max Pooling Layer (2x2)
3. Convolutional Layer (64 filters, 3x3 kernel)
4. Max Pooling Layer (2x2)
5. Convolutional Layer (128 filters, 3x3 kernel)
6. Max Pooling Layer (2x2)
7. Flatten Layer
8. Dense Layer (128 units, ReLU activation)
9. Dropout Layer (0.5)
10. Dense Layer (1 unit, Sigmoid activation)

The model is compiled with the Adam optimizer and binary cross-entropy loss function. The accuracy metric is used for evaluation.

## Training

The model is trained for 50 epochs with early stopping patience of 10 epochs. The training and validation generators are used to feed the data to the model during training.

## Evaluation

After training, the model is evaluated on the validation set. The following metrics are reported:

- Validation Loss
- Validation Accuracy
- Precision
- Recall
- F1-Score

## Usage

1. Clone the repository
2. Download the CEDAR dataset and extract it to the project directory
3. Run the Jupyter Notebook (`Signature.ipynb`)

Note: Make sure to install the required Python libraries (listed in the notebook) before running the code.

## Contributing

Contributions are welcome! If you find any issues or have suggestions for improvements, please open an issue or submit a pull request.
