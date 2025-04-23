# Neural Color Generator

## Overview
The **Neural Color Generator** is an AI-powered tool that **predicts RGB color values from text descriptions** using a t**ransformer-based neural network**. It leverages pretrained GloVe word embeddings and a multi-head attention mechanism to generate accurate color predictions. The project includes a Gradio-based web interface for interactive use and a CI/CD pipeline for deployment to Hugging Face Spaces.

## Features
- **Color Prediction**: Predicts RGB values from color names or descriptions.
- **Transformer Architecture**: Utilizes multi-head attention and GloVe embeddings for robust text-to-color mapping.
- **Gradio Interface**: Interactive web interface for real-time color predictions.
- **CI/CD Pipeline**: Automated deployment to Hugging Face Spaces via GitHub Actions.
- **Data Augmentation**: Enhances dataset with synthetic color names and RGB variations.
- **Performance Metrics**: Evaluates predictions using Mean Absolute Error (MAE) and CIEDE2000 color difference.


# Project Structure

**NeuralColorGenerator.ipynb:** Main Jupyter notebook with data processing, model training, and Gradio interface.
**github_actions_workflow.yml:** GitHub Actions configuration for CI/CD.
**char_tokenizer.pkl / word_tokenizer.pkl:** Saved tokenizers for character and word-level processing.
**color_transformer_final.keras:** Saved transformer model.
**glove/:** Directory for GloVe embeddings.
**test_color_model.py:** Test script for CI/CD (create this for production use).

Dataset
The project uses a colors.csv dataset containing color names and their corresponding RGB values. The dataset is augmented with:

Synthetic color name variations (e.g., character deletion, swapping).
RGB noise to preserve natural color distribution.

# Model Architecture

**Input:** Character-level and word-level tokenized color descriptions.
**Embedding:** GloVe 6B 100d pretrained word embeddings.
**Layers:** Transformer with multi-head attention, bidirectional LSTM, and dense layers.
**Output:** RGB values (0-255) for the predicted color.
**Metrics:** MAE and CIEDE2000 for evaluating color accuracy.

# Deployment
The model is deployed to Hugging Face Spaces using Gradio for the frontend. The **CI/CD pipeline**:

*Runs tests using test_color_model.py.
*Deploys the model and interface to a Hugging Face Space.
*Requires a Hugging Face API token (HF_TOKEN) stored in GitHub Secrets.
