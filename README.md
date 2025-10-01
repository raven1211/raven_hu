# Ruiwen (Raven) HU - Portfolio Website

A minimalist portfolio website based on resume content, featuring a green and white theme with Notion-like design style.

## Features

- 🎨 Clean and modern design style
- 🟢 Green and white color theme
- 📱 Fully responsive design
- 🚀 Python Flask server
- ✨ Smooth animations
- 📋 Complete resume content display

## File Structure

```
Portofolio/
├── index.html          # Main HTML file
├── styles.css          # CSS styles
├── script.js          # JavaScript functionality
├── server.js          # Node.js server
├── package.json       # Node.js dependencies
├── README.md         # Documentation
└── Raven_Hu_Resume_CEIBS_EN.md  # Original resume file
```

## Installation and Running

### Option 1: Node.js Server (Recommended)

```bash
# Start the server
node server.js

# Or using npm
npm start
```

### Option 2: Python Simple Server

```bash
# Python 3
python3 -m http.server 3000

# Python 2
python -m SimpleHTTPServer 3000
```

### Option 3: Open Directly

Simply open `index.html` in your browser (some features may not work due to CORS restrictions).

### Access Website

Open browser and visit: http://localhost:3000

## Tech Stack

- **Frontend**: HTML5, CSS3, Vanilla JavaScript
- **Server**: Node.js HTTP Server (or Python SimpleHTTPServer)
- **Fonts**: Inter (Google Fonts)
- **Design**: Responsive design, mobile-friendly
- **Features**: Dark/Light theme, smooth animations, keyboard navigation

## Design Features

- **Color Theme**: Green (#48bb78) and white (#ffffff) with dark mode support
- **Card Design**: Notion-like card layout with shadow effects
- **Animations**: Hover animations, page load animations, and smooth scrolling
- **Responsive**: Supports desktop, tablet, and mobile devices
- **Interactive**: Theme toggle, back-to-top button, keyboard navigation
- **Performance**: Optimized loading with intersection observer

## Customization

You can customize the website by modifying these files:

- `index.html`: Modify content and structure
- `styles.css`: Modify styles, colors, and animations
- `script.js`: Modify JavaScript functionality and interactions
- `server.js`: Modify server configuration (if using Node.js)

## Deployment

This website can be easily deployed to various platforms:

- **Local Run**: Use `node server.js` or `npm start`
- **Heroku**: Add `Procfile` with `web: node server.js`
- **Vercel**: Add `vercel.json` configuration
- **GitHub Pages**: Use static file hosting
- **Netlify**: Drag and drop the folder
- **AWS S3**: Upload static files to S3 bucket

## License

© 2024 Ruiwen (Raven) HU. All rights reserved.
