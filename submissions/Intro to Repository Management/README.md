# Securing & Collaborating on GitHub — MLH Global Hack Week GenAI '25

## Challenge
Introduction to GitHub Collaboration & Repository Protection

## Description
This submission documents our team's completion of the **GitHub Skills: Collaborative Features** exercise, part of MLH Global Hack Week GenAI 2025. The exercise walks through the key GitHub tools that keep a shared repository healthy as more contributors join — from branch protection rules and required reviews to issue templates and community guidelines. As a practical scenario, we prepared the fictional **Mergington High School extracurricular activities website** repository so that additional teachers could collaborate safely without breaking the main codebase.

<img width="802" height="911" alt="Intro_to_Repository_Management" src="https://github.com/user-attachments/assets/4b621eb9-c18f-44bf-acc6-c7ba876bbc26" />


## Features
- Configured **branch protection rules** to prevent direct pushes to `main` and require pull request reviews before merging
- Set up **required status checks** so code must pass automated checks before it can be merged
- Added a **CODEOWNERS file** to automatically assign reviewers based on the files changed in a pull request
- Created **issue templates** to standardize bug reports and feature requests from collaborators
- Added a **CONTRIBUTING.md** guide outlining how new contributors can participate in the project safely and effectively
- Enabled **repository rulesets** for a scalable, policy-driven approach to access control

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

### Repository Collaboration Setup
1. Go to **Settings → Branches** and add a branch protection rule for `main`
2. Enable **"Require a pull request before merging"** and set the required number of reviewers
3. Enable **"Require status checks to pass before merging"**
4. Add a `CODEOWNERS` file at the root or in `.github/` to auto-assign reviewers
5. Create issue templates under `.github/ISSUE_TEMPLATE/`

## Team Members
- José Peñalba
- Maryfer Higuera
- José Echeverría
- Tomas Strandgard

## Repository
🔗 [GitHub Repository](https://github.com/<your-repo-here>)

## What We Learned
This exercise made us realize how easy it is for an unprotected repository to become chaotic as the team grows. Setting up branch protection rules and a `CODEOWNERS` file shifted the review process from informal to structured — no one can accidentally merge untested code into `main`, and the right person is always automatically looped in for review. Writing a `CONTRIBUTING.md` also forced us to articulate our workflow clearly, which improved communication across the whole team.

## Future Improvements
- Implement **GitHub Actions workflows** as required status checks to run tests and linting on every pull request automatically
- Add a **pull request template** to standardize the information contributors provide when opening a PR
- Explore **GitHub Environments** to set deployment protection rules for staging and production
- Set up **Dependabot alerts** to keep dependencies secure as the project evolves
- Use **GitHub Discussions** as a dedicated space for broader team conversations, separate from issues and pull requests
