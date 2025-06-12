# **Harsh Gidwani** - Generative AI With Cloud

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-blue)](https://www.linkedin.com/in/harsh-gidwani-497a63243/)
[![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://www.python.org/)
[![AWS](https://img.shields.io/badge/AWS-Bedrock-orange.svg)](https://aws.amazon.com/bedrock/)
[![SageMaker](https://img.shields.io/badge/AWS-SageMaker-green.svg)](https://aws.amazon.com/sagemaker/)

## 🚀 Project Overview

This repository contains a comprehensive collection of Generative AI implementations using cloud platforms (AWS and Azure). The project demonstrates various approaches to deploying and utilizing large language models (LLMs) for real-world applications including automated blog generation, question-answering systems, and AI-powered content creation.

## ✨ Features

- **🤖 AWS Bedrock Integration**: Automated blog generation using Meta Llama2 models
- **📊 SageMaker Deployments**: Question-answering systems with DistilBERT and Falcon-40B-Instruct
- **☁️ Cloud-Native Architecture**: Serverless AWS Lambda functions with S3 storage
- **🎯 Production-Ready**: Error handling, logging, and scalable deployment patterns
- **📝 Interactive Notebooks**: Jupyter notebooks for experimentation and learning

## 🏗️ Project Structure

```
Generative-AI-With-Cloud-main/
├── Blog generation in aws/
│   ├── app.py                    # AWS Lambda function for blog generation
│   └── requirements.txt          # Python dependencies
├── AWS sagemaker/
│   ├── Untitled (2).ipynb      # DistilBERT Q&A deployment notebook
│   └── falcon40B-instruct-notebook-full.ipynb  # Falcon-40B deployment guide
└── README.md                    # This file
```

## 🛠️ Technologies Used

- **Cloud Platforms**: AWS (Bedrock, SageMaker, Lambda, S3)
- **AI/ML Models**: 
  - Meta Llama2-13B-Chat
  - DistilBERT (Question-Answering)
  - Falcon-40B-Instruct
- **Languages**: Python 3.8+
- **Frameworks**: Boto3, SageMaker SDK, Hugging Face Transformers
- **Infrastructure**: Serverless Architecture, GPU-accelerated instances

## 📋 Prerequisites

- AWS Account with appropriate permissions
- Python 3.8 or higher
- AWS CLI configured
- Basic understanding of:
  - Machine Learning concepts
  - AWS services (Lambda, S3, SageMaker, Bedrock)
  - Python programming

## ⚙️ Installation & Setup

### 1. Clone the Repository
```bash
git clone https://github.com/your-username/Generative-AI-With-Cloud-main.git
cd Generative-AI-With-Cloud-main
```

### 2. AWS Configuration
```bash
aws configure
# Enter your AWS Access Key ID, Secret Access Key, and region
```

### 3. Install Dependencies

For Blog Generation:
```bash
cd "Blog generation in aws"
pip install -r requirements.txt
```

For SageMaker Notebooks:
```bash
pip install sagemaker boto3 --upgrade
```

## 🚀 Usage

### Blog Generation with AWS Bedrock

The blog generation system uses AWS Lambda and Bedrock to create content automatically:

```python
# Example usage
payload = {
    "body": json.dumps({
        "blog_topic": "Artificial Intelligence in Healthcare"
    })
}

# Deploy as Lambda function or run locally
response = lambda_handler(payload, context)
```

**Features:**
- 200-word blog generation
- Automatic S3 storage
- Error handling and logging
- Configurable temperature and parameters

### Question-Answering with SageMaker

Deploy DistilBERT for real-time Q&A:

```python
# Example question-answering
data = {
    "inputs": {
        "question": "What is machine learning?",
        "context": "Machine learning is a subset of artificial intelligence..."
    }
}

response = predictor.predict(data)
```

### Large Language Model Deployment (Falcon-40B)

Deploy Falcon-40B-Instruct for advanced text generation:

```python
# Advanced prompt engineering example
prompt = """You are a helpful AI assistant specializing in cloud computing.

User: Explain the benefits of serverless architecture
Assistant:"""

payload = {
    "inputs": prompt,
    "parameters": {
        "max_new_tokens": 512,
        "temperature": 0.8,
        "top_p": 0.9
    }
}
```

## 🎯 Key Components

### 1. Blog Generation Service (`app.py`)
- **Purpose**: Automated content creation using AWS Bedrock
- **Model**: Meta Llama2-13B-Chat
- **Features**: Lambda integration, S3 storage, error handling

### 2. DistilBERT Q&A (`Untitled (2).ipynb`)
- **Purpose**: Question-answering system deployment
- **Model**: DistilBERT-base-uncased
- **Instance**: ml.m5.xlarge

### 3. Falcon-40B Deployment (`falcon40B-instruct-notebook-full.ipynb`)
- **Purpose**: Large-scale language model hosting
- **Model**: Falcon-40B-Instruct (40B parameters)
- **Instance**: ml.g5.12xlarge (4x NVIDIA A10G GPUs)
- **Features**: Prompt engineering, few-shot learning examples

## 🔧 Configuration

### AWS Bedrock Settings
```python
config = {
    "max_gen_len": 512,
    "temperature": 0.5,  # Controls randomness (0.0-1.0)
    "top_p": 0.9        # Nucleus sampling parameter
}
```

### SageMaker Instance Configuration
```python
# For Falcon-40B deployment
instance_type = "ml.g5.12xlarge"
number_of_gpu = 4
config = {
    'MAX_INPUT_LENGTH': 1024,
    'MAX_TOTAL_TOKENS': 2048
}
```

## 📊 Performance Metrics

- **Blog Generation**: ~30-60 seconds per 200-word blog
- **Q&A Response Time**: ~2-5 seconds per query
- **Falcon-40B**: ~10-30 seconds for complex prompts
- **Cost Optimization**: Pay-per-use serverless architecture

## 🤝 Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙋‍♂️ Support

If you have any questions or need support, feel free to:
- Open an issue in this repository
- Connect with me on [LinkedIn](https://www.linkedin.com/in/harsh-gidwani-497a63243/)

## 🏆 Acknowledgments

- AWS for providing robust cloud AI services
- Hugging Face for open-source model access
- Meta for Llama2 model
- Technology Innovation Institute for Falcon models

---

### **Created by [Harsh Gidwani](https://www.linkedin.com/in/harsh-gidwani-497a63243/)**

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-blue)](https://www.linkedin.com/in/harsh-gidwani-497a63243/)

*Passionate about Generative AI, Cloud Computing, and Machine Learning*

