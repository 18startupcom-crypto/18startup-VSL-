# 📚 GitHub + Vercel Deployment Guide

## Step 1️⃣: Set Up GitHub Repository

### A. Create GitHub Repository

1. Go to [github.com](https://github.com) and sign in
2. Click **+** → **New repository**
3. Name it: `18startup-index`
4. Description: `18startup Idea Validation Course`
5. Choose **Public** (or Private)
6. Click **Create repository**

### B. Push Code to GitHub

From your terminal:

```bash
cd /path/to/18startup-index

# Initialize git
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"

git init
git add .
git commit -m "Initial commit: 18startup course platform"
git branch -M main
git remote add origin https://github.com/YOUR-USERNAME/18startup-index.git
git push -u origin main
```

✅ Your code is now on GitHub!

---

## Step 2️⃣: Deploy to Vercel

### Option A: Auto-Deploy from GitHub (Easiest)

1. Go to [vercel.com](https://vercel.com)
2. Click **"Sign Up"** → Choose **"Continue with GitHub"**
3. Authorize Vercel to access your GitHub
4. You'll be redirected to Vercel dashboard
5. Click **"New Project"**
6. Find and select `18startup-index` repository
7. Leave settings as default
8. Click **"Deploy"**
9. Wait ~30 seconds...
10. ✅ Your site is live! (You'll get a `.vercel.app` URL)

### Option B: Deploy via Vercel CLI

```bash
# Install Vercel CLI
npm install -g vercel

# Deploy
cd /path/to/18startup-index
vercel

# Follow the prompts and you're done!
```

---

## Step 3️⃣: Configure Environment Variables (Optional)

If using Anthropic API:

1. In Vercel dashboard, go to **Settings → Environment Variables**
2. Add variable:
   - **Name:** `ANTHROPIC_API_KEY`
   - **Value:** `sk-your-actual-key-here`
3. Click **Save**
4. Redeploy: Click **Deployments → Select Latest → Redeploy**

---

## Step 4️⃣: Set Up Custom Domain (Optional)

If you want `course.18startup.com` instead of `xyz.vercel.app`:

1. In Vercel dashboard, go to **Settings → Domains**
2. Enter your domain: `course.18startup.com`
3. Follow DNS setup instructions
4. Wait 24–48 hours for DNS to propagate

---

## Step 5️⃣: Test Your Deployment

1. Click the Vercel URL from the dashboard
2. Try these:
   - ✅ Load the page
   - ✅ Fill out founder form
   - ✅ Take a lesson
   - ✅ Submit feedback
   - ✅ Check browser console (F12) for errors

---

## 🔄 Making Updates

From now on, updates are **automatic**:

```bash
# Make changes to index.html or other files
# Commit and push to GitHub
git add .
git commit -m "Update course content"
git push

# Vercel automatically redeploys within 30 seconds!
```

No manual Vercel deploys needed.

---

## 📊 Monitor Your Deployment

In Vercel dashboard:
- **Deployments** tab → see all deploys + rollback
- **Analytics** tab → view traffic, performance
- **Settings** → configure domains, env vars, git integrations

---

## 🆘 Troubleshooting

### "Can't push to GitHub — authentication failed"

Use GitHub token instead of password:

```bash
# When prompted for password, use GitHub Personal Access Token
# Create one at: github.com/settings/tokens
```

### "Vercel deployment says 'Build Failed'"

Check build logs:
1. Vercel dashboard → Deployments
2. Click the failed deployment
3. See logs and error messages
4. Fix the issue and push again

### "Site shows blank page"

1. Open browser DevTools (F12)
2. Check Console for errors
3. Check Network tab for failed requests
4. Verify all assets loaded correctly

### "Anthropic API errors"

- Get API key: [console.anthropic.com](https://console.anthropic.com)
- Verify key starts with `sk-`
- Check that key is set in environment variables
- Ensure account has credits

---

## 📈 Next Steps

Once deployed:

1. ✅ Share the Vercel URL with founders
2. ✅ Monitor analytics in Vercel dashboard
3. ✅ Update course content as needed (just push to GitHub)
4. ✅ Track student responses in Google Sheets (if connected)
5. ✅ Iterate based on feedback

---

## 🎯 Useful Links

- **Vercel Docs:** https://vercel.com/docs
- **GitHub Docs:** https://docs.github.com
- **Anthropic API:** https://console.anthropic.com
- **18startup:** https://18startup.com

---

**You're all set! 🚀**

Your course is now live and updates automatically. Happy deploying!
