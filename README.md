# CLIP-Classification

This project perfoms a 45-way classification on fashion products using this [Fashion Product Images Dataset](https://www.kaggle.com/datasets/paramaggarwal/fashion-product-images-dataset/ "Fashion Product Images Dataset"). It compares finetuning CLIP by adding a softmax layer for classification, and finetuning CLIP by maximizing the similarities of images and the label text with predicting the label with the most similarity.

Finetuning CLIP by classifiction achieves accuracy 92.91% which out-performs finetuning by maximizing the similarties with accuracy 74.77%. It probably because for this classification task, optimizing the softmax layer for classification is more direct than optimizing the similarities.

## Environment
Install the required packages by `install -r requirements.txt`

## Dataset
1. download under CLIP-FP/data 
`kaggle datasets download -d paramaggarwal/fashion-product-images-dataset`
2. unzip the dataset 
`unzip -q fashion-product-images-dataset.zip`

## Training
Run the code on train_classification.ipynb and train_similarity.ipynb