# Sentiment Analysis Web Application Using Amazon SageMaker

## Project Overview

This project builds an end-to-end machine learning solution using Amazon SageMaker to analyze sentiment (positive/negative) in movie reviews. The implementation creates a system where users can input movie reviews through a web page and have the deployed model predict the sentiment of the review.

## Dataset

This project uses the IMDb dataset from Stanford University. The dataset includes 25,000 training reviews (12,500 positive and 12,500 negative) and 25,000 test reviews (12,500 positive and 12,500 negative).

## Implementation Approach

The project is divided into these main steps:

1. **Data Acquisition and Preprocessing**:
   - Downloading and loading the IMDb dataset
   - Removing HTML tags, tokenizing, removing stopwords, and stemming
   - Creating a dictionary based on high-frequency words (vocabulary size 5,000)
   - Converting each review into a fixed-length (500 words) sequence of integers

2. **Model Building and Training**:
   - Implementing an LSTM (Long Short-Term Memory) based sentiment analysis model using PyTorch
   - Training the model with Amazon SageMaker
   - Customizing training scripts

3. **Model Deployment and Testing**:
   - Deploying the model to a SageMaker endpoint
   - Evaluating test data using the deployed model

4. **Web Application Construction**:
   - Creating AWS Lambda functions and setting up IAM roles
   - Creating a public API using Amazon API Gateway
   - Implementing the web interface

## LSTM Model Architecture

The LSTM model used in this project has the following structure:

1. **Input Layer**: Word ID sequences from reviews (converted from word dictionary)
2. **Embedding Layer**: Converts each word ID to a fixed-dimensional vector
3. **LSTM Layer**: Processes sequence information and learns temporal dependencies
4. **Fully Connected Layer**: Generates final prediction (0 or 1) from LSTM layer output
5. **Sigmoid Activation Function**: Outputs final sentiment score (0-1)

## Technical Details of LSTM

### What is LSTM?
Long Short-Term Memory (LSTM) networks are a type of recurrent neural network (RNN) with enhanced ability to learn long-term dependencies. LSTMs mitigate the vanishing gradient problem and can effectively process long sequences such as text data.

### LSTM Structure
LSTM cells include the following components:

1. **Forget Gate**: Determines what information to discard
2. **Input Gate**: Determines how much new information to add to the cell
3. **Cell State**: Maintains long-term memory
4. **Output Gate**: Determines what to output from the updated cell state

### Model Hyperparameters

- **Embedding Size**: 32
- **Hidden Layer Size**: 200 (during training)
- **Vocabulary Size**: 5,000
- **Learning Rate**: Using Adam optimization algorithm
- **Loss Function**: Binary Cross Entropy

## Detailed AWS Services Overview

### Amazon SageMaker
Amazon SageMaker is a fully managed service that enables building, training, and deploying machine learning models.

#### Key Features of SageMaker
- **Notebook Instances**: Jupyter Notebook-based environment for data exploration and model development
- **Training Jobs**: Efficient model training in scalable compute environments
- **Hyperparameter Optimization**: Automated discovery of optimal hyperparameters
- **Model Deployment**: One-click deployment of models to endpoints accessible via RESTful APIs
- **Managed Spot Training**: Utilization of spot instances for cost reduction

#### SageMaker's Role in This Project
- Providing a training environment for PyTorch-based LSTM models
- Efficient model training using GPU instances (ml.p2.xlarge)
- Hosting models and providing inference endpoints
- Managing model artifacts

### AWS Lambda
AWS Lambda is a compute service that enables running code without managing servers. It automatically executes code in response to events and scales automatically as needed.

#### Key Features of AWS Lambda
- **Serverless Architecture**: No server management required
- **Event-Driven**: Triggered by events such as API requests or file changes
- **Automatic Scaling**: Scales automatically based on traffic
- **Pricing Model**: Pay only for compute time used
- **Multi-Language Support**: Supports Python, Node.js, Java, Go, Ruby, and more

#### Lambda's Role in This Project
- Bridging the web application and SageMaker endpoint
- Processing requests received from API Gateway
- Invoking the SageMaker endpoint and returning results
- Preprocessing input data and formatting responses

### Amazon API Gateway
Amazon API Gateway is a fully managed service for creating, publishing, maintaining, and monitoring APIs at any scale.

#### Key Features of API Gateway
- **RESTful and WebSocket APIs**: Ability to create various types of APIs
- **Traffic Management**: Features like throttling and caching
- **Authentication & Authorization**: Authentication using IAM, Cognito, or Lambda Authorizers
- **API Monitoring**: Monitoring through CloudWatch integration
- **API Stage Management**: Management of development, staging, production environments

#### API Gateway's Role in This Project
- Providing a public HTTP API accessible from the web application
- Routing client requests to Lambda functions
- Processing cross-origin requests through CORS support
- Providing a communication interface between client and server

## AWS Architecture and Service Integration

This project integrates multiple AWS services:

1. **Amazon SageMaker**: Manages model training, testing, and deployment
2. **AWS Lambda**: Handles communication between web app and SageMaker endpoint
3. **Amazon API Gateway**: Creates RESTful API to receive HTTP requests and invoke Lambda functions
4. **Amazon S3**: Stores training data and model artifacts

## Results and Evaluation

- Accuracy on test dataset: Approximately 85%
- Real-time movie review analysis possible through web application

## Discussion and Areas for Improvement

1. Consideration of more complex model architectures
2. Leveraging large pre-trained language models
3. Application of more sophisticated preprocessing techniques
4. Hyperparameter optimization

## Technologies Used

- Python
- PyTorch
- Amazon SageMaker
- AWS Lambda
- Amazon API Gateway
- HTML/JavaScript (Web Application)
- Natural Language Processing (NLP) techniques
