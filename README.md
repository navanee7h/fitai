# FitAI: Intelligent Personalized Health System

[![React](https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)](https://reactjs.org/)
[![TypeScript](https://img.shields.io/badge/TypeScript-007ACC?style=for-the-badge&logo=typescript&logoColor=white)](https://www.typescriptlang.org/)
[![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white)](https://tailwindcss.com/)
[![Django](https://img.shields.io/badge/Django-092E20?style=for-the-badge&logo=django&logoColor=white)](https://www.djangoproject.com/)
[![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/)
[![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white)](https://scikit-learn.org/)

FitAI is a highly dynamic, full-stack healthcare platform that leverages Machine Learning and Large Language Models (LLMs) to construct intelligent daily workout and nutrition regimens tailored precisely to a user's health metrics and medical constraints.

---

## 🌟 Key Features

*   **ML-Powered Recommendations:** Utilizes a custom recommendation engine built with Scikit-Learn utilizing Cosine Similarity to dynamically process workouts and meals based on your unique health profile, injuries, and goals.
*   **Intelligent Split Rotation:** The backend intelligently tracks your workout history and organically rotates targeted muscle groups (Chest, Back, Legs, etc.) to ensure balanced physical training without requiring manual selection.
*   **Context-Aware AI Chatbot:** Embedded Groq API integration (powered by Llama 3) reads live user database metrics (Weight, Height, TDEE, Goals) to formulate deeply personalized, low-latency fitness guidance.
*   **Full-Stack Ecosystem:** Robust Django REST API backend coupled with a blazing fast frontend built on React, Vite, TypeScript, and modern Tailwind CSS.

---

## 🚀 Quick Start Guide

### Prerequisites
*   Node.js (v18+)
*   Python 3.10+
*   Git

### Setting up the Environment
1. **Clone the repo**
   ```bash
   git clone https://github.com/navanee7h/fitai.git
   cd fitai
   ```

2. **Configure your API Keys**
   Navigate to the `backend` folder and create a `.env` file for the AI dependencies:
   ```bash
   # In fitai/backend/.env
   GROQ_API_KEY=your_groq_api_key_here
   ```

3. **Install Dependencies & Seed the Database**
   
   **Frontend:**
   ```bash
   cd frontend
   npm install
   ```

   **Backend:**
   ```bash
   cd backend
   python -m venv .venv
   
   # Activate your environment
   # Windows: .\.venv\Scripts\activate
   # Linux/Mac: source .venv/bin/activate
   
   pip install -r requirements.txt
   python manage.py migrate
   python seed_db.py  # Populates the database with AI Presets!
   ```

### Running the Application

For a quick unified boot (if you are on Windows), you can simply run the provided batch file from the root directory:
```bash
.\start.bat
```

**Manual Start:**
If you prefer starting them individually:
*   **Frontend:** `npm run dev` (Runs on `localhost:5173`)
*   **Backend:** `python manage.py runserver` (Runs on `localhost:8000`)

---

## 🧠 Architecture Overview
*   **Frontend**: Handled efficiently via `React` and `Vite`, relying heavily on functional components with complex state management communicating seamlessly with the REST APIs.
*   **Backend**: A specialized `Django` core serving RESTful endpoints. The core computational logic lives here, parsing matrix arrays and applying base heuristics + +50 priority boosts for target body part tracking.
*   **Machine Learning**: Sklearn's `MinMaxScaler` and `cosine_similarity` are used heavily in `ml_recommender.py` to shape user vectors into personalized, deployable plans.

---

> Made with ❤️ to simplify personal health and fitness using AI.
