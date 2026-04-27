# GitHub Pages Setup Guide

## Step-by-Step Instructions

### 1. Update Configuration
Replace these placeholders in your files:

**In `package.json` (line 7):**
```json
"homepage": "https://YOUR-USERNAME.github.io/YOUR-REPO-NAME",
```

**In `vite.config.ts` (line 5):**
```typescript
base: process.env.GITHUB_PAGES ? '/YOUR-REPO-NAME/' : '/',
```

Replace:
- `YOUR-USERNAME` with your GitHub username
- `YOUR-REPO-NAME` with your repository name

---

### 2. Install Dependencies
```bash
npm install
```

This installs the `gh-pages` package and all other dependencies.

---

### 3. Deploy Your Site
```bash
npm run deploy
```

This command will:
1. Build your project with `npm run build`
2. Deploy the `dist` folder to the `gh-pages` branch
3. Push the `gh-pages` branch to your GitHub repository

---

### 4. Configure GitHub Repository Settings

1. Go to your repository on GitHub
2. Navigate to **Settings** → **Pages**
3. Under "Build and deployment":
   - **Source:** Select "Deploy from a branch"
   - **Branch:** Select `gh-pages`
   - **Folder:** Select `/ (root)`
4. Click "Save"

Your site will be live at: `https://YOUR-USERNAME.github.io/YOUR-REPO-NAME`

---

### 5. Automatic Deployment with GitHub Actions (Recommended)

The `.github/workflows/deploy.yml` file has been created for you. This automatically deploys whenever you push to the `main` branch.

**To enable:**
1. Push your code to the `main` branch
2. GitHub Actions will automatically build and deploy
3. Check the **Actions** tab in your repository to see deployment status

---

## Key Files Updated

| File | Change |
|------|--------|
| `vite.config.ts` | Added `base` path and build configuration for GitHub Pages |
| `package.json` | Added `homepage`, `gh-pages` dependency, and `deploy` script |
| `.gitignore` | Added `.gh-pages` folder |
| `.github/workflows/deploy.yml` | New GitHub Actions workflow for automatic deployment |

---

## Deployment Methods

### Method 1: Manual Deployment (Quick)
```bash
npm run deploy
```

### Method 2: Automatic Deployment (Recommended)
- Push to `main` branch
- GitHub Actions automatically builds and deploys
- No manual steps needed

---

## Troubleshooting

### 404 Errors on Site
**Problem:** Resources not loading after deployment
**Solution:**
- Verify `base` in `vite.config.ts` matches your repository name exactly
- Verify `homepage` in `package.json` is correct
- Run `npm run build && npm run preview` locally to test

### Deploy Command Fails
**Problem:** `npm run deploy` returns an error
**Solutions:**
- Ensure `npm install` completed successfully
- Check Git is configured: `git config --global user.email` and `git config --global user.name`
- Verify you have push access to the repository
- Check your GitHub token has appropriate permissions

### GitHub Actions Deployment Fails
**Problem:** Automatic deployment via Actions doesn't work
**Solutions:**
- Check the **Actions** tab for error logs
- Ensure the workflow file is in `.github/workflows/deploy.yml`
- Verify your default branch is `main` (not `master`)
- Check repository Settings → Actions → General → "Workflow permissions" is set to "Read and write permissions"

### Static Assets Not Loading
**Problem:** Images, fonts, or other assets return 404
**Solutions:**
- Use relative paths for assets: `./image.png` (not `/image.png`)
- If using the `public` folder, ensure assets are there
- Check that the `base` path in `vite.config.ts` is set correctly

### Site Shows Old Version
**Problem:** Changes don't appear after deployment
**Solutions:**
- Hard refresh your browser (Ctrl+Shift+R or Cmd+Shift+R)
- Clear browser cache
- Check that the build completed successfully
- Verify changes were pushed to the correct branch

---

## Additional Resources

- [Vite Deployment Guide](https://vitejs.dev/guide/static-deploy.html)
- [GitHub Pages Documentation](https://docs.github.com/en/pages)
- [gh-pages npm Package](https://www.npmjs.com/package/gh-pages)

---

## Next Steps

1. **Update the placeholders** in `package.json` and `vite.config.ts`
2. **Run** `npm install` to install dependencies
3. **Deploy** with `npm run deploy`
4. **Configure** GitHub Pages in your repository settings
5. **Visit** your live site at the URL provided

Good luck! 🚀
