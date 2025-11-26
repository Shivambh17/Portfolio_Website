# Updated Steps - If You Selected "Initialize with README"

## Step 2: Push Your Code to GitHub (Updated)

Since you selected "Initialize with README", you need to pull first, then push:

**Open PowerShell in your portfolio folder:**

1. **Navigate to your portfolio folder:**
   ```powershell
   cd C:\Users\shiva\Desktop\portfolio
   ```

2. **Initialize Git:**
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

5. **Rename branch to main:**
   ```powershell
   git branch -M main
   ```

6. **Connect to GitHub (replace YOUR_USERNAME):**
   ```powershell
   git remote add origin https://github.com/YOUR_USERNAME/portfolio.git
   ```

7. **Pull the README first (this is the new step!):**
   ```powershell
   git pull origin main --allow-unrelated-histories
   ```
   This will merge the README.md from GitHub with your local files.

8. **Push to GitHub:**
   ```powershell
   git push -u origin main
   ```

**That's it!** Your files will be pushed along with the README.md file.

---

## Alternative: Delete README (Optional)

If you don't want the README.md file, you can delete it:

1. After pulling (step 7 above), delete the README:
   ```powershell
   git rm README.md
   git commit -m "Remove README"
   git push
   ```

But honestly, **keeping the README is fine** - it won't affect your website at all!

---

## Continue with Step 3

After pushing successfully, continue with **Step 3: Connect to Netlify** from the original guide.

