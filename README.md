Novo Enviro Corporate Website

A clean, modern, and brand-consistent corporate website for Novo Enviro. This platform serves as the digital storefront for the company's project development services, specializing in high-integrity carbon reduction, carbon removal projects, and expert consultancy for internationally certified plastic credits.

🚀 Key Features

Modern UI/UX: A professional, minimalistic design utilizing the official Novo Enviro branding and typography.

Fully Responsive: Optimized for desktop, tablet, and mobile devices using Tailwind CSS fluid scaling and flexbox/grid layouts.

Dynamic Routing: Built with Nuxt 3's file-based routing system for fast, seamless navigation.

Optimized Assets: Uses cropped SVG logos and WebP/optimized imagery for fast loading times.

Interactive Navigation: Mobile-friendly hamburger menu and sticky transparent-to-solid desktop navigation.

🛠️ Tech Stack

Framework: Nuxt 3 (Vue.js)

Styling: Tailwind CSS

Icons: Nuxt Icon (Phosphor Icons pack)

Typography: EB Garamond (Headings) & Lexend (Body) via Google Fonts

Hosting/Deployment: Cloudflare Pages

📂 Project Structure

novo enviro company page/
├── assets/         # Uncompiled assets (CSS, SCSS, etc.)
├── components/     # Reusable Vue components 
├── layouts/        # Shared layouts (e.g., default.vue with Header/Footer)
├── pages/          # Application routes (index, careers, contact, etc.)
├── public/         # Static assets served at the root (logos, mockups, favicon)
├── nuxt.config.ts  # Nuxt framework configuration
└── package.json    # Project metadata and dependencies


💻 Local Development

To get this project running on your local machine, ensure you have Node.js installed.

Install the dependencies:

npm install


Start the development server:

npm run dev


The site will be available locally at http://localhost:3000

☁️ Production & Deployment

This project is configured to be statically generated and deployed seamlessly to Cloudflare Pages.

Local Build Testing

To build the application locally and verify the production output:

npm run generate


This command pre-renders all routes and generates a static version of the site in the .output/public directory.

Cloudflare Pages Setup

When connecting this GitHub repository to Cloudflare Pages, use the following build settings to ensure a successful deployment:

Framework preset: Nuxt.js

Build command: npm run generate

Build output directory: .output/public

📞 Support & Contact

For inquiries regarding the website or Novo Enviro services, please reach out to:

Email: info@novoenviro.com

LinkedIn: Novo Enviro