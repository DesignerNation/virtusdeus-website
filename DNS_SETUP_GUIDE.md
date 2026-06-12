# DNS Setup Guide for virtusdeus.com

This guide will help you configure your domain's DNS records to point to GitHub Pages.

## Current Status

- **Repository:** https://github.com/DesignerNation/virtusdeus-website
- **GitHub Pages URL:** https://designernation.github.io/virtusdeus-website/
- **Custom Domain:** virtusdeus.com
- **CNAME File:** ✅ Already created in repository

## DNS Configuration Steps

### Step 1: Access Your Domain Registrar

Go to your domain registrar where you purchased **virtusdeus.com**. Common registrars include:
- Namecheap (https://www.namecheap.com)
- GoDaddy (https://www.godaddy.com)
- Google Domains (https://domains.google)
- Bluehost
- HostGator

### Step 2: Find DNS Settings

1. Log in to your registrar account
2. Find "Domain Management" or "My Domains"
3. Select **virtusdeus.com**
4. Look for "DNS Settings," "Name Servers," or "DNS Management"

### Step 3: Add DNS Records

You have two options. **Option A (Recommended)** is simpler:

#### Option A: Using CNAME Record (Recommended)

1. Find the DNS records section
2. Add a new **CNAME** record:
   - **Name/Host:** www
   - **Type:** CNAME
   - **Value/Points to:** designernation.github.io
   - **TTL:** 3600 (or default)

3. Add an **A** record for the root domain:
   - **Name/Host:** @ (or leave blank)
   - **Type:** A
   - **Value/Points to:** Use one of these GitHub Pages IP addresses:
     - 185.199.108.153
     - 185.199.109.153
     - 185.199.110.153
     - 185.199.111.153
   - **TTL:** 3600 (or default)

#### Option B: Using Alias Record (if your registrar supports it)

Some registrars (like Namecheap) support ALIAS records:
- **Name/Host:** @
- **Type:** ALIAS
- **Value:** designernation.github.io

### Step 4: Wait for DNS Propagation

DNS changes can take **15 minutes to 48 hours** to propagate globally. You can check status at:
- https://www.whatsmydns.net/?q=virtusdeus.com

### Step 5: Verify in GitHub

1. Go to: https://github.com/DesignerNation/virtusdeus-website/settings/pages
2. Under "Custom domain," you should see **virtusdeus.com**
3. Check the box for "Enforce HTTPS" (recommended)
4. Wait for the DNS check to show ✅ (may take a few minutes)

### Step 6: Test Your Domain

Once DNS propagates:
- Visit https://virtusdeus.com
- You should see your website
- HTTPS should be enabled automatically

## Troubleshooting

### Domain not resolving?
- Wait 24-48 hours for DNS propagation
- Clear your browser cache (Ctrl+Shift+Delete)
- Try in an incognito/private window
- Check DNS propagation: https://www.whatsmydns.net/?q=virtusdeus.com

### HTTPS not working?
- Wait 5-10 minutes after DNS is set up
- GitHub Pages will automatically provision an SSL certificate
- Refresh the GitHub Pages settings page

### Still having issues?
- Verify your DNS records are correct
- Ensure the CNAME file exists in your repository at `/CNAME`
- Check GitHub Pages settings: https://github.com/DesignerNation/virtusdeus-website/settings/pages

## GitHub Pages IP Addresses (for A records)

If using A records instead of CNAME:
```
185.199.108.153
185.199.109.153
185.199.110.153
185.199.111.153
```

## Reference: GitHub Pages Documentation

- Official Guide: https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site
- Troubleshooting: https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/troubleshooting-custom-domains-and-github-pages

## Next Steps

1. ✅ Configure DNS records (this guide)
2. ✅ Wait for DNS propagation
3. ⏳ Verify HTTPS is working
4. ⏳ Submit to Google Search Console
5. ⏳ Submit to Bing Webmaster Tools

---

**Need help?** Refer to the main README.md or contact GitHub Support.
