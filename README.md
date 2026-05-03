# Axiom AI 

An intelligent, multi-agent AI system designed to automate and optimize business operations. This platform leverages specialized AI agents to analyze data, assess risks, make strategic decisions, and execute operational tasks.

## 🚀 Features

- **Multi-Agent Architecture**: Discrete agents for Analysis, Risk Assessment, Decision Making, and Execution.
- **Intelligent Analysis**: Deep data insights using LLMs (GPT-4o via GitHub Models).
- **Interactive Dashboard**: Modern React-based frontend with real-time data visualization using Recharts.
- **Reporting**: Automated PDF report generation for business insights.
- **Cloud Native**: Ready for deployment on Vercel with a FastAPI backend.

## 🛠️ Technology Stack

- **Backend**: FastAPI (Python 3.9+)
- **Frontend**: React, Vite, TailwindCSS (Lucide Icons, Framer Motion, Recharts)
- **AI/LLM**: GPT-4o via GitHub Models / OpenAI API
- **Deployment**: Vercel

## 📂 Project Structure

```bash
├── api/                # Vercel serverless functions entry point
├── backend/            # FastAPI backend application
│   ├── app/            # Core application logic
│   │   ├── agents/     # specialized AI agents
│   │   ├── core/       # Configuration and security
│   │   ├── routes/     # API endpoints
│   │   └── services/   # Business logic and LLM integration
│   └── main.py         # Backend entry point
├── frontend/           # React + Vite frontend
│   ├── src/            # Frontend components and logic
│   └── package.json    # Frontend dependencies
├── sample-data/        # Example data for testing
└── vercel.json         # Vercel deployment configuration
```

## ⚙️ Setup & Installation

### Prerequisites
- Python 3.9+
- Node.js 18+
- GitHub Token (PAT) with access to GitHub Models

### Backend Setup
1. Navigate to the backend directory:
   ```bash
   cd backend
   ```
2. Create a virtual environment:
   ```bash
   python -m venv venv
   source venv/bin/scripts/activate  # On Windows: venv\Scripts\activate
   ```
3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
4. Configure environment variables in `.env`:
   ```env
   OPENAI_API_KEY=your_github_pat_here
   OPENAI_BASE_URL=https://models.inference.ai.azure.com
   OPENAI_MODEL_NAME=gpt-4o
   ```

### Frontend Setup
1. Navigate to the frontend directory:
   ```bash
   cd frontend
   ```
2. Install dependencies:
   ```bash
   npm install
   ```

## 🏃 How to Run

### 1. Start the Backend
```bash
cd backend
uvicorn app.main:app --reload --port 8000
```
The API will be available at `http://localhost:8000`.

### 2. Start the Frontend
```bash
cd frontend
npm run dev
```
The application will be available at `http://localhost:5173`.

## 🌐 Deployment (Vercel)

This project is configured for Vercel. To deploy:
1. Push your code to GitHub.
2. Connect your repository to Vercel.
3. Configure the `OPENAI_API_KEY` environment variable in Vercel project settings.
4. Vercel will automatically detect the configuration and deploy.

## 📄 License

MIT License - See the project for details.
