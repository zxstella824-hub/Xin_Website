# Setting Up Custom Domain: xinzhouvoice.com

## Step-by-Step Guide

### Step 1: CNAME File ✅
The `CNAME` file has been created with your domain name. Upload this file to your GitHub repository.

### Step 2: Configure DNS at Your Domain Registrar

Go to your domain registrar's DNS management panel (where you bought xinzhouvoice.com) and add these records:

#### Option A: A Records (Recommended - Works with both root and www)

Add **4 A records** for the root domain (`@`):

| Type | Name | Value | TTL |
|------|------|-------|-----|
| A | @ | 185.199.108.153 | 3600 |
| A | @ | 185.199.109.153 | 3600 |
| A | @ | 185.199.110.153 | 3600 |
| A | @ | 185.199.111.153 | 3600 |

**For www subdomain (optional):**
| Type | Name | Value | TTL |
|------|------|-------|-----|
| CNAME | www | zxstella824-hub.github.io | 3600 |

#### Option B: CNAME Record (Simpler, but some registrars don't support CNAME on root)

| Type | Name | Value | TTL |
|------|------|-------|-----|
| CNAME | @ | zxstella824-hub.github.io | 3600 |
| CNAME | www | zxstella824-hub.github.io | 3600 |

**Note:** If your registrar doesn't allow CNAME on root domain (@), use Option A (A records).

### Step 3: Enable Custom Domain on GitHub

1. Go to: https://github.com/zxstella824-hub/Xin_Website/settings/pages
2. Under **"Custom domain"**, enter: `xinzhouvoice.com`
3. Click **Save**
4. Wait a few minutes, then check **"Enforce HTTPS"** (this will be available after DNS propagates)

### Step 4: Verify DNS Propagation

Check if DNS is working:
- Visit: https://www.whatsmydns.net/#A/xinzhouvoice.com
- You should see the GitHub IP addresses: 185.199.108.153, 185.199.109.153, etc.

### Step 5: Wait for SSL Certificate

- GitHub will automatically provision an SSL certificate
- This usually takes 10-30 minutes after DNS is active
- You'll see a green checkmark next to "Enforce HTTPS" when ready

### Step 6: Test Your Site

Once everything is configured:
- Visit: `https://xinzhouvoice.com`
- Your site should load!

## Common Domain Registrars Instructions

### GoDaddy
1. Log in → My Products → DNS
2. Scroll to "Records" section
3. Add A records (Type: A, Name: @, Value: IP addresses above)
4. Add CNAME for www (Type: CNAME, Name: www, Value: zxstella824-hub.github.io)

### Namecheap
1. Log in → Domain List → Manage → Advanced DNS
2. Add A records in "Host Records"
3. Add CNAME for www

### Google Domains
1. Log in → DNS → Custom records
2. Add A records and CNAME records

### Cloudflare
1. Log in → Select domain → DNS
2. Add A records (Proxied = OFF for GitHub Pages)
3. Add CNAME for www

## Troubleshooting

### DNS Not Working?
- Wait 24-48 hours for full propagation
- Check DNS at: https://www.whatsmydns.net/
- Make sure you removed any conflicting records

### HTTPS Not Working?
- Wait 10-30 minutes after DNS is active
- Make sure "Enforce HTTPS" is checked in GitHub Pages settings
- Clear your browser cache

### Site Shows GitHub 404?
- Make sure `CNAME` file is in the root of your repository
- Make sure GitHub Pages is enabled (Settings → Pages)
- Make sure you're using the main branch

### Still Having Issues?
- Check GitHub Pages status: https://www.githubstatus.com/
- Verify CNAME file content: Should only contain `xinzhouvoice.com` (no www, no http://)
- Contact your domain registrar's support

## Your Final URLs

After setup is complete:
- **Primary:** https://xinzhouvoice.com
- **With www:** https://www.xinzhouvoice.com (if configured)
- **GitHub URL still works:** https://zxstella824-hub.github.io/Xin_Website/

