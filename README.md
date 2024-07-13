## Summary
This repository contains a model designed to determine the signature presence on a document.

## Dataset
The model was trained using the Tobacco 800 dataset, available at [Tobacco 800 Dataset](http://tc11.cvc.uab.es/datasets/Tobacco800_1).  
This dataset consists of documents in TIFF format, with signature positions marked in XML files.

## Classification
The process of extracting signature fragments (class 1) and sampling non-signature fragments (class 0) is detailed in `data_preparation.ipynb`.

## Model Description
The model architecture includes three convolutional layers with 32, 32, and 64 neurons respectively, followed by a fully connected layer with 64 neurons.
This simple configuration could achieved excellent results:
- Binary Accuracy: 99.9% on test and 99.8% on validation
