# GitHub Pages Deployment Guide

## 🚀 Deploy Your Saltash WebAR Tour to GitHub Pages (5 minutes)

This guide will help you deploy your website to GitHub Pages for free, permanent hosting.

---

## Step 1: Create a GitHub Account

1. **Go to [github.com](https://github.com)**
2. **Click "Sign up"**
3. **Enter your email address**
4. **Create a password**
5. **Choose username** (e.g., `your-username`)
6. **Complete verification** (email confirmation)

---

## Step 2: Create a New Repository

1. **After signing in, click the "+" icon** in the top right corner
2. **Select "New repository"**
3. **Fill in the details:**
   - **Repository name:** `saltash-webar-tour`
   - **Description:** "Saltash WebAR Historical Tour - Explore Cornwall's heritage in augmented reality"
   - **Visibility:** Select "Public"
   - **Initialize with README:** Leave unchecked (we have our own)

4. **Click "Create repository"**

---

## Step 3: Upload Files to GitHub

### Method A: Using GitHub Web Interface (Easiest)

1. **In your new repository, click "Add file" → "Upload files"**
2. **Drag and drop all files** from `/home/ubuntu/saltash-webar-site/`:
   - `index.html`
   - `tour.html`
   - `markers.html`
   - `README.md`
   - `DEPLOYMENT.md`
   - `QUICK_START.md`
   - `netlify.toml`
   - `vercel.json`
   - `package.json`
   - `.gitignore`
   - `.github/workflows/deploy.yml`

3. **Add commit message:** "Initial commit: Saltash WebAR Historical Tour"
4. **Click "Commit changes"**

### Method B: Using Git Command Line (Advanced)

```bash
cd /home/ubuntu/saltash-webar-site
git remote add origin https://github.com/YOUR-USERNAME/saltash-webar-tour.git
git branch -M main
git push -u origin main
```

Replace `YOUR-USERNAME` with your actual GitHub username.

---

## Step 4: Enable GitHub Pages

1. **Go to your repository**
2. **Click "Settings"** (top right)
3. **In the left sidebar, click "Pages"**
4. **Under "Build and deployment":**
   - **Source:** Select "Deploy from a branch"
   - **Branch:** Select "main" (or "master" if that's your default)
   - **Folder:** Select "/ (root)"

5. **Click "Save"**

---

## Step 5: Wait for Deployment

1. **Go back to the main repository page**
2. **You'll see a yellow/orange dot** next to "Deployments" (top right)
3. **Wait 1-2 minutes** for it to turn green ✅
4. **Your site is now live!**

---

## Step 6: Access Your Website

Your website will be available at:

```
https://YOUR-USERNAME.github.io/saltash-webar-tour
```

**Example:** If your username is `john-smith`, your URL will be:
```
https://john-smith.github.io/saltash-webar-tour
```

---

## 🎉 Your Site is Live!

**Share your URL:**
- Social media
- Email to friends and family
- Tourism websites
- Educational institutions
- QR code (use [qr-code-generator.com](https://qr-code-generator.com))

---

## Optional: Add a Custom Domain

If you want a custom domain like `saltash-webar-tour.com`:

1. **Buy a domain** from:
   - [Namecheap](https://namecheap.com)
   - [GoDaddy](https://godaddy.com)
   - [Google Domains](https://domains.google.com)

2. **In your GitHub repository, go to Settings → Pages**

3. **Under "Custom domain", enter your domain name**

4. **GitHub will show you DNS records to add** at your domain registrar

5. **Add the DNS records** at your registrar's website

6. **Wait 24-48 hours** for DNS to propagate

7. **GitHub automatically provisions an SSL certificate** (green lock icon)

---

## 🔧 Making Updates

After your site is live, you can update it anytime:

1. **Make changes** to your HTML/CSS files
2. **Go to GitHub repository**
3. **Click "Add file" → "Upload files"** or edit directly
4. **Commit changes**
5. **GitHub automatically redeploys** (takes 1-2 minutes)

---

## 📱 Test Your Site

After deployment:

1. **Open your GitHub Pages URL** on your smartphone
2. **Click "Start AR Tour"**
3. **Grant camera permission**
4. **Download AR markers** from the Markers Guide
5. **Print the markers**
6. **Point camera at markers** to see the AR experience

---

## 🆘 Troubleshooting

### Site not showing after 5 minutes
- Refresh the page (Ctrl+F5 or Cmd+Shift+R)
- Check that you selected "Deploy from a branch" in Pages settings
- Verify branch name is correct (main or master)
- Check that files were uploaded successfully

### Getting 404 error
- Verify repository name is correct
- Check that `index.html` is in the root directory
- Make sure visibility is set to "Public"

### Camera not working
- Ensure you're using HTTPS (GitHub Pages provides this automatically)
- Grant camera permissions in browser settings
- Try a different browser
- Check that you're on a smartphone or device with camera

### DNS/Custom domain not working
- Wait 24-48 hours for DNS propagation
- Check DNS records at your registrar
- Use online DNS checker tools to verify
- Contact your domain registrar support

---

## 📊 Monitor Your Site

GitHub provides analytics:

1. **Go to your repository**
2. **Click "Insights"** (top)
3. **Click "Traffic"** to see visitor stats

---

## 🔒 Security & Privacy

✅ **HTTPS enabled** - Automatic SSL certificate  
✅ **No data collection** - Static site, no tracking  
✅ **Privacy-focused** - All processing on user's device  
✅ **Open source** - Transparent and auditable code  

---

## 📞 Support

**GitHub Help:**
- [GitHub Pages Documentation](https://docs.github.com/en/pages)
- [GitHub Support](https://support.github.com)

**Project Documentation:**
- See `README.md` for full project info
- See `DEPLOYMENT.md` for other deployment options
- See `QUICK_START.md` for quick reference

---

## 🎯 Next Steps

1. ✅ Create GitHub account
2. ✅ Create repository
3. ✅ Upload files
4. ✅ Enable GitHub Pages
5. ✅ Share your URL
6. ✅ Celebrate! 🎉

---

**Your Saltash WebAR Historical Tour is now permanently hosted and accessible to the world!**

**Version:** 1.0.0  
**Last Updated:** June 2026  
**Status:** Production Ready ✅
