# Udacity Deep Learning Projects Overview

This repository contains multiple projects implemented as part of Udacity's Deep Learning Nanodegree program. Each project explores different deep learning architectures and applications.

## Project List

### 1. Sentiment Analysis Web Application (Amazon SageMaker)

**Overview**: An end-to-end machine learning solution using Amazon SageMaker to analyze sentiment (positive/negative) in movie reviews. Users can input movie reviews through a web page, and the deployed model predicts the sentiment.

**Technologies Used**:
- LSTM model using PyTorch
- Amazon SageMaker (for model training and deployment)
- AWS Lambda & API Gateway (for web application integration)
- Natural Language Processing techniques

**Key Achievements**:
- Accuracy on test dataset: Approximately 85%
- Real-time movie review sentiment analysis through a web application

[Learn more](project-sagemaker/project_description_en.md)

### 2. TV Script Generation

**Overview**: Uses Recurrent Neural Networks (RNN/LSTM) to automatically generate new scripts for the Seinfeld TV show. The model generates coherent TV scripts based on patterns learned from training data.

**Technologies Used**:
- Recurrent Neural Networks (RNN)
- Long Short-Term Memory (LSTM)
- Natural Language Processing and Generation

**Key Features**:
- Learning character conversation patterns
- Predicting next words based on context
- Probabilistic text generation

[Learn more](project-tv-script-generation/project_description_en.md)

### 3. Bike Sharing Prediction

**Overview**: Builds a model using artificial neural networks to predict usage patterns in bike sharing services. The model considers factors like time of day, weather, and season to forecast the number of bicycle rentals.

**Technologies Used**:
- Feedforward Neural Networks
- Gradient Descent and Backpropagation algorithms
- Feature Engineering
- Data Normalization and Preprocessing

**Key Features**:
- Time series data analysis and prediction
- Hyperparameter tuning (learning rate, hidden layer nodes)
- Model evaluation (mean squared error)
- Input feature importance analysis

[Learn more](project-bikesharing/project_description_en.md)

### 4. Dog Breed Classification

**Overview**: Creates an image classification system using Convolutional Neural Networks (CNN) to identify 133 different dog breeds. The application predicts the breed when given a dog image and suggests the most resembling dog breed when given a human image.

**Technologies Used**:
- Convolutional Neural Networks (CNN)
- Transfer Learning (VGG-16, ResNet-50)
- OpenCV (for face detection)
- PyTorch

**Key Features**:
- Human and dog detection algorithms
- CNN model building from scratch
- Leveraging pre-trained models through transfer learning
- Architecture optimization for improved accuracy

[Learn more](project-dog-classification/project_description_en.md)

### 5. Face Generation

**Overview**: Develops a model using Generative Adversarial Networks (GAN) to create realistic human face images. Starting from random noise, the goal is to generate photorealistic images of people who don't exist.

**Technologies Used**:
- Generative Adversarial Networks (GAN)
- Convolutional and Transposed Convolutional Neural Networks
- Batch Normalization
- Adam Optimization Algorithm

**Key Features**:
- Adversarial training process between generator and discriminator
- Training with the CelebA dataset
- GAN training stabilization techniques
- Latent space interpolation for facial feature manipulation

[Learn more](project-face-generation/project_description_en.md)

## AWS Technologies Overview

### Amazon SageMaker

Amazon SageMaker is a fully managed service for building, training, and deploying machine learning models.

**Key Features**:
- Jupyter Notebook-based development environment
- Scalable training environment
- One-click model deployment
- Automated hyperparameter optimization

### AWS Lambda

AWS Lambda is a serverless computing service that runs code in response to events and automatically scales.

**Key Features**:
- Serverless architecture
- Event-driven execution
- Automatic scaling
- Pay-per-use billing model

### Amazon API Gateway

Amazon API Gateway is a fully managed service for creating, publishing, maintaining, and monitoring APIs at any scale.

**Key Features**:
- RESTful and WebSocket API creation
- Traffic management capabilities
- Authentication and authorization integration
- API lifecycle management

## Deep Learning Technologies Overview

### Recurrent Neural Networks (RNN)

Specialized neural networks designed to process sequential data, with internal state (memory) to retain past information.

### Long Short-Term Memory (LSTM)

A type of RNN with enhanced ability to learn long-term dependencies. Memory cells with forget gates, input gates, and output gates enable long-term information retention.

### Convolutional Neural Networks (CNN)

Neural networks primarily used for image processing tasks, automatically learning image features through convolutional and pooling layers.

### Generative Adversarial Networks (GAN)

Generative models where two networks (generator and discriminator) compete during training, enabling the creation of realistic data (images, audio, etc.).

## Supplementary Materials

This repository also includes documents explaining the latest technologies in deep learning that weren't covered in the projects:

- [Advanced Deep Learning Technologies](ADVANCED_DL_TECHNOLOGIES_EN.md) - Transformers, BERT, GPT, NeRF, Diffusion Models, etc.
- [最新のディープラーニング技術の概要](ADVANCED_DL_TECHNOLOGIES.md) - Japanese version
