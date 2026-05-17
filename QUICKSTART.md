# Quick Start Guide

## 🚀 Get Started in 5 Minutes

### Step 1: Run the Website Locally
```bash
# Navigate to the project directory
cd c:\laragon\www\sjpgalido_va_portfolio

# If using Laragon, just open in browser:
# http://sjpgalido_va_portfolio.local

# Or start a Python server:
python -m http.server 8000

# Then open: http://localhost:8000
```

### Step 2: Customize Your Content
Edit `index.html` and update:
- **Name and Title** (line ~50)
- **About Me text** (line ~126)
- **Services offered** (lines ~156-209)
- **Email and social links** (lines ~94-100)

### Step 3: Personalize the Design
Edit `styles.css` to change:
```css
:root {
    --primary-color: #c4a574;      /* Main color */
    --primary-dark: #a68564;       /* Hover color */
    --bg-light: #f5f1ed;           /* Background */
}
```

### Step 4: Add Your Information
Update these key sections:
1. **Hero Section** - Main title and subtitle
2. **About Me** - Your professional description
3. **Services** - List your services
4. **Contact Info** - Email and social media

### Step 5: Deploy to GitHub
```bash
# Initialize git
git init
git add .
git commit -m "Initial portfolio"
git branch -M main

# Create repo at GitHub as: yourusername.github.io
git remote add origin https://github.com/yourusername/sjpgalido.github.io.git
git push -u origin main

# Live at: https://yourusername.github.io
```

---

## 📝 Easy Customizations

### Change Colors
In `styles.css`, update the `:root` section:
```css
--primary-color: #your-color;
--bg-light: #your-background;
```

### Add Your Services
Find `<!-- Services Section -->` in `index.html` and add:
```html
<div class="service-card">
    <div class="service-icon">
        <i class="fas fa-icon-name"></i>
    </div>
    <h3>Your Service</h3>
    <p>Service description</p>
</div>
```

### Update Social Links
Find the hero-social section and update:
```html
<a href="mailto:your-email@example.com">Email</a>
<a href="https://your-facebook-url">Facebook</a>
```

### Change Fonts
In `styles.css`, update font-family:
```css
body {
    font-family: 'Your Font', sans-serif;
}
```

---

## 🎨 Available Icons

All icons use Font Awesome. Popular ones:
- `fa-share-alt` - Social media
- `fa-envelope` - Email
- `fa-tasks` - Tasks
- `fa-database` - Data
- `fa-folder` - Files
- `fa-search` - Search
- `fa-calendar` - Calendar
- `fa-comments` - Chat
- `fa-tools` - Tools
- `fa-certificate` - Certificates

[View all icons](https://fontawesome.com/icons)

---

## 📱 Test on Mobile

1. Open DevTools: `F12`
2. Click device icon (top-left)
3. Select mobile device
4. Test all features and layouts

---

## ✅ Pre-Deployment Checklist

- [ ] Update all personal information
- [ ] Add correct email and social links
- [ ] Test on mobile devices
- [ ] Check all links work
- [ ] Verify images load
- [ ] Test contact forms/links
- [ ] Run on http://localhost:8000

---

## 🔗 Important Links

| Resource | URL |
|----------|-----|
| Font Awesome Icons | https://fontawesome.com/icons |
| Google Fonts | https://fonts.google.com |
| CSS Reference | https://developer.mozilla.org/en-US/docs/Web/CSS |
| HTML Reference | https://developer.mozilla.org/en-US/docs/Web/HTML |
| Deploy to GitHub | https://pages.github.com |
| Deploy to Netlify | https://netlify.com |

---

## ⚡ Quick Tips

1. **Mobile First** - Always test on mobile
2. **Keep It Simple** - Don't overcomplicate
3. **Fast Loading** - Optimize images
4. **Clear Navigation** - Easy to find content
5. **Call to Action** - Make it obvious how to contact you
6. **Regular Updates** - Keep content fresh

---

## 🆘 Common Issues

### Portfolio not showing locally?
```bash
# Make sure you're in the right directory
cd c:\laragon\www\sjpgalido_va_portfolio

# Check if server is running
# Try: http://localhost:8000
```

### Styles not working?
- Clear cache: `Ctrl+Shift+Del`
- Check file paths are correct
- Verify CSS file link in HTML

### Images not loading?
- Use absolute URLs or correct relative paths
- Check image file names (case-sensitive)
- Verify image files exist

### Git commands not working?
```bash
# Install Git: https://git-scm.com/download/win

# Verify installation
git --version
```

---

## 📚 File Guide

```
sjpgalido_va_portfolio/
├── index.html          ← Edit for content
├── styles.css          ← Edit for design
├── script.js           ← JavaScript interactions
├── README.md           ← Full documentation
├── DEPLOYMENT.md       ← How to deploy
├── QUICKSTART.md       ← This file
└── config.env          ← Configuration
```

---

## 🎯 Next Steps

1. ✅ **Get it running** - Open in browser
2. ✅ **Customize it** - Update your info
3. ✅ **Test it** - Check on mobile
4. ✅ **Deploy it** - Put it online
5. ✅ **Share it** - Tell the world!

---

**Questions?** Check README.md or DEPLOYMENT.md

**Happy Building! 🎉**
