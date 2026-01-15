# GitHub Pages Deployment Guide

## Quick Start

Your website is ready to be hosted on GitHub Pages! Here's how to set it up:

### Step 1: Push Your Changes to GitHub

First, make sure all files are committed and pushed to your GitHub repository:

```bash
git add .
git commit -m "Add Program Development Cycle interactive website"
git push origin main
```

### Step 2: Enable GitHub Pages

1. Go to your repository on GitHub: `https://github.com/BrickPiGuy/program-development-cycle`
2. Click **Settings** (gear icon in the top right)
3. Scroll down to the **Pages** section (on the left sidebar)

#### Choose Your Deployment Method

**Option A: Deploy from Branch (Recommended for this project) ✅**
- Simplest approach for static HTML/CSS/JS sites
- No build process needed
- Deploys directly from your main branch
- Automatic updates on every push

Steps:
1. Under "Source", select:
   - **Deploy from a branch**
2. Select:
   - **Branch**: `main`
   - **Folder**: `/ (root)`
3. Click **Save**

**Option B: GitHub Actions (Advanced)**
- Better for sites requiring builds, minification, or tests
- More control over deployment pipeline
- Slower deployment (runs workflow before publishing)
- Unnecessary for this project

For this static website, **Option A (Deploy from Branch)** is faster and simpler.

### Step 3: Access Your Website

Your website will be available at:

```
https://BrickPiGuy.github.io/program-development-cycle/
```

GitHub will automatically build and deploy your site. You should see a green checkmark within a minute or two.

## What Happens Next

- GitHub Pages automatically detects that this is a static HTML/CSS/JS site
- The `.nojekyll` file tells GitHub Pages not to process the site with Jekyll (since we don't need it)
- Your site is now live and publicly accessible
- Any changes you push to the main branch will automatically update the live site

## Custom Domain (Optional)

If you want to use a custom domain like `www.yoursite.com`:

1. In the **Pages** settings, scroll to "Custom domain"
2. Enter your domain name
3. Follow the DNS configuration instructions from your domain registrar
4. GitHub will handle the SSL certificate automatically

## Troubleshooting

### Site not appearing?
- Wait 1-2 minutes for GitHub to build and deploy
- Check the **Actions** tab to see the deployment status
- Look for any error messages in the deployment logs

### 404 error?
- Make sure `index.html` is in the root directory
- Clear your browser cache (Ctrl+Shift+Delete or Cmd+Shift+Delete)
- Verify the URL is: `https://BrickPiGuy.github.io/program-development-cycle/`

### Site looks broken?
- Check that all file paths in HTML are relative (e.g., `styles.css` not `/styles.css`)
- All files are relative, so this should work fine

## Keeping Your Site Updated

Any time you make changes:

```bash
git add .
git commit -m "Update content or fix bugs"
git push origin main
```

Your site will automatically update within a minute or two!

## Files Included

- `index.html` - Main website
- `styles.css` - Styling
- `script.js` - Interactive features
- `README.md` - Documentation
- `.nojekyll` - Tells GitHub Pages this isn't a Jekyll site
- `GITHUB_PAGES_SETUP.md` - This file

## Performance & Security

✅ **Free SSL/TLS Certificate** - GitHub Pages provides HTTPS automatically
✅ **Fast CDN** - Content delivered from GitHub's global network
✅ **No Server Costs** - Completely free hosting
✅ **Version Control** - Full Git history available
✅ **Automatic Backups** - Protected by GitHub's infrastructure

## Need Help?

- [GitHub Pages Documentation](https://docs.github.com/en/pages)
- [GitHub Pages Troubleshooting](https://docs.github.com/en/pages/getting-started-with-github-pages/troubleshooting-publication-of-your-site-with-github-pages)

---

Your Program Development Cycle website is ready for the world! 🚀
