# Image Caption Generation using Deep Learning

[![Python](https://img.shields.io/badge/-Python-3776AB?logo=python&logoColor=white)](https://www.python.org/)
[![TensorFlow](https://img.shields.io/badge/-TensorFlow-FF6F00?logo=tensorflow&logoColor=white)](https://www.tensorflow.org/)
![Pandas](https://img.shields.io/badge/-Pandas-150458?logo=pandas&logoColor=white)
![NumPy](https://img.shields.io/badge/-NumPy-013243?logo=numpy&logoColor=white)
![Jupyter](https://img.shields.io/badge/-Jupyter-F37626?logo=jupyter&logoColor=white)
[![Streamlit](https://img.shields.io/badge/-Streamlit-FF4B4B)](https://www.streamlit.io/)

## Table of Contents

- [Demo](#demo)
- [Overview](#overview)
- [About the Dataset](#about-the-dataset)
- [Installation](#installation)
- [Deployement on Streamlit](#deployement-on-streamlit)
- [Directory Tree](#directory-tree)
- [Bug / Feature Request](#bug--feature-request)
- [Future Scope](#future-scope)



## Overview

This repository contains code for an image caption generation system using deep learning techniques. The system leverages a pretrained VGG16 model for feature extraction and a custom captioning model which was trained using LSTM for generating captions. The model is trained on the Flickr8k dataset using an attention mechanism to improve caption quality.

**Note:** While using the `VGG16` model for feature extraction provides accurate results, it's important to be mindful of memory usage. The VGG16 model can consume a significant amount of memory, potentially causing issues in resource-constrained environments. To address this, it's advised to consider using the `MobileNetV2` model for feature extraction. MobileNetV2 strikes a balance between memory efficiency and performance, making it a practical choice for scenarios with limited resources. Consequently, in my deployed app, I've opted for `MobileNetV2`.

The key components of the project include:

- Image feature extraction using a pretrained VGG16 model (Consider using MobileNetV2 for memory efficiency)
- Caption preprocessing and tokenization
- Custom captioning model architecture with attention mechanism
- Model training and evaluation
- Streamlit app for interactive caption generation

## About the Dataset

The [Flickr8k dataset](https://www.kaggle.com/adityajn105/flickr8k) is used for training and evaluating the image captioning system. It consists of 8,091 images, each with five captions describing the content of the image. The dataset provides a diverse set of images with multiple captions per image, making it suitable for training caption generation models.

Download the dataset from [Kaggle](https://www.kaggle.com/adityajn105/flickr8k) and organize the files as follows:

- flickr8k
  - Images
    - (image files)
  - captions.txt

## Directory Tree

```
|   app.py
|   image-captioner.ipynb
|   README.md
|   requirements.txt
|   tokenizer.pkl
\---resource
        demo.gif
```

## Bug / Feature Request

If you encounter any bugs or issues with the loan status predictor app, please let me know . Be sure to include the details of your query and the expected results. Your feedback is valuable in helping me improve the app for all users. Thank you for your support!

## Future Scope

1. **Fine-tuning**: Experiment with fine-tuning the captioning model architecture and hyperparameters for improved performance.
2. **Dataset Expansion**: Incorporate additional datasets to increase the diversity and complexity of the trained model for example we can train the model on [Flickr30k dataset](https://www.kaggle.com/datasets/hsankesara/flickr-image-dataset).
3. **Beam Search**: Implement beam search decoding for generating multiple captions and selecting the best one.
4. **User Interface Enhancements**: Improve the Streamlit app's user interface and add features such as image previews and caption confidence scores.
5. **Multilingual Captioning**: Extend the model to generate captions in multiple languages by incorporating multilingual datasets.
