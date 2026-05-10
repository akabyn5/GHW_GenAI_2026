# Code with Codespaces — MLH Global Hack Week Cloud

## Challenge
Code with Codespaces

## Description
This submission documents our team's completion of the **GitHub Skills: Code with Codespaces** exercise, part of MLH Global Hack Week Cloud. GitHub Codespaces is a fully configured cloud development environment that runs directly in the browser or in Visual Studio Code — no local setup needed. Through this exercise, we created and customized a codespace, learned how to configure the development container, and practiced the full cloud-based development workflow from within a GitHub repository.

<img width="1176" height="888" alt="Code_with_Codespaces2" src="https://github.com/user-attachments/assets/df03a510-2aa6-4ac7-bc53-3f6ebe88a389" />


## Features
- Created a **codespace from a GitHub repository** and ran the project entirely in the cloud
- Customized the environment using a **`devcontainer.json`** configuration file
- Installed **VS Code extensions** and applied personal editor settings inside the codespace
- Made and committed **code changes** directly from the browser-based editor
- Practiced the full development loop — edit, run, preview, and push — without any local installation

## Technologies Used
- React
- Next.js
- Auth0
- Cloudinary
- Presage
- GitHub Copilot

## Installation

### Running Locally
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

### Running with GitHub Codespaces
1. Navigate to the repository on GitHub
2. Click the green **`<> Code`** button → **Codespaces** tab
3. Click **"Create codespace on main"**
4. Wait for the environment to build — all dependencies are installed automatically
5. The dev server starts automatically; click **"Open in Browser"** when prompted

No local setup required. Everything runs in the cloud.

## Team Members
- José Peñalba
- Maryfer Higuera
- José Echeverría
- Tomas Strandgard

## Repository
🔗 [GitHub Repository](https://github.com/<your-repo-here>)

## What We Learned
Codespaces completely removed the "it works on my machine" problem. Spinning up a fully configured environment from a repository in under two minutes — with the correct Node version, extensions, and port forwarding already in place — made onboarding to a new project feel effortless. We also learned how powerful `devcontainer.json` is for standardizing the development environment across the entire team, ensuring everyone writes and runs code under identical conditions regardless of their local machine setup.

## Future Improvements
- Extend the **`devcontainer.json`** with post-create scripts to automate database seeding and environment variable injection
- Add a **Codespaces secrets** configuration so sensitive credentials are pre-loaded securely when a codespace starts
- Define **multiple dev container profiles** for different roles (frontend, backend, full-stack) within the same repository
- Explore **Codespaces prebuilds** to reduce environment startup time for the team
- Integrate **GitHub Copilot** directly within the Codespaces editor for an AI-assisted cloud development experience
