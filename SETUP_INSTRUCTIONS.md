# Setup & Deployment Instructions

## For IT Administrators & Educators

---

## 🚀 Local Testing (Development Machine)

### Windows
```powershell
# Navigate to the folder
cd C:\path\to\olds-theory-open-source-exotic-energy-conduit

# Start Python HTTP server
python -m http.server 8000

# Open browser to:
http://localhost:8000/exotic-energy-framework.html
```

### macOS / Linux
```bash
# Navigate to the folder
cd /path/to/olds-theory-open-source-exotic-energy-conduit

# Start Python HTTP server (Python 3)
python3 -m http.server 8000

# Start Python HTTP server (Python 2)
python -m SimpleHTTPServer 8000

# Open browser to:
http://localhost:8000/exotic-energy-framework.html
```

---

## 🌐 Deploy to Static Hosting

### Option 1: GitHub Pages (Free, Easy)

```bash
# Clone your repo
git clone https://github.com/mars-city-dev/olds-theory-open-source-exotic-energy-conduit.git
cd olds-theory-open-source-exotic-energy-conduit

# Make sure you have the files in root or /docs folder
# Then push to GitHub

# Enable GitHub Pages in repository settings:
# Settings → Pages → Source: main branch → /root (or /docs)

# Access at: https://mars-city-dev.github.io/olds-theory-open-source-exotic-energy-conduit/
```

### Option 2: Netlify (Recommended for Educators)

```bash
# Create Netlify account at netlify.com
# Connect your GitHub repo
# Deploy settings:
# - Base directory: (leave blank)
# - Build command: (leave blank)
# - Publish directory: . (root)

# Get instant HTTPS, analytics, and share link
```

### Option 3: Vercel

```bash
# Install Vercel CLI
npm install -g vercel

# Deploy
vercel

# Follow prompts - select current directory as project root
```

### Option 4: Any Static Web Server

```bash
# Upload entire folder to your server via FTP/SSH
# Ensure web server serves .html files
# Point domain to the folder
```

---

## 🏫 Classroom LMS Integration

### Canvas LMS
1. Go to Courses → Course Content
2. Add → External Tool
3. Name: "Exotic Energy Framework"
4. URL: `https://your-hosted-url/exotic-energy-framework.html`
5. Save

### Blackboard
1. Course Management → Content
2. Build Content → Web Link
3. Name: "Exotic Energy Framework"
4. URL: `https://your-hosted-url/exotic-energy-framework.html`
5. Submit

### Moodle
1. Turn editing on
2. Add activity/resource → External tool
3. Name: "Exotic Energy Framework"
4. URL: `https://your-hosted-url/exotic-energy-framework.html`
5. Save

### Embed in Iframe
```html
<!-- Add to any webpage -->
<iframe src="https://your-hosted-url/exotic-energy-framework.html" 
        width="100%" 
        height="1200px" 
        style="border: none;"></iframe>
```

---

## 🔒 Security Considerations

### This Package is Safe to Deploy Anywhere Because:
✅ No backend server required  
✅ No database connections  
✅ No user authentication needed  
✅ No data collection  
✅ No API calls to external services  
✅ All libraries loaded from public CDNs  

### Best Practices:
1. Deploy to HTTPS (required for most school networks)
2. No need for special firewall rules
3. Works in school networks with restrictions
4. Can be served from any static host
5. Safe to use in air-gapped networks (after initial load)

---

## 📱 Browser Compatibility

| Browser | Version | Support |
|---------|---------|---------|
| Chrome  | 90+     | ✅ Full |
| Firefox | 88+     | ✅ Full |
| Safari  | 14+     | ✅ Full |
| Edge    | 90+     | ✅ Full |
| IE 11   | -       | ❌ No  |

### Requirements:
- JavaScript enabled
- WebGL support (for 3D visualizations)
- 50MB+ available RAM
- 15Mbps+ internet (for CDN loading)

---

## 📊 File Size & Performance

### Package Size
- Total HTML files: ~2MB
- External libraries (CDN): ~5MB
- Typical first load: 30-60 seconds
- Subsequent loads: Cached (instant)

### Performance Tips
1. **For schools:** Cache the CDN libraries in your proxy
2. **For museums:** Host on CDN for global distribution
3. **For remote:** Works on laptop, tablet, even smartphones
4. **Offline:** Download HTML files once, can work offline after that

---

## 🔧 Customization

### Changing Colors
All files use Tailwind CSS utility classes. Easy to customize:

```html
<!-- Change the accent color from purple to your school colors -->
<!-- Find: text-purple-400 or from-purple-600 -->
<!-- Replace with: text-blue-400 or from-blue-600 -->
```

### Adding Your Logo
```html
<!-- In exotic-energy-framework.html, find the header -->
<!-- Replace the zap icon with your institution logo -->
<img src="your-logo.png" style="width: 40px; height: 40px;">
```

### Translating to Other Languages
1. Duplicate HTML files
2. Replace text strings (keep HTML structure)
3. Create language switcher in navigation
4. Deploy translations alongside English version

---

## 📞 Troubleshooting

### "Page doesn't load"
- Check browser console (F12)
- Ensure JavaScript is enabled
- Clear browser cache
- Try different browser
- Check internet connection (CDN access)

### "Simulations are slow"
- Close other browser tabs
- Reduce browser zoom (100%)
- Check GPU acceleration enabled
- Try Chrome instead of Firefox
- Upgrade graphics drivers

### "Charts don't display"
- Enable JavaScript
- Check ad blocker (might block Chart.js)
- Clear browser cache
- Update browser to latest version

### "Can't reach the page"
- Check hosting is active
- Verify DNS points to server
- Check firewall allows port 80/443
- Try accessing from different network
- Contact your ISP/hosting provider

---

## 📈 Monitoring & Analytics (Optional)

### Add Google Analytics
```html
<!-- In <head> of exotic-energy-framework.html -->
<script async src="https://www.googletagmanager.com/gtag/js?id=GA_MEASUREMENT_ID"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'GA_MEASUREMENT_ID');
</script>
```

### Track Engagement
- Which tools get used most?
- How long do students spend?
- Which pages need improvement?
- What's working for your audience?

---

## 🔄 Version Control & Updates

### Keep Your Installation Updated
```bash
# Check for updates
git fetch origin

# Update to latest
git pull origin main

# Your customizations stay (if in separate branches)
```

### Contributing Improvements
Found a bug? Want to add a feature?
```bash
# Create feature branch
git checkout -b feature/my-improvement

# Make changes
# Commit
git commit -m "docs: Add new feature"

# Push
git push origin feature/my-improvement

# Open Pull Request on GitHub
```

---

## 📚 Documentation Checklist

Before deploying to your institution:

- [ ] Read README.md
- [ ] Review EDUCATIONAL_GUIDE.md
- [ ] Test locally first (http://localhost:8000)
- [ ] Choose deployment platform
- [ ] Set up HTTPS
- [ ] Test in all supported browsers
- [ ] Integrate with LMS (if applicable)
- [ ] Create institutional version (logo, colors)
- [ ] Train teachers/staff
- [ ] Share with students
- [ ] Gather feedback
- [ ] Monitor usage/issues

---

## ✅ Pre-Launch Checklist

### Technical
- [ ] All files copied correctly
- [ ] External CDN links working
- [ ] HTTPS enabled
- [ ] Mobile responsive tested
- [ ] All browsers tested
- [ ] No console errors (F12)

### Educational
- [ ] Teachers trained
- [ ] Lesson plans ready
- [ ] Student guidelines provided
- [ ] Discussion prompts prepared
- [ ] Assessment rubrics created

### Institutional
- [ ] School district approval (if needed)
- [ ] Copyright/license reviewed
- [ ] IT security sign-off
- [ ] Accessibility (ADA) reviewed
- [ ] Parent communication (K-12)

---

## 🎓 Launch Announcement

### Sample Email to Teachers

```
Subject: New Educational Physics Tool: Exotic Energy Framework

Colleagues,

We're launching an interactive physics education tool for students. 
It's a free, open-source simulation environment exploring theoretical 
physics concepts through interactive labs.

Perfect for:
- High school physics classes
- College STEM courses  
- Science club exploration
- Student independent projects

Access: [your-url]/exotic-energy-framework.html

Resources for educators:
- Teacher guide: EDUCATIONAL_GUIDE.md
- Lesson plans: [included]
- Learning objectives: LEARNING_OBJECTIVES.md

Questions? See the README or contact [your-contact]

Happy exploring!
```

---

## 🌟 Success Metrics

Track these to know if the tool is working:

✅ **Engagement:** Students spending 15+ minutes per session  
✅ **Learning:** Quiz scores improve after using tool  
✅ **Excitement:** Positive comments and questions  
✅ **Extensions:** Students propose improvements  
✅ **Community:** Teachers sharing lesson plans  
✅ **Reach:** Other schools adopt the tool  

---

**Generated:** January 1, 2026  
**For:** IT Administrators & Educators  
**Status:** Ready to Deploy
