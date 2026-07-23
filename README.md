<div align="center">
  <h1>🧠 SmartCorp AI: Corporate Insights Platform</h1>
  <p><i>Transforming raw employee data into actionable predictive intelligence.</i></p>

  <!-- Badges -->
  <img src="https://img.shields.io/badge/Python-3.9+-blue.svg" alt="Python Version">
  <img src="https://img.shields.io/badge/React-61DAFB.svg?logo=react&logoColor=black" alt="React">
  <img src="https://img.shields.io/badge/Flask-000000.svg?logo=flask&logoColor=white" alt="Flask">
  <img src="https://img.shields.io/badge/PyTorch-EE4C2C.svg?logo=pytorch&logoColor=white" alt="PyTorch">
  <img src="https://img.shields.io/badge/Firebase-FFCA28.svg?logo=firebase&logoColor=black" alt="Firebase">
</div>

---

## 📖 Overview

**SmartCorp AI** is an advanced, full-stack analytical dashboard built to empower HR and enterprise management teams. Instead of relying on static spreadsheets, this platform dynamically evaluates employee sentiment, forecasts critical KPIs, and flags high-risk departments before issues escalate. 

By leveraging native GPU-accelerated Natural Language Processing (NLP) alongside classic Machine Learning, SmartCorp uncovers the hidden stories within your company's data.

## ✨ Key Capabilities

*   **📊 Predictive Risk Modeling:** Utilizes a custom-trained `DecisionTreeClassifier` to label departmental risk (Low/Medium/High) based on cascading thresholds in attrition, engagement, and project delays.
*   **🗣️ Contextual Sentiment Analysis:** Feeds raw employee feedback into a fine-tuned `DistilBERT` model to automatically categorize company morale into Positive, Neutral, or Negative bands.
*   **📈 Automated Forecasting:** Generates forecasts on departmental performance and translates them into responsive React-based charts using `Chart.js`.
*   **📝 NLP Meeting Summarization:** Pre-configured Hugging Face pipelines to condense massive departmental transcripts into digestible executive summaries.
*   **⚡ Real-Time Interactive UI:** A zero-latency React (Vite) frontend allowing managers to seamlessly explore data, powered by Firebase and a lightweight Flask backend.

---

## 🏗️ System Architecture & Tech Stack

The platform is cleanly separated into a robust backend API and a dynamic React frontend.

| Category | Technology | Purpose |
| :--- | :--- | :--- |
| **Frontend UI** | React (Vite), Chart.js | Reactive dashboard, interactive charting, and dynamic user controls. |
| **Backend API** | Flask, Firebase Admin | Serves data to the frontend, manages authentication, and processes data requests. |
| **Deep Learning** | PyTorch, Hugging Face | GPU-enabled inference for zero-shot text classification and summarization. |
| **Machine Learning** | Scikit-Learn | Training local decision trees for risk assessment and regression lines for forecasting. |
| **Data Engine** | Pandas, NumPy | In-memory massive dataset manipulation and aggregation. |

---

## 🚦 Getting Started

### Prerequisites
*   Node.js & npm (for frontend)
*   Python 3.9+ (for backend)
*   Firebase service account credentials (`firebase-service-account.json` placed in the `backend/` directory)

### Local Installation

**1. Clone the repository**
```bash
git clone https://github.com/sachin-185/AI-Powered-Corporate-Insights-Platform.git
cd AI-Powered-Corporate-Insights-Platform
```

**2. Setup Backend**
```bash
# Navigate to the backend directory
cd backend

# Create and activate a virtual environment
python -m venv venv
# On Windows:
venv\Scripts\activate
# On macOS/Linux:
source venv/bin/activate

# Install dependencies
pip install -r requirements.txt # (or manually install dependencies like Flask, transformers, torch, scikit-learn, etc.)

# Start the Flask server
python main.py
```

**3. Setup Frontend**
```bash
# Open a new terminal and navigate to the frontend directory
cd frontend

# Install Node dependencies
npm install

# Start the Vite development server
npm run dev
```
> 🌐 **Access the UI:** The terminal will output a local network address, typically `http://localhost:5173`.

---

## 🗺️ Roadmap & Future Vision

- [ ] **Live Data Streaming:** Transition from static `data/company_data.csv` to active Snowflake / PostgreSQL websockets.
- [ ] **Generative AI Reports:** Implement an LLM call to produce a human-readable, 3-paragraph summary of the entire dashboard's current state.
- [ ] **Role-Based Access (RBAC):** Integrate Azure AD or Auth0 so managers are hard-locked into viewing only their respective departments.