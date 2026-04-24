# Portfolio Website

A modern one-page portfolio built with Next.js, React, Tailwind CSS v4, and Framer Motion.

This project is designed to be easy to customize through a single content file: [`settings.json`](./settings.json). Personal info, social links, SEO metadata, projects, experience, certifications, stats, and resume download settings are all managed there.

## Overview

The site includes:

- Animated hero section with availability status and CV download
- About, skills, stats, experience, education, and certifications sections
- Featured projects with a modal for deeper project details
- Testimonials and contact section
- Smooth scrolling, custom cursor, loading screen, section indicator, and animated background
- SEO metadata configured from `settings.json`

## Tech Stack

- Next.js 16
- React 19
- TypeScript
- Tailwind CSS v4
- Framer Motion
- Lucide React

## Getting Started

### Prerequisites

- Node.js 20+ recommended
- npm

### Install dependencies

```bash
npm install
```

### Start the development server

```bash
npm run dev
```

Open [http://localhost:3000](http://localhost:3000) in your browser.

### Production build

```bash
npm run build
npm run start
```

### Lint

```bash
npm run lint
```

## Project Structure

```text
app/
  components/        Reusable UI sections and motion components
  globals.css        Global styles and theme variables
  layout.tsx         Root layout and metadata setup
  page.tsx           Main one-page portfolio composition
public/
  Rui_Jin_Resume.docx
  robots.txt
  sitemap.xml
settings.json        Main content and configuration source
```

## Customization

Most of the site content comes from [`settings.json`](./settings.json).

### Update personal details

Edit:

- `personal`
- `social`
- `contact`
- `files`

### Update portfolio content

Edit:

- `projects`
- `experience`
- `education`
- `certifications`
- `testimonials`
- `skills`
- `services`
- `stats`

### Update SEO settings

Edit the `seo` section in [`settings.json`](./settings.json):

- `siteUrl`
- `siteName`
- `siteDescription`
- `keywords`
- `ogImage`
- `twitterHandle`
- `googleSiteVerification`

Before deploying, replace placeholder values like:

- `https://yourwebsite.com`
- `your-verification-code`

## Resume Download

The CV download button uses the file path in:

```json
"files": {
  "cv": "/Rui_Jin_Resume.docx"
}
```

To change the downloadable file:

1. Add your resume to `public/`
2. Update `settings.json`
3. If needed, adjust the filename in [`app/components/DownloadCV.tsx`](./app/components/DownloadCV.tsx)

## Notes

- The contact form is currently UI-only and simulates success locally. It is not connected to an email service or backend endpoint yet.
- The site metadata is generated from [`app/layout.tsx`](./app/layout.tsx) using values from [`settings.json`](./settings.json).
- The design uses a dark visual theme defined in [`app/globals.css`](./app/globals.css).

## Available Scripts

- `npm run dev` - Start the local development server
- `npm run build` - Create the production build
- `npm run start` - Run the production server
- `npm run lint` - Run ESLint

## Deployment

This project can be deployed on Vercel or any platform that supports Next.js.

Recommended pre-deploy checklist:

- Update `seo.siteUrl`
- Replace the resume file if needed
- Verify social links
- Replace any placeholder portfolio content
- Connect the contact form if you want live submissions

## License

This project includes an MIT [`LICENSE`](./LICENSE).
