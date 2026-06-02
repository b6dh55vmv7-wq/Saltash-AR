# Deployment Guide - Saltash WebAR Historical Tour

This guide provides step-by-step instructions for deploying your website to permanent hosting platforms.

## 🚀 Quick Deployment (Recommended)

### Option 1: Netlify (Easiest - 2 minutes)

**Best for:** Quick setup, automatic deployments, free SSL

1. **Go to [netlify.com](https://netlify.com)**
2. **Sign up** with GitHub, GitLab, or email
3. **Click "Add new site"** → **"Deploy manually"**
4. **Drag and drop** the entire `saltash-webar-site` folder
5. **Your site is live!** Netlify generates a URL like `https://your-site-name.netlify.app`

**To use a custom domain:**
- Go to Site settings → Domain management
- Add your custom domain
- Follow DNS configuration instructions

---

### Option 2: Vercel (Fast - 2 minutes)

**Best for:** Excellent performance, GitHub integration, free tier

1. **Go to [vercel.com](https://vercel.com)**
2. **Sign up** with GitHub or email
3. **Click "New Project"**
4. **Upload your project** or connect GitHub repository
5. **Deploy** - Vercel handles everything automatically
6. **Your URL:** `https://your-project.vercel.app`

**To use a custom domain:**
- Go to Project Settings → Domains
- Add your custom domain
- Update DNS records at your domain registrar

---

### Option 3: GitHub Pages (Free - 5 minutes)

**Best for:** Free hosting, GitHub integration, no vendor lock-in

1. **Create a GitHub account** at [github.com](https://github.com)
2. **Create a new repository** named `saltash-webar-tour`
3. **Upload all files** from the `saltash-webar-site` folder
4. **Go to Settings** → **Pages**
5. **Select "Deploy from a branch"**
6. **Choose "main" branch** and save
7. **Your site is live at:** `https://yourusername.github.io/saltash-webar-tour`

**To use a custom domain:**
- Add `CNAME` file with your domain name
- Update DNS records at your registrar
- GitHub Pages will handle SSL automatically

---

## 📋 Detailed Deployment Instructions

### Netlify Detailed Setup

#### Via Drag & Drop (Simplest)
```
1. Visit netlify.com
2. Sign in or create account
3. Click "Add new site" → "Deploy manually"
4. Drag the saltash-webar-site folder into the drop zone
5. Wait for deployment to complete
6. Your site is live!
```

#### Via Git Integration (Recommended for updates)
```
1. Push your code to GitHub
2. Visit netlify.com and sign in
3. Click "New site from Git"
4. Select GitHub and authorize
5. Choose your repository
6. Configure build settings:
   - Build command: (leave empty)
   - Publish directory: .
7. Click "Deploy site"
8. Enable auto-deploys for future updates
```

#### Custom Domain on Netlify
```
1. Go to Site settings → Domain management
2. Click "Add custom domain"
3. Enter your domain (e.g., saltash-webar-tour.com)
4. Netlify provides DNS records to add
5. Update your domain registrar's DNS settings
6. Wait 24-48 hours for propagation
7. Netlify automatically provisions SSL certificate
```

---

### Vercel Detailed Setup

#### Via Project Upload
```
1. Visit vercel.com
2. Sign in with GitHub or email
3. Click "New Project"
4. Click "Continue with File Upload"
5. Upload the saltash-webar-site folder
6. Vercel analyzes and deploys automatically
7. Your URL is ready to share
```

#### Via GitHub Integration
```
1. Push code to GitHub repository
2. Visit vercel.com
3. Click "New Project"
4. Click "Import Git Repository"
5. Select your GitHub repository
6. Vercel auto-configures for static sites
7. Click "Deploy"
8. Enable automatic deployments
```

#### Custom Domain on Vercel
```
1. Go to Project Settings → Domains
2. Click "Add"
3. Enter your domain name
4. Select "Using external nameservers"
5. Add provided nameserver records to your registrar
6. Or use CNAME records for subdomain
7. Vercel provisions SSL automatically
```

---

### GitHub Pages Detailed Setup

#### Step-by-Step
```
1. Create GitHub account at github.com
2. Click "+" → "New repository"
3. Name: saltash-webar-tour
4. Description: Saltash WebAR Historical Tour
5. Select "Public"
6. Click "Create repository"
7. Upload files:
   - Click "Add file" → "Upload files"
   - Drag and drop all files from saltash-webar-site
   - Click "Commit changes"
8. Go to Settings → Pages
9. Under "Build and deployment":
   - Source: Deploy from a branch
   - Branch: main (or master)
   - Folder: / (root)
10. Click "Save"
11. Wait 1-2 minutes for deployment
12. Your site: https://yourusername.github.io/saltash-webar-tour
```

#### Custom Domain on GitHub Pages
```
1. Purchase a domain from a registrar (GoDaddy, Namecheap, etc.)
2. In your repository, create a file named CNAME
3. Add your domain: saltash-webar-tour.com
4. Commit and push
5. Go to Settings → Pages
6. Under "Custom domain", enter your domain
7. At your registrar, add DNS records:
   - For apex domain (@): Add A records pointing to GitHub IPs
   - For subdomain (www): Add CNAME record
8. Wait 24-48 hours for DNS propagation
9. GitHub automatically provisions SSL
```

---

## 🔧 Configuration Files Included

### `netlify.toml`
Netlify-specific configuration:
- Build settings
- Redirect rules
- Security headers
- Camera permissions for AR

### `vercel.json`
Vercel-specific configuration:
- Build command
- Output directory
- Headers for AR functionality

### `.github/workflows/deploy.yml`
GitHub Actions workflow for automatic deployment to GitHub Pages

---

## 🌐 Domain Registration

If you want a custom domain, register one at:
- **Namecheap** - Affordable, great support
- **GoDaddy** - Popular, many extensions
- **Google Domains** - Simple, integrated with Google services
- **Cloudflare** - Advanced features, free DNS

**Recommended domain names:**
- `saltash-webar-tour.com`
- `saltash-ar-tour.com`
- `explore-saltash.com`
- `saltash-heritage.com`

---

## ✅ Post-Deployment Checklist

After deploying, verify everything works:

- [ ] Home page loads correctly
- [ ] AR tour page opens without errors
- [ ] Camera permission request appears
- [ ] Markers guide page displays properly
- [ ] All links work correctly
- [ ] Mobile responsiveness is good
- [ ] HTTPS is enabled (green lock icon)
- [ ] Page loads quickly
- [ ] No console errors (check browser DevTools)

---

## 🔒 Security Best Practices

1. **Enable HTTPS** - All platforms provide free SSL
2. **Set security headers** - Already configured in netlify.toml
3. **Keep dependencies updated** - No backend dependencies in this project
4. **Monitor uptime** - Use free tools like UptimeRobot
5. **Backup files** - Keep local copy and GitHub repository

---

## 📊 Monitoring & Analytics (Optional)

Add Google Analytics to track visitors:

1. **Create Google Analytics account** at [analytics.google.com](https://analytics.google.com)
2. **Add tracking code** to `index.html`, `tour.html`, and `markers.html`:

```html
<!-- Google Analytics -->
<script async src="https://www.googletagmanager.com/gtag/js?id=GA_MEASUREMENT_ID"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'GA_MEASUREMENT_ID');
</script>
```

Replace `GA_MEASUREMENT_ID` with your actual ID.

---

## 🚨 Troubleshooting

### Site not loading
- Check that all files were uploaded
- Verify file names are correct (case-sensitive)
- Clear browser cache (Ctrl+Shift+Delete)
- Check platform's deployment logs

### Camera not working
- Ensure HTTPS is enabled
- Check browser permissions
- Try different browser
- Verify camera permissions in OS settings

### AR markers not detecting
- Check file uploads were successful
- Verify A-Frame and AR.js libraries loaded
- Check browser console for errors
- Try different device/browser

### DNS not resolving
- Wait 24-48 hours for propagation
- Check DNS records at your registrar
- Use online DNS checker tools
- Contact registrar support if issues persist

---

## 📞 Support

**Platform Support:**
- **Netlify:** [netlify.com/support](https://netlify.com/support)
- **Vercel:** [vercel.com/support](https://vercel.com/support)
- **GitHub:** [github.com/support](https://github.com/support)

**AR.js Documentation:**
- [ar-js-org.github.io](https://ar-js-org.github.io/AR.js-Docs/)

**A-Frame Documentation:**
- [aframe.io](https://aframe.io)

---

## 🎉 You're Done!

Your Saltash WebAR Historical Tour is now permanently hosted and accessible to the world!

**Share your URL:**
- Social media
- Email
- QR code (use a QR code generator)
- Tourism websites
- Educational institutions

---

**Version:** 1.0.0  
**Last Updated:** June 2026  
**Status:** Production Ready ✅
