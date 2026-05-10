# Getting Started with GitHub Copilot — MLH Global Hack Week GenAI '25

## Challenge
Get Started with GitHub Copilot

## Description
This submission documents our team's completion of the **GitHub Skills: Getting Started with GitHub Copilot** exercise, part of MLH Global Hack Week GenAI 2025. The exercise explores the different ways developers can interact with GitHub Copilot — an AI pair programmer powered by large language models — to explain existing code, generate new functions, plan features, and refactor logic. As the hands-on scenario, we used Copilot to guide updates to the **Mergington High School extracurricular activities website**, practicing real prompting strategies along the way.

<img width="800" height="916" alt="Getting_Started_with_Copilot" src="https://github.com/user-attachments/assets/aa8764eb-b02d-442e-b4d8-e3ca63d25af6" />


## Features
- Used **Copilot Chat** to explain unfamiliar code sections and understand the existing codebase faster
- Generated new **functions and components** by describing intent in plain English via inline Copilot suggestions
- Leveraged **Copilot for planning** by asking it to outline implementation steps before writing a single line of code
- Practiced **prompt engineering** techniques — providing context, constraints, and examples — to get higher-quality suggestions
- Refactored existing code with Copilot's help to improve readability and reduce duplication
- Completed the full exercise in **under one hour** using GitHub Codespaces + Copilot

## Technologies Used
- React
- Next.js
- Auth0
- Cloudinary
- Presage
- GitHub Copilot

## Installation
```bash
# Clone the repository
git clone https://github.com/<your-repo-here>.git

# Navigate to the project folder
cd <project-folder>

# Install dependencies
npm install

# Set up environment variables
cp .env.example .env.local
# Fill in your credentials in .env.local

# Run the development server
npm run dev
```

Open [http://localhost:3000](http://localhost:3000) in your browser.

### Enabling GitHub Copilot
1. Make sure you have an active **GitHub Copilot** subscription (free for students via the GitHub Student Developer Pack)
2. Install the **GitHub Copilot** and **GitHub Copilot Chat** extensions in VS Code
3. Sign in with your GitHub account when prompted
4. Open any file and start typing — Copilot suggestions appear automatically as grey ghost text
5. Press `Tab` to accept a suggestion or `Ctrl + Enter` to open the full suggestions panel

## Team Members
- José Peñalba
- Maryfer Higuera
- José Echeverría
- Tomas Strandgard

## Repository
🔗 [GitHub Repository](https://github.com/<your-repo-here>)

## What We Learned
GitHub Copilot changed how we approach starting a new task. Instead of staring at a blank file, we learned to describe what we want in a comment or chat prompt and let Copilot generate the scaffolding — then we review, adjust, and iterate. The most valuable skill was learning *how* to prompt effectively: giving Copilot enough context (file purpose, expected inputs/outputs, edge cases) consistently produced more accurate and useful suggestions. We also discovered that Copilot Chat is particularly powerful for understanding legacy code, since it can walk through a function line by line and explain what it does in plain language.

## Future Improvements
- Explore **Copilot Edits (multi-file)** to apply coordinated changes across several files in a single prompt
- Use **Copilot for test generation** to automatically scaffold unit tests for existing functions
- Experiment with **custom instructions** to give Copilot persistent context about the project's coding style and conventions
- Integrate **Copilot code review suggestions** into the pull request workflow to catch issues before human review
- Try **Copilot CLI** (`gh copilot`) to get AI assistance directly in the terminal for shell commands and Git operations
