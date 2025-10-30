# Brooklyn Tech Environmental Justice X Sunrise

Landing page for the Brooklyn Tech Environmental Justice X Sunrise club. Built with Astro and Tailwind CSS, optimized for deployment on Cloudflare Pages.

## Features

- Modern, responsive design with Tailwind CSS
- Executive board member showcase with bios and photos
- Auto-playing image carousel highlighting club activities
- Optimized for performance with Astro's static site generation
- Ready for deployment to Cloudflare Pages

## Project Structure

```
/
├── public/
│   └── images/
│       ├── execs/          # Executive board member photos
│       └── carousel/       # Carousel images
├── src/
│   ├── components/
│   │   ├── ExecCard.astro  # Executive card component
│   │   └── ImageCarousel.astro  # Image carousel component
│   ├── data/
│   │   └── execs.json      # Executive board data
│   ├── pages/
│   │   └── index.astro     # Main landing page
│   └── styles/
│       └── global.css      # Global Tailwind CSS
└── astro.config.mjs        # Astro configuration
```

## Getting Started

### Prerequisites

- Node.js 18+ and npm

### Installation

1. Clone the repository (or download the files)

2. Install dependencies:
```sh
npm install
```

3. Start the development server:
```sh
npm run dev
```

The site will be available at `http://localhost:4321`

## Customization

### Update Executive Board Members

Edit `src/data/execs.json` with your actual executive board information:

```json
[
  {
    "id": 1,
    "name": "Your Name",
    "role": "Your Role",
    "bio": "Your bio here...",
    "image": "/images/execs/your-photo.jpg"
  }
]
```

Add corresponding photos to `public/images/execs/`

### Update Carousel Images

1. Add your images to `public/images/carousel/`
2. Update the `carouselImages` array in `src/pages/index.astro`:

```js
const carouselImages = [
  { src: '/images/carousel/your-image-1.jpg', alt: 'Description' },
  { src: '/images/carousel/your-image-2.jpg', alt: 'Description' },
];
```

### Update Contact Information

In `src/pages/index.astro`, update the email link in the "Get Involved" section:

```html
<a href="mailto:your-email@example.com">Contact Us</a>
```

## Building for Production

Build the site for production:

```sh
npm run build
```

Preview the production build locally:

```sh
npm run preview
```

## Deploying to Cloudflare Pages

### Option 1: Git Integration (Recommended)

1. Push your code to GitHub, GitLab, or Bitbucket

2. Log in to [Cloudflare Dashboard](https://dash.cloudflare.com/)

3. Go to **Pages** > **Create a project** > **Connect to Git**

4. Select your repository

5. Configure build settings:
   - **Framework preset:** Astro
   - **Build command:** `npm run build`
   - **Build output directory:** `dist`

6. Click **Save and Deploy**

Your site will be automatically deployed and updated on every push to your repository!

### Option 2: Direct Upload

1. Build the site:
```sh
npm run build
```

2. Install Wrangler CLI:
```sh
npm install -g wrangler
```

3. Deploy to Cloudflare Pages:
```sh
wrangler pages deploy dist
```

4. Follow the prompts to authenticate and deploy

## Commands Reference

| Command | Action |
| :------ | :------ |
| `npm install` | Install dependencies |
| `npm run dev` | Start dev server at `localhost:4321` |
| `npm run build` | Build production site to `./dist/` |
| `npm run preview` | Preview production build locally |
| `npm run astro ...` | Run Astro CLI commands |

## Technologies Used

- [Astro](https://astro.build/) - Static site generator
- [Tailwind CSS](https://tailwindcss.com/) - Utility-first CSS framework
- [Cloudflare Pages](https://pages.cloudflare.com/) - Hosting platform

## License

This project is open source and available for use by the Brooklyn Tech Environmental Justice X Sunrise club.
