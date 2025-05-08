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

### 6. Semantic Segmentation

**Overview**: Performs pixel-level classification (semantic segmentation) of road images using a Fully Convolutional Network (FCN). Focusing on road detection for autonomous vehicles, this project identifies "road" and "non-road" regions in images.

**Technologies Used**:
- Fully Convolutional Network (FCN-8)
- Transposed Convolution
- Skip Connections
- Transfer Learning with pre-trained VGG-16 model

**Key Features**:
- Pixel-level road area detection
- High-precision segmentation through encoder-decoder architecture
- Detailed boundary detection through multi-scale feature integration
- Applicability to autonomous driving systems

[Learn more](../self-driving-nd/CarND-Semantic-Segmentation/project_description_en.md)

### 7. Vehicle Detection

**Overview**: Implements a pipeline to detect vehicles in video footage by combining computer vision techniques and machine learning. Uses HOG (Histogram of Oriented Gradients) features and linear SVM to identify and track vehicles in images.

**Technologies Used**:
- HOG feature extraction
- Linear SVM classifier
- Sliding window search
- False positive removal using heatmaps

**Key Features**:
- Vehicle detection at multiple scales
- Stable tracking through cross-frame integration
- Combination of color and HOG features
- Optimization for real-time processing

[Learn more](../self-driving-nd/CarND-Vehicle-Detection/project_description_en.md)

### 8. Object Detection Lab

**Overview**: Builds an object detection system for autonomous driving using MobileNet and SSD (Single Shot Detection) architectures. The project covers everything from the concept of depthwise separable convolutions to utilizing pre-trained models and applying detection to video streams.

**Technologies Used**:
- MobileNet architecture (depthwise separable convolutions)
- SSD object detection framework
- Pre-trained TensorFlow models
- Video stream analysis

**Key Features**:
- Computationally efficient network design
- End-to-end object detection
- Performance comparison of different model architectures
- Real-time object detection implementation

[Learn more](../self-driving-nd/CarND-Object-Detection-Lab/project_description_en.md)

### 9. Advanced Lane Finding

**Overview**: Develops a pipeline to detect lane lines on the road with high precision using computer vision techniques. Going beyond simple edge detection, it combines advanced techniques such as camera calibration, perspective transformation, color space and gradient-based thresholding, and curve fitting to build a robust lane detection system that functions effectively in various road conditions.

**Technologies Used**:
- Image processing with OpenCV
- Camera calibration and distortion correction
- Perspective transformation (bird's-eye view)
- Polynomial fitting

**Key Features**:
- Robust binary thresholding combining multiple color spaces and gradients
- Lane pixel detection using sliding window approach
- Calculation of radius of curvature and vehicle position
- Visualization of detection results and video processing

[Learn more](../self-driving-nd/CarND-Advanced-Lane-Lines/project_description_en.md)

### 10. Traffic Sign Classification

**Overview**: Builds a convolutional neural network (CNN) system to automatically recognize and classify traffic signs. The model is trained on the German Traffic Sign Dataset and evaluated with real-world road sign images. Implements a critical component of autonomous driving systems for sign recognition.

**Technologies Used**:
- Deep learning with TensorFlow/Keras
- Convolutional Neural Networks (CNNs)
- Image preprocessing and normalization
- Data augmentation

**Key Features**:
- Design and implementation of multi-layer CNN architecture
- Dropout regularization to prevent overfitting
- Performance evaluation and visualization on test images
- Analysis of prediction confidence using softmax probabilities

[Learn more](../self-driving-nd/CarND-Traffic-Sign-Classifier-Project/project_description_en.md)

### 11. Behavioral Cloning

**Overview**: Develops an autonomous driving system that mimics human driving behavior using deep neural networks, specifically convolutional neural networks (CNNs). The model is trained on data recorded from a user manually driving a vehicle in a simulator (camera images and steering angles), implementing an end-to-end learning approach.

**Technologies Used**:
- Deep learning with Keras
- NVIDIA model-based CNN architecture
- Data generators and batch processing
- Simulator communication (SocketIO, Flask)

**Key Features**:
- End-to-end learning of human driving behavior
- Image preprocessing (normalization, cropping)
- Data augmentation (horizontal flipping, multiple camera utilization)
- Real-time inference and autonomous driving

[Learn more](../self-driving-nd/CarND-Behavioral-Cloning-P3/project_description_en.md)

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
