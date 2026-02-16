# How to Publish Athena 3.0 Website to GoDaddy

## Step-by-Step Guide for Beginners

### What You Need
- GoDaddy account with hosting plan
- Your website files (already ready!)
- 10-15 minutes of time

---

## Method 1: Using GoDaddy File Manager (EASIEST - Recommended)

### Step 1: Download Your Website Files

First, get all your website files in one folder on your computer:

**Required Files (5 files):**
1. `index.html` - Main website page
2. `styles.css` - Design and colors
3. `script.js` - Interactive features
4. `logo.svg` - Your logo
5. `favicon.svg` - Browser tab icon

**How to get them:**
- If you're on your computer where we built the site, they're in your `pp-realestate` folder
- Or download from GitHub: https://github.com/ahmadjkd1/athena-pali
  - Click the green "Code" button
  - Select "Download ZIP"
  - Extract the ZIP file
  - Find the 5 files listed above

---

### Step 2: Login to GoDaddy

1. Go to **https://www.godaddy.com**
2. Click **"Sign In"** (top right)
3. Enter your email and password
4. Click **"Sign In"**

---

### Step 3: Access Your Hosting

1. After login, click **"My Products"** at the top
2. Find your **"Web Hosting"** section
3. Click the **"Manage"** button next to your hosting plan
4. You'll see the cPanel dashboard

---

### Step 4: Open File Manager

1. In cPanel, scroll down to **"Files"** section
2. Click on **"File Manager"**
3. A new window/tab will open

---

### Step 5: Navigate to public_html

1. In File Manager, you'll see folders on the left
2. Click on **"public_html"** folder
3. This is where your website files go

**Important:** If you see any existing files like:
- `index.html`
- `coming-soon.html`
- `default.html`

**Delete them first:**
- Select the file (checkbox)
- Click "Delete" button at the top
- Confirm deletion

---

### Step 6: Upload Your Files

1. Make sure you're inside the `public_html` folder
2. Click the **"Upload"** button at the top
3. Click **"Select File"** button
4. Navigate to where you saved your 5 website files
5. Select ALL 5 files at once:
   - Hold `Ctrl` (Windows) or `Cmd` (Mac)
   - Click each file
   - Click "Open"
6. Wait for the upload to complete (you'll see a progress bar)
7. When done, click "Go Back to..." link

---

### Step 7: Verify Upload

Back in File Manager, you should see:
```
public_html/
├── index.html
├── styles.css
├── script.js
├── logo.svg
└── favicon.svg
```

✅ All 5 files should be there!

---

### Step 8: Check File Permissions (Important!)

1. Right-click on `index.html`
2. Select "Change Permissions"
3. Make sure it shows: **644**
4. Click "Change Permissions"
5. Repeat for all other files

**What 644 means:**
- Owner can read and write
- Others can only read
- This is the correct setting for website files

---

### Step 9: Test Your Website

1. Open a new browser tab
2. Type your domain name:
   - `http://yourdomain.com` OR
   - `http://www.yourdomain.com`
3. Press Enter

**🎉 Your website should be LIVE!**

---

## Troubleshooting

### Problem: Website shows "Coming Soon" or old page
**Solution:**
- Go back to File Manager
- Make sure you deleted old `index.html`
- Verify your new `index.html` is uploaded
- Clear browser cache: Press `Ctrl + F5` (Windows) or `Cmd + Shift + R` (Mac)

### Problem: Website shows but no styling (looks plain)
**Solution:**
- Check if `styles.css` is uploaded
- Verify it's in the same folder as `index.html` (public_html)
- Clear browser cache

### Problem: Logo not showing
**Solution:**
- Check if `logo.svg` is uploaded
- Verify file name is exactly `logo.svg` (lowercase)
- Clear browser cache

### Problem: "403 Forbidden" error
**Solution:**
- Check file permissions (should be 644)
- Make sure `index.html` exists in public_html

### Problem: Changes not showing
**Solution:**
- Clear browser cache: `Ctrl + F5`
- Wait 5-10 minutes for server to update
- Try in incognito/private browsing mode

---

## Method 2: Using FTP (For Advanced Users)

If you're comfortable with FTP clients:

### Download FileZilla
- Visit: https://filezilla-project.org/
- Download and install

### Get FTP Credentials from GoDaddy
1. In cPanel, find "FTP Accounts"
2. Note your:
   - **Host:** `ftp.yourdomain.com`
   - **Username:** (shown in FTP Accounts)
   - **Password:** (create or retrieve)
   - **Port:** 21

### Connect and Upload
1. Open FileZilla
2. Enter Host, Username, Password, Port
3. Click "Quickconnect"
4. Navigate to `/public_html` on right side (remote)
5. Drag your 5 files from left (local) to right (remote)
6. Wait for upload to complete

---

## After Publishing - Important Steps

### 1. Enable HTTPS (SSL Certificate)
1. In cPanel, find "SSL/TLS Status"
2. Click "Run AutoSSL"
3. Wait for completion
4. Your site will be accessible via `https://yourdomain.com`

### 2. Set Up Email (Optional)
1. In cPanel, find "Email Accounts"
2. Create: `info@yourdomain.com`
3. Use for contact form

### 3. Add Google Analytics (Optional)
1. Get tracking code from Google Analytics
2. Add to `index.html` before `</head>` tag

### 4. Submit to Google
1. Go to Google Search Console
2. Add your website
3. Submit sitemap

---

## Making Updates Later

When you want to change content:

1. Edit files on your computer
2. Go to GoDaddy File Manager
3. Select the file you want to update
4. Click "Delete"
5. Upload the new version
6. Clear browser cache to see changes

**OR**

Use FTP to upload updated files (will overwrite automatically)

---

## Quick Reference Card

```
✅ CHECKLIST FOR PUBLISHING

□ Have GoDaddy hosting account
□ Downloaded all 5 website files
□ Logged into GoDaddy
□ Opened File Manager
□ Navigated to public_html
□ Deleted old files
□ Uploaded 5 new files
□ Set permissions to 644
□ Tested website in browser
□ Enabled HTTPS/SSL
```

---

## Need Help?

**GoDaddy Support:**
- Phone: 1-480-505-8877 (24/7)
- Live Chat: Available in your GoDaddy account
- Help Center: https://www.godaddy.com/help

**Common Support Questions:**
- "How do I access File Manager?"
- "How do I upload files to my website?"
- "How do I enable SSL certificate?"

---

## Video Tutorial (Recommended)

Search YouTube for: "How to upload website to GoDaddy cPanel"

Recommended videos:
- "GoDaddy cPanel File Manager Tutorial"
- "Upload HTML website to GoDaddy"

---

## Your Website is Ready! 🚀

Once published, share your website:
- `https://yourdomain.com`

**Next Steps:**
1. Test on mobile devices
2. Share with friends/family for feedback
3. Add to Google My Business
4. Share on social media
5. Add to business cards

---

**Questions?** Refer to DEPLOYMENT_GUIDE.md for more detailed information.

**Need to implement the 12 improvements?** See IMPLEMENTATION_PLAN.md and CONTENT_NEEDED.md
