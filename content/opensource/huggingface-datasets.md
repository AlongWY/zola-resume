---
title: Huggingface/datasets
date: 2021-08-28T14:13:14.674Z
extra:
  featured: true
  link: https://github.com/huggingface/datasets
  image: /media/huggingface_logo.svg
description: 🤗 The largest hub of ready-to-use datasets for ML models with
  fast, easy-to-use and efficient data manipulation tools
taxonomies:
  tags:
    - NLP
    - Datasets
---
🤗 Datasets is a lightweight library providing two main features:

one-line dataloaders for many public datasets: 

+ one liners to download and pre-process any of the number of datasets major public datasets (in 467 languages and dialects!) provided on the HuggingFace Datasets Hub. With a simple command like `squad_dataset = load_dataset("squad")`, get any of these datasets ready to use in a dataloader for training/evaluating a ML model (Numpy/Pandas/PyTorch/TensorFlow/JAX),
+ efficient data pre-processing: simple, fast and reproducible data pre-processing for the above public datasets as well as your own local datasets in CSV/JSON/text. With simple commands like `tokenized_dataset = dataset.map(tokenize_example)`, efficiently prepare the dataset for inspection and ML model evaluation and training.