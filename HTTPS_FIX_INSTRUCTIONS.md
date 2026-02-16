# HTTPS Fix Instructions

## Current Status
✅ Website is live at http://athenapali.in  
✅ Loading screen implemented  
✅ Mobile optimizations complete  
⚠️ HTTPS not working due to GoDaddy locked A record  

## Problem
GoDaddy has locked the A record (15.197.225.128) from domain parking/forwarding, preventing GitHub Pages from issuing an SSL certificate for the apex domain (athenapali.in).

## Solution: Use www Subdomain

### Step 1: Update GitHub Pages Settings
1. Go to your GitHub repository: https://github.com/ahmadjkd1/athena-pali
2. Click on **Settings** tab
3. Scroll down to **Pages** section (left sidebar)
4. Under **Custom domain**, change from `athenapali.in` to `www.athenapali.in`
5. Click **Save**

### Step 2: Wait for DNS Check
- GitHub will verify the DNS configuration
- This usually takes 5-10 minutes
- You'll see a green checkmark when ready

### Step 3: Enable HTTPS
1. Once DNS check passes, the **Enforce HTTPS** checkbox will become available
2. Check the **Enforce HTTPS** box
3. Wait 5-10 minutes for SSL certificate to be issued

### Step 4: Verify
Your site will be accessible at:
- ✅ https://www.athenapali.in (secure)
- ✅ http://www.athenapali.in (redirects to HTTPS)
- ✅ http://athenapali.in (redirects to www)

## What I've Done
✅ Updated CNAME file to `www.athenapali.in`  
✅ Committed the change to git  

## What You Need to Do
1. Push the CNAME change to GitHub (if not auto-synced)
2. Update GitHub Pages custom domain setting to `www.athenapali.in`
3. Wait for DNS verification
4. Enable "Enforce HTTPS"

## Alternative: Contact GoDaddy Support
If you prefer to use the apex domain (athenapali.in without www):
1. Contact GoDaddy support
2. Ask them to unlock/remove the A record at 15.197.225.128
3. Then add GitHub's A records:
   - 185.199.108.153
   - 185.199.109.153
   - 185.199.110.153
   - 185.199.111.153

## Timeline
- DNS propagation: 5-10 minutes
- SSL certificate issuance: 5-10 minutes
- Total time: ~15-20 minutes

Your site will be fully secure with HTTPS after these steps!
