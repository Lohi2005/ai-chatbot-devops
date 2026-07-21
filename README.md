AI Chatbot DevOps

A simple AI-powered chatbot built with Flask and Google Gemini, fully containerized with Docker and deployed through an automated Jenkins CI/CD pipeline. Selenium is used for end-to-end UI testing.

Features
🤖 Conversational AI powered by Google's Gemini API (gemini-1.5-flash)
🌐 Lightweight Flask web app with a simple chat UI
🐳 Dockerized for consistent, portable deployments
🔁 Jenkins pipeline for automated build, test, and deployment
✅ Selenium-based end-to-end test suite
Tech Stack
Layer	Technology
Backend	Python, Flask
AI Model	Google Gemini (google-genai)
Frontend	HTML, vanilla JS
Testing	Selenium, pytest
Containerization	Docker
CI/CD	Jenkins
Project Structure
ai-chatbot-devops/
├── app.py              # Flask app & routes
├── chatbot.py           # Gemini API integration
├── list_models.py        # Utility script to list available Gemini models
├── test_app.py           # Selenium end-to-end tests
├── requirements.txt        # Python dependencies
├── Dockerfile            # Container build definition
├── Jenkinsfile           # CI/CD pipeline definition
└── templates/
    └── index.html         # Chat UI
Getting Started
Prerequisites
Python 3.9+
A Google Gemini API key
Docker (optional, for containerized run)
1. Clone the repo
bash
git clone https://github.com/Lohi2005/ai-chatbot-devops.git
cd ai-chatbot-devops
2. Set your API key
bash
export GEMINI_API_KEY=your_api_key_here      # macOS/Linux
set GEMINI_API_KEY=your_api_key_here         # Windows
3. Install dependencies & run
bash
pip install -r requirements.txt
python app.py

The app will be available at http://127.0.0.1:5000.

Running with Docker
bash
docker build -t ai-chatbot .
docker run -d -p 5000:5000 -e GEMINI_API_KEY=your_api_key_here ai-chatbot
Running Tests
bash
python test_app.py

Requires Microsoft Edge and the corresponding WebDriver (auto-installed via webdriver-manager).

CI/CD Pipeline

The included Jenkinsfile automates:

Cloning the repository
Installing dependencies
Building the Docker image
Running the container with the Gemini API key injected as an environment variable
Roadmap / Ideas
 Add conversation history / memory
 Improve chat UI styling
 Add automated tests to the Jenkins pipeline
 Add environment-based config for staging/production
