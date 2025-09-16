# 🏥 Medical Chatbot with LLMs, LangChain, Pinecone, Flask, Groq & AWS

<p align="center">
   <b>Build and Deploy a Medical Question-Answering Chatbot using modern AI stacks</b> 🚀
</p>

<p align="center">
   <img src="https://img.shields.io/badge/Python-3.10-blue?logo=python" alt="Python"/>
   <img src="https://img.shields.io/badge/Flask-2.3-green?logo=flask" alt="Flask"/>
   <img src="https://img.shields.io/badge/LangChain-0.2.0-orange" alt="LangChain"/>
   <img src="https://img.shields.io/badge/Pinecone-VectorDB-yellow?logo=pinecone" alt="Pinecone"/>
   <img src="https://img.shields.io/badge/Groq-LLMs-red" alt="Groq"/>
   <img src="https://img.shields.io/badge/AWS-Cloud-orange?logo=amazonaws" alt="AWS"/>
</p>

---

## ⚡ How to Run Locally

### 1️⃣ Clone the Repository

```bash
git clone https://github.com/atihsir/Medical-Chatbot-App-using-RAG-.git
cd Medical-Chatbot-App-using-RAG-
```

### 2️⃣ Create a Conda Environment

```bash
conda create -n medibot python=3.10 -y
conda activate medibot
```

### 3️⃣ Install Requirements

```bash
pip install -r requirements.txt
```

### 4️⃣ Setup Environment Variables

Create a `.env` file in the root directory and add:

```bash
PINECONE_API_KEY=xxxxxxxxxxxxxxxxxxxxxxxxxxxxx
GROQ_API_KEY=xxxxxxxxxxxxxxxxxxxxxxxxxxxxx
```

### 5️⃣ Store Embeddings to Pinecone

```bash
python store_index.py
```

### 6️⃣ Run the Flask App

```bash
python app.py
```

👉 **Open in browser:** http://localhost:8080

## 🛠️ Tech Stack

- 🐍 **Python**
- ⚡ **LangChain**
- 🌐 **Flask**
- 🌲 **Pinecone**
- 🤖 **Groq (LLMs)**
- ☁️ **AWS (CI/CD with GitHub Actions)**

## ☁️ AWS Deployment Steps

### 1. IAM User Setup

Create an IAM user with these policies:
- `AmazonEC2FullAccess`
- `AmazonEC2ContainerRegistryFullAccess`

### 2. Create an ECR Repository

Save the URI (example):

```bash
315865595366.dkr.ecr.us-east-1.amazonaws.com/medicalbot
```

### 3. Launch EC2 Instance & Install Docker

```bash
sudo apt-get update -y
sudo apt-get upgrade -y
curl -fsSL https://get.docker.com -o get-docker.sh
sudo sh get-docker.sh
sudo usermod -aG docker ubuntu
newgrp docker
```

### 4. Configure GitHub Runner

Go to: **GitHub → Settings → Actions → Runners**

Add a self-hosted runner → Choose OS → Run commands provided.

### 5. Setup GitHub Secrets

Add the following secrets in your repository:

```
AWS_ACCESS_KEY_ID
AWS_SECRET_ACCESS_KEY
AWS_DEFAULT_REGION
ECR_REPO
PINECONE_API_KEY
GROQ_API_KEY
```

---

## 🚀 Features

- **RAG-based Architecture**: Retrieval-Augmented Generation for accurate medical responses
- **Vector Search**: Pinecone for efficient similarity search
- **Modern LLMs**: Powered by Groq for fast inference
- **Web Interface**: Clean Flask-based UI
- **Cloud Deployment**: Automated CI/CD with AWS and GitHub Actions
- **Scalable**: Docker containerization for easy deployment

## 📁 Project Structure

```
Medical-Chatbot-App-using-RAG-/
├── app.py                 # Flask application
├── store_index.py         # Script to store embeddings
├── requirements.txt       # Python dependencies
├── .env                   # Environment variables
├── Dockerfile            # Container configuration
├── .github/
│   └── workflows/        # CI/CD pipeline
└── templates/            # HTML templates
```

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Submit a pull request

## 📝 License

This project is open source and available under the [MIT License](LICENSE).
