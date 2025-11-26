# Agent Development Kit (ADK) Crash Course

This repository contains examples for learning Google's Agent Development Kit (ADK), a powerful framework for building LLM-powered agents.

## Getting Started

### Setup Environment

You only need to create one virtual environment for all examples in this course. Follow these steps to set it up:

```bash
# Create virtual environment in the root directory
python -m venv .venv

# Activate (each new terminal)
# macOS/Linux:
source .venv/bin/activate
# Windows CMD:
.venv\Scripts\activate.bat
# Windows PowerShell:
.venv\Scripts\Activate.ps1

# Install dependencies
pip install -r requirements.txt
```

Once set up, this single environment will work for all examples in the repository.

### Setting Up API Keys

1. Create an account in Google Cloud https://cloud.google.com/?hl=en
2. Create a new project
3. Go to https://aistudio.google.com/apikey
4. Create an API key
5. Assign key to the project
6. Connect to a billing account

Each example folder contains a `.env.example` file. For each project you want to run:

1. Navigate to the example folder
2. Rename `.env.example` to `.env` 
3. Open the `.env` file and replace the placeholder with your API key:
   ```
   GOOGLE_API_KEY=your_api_key_here
   ```

You'll need to repeat this for each example project you want to run.

## Examples Overview

Here's what you can learn from each example folder:

### 1. Basic Agent
Introduction to the simplest form of ADK agents. Learn how to create a basic agent that can respond to user queries.

### 2. Tool Agent
Learn how to enhance agents with tools that allow them to perform actions beyond just generating text.

### 3. LiteLLM Agent
Example of using LiteLLM to abstract away LLM provider details and easily switch between different models.

### 4. Structured Outputs
Learn how to use Pydantic models with `output_schema` to ensure consistent, structured responses from your agents.

### 5. Sessions and State
Understand how to maintain state and memory across multiple interactions using sessions.

### 6. Persistent Storage
Learn techniques for storing agent data persistently across sessions and application restarts.

### 7. Multi-Agent
See how to orchestrate multiple specialized agents working together to solve complex tasks.

### 8. Stateful Multi-Agent
Build agents that maintain and update state throughout complex multi-turn conversations.

### 9. Callbacks
Implement event callbacks to monitor and respond to agent behaviors in real-time.

### 10. Sequential Agent
Create pipeline workflows where agents operate in a defined sequence to process information.

### 11. Parallel Agent
Leverage concurrent operations with parallel agents for improved efficiency and performance.

### 12. Loop Agent
Build sophisticated agents that can iteratively refine their outputs through feedback loops.

## Official Documentation

For more detailed information, check out the official ADK documentation:
- https://google.github.io/adk-docs/get-started/quickstart


# Git main commands
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/ivesh/Google-adk-masterclass.git
git push -u origin main

That's a great idea for clarity! I can certainly provide you with a chronological table summarizing the workflow and the corresponding **GitHub commands** or actions for each step.

## 🧑‍💻 GitHub Workflow and Commands


| Step | Who | Action/Purpose | GitHub Command/Action |
| :--- | :--- | :--- | :--- |
| **1. Set up** | Team Member | **Clone the repository** to their local machine. | `git clone [repo_url]` |
| **2. Update** | Team Member | **Create a new branch** for their feature/work. | `git checkout -b feature/my-new-agent` |
| **3. Develop** | Team Member | **Make code changes** and stage them. | `git add .` |
| **4. Commit** | Team Member | **Save changes** locally to their branch history. | `git commit -m "Implemented core agent logic"` |
| **5. Push** | Team Member | **Upload the new branch** to GitHub. | `git push origin feature/my-new-agent` |
| **6. Request Review** | Team Member | **Open a Pull Request (PR)** on GitHub, targeting `main`. | **GitHub UI Action:** Click the "Compare & pull request" button. |
| **7. Review** | **You (Reviewer)** | **Check the code** in the PR for errors, style, and logic. | **GitHub UI Action:** Go to the PR, review "Files changed," and add comments. |
| **8. Approve/Request Changes** | **You (Reviewer)** | **Submit your formal review** (approval is required for merge). | **GitHub UI Action:** Click "Review changes" $\rightarrow$ select **"Approve"** or **"Request changes."** |
| **9. Merge** | **You (or Approved User)** | **Integrate the changes** into the protected `main` branch. | **GitHub UI Action:** Click the green **"Merge pull request"** button on the PR page (only active after approval). |
| **10. Cleanup** | Team Member | **Sync their local `main` branch** with the new changes. | `git checkout main` $\rightarrow$ `git pull origin main` |