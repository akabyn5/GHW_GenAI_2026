# Sign Up for Cloudinary — MLH Global Hack Week GenAI '25

## Challenge
Sign Up for Your Free Cloudinary Account

## Description
This submission documents our team's registration with **Cloudinary**, a cloud-based media platform that provides developers with AI-powered tools for the optimization, transformation, and management of images and videos, as part of MLH Global Hack Week GenAI 2025. Cloudinary eliminates the need to build and maintain custom media pipelines — uploads, resizing, format conversion, AI tagging, and delivery through a global CDN are all handled through a single API. Integrating Cloudinary into our stack means we can focus on product logic while media management runs automatically in the background.

<img width="942" height="729" alt="Sign up for a free Cloundinary Account!" src="https://github.com/user-attachments/assets/2ccdfc60-ba09-42df-ae14-99375edae0f0" />


## Features
- Created a **free Cloudinary account** and accessed the media dashboard
- Explored the **Media Library** for centralized storage and organization of images and videos
- Reviewed **AI-powered transformation tools**: auto-cropping, background removal, format optimization, and smart resizing
- Located the **API credentials** (Cloud Name, API Key, API Secret) needed for SDK integration
- Identified upload presets and delivery URL patterns for use in our **Next.js** application

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

# Install the Cloudinary Node.js SDK
npm install cloudinary next-cloudinary

# Set up environment variables
cp .env.example .env.local
# Add your Cloudinary credentials to .env.local
```

Add the following to your `.env.local` file:
```env
NEXT_PUBLIC_CLOUDINARY_CLOUD_NAME=<your-cloud-name>
CLOUDINARY_API_KEY=<your-api-key>
CLOUDINARY_API_SECRET=<your-api-secret>
```

```bash
# Run the development server
npm run dev
```

Open [http://localhost:3000](http://localhost:3000) in your browser.

### Cloudinary Setup
1. Sign up for a free account at [cloudinary.com](https://cloudinary.com)
2. From the **Dashboard**, copy your **Cloud Name**, **API Key**, and **API Secret** into `.env.local`
3. Go to **Settings → Upload** and create an **unsigned upload preset** for client-side uploads
4. Use `next-cloudinary`'s `<CldImage />` and `<CldUploadWidget />` components for seamless Next.js integration:
   ```jsx
   import { CldImage } from 'next-cloudinary';

   <CldImage
     src="your-public-id"
     width={800}
     height={600}
     alt="Uploaded image"
   />
   ```

## Team Members
- José Peñalba
- Maryfer Higuera
- José Echeverría
- Tomas Strandgard

## Repository
🔗 [GitHub Repository](https://github.com/<your-repo-here>)

## What We Learned
Setting up Cloudinary showed us how much invisible complexity exists in media handling. Serving the right image format (WebP vs AVIF vs JPEG) to the right browser, resizing on the fly without storing multiple versions, and removing backgrounds with a single URL parameter — all of that would take significant engineering effort to build in-house. Cloudinary's AI transformation layer in particular stood out: auto-cropping that detects and centers on faces or objects means we never have to worry about poorly framed thumbnails, regardless of what the user uploads.

## Future Improvements
- Implement **AI-powered background removal** on user-uploaded profile images using Cloudinary's `e_background_removal` transformation
- Use **Cloudinary's auto-format and auto-quality** delivery flags (`f_auto,q_auto`) across all images to minimize page load times
- Set up a **Cloudinary upload widget** with custom styling so users can drag and drop media directly from the browser
- Explore **video transformation features** — trimming, subtitles, and thumbnail generation — for any video content in the app
- Connect **Cloudinary webhooks** to trigger server-side processing automatically when new media is uploaded
