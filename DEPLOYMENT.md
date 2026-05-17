# Deployment Guide

## Option 1: Deploy to GitHub Pages (Recommended)

### Step 1: Create a GitHub Repository
1. Go to [GitHub.com](https://github.com)
2. Create a new repository named `sjpgalido.github.io`
3. Make sure it's set to public

### Step 2: Push Files to GitHub
```bash
# Initialize git in your project
git init

# Add all files
git add .

# Commit
git commit -m "Initial commit: Portfolio website"

# Add remote repository
git remote add origin https://github.com/yourusername/sjpgalido.github.io.git

# Push to main branch
git branch -M main
git push -u origin main
```

### Step 3: Access Your Portfolio
- Your portfolio will be live at: `https://yourusername.github.io`
- GitHub automatically publishes from the main branch

---

## Option 2: Deploy to Netlify

### Step 1: Connect Netlify
1. Go to [Netlify.com](https://netlify.com)
2. Sign up with GitHub
3. Click "New site from Git"
4. Select your GitHub repository

### Step 2: Configure Build Settings
- **Build command**: (leave empty for static site)
- **Publish directory**: `.` (root directory)

### Step 3: Deploy
Netlify will automatically deploy whenever you push to GitHub.

---

## Option 3: Deploy to Vercel

### Step 1: Connect Vercel
1. Go to [Vercel.com](https://vercel.com)
2. Sign up with GitHub
3. Import your repository

### Step 2: Configure
- Framework preset: None (static)
- Root directory: `.`

### Step 3: Deploy
Click deploy and Vercel will publish your site.

---

## Option 4: Manual Hosting (cPanel, Shared Hosting)

### Step 1: Prepare Files
1. Create a zip file of all project files
2. Extract the zip on your hosting server

### Step 2: Upload Files
```bash
# Using FTP
# Connect to your hosting FTP credentials
# Upload all files to the public_html directory

# Or using SFTP
sftp user@yourhost.com
cd public_html
put -r *
```

### Step 3: Update DNS
1. Go to your domain registrar
2. Update DNS records to point to your hosting provider
3. Wait for DNS propagation (up to 24 hours)

---

## Custom Domain Setup

### For GitHub Pages with Custom Domain
1. Create a CNAME file in your repo with your domain
2. Update DNS settings at your domain registrar
3. Add CNAME record pointing to `yourusername.github.io`

### For Netlify with Custom Domain
1. Go to Netlify site settings
2. Under Domain management, add your custom domain
3. Update DNS records as instructed by Netlify

### For Vercel with Custom Domain
1. Go to project settings
2. Add domain
3. Update DNS records as instructed by Vercel

---

## Environment Variables

If you need environment variables:

1. Create `.env` file (not tracked in git)
2. Add your configuration:
   ```
   ANALYTICS_ID=your_id_here
   EMAIL=your_email@example.com
   ```

3. Reference in JavaScript:
   ```javascript
   const analyticsId = process.env.ANALYTICS_ID;
   ```

---

## Performance Optimization

### Before Deployment

1. **Minify CSS & JavaScript**
   - Use tools like [CSS Minifier](https://cssminifier.com)
   - Use [JavaScript Minifier](https://www.minifier.org)

2. **Optimize Images**
   ```bash
   # Use ImageOptim, TinyPNG, or similar
   # Compress images to reduce file size
   ```

3. **Enable Caching**
   - Netlify and Vercel enable caching automatically
   - GitHub Pages uses GitHub's CDN

4. **Monitor Performance**
   - Use [Google PageSpeed Insights](https://pagespeed.web.dev)
   - Use [WebPageTest](https://www.webpagetest.org)

---

## SSL Certificate

- **GitHub Pages**: Free automatic SSL (HTTPS)
- **Netlify**: Free automatic SSL (HTTPS)
- **Vercel**: Free automatic SSL (HTTPS)
- **Manual Hosting**: Use Let's Encrypt (free) or purchase SSL

---

## Continuous Deployment

Most platforms automatically deploy when you push to GitHub:

```bash
# Make changes
git add .
git commit -m "Update portfolio content"
git push

# Automatically deploys to your live site!
```

---

## Troubleshooting

### Site not loading
- Check DNS propagation: [DNSChecker.org](https://dnschecker.org)
- Clear browser cache
- Check file paths are correct

### Images not showing
- Verify image file names (case-sensitive on Linux servers)
- Update image paths if different from local

### Styling looks wrong
- Clear browser cache (Ctrl+Shift+Del)
- Check CSS file is loading (F12 Developer Tools)
- Verify file paths are correct

### Domain not connecting
- Wait 24 hours for DNS propagation
- Verify DNS records are correct
- Check domain registrar settings

---

## Updating Your Portfolio

1. Make changes to your files
2. Test locally
3. Commit and push to GitHub:
   ```bash
   git add .
   git commit -m "Update: description of changes"
   git push
   ```
4. Your site updates automatically!

---

## Monitoring & Analytics

### Add Google Analytics
1. Create Google Analytics account
2. Get your tracking ID
3. Add to `index.html` before `</head>`:
   ```html
   <script async src="https://www.googletagmanager.com/gtag/js?id=YOUR_ID"></script>
   <script>
       window.dataLayer = window.dataLayer || [];
       function gtag(){dataLayer.push(arguments);}
       gtag('js', new Date());
       gtag('config', 'YOUR_ID');
   </script>
   ```

---

## Regular Maintenance

- Update contact information as needed
- Add new certificates when earned
- Update portfolio works with new projects
- Review and fix broken links quarterly
- Monitor site performance monthly
- Update social media links if they change

---

**Need Help?**
- Check the README.md for additional information
- Contact your hosting provider's support
- Visit deployment platform documentation

