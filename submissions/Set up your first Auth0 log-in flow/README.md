# Auth0 First Login Flow — MLH Global Hack Week GenAI '25

## Challenge
Auth0 Getting Started — Set Up Your First Login Flow

## Description
This submission documents our team's implementation of a fully functional **Auth0 login flow** following the official Auth0 Getting Started Guide, as part of MLH Global Hack Week GenAI 2025. Starting from a free Auth0 account, we configured an application, set up a login and logout flow, and protected routes so that only authenticated users can access them. The integration was built on top of our existing **Next.js** stack using the Auth0 Next.js SDK, and the entire setup — from account creation to a working login screen — was completed in under an hour.

https://developer.auth0.com/resources/get-started/mlh

## Features
- Configured an **Auth0 Application** (Regular Web App) in the Auth0 dashboard with correct callback and logout URLs
- Implemented a **login and logout flow** using the Auth0 Next.js SDK (`@auth0/nextjs-auth0`)
- Protected private routes using **`withPageAuthRequired`** so unauthenticated users are redirected to login automatically
- Displayed the **logged-in user's profile** (name, email, avatar) after a successful authentication
- Enabled **social login** with Google as an identity provider through the Auth0 dashboard
- Handled **session management** server-side using Auth0's built-in session cookie strategy

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
```

Add the following to your `.env.local` file:
```env
AUTH0_SECRET=<a-long-random-string-at-least-32-chars>
AUTH0_BASE_URL=http://localhost:3000
AUTH0_ISSUER_BASE_URL=https://<your-auth0-domain>.auth0.com
AUTH0_CLIENT_ID=<your-auth0-client-id>
AUTH0_CLIENT_SECRET=<your-auth0-client-secret>
```

```bash
# Run the development server
npm run dev
```

Open [http://localhost:3000](http://localhost:3000) and click **Login** to test the Auth0 flow.

### Auth0 Dashboard Setup
1. Create a free account at [auth0.com](https://auth0.com)
2. Go to **Applications → Create Application** and select **Regular Web Application**
3. Under **Settings**, add to **Allowed Callback URLs**: `http://localhost:3000/api/auth/callback`
4. Add to **Allowed Logout URLs**: `http://localhost:3000`
5. Copy your **Domain**, **Client ID**, and **Client Secret** into `.env.local`
6. In `pages/api/auth/[...auth0].js` (or `app/api/auth/[auth0]/route.js` for App Router), add the Auth0 handler:
   ```js
   import { handleAuth } from '@auth0/nextjs-auth0';
   export default handleAuth();
   ```

## Team Members
- José Peñalba
- Maryfer Higuera
- José Echeverría
- Tomas Strandgard

## Repository
🔗 [GitHub Repository](https://github.com/<your-repo-here>)

## What We Learned
Following the Auth0 Getting Started Guide gave us a clear picture of what an industry-standard authentication flow actually looks like under the hood. We learned that a well-implemented login flow isn't just a username and password form — it involves secure token exchange, callback URL validation, session handling, and logout that properly clears both the application session and the Auth0 session. Having the SDK abstract all of that away was convenient, but tracing through the flow manually helped us understand *why* each step exists and what security problem it solves.

## Future Improvements
- Add **Multi-Factor Authentication (MFA)** through the Auth0 dashboard to strengthen account security
- Implement **Role-Based Access Control (RBAC)** using Auth0 Roles and Permissions to gate specific features by user type
- Explore **Auth0 Actions** to inject custom claims into the JWT on login, such as a user's subscription tier or team membership
- Set up **Auth0 Log Streams** to pipe authentication events to a monitoring tool for real-time alerting on suspicious activity
- Replace social login with **passwordless authentication** (magic link or passkey) for a frictionless user experience
