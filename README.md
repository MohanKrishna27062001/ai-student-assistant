# ai-student-assistant
# AI Study Assistant for Programming Students

## What This Is

A web-based tutoring tool that helps beginner programming students get unstuck when they can't access office hours. Students can either ask for a plain-language explanation of a concept they're struggling with, or paste in buggy code to get guided, step-by-step feedback — similar to how a real teaching assistant would walk them through a problem, rather than just handing over a fixed answer.

## Why I Built This

While teaching 100+ undergraduates across Python and Java/C# labs as a Graduate Teaching Assistant at University, I noticed that limited office-hours availability left many students — especially those balancing jobs, commuting, or new to classroom norms — without anywhere to turn when they got stuck. This tool is an attempt to extend that support beyond scheduled hours, using Claude to explain concepts clearly and review code the way a TA would.

## How It Works

1. A student selects either **Concept Mode** (explain a topic) or **Code Review Mode** (review buggy code)
2. They submit their topic or code through a simple web interface
3. The request goes to a backend server, which sends it to Claude with instructions to:
   - Explain concepts in plain, jargon-free language with practice problems, or
   - Walk through what's wrong with submitted code and guide the student toward the fix, rather than just handing over a corrected answer
4. The response is displayed back to the student in a clean, readable format

## Tech Stack

- **Frontend:** React (Vite)
- **Backend:** FastAPI (Python)
- **AI:** Anthropic Claude API (Claude Sonnet 4.6)
- **Server:** Uvicorn

## Running This Locally

### Backend Setup
```bash
cd backend
python3 -m venv venv
source venv/bin/activate   # On Windows: venv\Scripts\activate
pip install fastapi uvicorn anthropic python-dotenv
```

Create a `.env` file in the `backend` folder with your own Anthropic API key:
