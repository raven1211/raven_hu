# Deployment Guide for Raven HU Portfolio

This guide will help you deploy the portfolio website to Vercel.

## Prerequisites

- GitHub account
- Vercel account (free tier available)
- Git installed on your machine

## Step 1: Push to GitHub

### 1.1 Create GitHub Repository

1. Go to [GitHub](https://github.com) and sign in
2. Click the "+" icon in the top right corner
3. Select "New repository"
4. Name it `portfolio` or `raven-hu-portfolio`
5. Make it public (required for free Vercel deployment)
6. Don't initialize with README (we already have files)
7. Click "Create repository"

### 1.2 Push Local Code to GitHub

```bash
# Add all files to git
git add .

# Commit the changes
git commit -m "Initial commit: Portfolio website with Vercel deployment config"

# Add GitHub remote (replace YOUR_USERNAME with your GitHub username)
git remote add origin https://github.com/YOUR_USERNAME/portfolio.git

# Push to GitHub
git push -u origin main
```

## Step 2: Deploy to Vercel

### 2.1 Connect GitHub to Vercel

1. Go to [Vercel](https://vercel.com) and sign in
2. Click "New Project"
3. Import your GitHub repository
4. Select the `portfolio` repository
5. Click "Import"

### 2.2 Configure Deployment

Vercel will automatically detect the configuration from `vercel.json`. The default settings should work:

- **Framework Preset**: Other
- **Root Directory**: `./` (default)
- **Build Command**: `npm run build` (optional, not required for static site)
- **Output Directory**: `./` (default)
- **Install Command**: `npm install` (optional)

### 2.3 Deploy

1. Click "Deploy"
2. Wait for the deployment to complete (usually 1-2 minutes)
3. Your site will be available at a URL like: `https://portfolio-xxx.vercel.app`

## Step 3: Custom Domain (Optional)

### 3.1 Add Custom Domain

1. In your Vercel dashboard, go to your project
2. Click "Settings" tab
3. Click "Domains" in the sidebar
4. Add your custom domain (e.g., `yourname.com`)
5. Follow the DNS configuration instructions

### 3.2 Configure DNS

You'll need to add DNS records to your domain provider:

- **A Record**: `@` → `76.76.19.61`
- **CNAME Record**: `www` → `cname.vercel-dns.com`

## Step 4: Environment Variables (Optional)

If you need environment variables:

1. Go to your Vercel project settings
2. Click "Environment Variables"
3. Add any required variables
4. Redeploy the project

## Step 5: Automatic Deployments

Vercel automatically deploys when you push to your main branch:

```bash
# Make changes to your code
git add .
git commit -m "Update portfolio content"
git push origin main
```

The deployment will start automatically and be available in a few minutes.

## Troubleshooting

### Common Issues

1. **Build Fails**: Check the build logs in Vercel dashboard
2. **404 Errors**: Ensure `vercel.json` is configured correctly
3. **CSS/JS Not Loading**: Check file paths and MIME types
4. **Domain Not Working**: Verify DNS configuration

### Useful Commands

```bash
# Check git status
git status

# View commit history
git log --oneline

# Pull latest changes
git pull origin main

# Force push (use with caution)
git push -f origin main
```

## File Structure for Deployment

```
portfolio/
├── index.html          # Main page
├── styles.css          # Styles
├── script.js           # JavaScript
├── vercel.json         # Vercel configuration
├── package.json        # Node.js configuration
├── api/
│   └── index.js        # Vercel API route
├── .gitignore          # Git ignore rules
├── README.md           # Documentation
└── DEPLOYMENT.md       # This file
```

## Performance Optimization

The site is already optimized for Vercel:

- Static file serving for fast loading
- Proper caching headers
- Compressed assets
- CDN distribution
- HTTPS by default

## Support

If you encounter issues:

1. Check Vercel documentation: https://vercel.com/docs
2. Check build logs in Vercel dashboard
3. Verify GitHub repository is public
4. Ensure all files are committed and pushed

## Next Steps

After successful deployment:

1. Share your portfolio URL
2. Update your resume with the new link
3. Add analytics (Google Analytics, etc.)
4. Set up monitoring and alerts
5. Consider adding a contact form
6. Implement SEO optimizations

---

**Happy Deploying! 🚀**
