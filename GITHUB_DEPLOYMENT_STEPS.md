# Step-by-Step: Deploy to Netlify via GitHub

## Prerequisites
- GitHub account (free) - [Sign up here](https://github.com/signup)
- Netlify account (free) - [Sign up here](https://app.netlify.com/signup)
- Git installed on your computer (download from [git-scm.com](https://git-scm.com/downloads))

---

## Step 1: Create GitHub Repository

1. **Go to GitHub:**
   - Visit [https://github.com](https://github.com)
   - Sign in or create an account

2. **Create a new repository:**
   - Click the **"+"** icon in the top right → **"New repository"**
   - Repository name: `portfolio` (or any name you like)
   - Description: "WealthArena Portfolio Website" (optional)
   - Choose **Public** (free) or Private
   - **DO NOT** check "Initialize with README" (we'll push existing files)
   - Click **"Create repository"**

3. **Copy the repository URL:**
   - After creating, GitHub will show you a page with commands
   - Copy the HTTPS URL (looks like: `https://github.com/YOUR_USERNAME/portfolio.git`)
   - You'll need this in Step 2

---

## Step 2: Push Your Code to GitHub

**Open PowerShell or Command Prompt in your portfolio folder:**

1. **Navigate to your portfolio folder:**
   ```powershell
   cd C:\Users\shiva\Desktop\portfolio
   ```

2. **Initialize Git (if not already done):**
   ```powershell
   git init
   ```

3. **Add all files:**
   ```powershell
   git add .
   ```

4. **Create your first commit:**
   ```powershell
   git commit -m "Initial commit - WealthArena portfolio"
   ```

5. **Rename branch to main (if needed):**
   ```powershell
   git branch -M main
   ```

6. **Connect to GitHub (replace YOUR_USERNAME with your GitHub username):**
   ```powershell
   git remote add origin https://github.com/YOUR_USERNAME/portfolio.git
   ```
   Example: `git remote add origin https://github.com/shiva/portfolio.git`

7. **Push to GitHub:**
   ```powershell
   git push -u origin main
   ```

8. **Enter credentials:**
   - Username: Your GitHub username
   - Password: Use a **Personal Access Token** (see note below)

**Note:** GitHub no longer accepts passwords. You need a Personal Access Token:
- Go to GitHub → Settings → Developer settings → Personal access tokens → Tokens (classic)
- Click "Generate new token (classic)"
- Name it "Netlify Deployment"
- Check "repo" scope
- Generate and copy the token (use this as your password)

---

## Step 3: Connect GitHub to Netlify

1. **Go to Netlify:**
   - Visit [https://app.netlify.com](https://app.netlify.com)
   - Sign in or create an account (free)

2. **Import your project:**
   - Click **"Add new site"** button
   - Select **"Import an existing project"**

3. **Authorize GitHub:**
   - Click **"GitHub"** or **"Deploy with GitHub"**
   - You'll be asked to authorize Netlify
   - Click **"Authorize Netlify"**
   - You may need to enter your GitHub password/token again

4. **Select your repository:**
   - You'll see a list of your GitHub repositories
   - Find and click on **"portfolio"** (or whatever you named it)

5. **Configure build settings:**
   - **Branch to deploy:** `main` (should be auto-selected)
   - **Build command:** Leave **EMPTY** (this is a static site, no build needed)
   - **Publish directory:** `/` or leave as is (root directory)
   - Click **"Deploy site"**

---

## Step 4: Wait for Deployment

1. **Watch the deployment:**
   - You'll see a deployment log
   - Wait 30-60 seconds for it to complete
   - Status will change from "Building" to "Published"

2. **Your site is live!**
   - You'll get a URL like: `https://random-name-123.netlify.app`
   - Click the URL to see your live site
   - You can change the site name in Site settings → General → Site details

---

## Step 5: Making Updates (The Easy Part!)

**Now whenever you make changes:**

1. **Make your changes** to `index.html`, `styles.css`, or `script.js`

2. **Open PowerShell in your portfolio folder:**
   ```powershell
   cd C:\Users\shiva\Desktop\portfolio
   ```

3. **Push changes to GitHub:**
   ```powershell
   git add .
   git commit -m "Updated website"
   git push
   ```

4. **Netlify automatically deploys!**
   - Go to your Netlify dashboard
   - You'll see a new deployment starting automatically
   - Wait 30-60 seconds
   - Your site is updated! ✨

---

## Troubleshooting

### "Repository not found" error:
- Check that you copied the correct repository URL
- Make sure the repository name matches exactly

### "Authentication failed" error:
- Use a Personal Access Token instead of password
- See Step 2, Note section above

### "Build failed" error:
- Make sure Build command is **EMPTY**
- Publish directory should be `/` or root

### Images not showing:
- Check that image paths in HTML match actual file names
- Make sure `images/` folder is included in your git push

### Changes not appearing:
- Wait 1-2 minutes for deployment to complete
- Hard refresh your browser (Ctrl+F5)
- Check Netlify dashboard for deployment status

---

## Quick Reference Commands

```powershell
# Navigate to folder
cd C:\Users\shiva\Desktop\portfolio

# Check status
git status

# Add all changes
git add .

# Commit changes
git commit -m "Your commit message"

# Push to GitHub (triggers Netlify auto-deploy)
git push
```

---

## What Happens Next?

✅ Your site is live on Netlify  
✅ Every `git push` automatically updates your site  
✅ You get free HTTPS (secure connection)  
✅ You can add a custom domain later (free)  
✅ All changes are tracked in GitHub  

**You're all set!** 🎉

