# Get Your Presage API Key — MLH Global Hack Week GenAI '25

## Challenge
Get Your Presage API Key

## Description
This submission documents our team's registration with **Presage**, a developer-focused platform that captures and analyzes real-time human biometric, physical, and emotional data using a standard camera — no specialized hardware required. As part of MLH Global Hack Week GenAI 2025, we signed up for a Presage account, explored the SDK resources and documentation, and obtained an API key ready to integrate into our hack. Presage's ability to detect emotional and physiological signals through an ordinary webcam opens exciting possibilities for GenAI applications that can adapt to the user's real-time state.

<img width="1600" height="850" alt="Get_Your_Presage_API_Key" src="https://github.com/user-attachments/assets/83870649-3cb9-46f7-8e8a-950d5650a962" />


## Features
- Created a **Presage developer account** and accessed the dashboard
- Located and reviewed the **Presage SDK documentation** and available integration resources
- Generated a **Presage API key** configured for our application
- Explored Presage's real-time detection capabilities: **emotion recognition**, **heart rate estimation**, **attention tracking**, and **stress level analysis**
- Identified integration points between Presage's biometric data stream and our **Next.js** frontend for use in future builds

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
# Add your Presage API key and other credentials to .env.local
```

Add the following to your `.env.local` file:
```env
PRESAGE_API_KEY=<your-presage-api-key>
AUTH0_SECRET=<your-auth0-secret>
AUTH0_BASE_URL=http://localhost:3000
AUTH0_ISSUER_BASE_URL=https://<your-auth0-domain>.auth0.com
AUTH0_CLIENT_ID=<your-auth0-client-id>
AUTH0_CLIENT_SECRET=<your-auth0-client-secret>
```

```bash
# Run the development server
npm run dev
```

Open [http://localhost:3000](http://localhost:3000) in your browser.

### Presage Setup
1. Sign up for a free developer account at [presagetech.com](https://presagetech.com)
2. Navigate to your **Profile / Developer** section in the Presage dashboard
3. Generate a new **API key** and copy it to your `.env.local` as `PRESAGE_API_KEY`
4. Download or install the **Presage SDK** following the official documentation
5. Grant **camera permissions** in the browser when your app initializes the Presage session

## Team Members
- José Peñalba
- Maryfer Higuera
- José Echeverría
- Tomas Strandgard

## Repository
🔗 [GitHub Repository](https://github.com/<your-repo-here>)

## What We Learned
Exploring Presage opened our eyes to a category of input we hadn't considered before: **passive biometric signals** captured through a device already present in almost every user's environment — their webcam. Most apps ask users to explicitly state how they feel through ratings or feedback forms; Presage makes it possible to infer emotional and physiological state in real time without interrupting the user experience at all. This changes how we think about building adaptive GenAI applications — instead of waiting for the user to tell the system something isn't working, the system can detect friction and respond proactively.

## Future Improvements
- Integrate the Presage SDK into the frontend to capture **real-time emotion and attention data** during user sessions
- Build a GenAI feature that adapts its responses or UI dynamically based on the **detected emotional state** of the user
- Use Presage's **stress and focus signals** to trigger contextual nudges — such as simplifying content when stress is high or offering a break prompt when attention drops
- Store anonymized biometric session summaries in **Cloudinary** alongside user-generated media for richer session analytics
- Explore combining Presage data with **Auth0 user profiles** to build personalized, mood-aware experiences at the individual level
