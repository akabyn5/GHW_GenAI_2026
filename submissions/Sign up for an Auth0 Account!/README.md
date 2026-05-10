# Auth0 Identity Management — MLH Global Hack Week GenAI '25

## Challenge
Sign up for an Auth0 Account!

## Description
This submission documents our team's registration for a free **Auth0** account as part of the MLH Global Hack Week GenAI 2025. Auth0 provides a flexible, drop-in identity management solution that lets developers add authentication and authorization to any application in minutes — without building it from scratch. Integrating Auth0 into our stack allowed us to focus on core product features while keeping user authentication secure and standards-compliant.

## Features
- Secure **user authentication** with zero custom auth logic required
- Support for **social logins** (Google, GitHub, and more) out of the box
- **Role-based access control (RBAC)** to manage permissions across the app
- Ready-made **Auth0 Actions** and hooks for custom identity flows
- Seamless integration with React and Next.js via the Auth0 SDK

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
# Fill in your Auth0 domain, client ID, and client secret in .env.local

# Run the development server
npm run dev
```

Open [http://localhost:3000](http://localhost:3000) in your browser to see the app running.

### Auth0 Configuration
1. Create a free account at [auth0.com](https://auth0.com)
2. Create a new **Regular Web Application** in the Auth0 dashboard
3. Copy your **Domain**, **Client ID**, and **Client Secret** into `.env.local`:
   ```
   AUTH0_SECRET=<random-32-char-string>
   AUTH0_BASE_URL=http://localhost:3000
   AUTH0_ISSUER_BASE_URL=https://<your-domain>.auth0.com
   AUTH0_CLIENT_ID=<your-client-id>
   AUTH0_CLIENT_SECRET=<your-client-secret>
   ```

## Team Members
- José Peñalba
- Maryfer Higuera
- José Echeverría
- Tomas Strandgard

## Repository
🔗 [GitHub Repository](https://github.com/<your-repo-here>)

## What We Learned
Setting up Auth0 showed us how much complexity a modern identity provider can abstract away. Things like secure token handling, session management, and OAuth flows — which would take days to implement correctly from scratch — were running in under an hour. We also learned how to configure Auth0 Actions to inject custom claims into JWTs, which gave us fine-grained control over what each user role can access across the app.

## Future Improvements
- Add **multi-factor authentication (MFA)** to strengthen account security
- Implement **Auth0 Organizations** to support multi-tenant use cases
- Explore **Auth0 Fine-Grained Authorization (FGA)** for more granular permission models
- Connect Auth0 logs to a monitoring tool for real-time anomaly detection
- Add **passwordless login** via magic links or passkeys for a smoother user experience
