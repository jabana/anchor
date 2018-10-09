This is an fork of the original work of Marco Tulio Ribeiro, Sameer Singh and Carlos Guestrin and their Method Anchor.

Unlike the idea of an model-agnostic approach for explaining machine learning models is the implementation not data-agnostic. Therefore, I changed anchor_tabluar.py to not use OneHotEncoding befor calling the prediction function. Otherwise, it would not be possible to use models with categorical or metrical features.
Also is it now possible to have features of type bool.

# Anchor
This repository has code for the paper [*High-Precision Model-Agnostic Explanations*](https://homes.cs.washington.edu/~marcotcr/aaai18.pdf).  

An anchor explanation is a rule that sufficiently “anchors” the
prediction locally – such that changes to the rest of the feature
values of the instance do not matter. In other words, for instances on which the anchor holds, the prediction is (almost)
always the same.

At the moment, we support explaining individual predictions for text classifiers or classifiers that act on tables (numpy arrays of numerical or categorical data). If there is enough interest, I can include code and examples for images.

The anchor method is able to explain any black box classifier, with two or more classes. All we require is that the classifier implements a function that takes in raw text or a numpy array and outputs a prediction (integer)

## Installation
The lime package is on pypi. Simply run:

    pip install anchor_exp
Or clone the repository and run:

    python setup.py install
