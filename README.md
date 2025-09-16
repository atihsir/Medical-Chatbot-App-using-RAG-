<h1 align="center">🏥 Medical Chatbot with LLMs, LangChain, Pinecone, Flask, Groq & AWS</h1>

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

<h2>⚡ How to Run Locally</h2>

<h3>1️⃣ Clone the Repository</h3>

```bash
git clone https://github.com/atihsir/Medical-Chatbot-App-using-RAG-.git
<h3>2️⃣ Create a Conda Environment</h3>
bash
Copy code
conda create -n medibot python=3.10 -y
conda activate medibot
<h3>3️⃣ Install Requirements</h3>
bash
Copy code
pip install -r requirements.txt
<h3>4️⃣ Setup Environment Variables</h3>
Create a .env file in the root directory and add:

bash
Copy code
PINECONE_API_KEY=xxxxxxxxxxxxxxxxxxxxxxxxxxxxx
GROQ_API_KEY=xxxxxxxxxxxxxxxxxxxxxxxxxxxxx
<h3>5️⃣ Store Embeddings to Pinecone</h3>
bash
Copy code
python store_index.py
<h3>6️⃣ Run the Flask App</h3>
bash
Copy code
python app.py
👉 Open in browser: http://localhost:8080

<h2>🛠️ Tech Stack</h2> <ul> <li>🐍 Python</li> <li>⚡ LangChain</li> <li>🌐 Flask</li> <li>🌲 Pinecone</li> <li>🤖 Groq (LLMs)</li> <li>☁️ AWS (CI/CD with GitHub Actions)</li> </ul>
<h2>☁️ AWS Deployment Steps</h2> <h3>1. IAM User Setup</h3> <p>Create an IAM user with these policies:</p> <ul> <li>AmazonEC2FullAccess</li> <li>AmazonEC2ContainerRegistryFullAccess</li> </ul> <h3>2. Create an ECR Repository</h3> <p>Save the URI (example):</p>
bash
Copy code
315865595366.dkr.ecr.us-east-1.amazonaws.com/medicalbot
<h3>3. Launch EC2 Instance & Install Docker</h3>
bash
Copy code
sudo apt-get update -y
sudo apt-get upgrade -y
curl -fsSL https://get.docker.com -o get-docker.sh
sudo sh get-docker.sh
sudo usermod -aG docker ubuntu
newgrp docker
<h3>4. Configure GitHub Runner</h3> Go to: <p><b>GitHub → Settings → Actions → Runners</b></p> Add a self-hosted runner → Choose OS → Run commands provided. <h3>5. Setup GitHub Secrets</h3> Add the following secrets in your repository: <ul> <li>AWS_ACCESS_KEY_ID</li> <li>AWS_SECRET_ACCESS_KEY</li> <li>AWS_DEFAULT_REGION</li> <li>ECR_REPO</li> <li>PINECONE_API_KEY</li> <li>GROQ_API_KEY</li> </ul>
<h2 align="center">✅ You are ready to build, run, and deploy your chatbot 🚀</h2> ```
