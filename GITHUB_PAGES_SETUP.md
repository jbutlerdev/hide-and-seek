# GitHub Pages Deployment Guide

Follow these steps to deploy your Hide and Seek game to GitHub Pages.

## Prerequisites

- A GitHub account
- Git installed on your computer
- This project files

## Step-by-Step Instructions

### 1. Create a GitHub Repository

1. Go to [GitHub](https://github.com)
2. Click the "+" icon in the top right corner
3. Select "New repository"
4. Name it `hide-and-seek`
5. Choose visibility (public or private)
6. **Do NOT** initialize with README (we already have files)
7. Click "Create repository"

### 2. Push Your Code to GitHub

In your terminal, run these commands from the project directory:

```bash
# Initialize git repository (if not already done)
git init

# Add all files
git add .

# Create initial commit
git commit -m "Initial commit: Hide and Seek game"

# Add your GitHub repository as remote
git remote add origin https://github.com/YOUR_USERNAME/hide-and-seek.git

# Push to GitHub
git push -u origin main
```

**Note:** Replace `YOUR_USERNAME` with your actual GitHub username.

If you get an error about the branch name, try:
```bash
git branch -M main
git push -u origin main
```

### 3. Enable GitHub Pages

1. Go to your repository on GitHub
2. Click on "Settings" (top navigation)
3. In the left sidebar, click "Pages" (under "Code and automation")
4. Under "Build and deployment":
   - **Source**: Select "GitHub Actions" from the dropdown
5. That's it! The workflow is already configured in `.github/workflows/deploy.yml`

### 4. Deploy

The site will automatically deploy when you push to the `main` branch.

To trigger the first deployment:
```bash
# Make a small change or just push again
git commit --allow-empty -m "Trigger deployment"
git push
```

### 5. Check Deployment Status

1. Go to the "Actions" tab in your GitHub repository
2. You should see a workflow run called "Deploy to GitHub Pages"
3. Wait for it to complete (usually takes 30-60 seconds)
4. Once complete, your site will be live!

### 6. Access Your Game

Your game will be available at:
```
https://YOUR_USERNAME.github.io/hide-and-seek
```

Replace `YOUR_USERNAME` with your actual GitHub username.

## Troubleshooting

### Deployment Failed

- Check the "Actions" tab for error messages
- Ensure GitHub Pages is enabled in Settings > Pages
- Make sure the source is set to "GitHub Actions"

### Site Not Loading

- Wait a few minutes - first deployment can take up to 10 minutes
- Check if the workflow completed successfully in the Actions tab
- Verify the URL is correct: `https://YOUR_USERNAME.github.io/hide-and-seek`

### 404 Error

- Ensure `index.html` is in the root directory of your repository
- Check that the deployment workflow completed successfully
- Try accessing the URL in an incognito/private window (cache issues)

## Updating Your Game

To update the game after making changes:

```bash
# Make your changes to index.html

# Stage changes
git add .

# Commit changes
git commit -m "Description of your changes"

# Push to GitHub (triggers automatic deployment)
git push
```

The site will automatically redeploy with your changes!

## Custom Domain (Optional)

If you want to use a custom domain:

1. Go to Settings > Pages
2. Under "Custom domain", enter your domain
3. Follow GitHub's instructions to configure your DNS
4. Enable "Enforce HTTPS" once DNS is configured

## Need Help?

- [GitHub Pages Documentation](https://docs.github.com/en/pages)
- [GitHub Actions Documentation](https://docs.github.com/en/actions)
