# 18startup — Idea Validation Course

Interactive learning platform for startup founders to validate ideas, analyze business models, and get AI-powered feedback.

**Live Demo:** [your-vercel-domain.vercel.app](https://your-vercel-domain.vercel.app)

---

## 📋 Features

✅ Interactive multi-lesson course  
✅ AI-powered analysis (Claude API integration)  
✅ Real-time feedback system  
✅ Admin dashboard for course editing  
✅ Student progress tracking  
✅ PDF export with feedback form  
✅ Google Sheets integration  

---

## 🚀 Quick Start

### Local Development

```bash
# Clone the repository
git clone https://github.com/YOUR-USERNAME/18startup-index.git
cd 18startup-index

# Run local server
python3 -m http.server 3000

# Open in browser
open http://localhost:3000
```

### Deploy to Vercel

#### Option 1: Connect GitHub + Vercel (Recommended)

1. **Push to GitHub**
   ```bash
   git init
   git add .
   git commit -m "Initial commit"
   git branch -M main
   git remote add origin https://github.com/YOUR-USERNAME/18startup-index.git
   git push -u origin main
   ```

2. **Connect to Vercel**
   - Go to [vercel.com](https://vercel.com)
   - Sign in with GitHub
   - Click **"New Project"**
   - Select `18startup-index` repository
   - Click **Deploy** (no build config needed)
   - Your site is live! 🎉

#### Option 2: Deploy Directly to Vercel

1. Install Vercel CLI:
   ```bash
   npm install -g vercel
   ```

2. Deploy:
   ```bash
   vercel
   ```

3. Follow prompts and your site will be live immediately.

---

## 📁 Project Structure

```
18startup-index/
├── index.html           # Main application (all-in-one HTML)
├── package.json         # Project metadata
├── vercel.json          # Vercel deployment config
├── .gitignore           # Git ignore rules
└── README.md            # This file
```

---

## ⚙️ Configuration

### Environment Variables (if using Apps Script backend)

Create a `.env.local` file (not tracked in git):

```env
ANTHROPIC_API_KEY=sk-your-api-key-here
APPS_SCRIPT_URL=https://script.google.com/your-web-app-url
```

> **Note:** The Anthropic API key can also be entered in the UI at runtime.

### Google Apps Script Integration (Optional)

If you're using the admin dashboard with Google Sheets sync:

1. Deploy `index.html` as a Google Apps Script web app
2. Set the Apps Script deployment URL in the HTML (line ~1190)
3. Update `google.script.run.callAnthropicAPI()` handlers in Apps Script

---

## 🔧 Customization

### Update Course Content

Edit the course data in the `index.html` file. Search for:
- `LESSONS` array - add/edit lessons
- `ASSESSMENTS` array - add/edit assessments
- `VIDEO_BLOCKS` - add/edit videos

### Change Brand Colors

Update CSS variables in `<style>` section:
```css
:root {
  --orange: #F37335;    /* Primary color */
  --yellow: #FFF392;    /* Secondary color */
  --dark: #1A1A1A;      /* Text color */
}
```

### Custom Domain on Vercel

1. In Vercel dashboard, go to **Settings → Domains**
2. Add your custom domain
3. Update DNS records as directed

---

## 📊 Analytics & Tracking

Student responses are saved to:
- **Browser localStorage** (local backup)
- **Google Sheets** (if connected via Apps Script)

---

## 🤖 AI Integration

This course uses **Anthropic's Claude API** for AI analysis:

- **Model:** Claude Sonnet 4.6
- **Free tier:** First 3 months included (then pay-as-you-go)
- **Get API key:** [console.anthropic.com](https://console.anthropic.com)

---

## 🐛 Troubleshooting

### "Google Apps Script not available" error
- Running locally? This is normal. The site works fine in standalone mode.
- Deploy to Vercel to use non-Apps Script features.

### Feedback form not submitting
- Check browser console (F12) for errors
- Verify Anthropic API key is set
- Check network tab to see if requests are failing

### Admin panel not opening
- Click the gear icon (⚙) in the sidebar
- Or press `Ctrl+Shift+A` (keyboard shortcut)

---

## 📈 Deployment Checklist

- [ ] Update course content (lessons, assessments, videos)
- [ ] Test locally (`python3 -m http.server 3000`)
- [ ] Update Anthropic API key (environment or in-app)
- [ ] Push to GitHub
- [ ] Deploy to Vercel (auto-deploys on GitHub push)
- [ ] Test live on Vercel domain
- [ ] Add custom domain (optional)
- [ ] Share with founders! 🚀

---

## 📞 Support

- **18startup:** [18startup.com](https://18startup.com)
- **GitHub Issues:** [Report bugs](https://github.com/YOUR-USERNAME/18startup-index/issues)
- **Vercel Support:** [vercel.com/help](https://vercel.com/help)

---

## 📄 License

MIT © 2026 18startup. All rights reserved.

---

## 🤝 Contributing

Found a bug? Have an idea? Open an issue or submit a PR!

```bash
git checkout -b feature/your-feature
git commit -m "Add your feature"
git push origin feature/your-feature
```

Then open a Pull Request on GitHub.

---

**Last Updated:** January 2026  
**Version:** 1.0.0
