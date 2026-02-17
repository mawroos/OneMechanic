# GitHub Pages Deployment Guide

This repository is configured to deploy automatically to GitHub Pages.

## Automatic Deployment

The website will automatically deploy when changes are pushed to the `main` branch.

## Manual Setup (First Time)

To enable GitHub Pages for this repository, follow these steps:

1. **Navigate to Repository Settings**
   - Go to your GitHub repository
   - Click on **Settings** tab

2. **Configure GitHub Pages**
   - In the left sidebar, click on **Pages** under "Code and automation"
   - Under "Build and deployment":
     - **Source**: Select "GitHub Actions"
   - Click **Save**

3. **Merge this PR to main**
   - Once this PR is merged to the main branch, the deployment workflow will run automatically

4. **Access Your Website**
   - After deployment completes (usually 1-2 minutes), your site will be available at:
   - `https://mawroos.github.io/OneMechanic/`

## Workflow File

The deployment is handled by `.github/workflows/deploy.yml` which:
- Triggers on pushes to the `main` branch
- Can also be triggered manually from the Actions tab
- Deploys all files from the repository to GitHub Pages

## Local Testing

To test the website locally before deploying:

```bash
# Navigate to the repository
cd OneMechanic

# Start a simple HTTP server
python3 -m http.server 8000

# Open in your browser
# Visit: http://localhost:8000
```

## Customization

After deployment, you can customize the website by:

1. Updating text and content in `index.html`
2. Replacing placeholder images in the `img/` folder
3. Modifying colors and styles in `css/style.css`
4. Adjusting behavior in `js/main.js`

All changes pushed to `main` will automatically redeploy the site.

## Troubleshooting

If deployment fails:
- Check the **Actions** tab in your repository for error messages
- Ensure GitHub Pages is enabled in repository settings
- Verify that the workflow file is present in `.github/workflows/deploy.yml`
- Make sure repository is public (or you have GitHub Pro/Enterprise for private repos)
