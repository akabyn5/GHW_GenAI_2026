# Complete Challenges with GitHub Copilot — MLH Global Hack Week GenAI '25

## Challenge
Use GitHub Copilot to Complete This Week's Challenges

## Description
This submission documents how our team used **GitHub Copilot** — accessed for free through the **GitHub Student Developer Pack** — to accelerate the completion of coding-based challenges throughout MLH Global Hack Week GenAI 2025. Rather than a single isolated exercise, this challenge captures our broader experience of integrating Copilot as an AI pair programmer across multiple builds during the week. From scaffolding components and writing authentication logic to debugging API integrations and generating boilerplate configuration, Copilot was active at every stage of our development workflow.

> 💬 Our builds have been shared in a GitHub Discussion as required by the challenge, along with a link to our code repository.

## Features
- Used **Copilot inline completions** to accelerate component and function scaffolding across all week's projects
- Leveraged **Copilot Chat** to debug errors, explain unfamiliar APIs, and plan implementation steps before writing code
- Applied **Copilot-generated Auth0 integration** to add secure authentication to the Next.js app in minutes
- Used Copilot to write and iterate on **Cloudinary upload and transformation logic** with natural language prompts
- Generated **environment configuration files**, setup scripts, and README drafts with Copilot's assistance
- Shared progress and builds in a **GitHub Discussion** to contribute to the GHW community

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
# Fill in your Auth0, Cloudinary, and other credentials in .env.local

# Run the development server
npm run dev
```

Open [http://localhost:3000](http://localhost:3000) in your browser.

### Activating GitHub Copilot via Student Developer Pack
1. Apply for the **GitHub Student Developer Pack** at [education.github.com/pack](https://education.github.com/pack)
2. Once approved, go to **GitHub Settings → Copilot** and enable it for your account
3. Install the **GitHub Copilot** and **GitHub Copilot Chat** extensions in VS Code
4. Sign in with your GitHub account — Copilot is now active across all your repositories

## Team Members
- José Peñalba
- Maryfer Higuera
- José Echeverría
- Tomas Strandgard

## Repository
🔗 [GitHub Repository](https://github.com/<your-repo-here>)

## What We Learned
Using Copilot as a constant companion throughout an entire hackathon week — rather than a one-off experiment — revealed how much its value compounds over time. The more context we gave it about the project (tech stack, file structure, naming conventions), the more accurate and relevant its suggestions became. We also found that Copilot Chat was transformative for unblocking stuck moments: instead of spending 30 minutes searching documentation, describing the problem in plain language and asking "what's wrong here?" consistently pointed us in the right direction within seconds. For a team working across multiple challenges simultaneously, this kind of speed multiplier was significant.

## Future Improvements
- Set up **custom Copilot instructions** (`.github/copilot-instructions.md`) to give the AI persistent context about our codebase conventions so suggestions stay consistent across the whole team
- Use **Copilot for pull request summaries** to auto-generate descriptions of what each PR changes and why
- Explore **Copilot Workspace** for end-to-end AI-assisted feature planning, from issue to implementation
- Contribute back to the **GitHub Discussion** with documented prompting strategies that worked well during the week, to help future hackathon participants
- Combine Copilot with **GitHub Actions** to build an AI-assisted CI pipeline that can suggest fixes when checks fail
