Laxmi AI - Personal Finance AI Agent
Laxmi AI is an intelligent, web-based AI agent designed to provide personalized financial guidance. By systematically analyzing over 10 user factors—including savings, age, income, financial goals, and risk appetite—it generates a tailored financial plan to help users achieve their objectives.

The application leverages a sophisticated backend to deliver high-quality, context-aware financial advice while minimizing AI hallucinations.

🎯 Project Goal
The primary goal is to create a trustworthy and accessible AI-powered financial advisor. The application is designed to:

Securely gather and analyze a user's complete financial profile.

Generate personalized, actionable financial plans using a powerful AI core.

Automate backend workflows for a scalable and efficient user experience.

Ensure the reliability of AI-generated advice through advanced prompting techniques.

🛠️ Tech Stack & Architecture
Frontend: React.js

Backend: Python, FastAPI

AI & LLM: Azure OpenAI

Workflow Automation: n8n

Database & Authentication: Google Firebase

Prompt Engineering: Custom multi-layer prompts

⚙️ System Workflow
User Authentication & Data Input: The user securely signs into their account (managed by Firebase) and inputs their financial details through the intuitive React.js interface.

API Request: The frontend securely transmits the user's data to the FastAPI backend.

Automated Workflow Trigger: The backend can trigger n8n workflows for pre-processing data or handling specific automated tasks.

Intelligent Prompt Construction: The backend constructs a detailed, multi-layered prompt containing the user's data and specific instructions designed to guide the AI and minimize hallucinations.

AI-Powered Analysis: The prompt is sent to the Azure OpenAI service, which analyzes the user's situation and generates a comprehensive financial plan.

Response to Frontend: The backend receives the generated plan and sends it back to the React frontend.

Display Results: The frontend displays the personalized financial plan to the user in a clear and understandable format.

🏁 How to Run
Prerequisites
Node.js and npm/yarn

Python 3.8+ and pip

An Azure OpenAI API Key and endpoint

A Google Firebase project with authentication enabled

An n8n instance for workflow automation (optional)

Installation & Setup
Clone the repository:

git clone https://github.com/upadhyay-jash/laxmi-ai.git
cd laxmi-ai

Setup Frontend:

cd frontend
npm install
# Create a .env.local file with your Firebase config
cp .env.example .env.local
npm start

Setup Backend:

cd ../backend
pip install -r requirements.txt
# Create a .env file with your Azure API keys
cp .env.example .env
uvicorn main:app --reload
