# Athena 3.0 - GoDaddy Deployment Guide

## Files to Upload

Upload these files to your GoDaddy hosting:

```
public_html/
├── index.html
├── styles.css
├── script.js
├── logo.svg
├── favicon.svg
└── README.md (optional)
```

## Method 1: GoDaddy File Manager (Recommended for Beginners)

1. **Login to GoDaddy**
   - Visit: https://www.godaddy.com
   - Click "Sign In"
   - Enter your credentials

2. **Access Your Hosting**
   - Go to "My Products"
   - Find your Web Hosting plan
   - Click "Manage"

3. **Open File Manager**
   - In cPanel, find "File Manager"
   - Click to open

4. **Navigate to public_html**
   - This is your website's root directory
   - Delete any default files (like `index.html` or `coming-soon.html`)

5. **Upload Your Files**
   - Click "Upload" button
   - Select all 5 files from your project
   - Wait for upload to complete

6. **Set Permissions**
   - Right-click each file
   - Set permissions to 644 (read/write for owner, read for others)

7. **Test Your Website**
   - Visit your domain: `http://yourdomain.com`
   - Your Athena 3.0 website should be live!

## Method 2: FTP Upload (For Advanced Users)

### Step 1: Get FTP Credentials

1. In GoDaddy cPanel, find "FTP Accounts"
2. Note your:
   - FTP Host: `ftp.yourdomain.com`
   - Username: Usually your domain or email
   - Password: Set or retrieve from GoDaddy

### Step 2: Use FTP Client

**Using FileZilla (Free FTP Client):**

1. Download FileZilla: https://filezilla-project.org/
2. Install and open FileZilla
3. Enter connection details:
   - Host: `ftp.yourdomain.com`
   - Username: Your FTP username
   - Password: Your FTP password
   - Port: 21
4. Click "Quickconnect"
5. Navigate to `/public_html` on the remote side
6. Drag and drop all files from your local folder

### Step 3: Verify Upload

- All files should appear in `/public_html`
- Visit your domain to test

## Method 3: Using Git (Most Professional)

If you want automatic deployments:

1. **Setup Git on GoDaddy**
   - Access SSH (if available on your plan)
   - Clone your GitHub repository

2. **Or use GoDaddy's Git Integration**
   - Some GoDaddy plans support Git deployment
   - Check your cPanel for "Git Version Control"

## Post-Deployment Checklist

- [ ] All files uploaded successfully
- [ ] Website loads at your domain
- [ ] Logo displays correctly
- [ ] All images load properly
- [ ] Navigation works
- [ ] Contact form displays
- [ ] Google Maps loads
- [ ] Mobile responsive design works
- [ ] All sections visible

## Custom Domain Setup

If you bought a domain from GoDaddy:

1. **Domain is automatically connected** to your hosting
2. Wait 24-48 hours for DNS propagation
3. Your site will be live at `http://yourdomain.com`

## SSL Certificate (HTTPS)

To enable HTTPS:

1. In cPanel, find "SSL/TLS"
2. Click "Manage SSL Sites"
3. Install free SSL certificate (Let's Encrypt)
4. Your site will be accessible via `https://yourdomain.com`

## Troubleshooting

### Website shows "Coming Soon" page
- Delete default `index.html` in `public_html`
- Upload your `index.html` file

### Images not loading
- Check file names match exactly (case-sensitive)
- Verify all files uploaded to correct directory

### CSS not applying
- Clear browser cache (Ctrl+F5)
- Check `styles.css` uploaded correctly

### 404 Error
- Ensure files are in `public_html`, not a subfolder
- Check file permissions (should be 644)

## Support

- **GoDaddy Support**: https://www.godaddy.com/help
- **Phone**: 1-480-505-8877
- **Live Chat**: Available 24/7 in GoDaddy account

## Updating Your Website

To make changes:

1. Edit files locally
2. Re-upload changed files via File Manager or FTP
3. Clear browser cache to see changes

## Performance Tips

1. **Enable Caching** in cPanel
2. **Compress Images** before uploading
3. **Enable Gzip Compression**
4. **Use CDN** for faster loading (optional)

---

**Your website is now ready to go live on GoDaddy!**

For any issues, contact GoDaddy support or refer to their documentation.
