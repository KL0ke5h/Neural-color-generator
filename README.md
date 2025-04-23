# Neural Color Generator

This project implements an AI-powered color generator that predicts RGB values from textual color descriptions. It utilizes a transformer architecture with attention mechanisms, leveraging pre-trained GloVe word embeddings for robust and perceptually accurate color predictions.

## Features

* Predicts RGB color values from textual color names or descriptions.
* Uses a transformer architecture with multi-head attention for text processing.
* Incorporates pre-trained GloVe word embeddings for semantic understanding of color names.
* Employs CIEDE2000 color difference metric for accurate evaluation.
* Provides a Gradio-based web interface for interactive color prediction.
* Supports model packaging for deployment.

## Dependencies

* Python 3.9
* TensorFlow 2.x
* colormath
* gradio
* transformers
* pygithub
* huggingface_hub

## Installation

1. Clone the repository: `git clone <repository_url>`
2. Install the required packages: `pip install -r requirements.txt`
3. Mount Google Drive and adjust the file path to your dataset:
