# Identifying Learning Rules From Neural Network Observables

**Aran Nayebi, Sanjana Srivastava, Surya Ganguli, Daniel L. K. Yamins**

*Neural Information Processing Systems (NeurIPS) 2020*

## Getting started

First clone this repo, then install dependencies
```
pip install -r requirements.txt
```
We recommend Python 3.6 if you run the above requirements file. 

For users who use older versions of Python, we note that in the original paper:
- We used Python 2.7, so the code is backwards-compatible with this version of Python.
- We used TensorFlow 1.13.1 for all of our model training experiments on TPU and for generating these observable statistics on GPU.
- We used `numpy` 1.16.3, `scipy` 1.2.1, and `scikit-learn` 0.20.4 to train classifiers on these generated observable statistics.

## TensorFlow implementations

The `tensorflow/` folder contains our implementations of models (`tensorflow/Models/`) and observable statistics (`tensorflow/Metrics/functions.py`).
It is mainly intended to be used for reference, as the code there is not meant to run.

## Downloading the dataset

To download the dataset of generated observable statistics, simply run

```
./get_dataset.sh
```
This will save `dataset.pkl` to the current directory.

## Downloading saved classifier results

To download results from pretrained classifiers (Random Forest, Linear SVM, and Conv1D MLP) when trained to separate all four learning rules on ten category-balanced 75%/25% train/test splits of the data using all of the observable statistics, simply run

```
./get_saved_results.sh
```
This will save the `.pkl` files to a new directory called `saved_classifier_results/`.
