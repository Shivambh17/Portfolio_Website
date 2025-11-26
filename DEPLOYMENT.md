# Deployment Guide for WealthArena Portfolio

## 🚀 Quick Answer: Auto-Updates

**Will updates be automatic?**
- ❌ **Drag & Drop method:** No - you need to manually drag and drop again
- ✅ **Git Integration method:** Yes! Every time you `git push`, Netlify automatically deploys your changes

**Recommendation:** Use Git Integration for automatic updates!

---

## Deploy to Netlify (Free)

### Option 1: Drag and Drop (Quickest)

⚠️ **Note:** With drag-and-drop, updates are NOT automatic. You'll need to drag and drop again for each update.

1. **Prepare your files:**
   - Make sure all files are in the `portfolio` folder:
     - `index.html`
     - `styles.css`
     - `script.js`
     - `images/` folder

2. **Deploy:**
   - Go to [https://app.netlify.com](https://app.netlify.com)
   - Sign up or log in (free account)
   - Drag and drop your entire `portfolio` folder onto the Netlify dashboard
   - Wait a few seconds for deployment
   - Your site will be live with a URL like: `https://random-name-123.netlify.app`

3. **To Update Later:**
   - Make your changes locally
   - Drag and drop the updated folder again to Netlify
   - Site will redeploy automatically

4. **Custom Domain (Optional):**
   - Go to Site settings → Domain management
   - Add your custom domain

### Option 2: Git Integration (Recommended)

1. **Push to GitHub:**
   ```bash
   git init
   git add .
   git commit -m "Initial commit"
   git branch -M main
   git remote add origin https://github.com/YOUR_USERNAME/portfolio.git
   git push -u origin main
   ```

2. **Connect to Netlify:**
   - Go to [https://app.netlify.com](https://app.netlify.com)
   - Click "Add new site" → "Import an existing project"
   - Choose GitHub and authorize Netlify
   - Select your repository
   - Netlify will auto-detect settings (no build command needed for static sites)
   - Click "Deploy site"

3. **Auto-deployment (This is the magic!):**
   - ✅ **Every time you push to GitHub, Netlify will automatically redeploy your site**
   - Workflow: Make changes → `git push` → Netlify auto-deploys → Site updates live
   - You'll get email notifications when deployment completes
   - Takes about 30-60 seconds per update

### Netlify Settings for This Project

- **Build command:** (Leave empty - static site)
- **Publish directory:** `/` (root)
- **Node version:** (Not needed for static sites)

### Important Notes

- ✅ **Free tier includes:**
  - 100 GB bandwidth/month
  - 300 build minutes/month
  - HTTPS automatically enabled
  - Custom domain support

- 📁 **File structure:**
  ```
  portfolio/
  ├── index.html
  ├── styles.css
  ├── script.js
  └── images/
      ├── shivam.jpg
      ├── harhsajpg.jpg
      ├── Kanika.jpg
      ├── Clifford.jpg
      ├── Neha.jpg
      └── Amruth.jpg
  ```

### Troubleshooting

- If images don't load: Check that image paths in `index.html` match the actual file names
- If styles don't apply: Ensure `styles.css` is in the same directory as `index.html`
- If JavaScript doesn't work: Check browser console for errors

### Alternative: GitHub Pages (Also Free)

You can also deploy to GitHub Pages:

1. Push your code to GitHub
2. Go to repository Settings → Pages
3. Select branch (usually `main`) and folder (`/root`)
4. Your site will be at: `https://YOUR_USERNAME.github.io/portfolio`

---

**Netlify is recommended** because it's faster, has better CDN, and easier custom domain setup.

