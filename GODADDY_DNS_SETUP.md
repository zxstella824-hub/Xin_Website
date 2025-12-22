# GoDaddy DNS Setup for xinzhouvoice.com

## Step-by-Step Instructions for GoDaddy

### Step 1: Log into GoDaddy
1. Go to: https://www.godaddy.com
2. Click **Sign In** (top right)
3. Enter your GoDaddy account credentials

### Step 2: Access DNS Management
1. After logging in, click **My Products** (or go to: https://sso.godaddy.com/products)
2. Find **xinzhouvoice.com** in your domain list
3. Click the **DNS** button (or click the three dots → **Manage DNS**)

### Step 3: Remove Default/Existing Records
**Important:** GoDaddy may have default records that need to be removed first.

1. Look for any existing **A records** for `@` (root domain)
2. Look for any records pointing to GoDaddy's servers or placeholder pages
3. **Delete these records:**
   - Click the **three dots** (⋮) next to each record
   - Click **Delete**
   - Confirm deletion

**Also check for:**
- Any "Parked" or "Forwarding" settings (disable these)
- Any "Coming Soon" page settings (disable these)

### Step 4: Add GitHub Pages A Records
1. Scroll to the **Records** section
2. Click **Add** button
3. Add **4 separate A records** (one at a time):

**A Record #1:**
- **Type:** Select `A` from dropdown
- **Name:** `@` (or leave blank/empty)
- **Value:** `185.199.108.153`
- **TTL:** `600` (or leave default)
- Click **Save**

**A Record #2:**
- **Type:** `A`
- **Name:** `@` (or leave blank)
- **Value:** `185.199.109.153`
- **TTL:** `600`
- Click **Save**

**A Record #3:**
- **Type:** `A`
- **Name:** `@` (or leave blank)
- **Value:** `185.199.110.153`
- **TTL:** `600`
- Click **Save**

**A Record #4:**
- **Type:** `A`
- **Name:** `@` (or leave blank)
- **Value:** `185.199.111.153`
- **TTL:** `600`
- Click **Save**

### Step 5: Add www CNAME Record (Optional but Recommended)
1. Click **Add** button again
2. **Type:** Select `CNAME` from dropdown
3. **Name:** `www`
4. **Value:** `zxstella824-hub.github.io`
5. **TTL:** `600` (or leave default)
6. Click **Save**

### Step 6: Disable GoDaddy Placeholder Page
1. Go back to your domain management page
2. Look for **"Parked"** or **"Forwarding"** settings
3. If enabled, **disable** or **remove** it
4. Look for **"Coming Soon"** page - disable if enabled

### Step 7: Verify Your DNS Records
After adding records, you should see:

**A Records:**
- `@` → `185.199.108.153`
- `@` → `185.199.109.153`
- `@` → `185.199.110.153`
- `@` → `185.199.111.153`

**CNAME Record:**
- `www` → `zxstella824-hub.github.io`

### Step 8: Wait for DNS Propagation
- DNS changes can take **15 minutes to 48 hours** to propagate
- Usually works within 1-2 hours
- Check status: https://www.whatsmydns.net/#A/xinzhouvoice.com

### Step 9: Configure GitHub Pages
1. Go to: https://github.com/zxstella824-hub/Xin_Website/settings/pages
2. Under **"Custom domain"**, enter: `xinzhouvoice.com`
3. Click **Save**
4. Wait 5-10 minutes
5. Check **"Enforce HTTPS"** (will be available after DNS propagates)

## Visual Guide (GoDaddy Interface)

### What the DNS Records Section Looks Like:
```
Records
┌─────────────────────────────────────────────┐
│ Type │ Name │ Value              │ TTL │    │
├──────┼──────┼────────────────────┼─────┼────┤
│ A    │ @    │ 185.199.108.153    │ 600 │ ⋮  │
│ A    │ @    │ 185.199.109.153    │ 600 │ ⋮  │
│ A    │ @    │ 185.199.110.153    │ 600 │ ⋮  │
│ A    │ @    │ 185.199.111.153    │ 600 │ ⋮  │
│ CNAME│ www  │ zxstella824-hub... │ 600 │ ⋮  │
└─────────────────────────────────────────────┘
```

## Troubleshooting GoDaddy-Specific Issues

### Issue: Can't find DNS Management
- Go to: https://sso.godaddy.com/products
- Click on your domain name
- Look for **DNS** tab or button

### Issue: "Name" field shows something other than "@"
- In GoDaddy, `@` represents the root domain
- If you see a dropdown, select `@` or leave blank
- Some interfaces show it as blank/empty for root domain

### Issue: Still seeing "Launching Soon" page
1. Check if **"Parked Domain"** is enabled - disable it
2. Check **"Forwarding"** settings - remove any forwarding
3. Make sure you deleted old A records pointing to GoDaddy servers
4. Wait for DNS to propagate (can take up to 48 hours)

### Issue: GoDaddy shows "DNS Error" or "Invalid"
- Make sure you entered the IP addresses correctly
- Don't include `http://` or `https://` in the Value field
- Make sure TTL is a number (600 is fine)

### Issue: Can't add multiple A records with same name
- This is normal! You need 4 separate A records, all with name `@`
- GoDaddy allows multiple A records with the same name
- Add them one at a time

## Quick Checklist

- [ ] Logged into GoDaddy
- [ ] Opened DNS Management for xinzhouvoice.com
- [ ] Deleted old/default A records
- [ ] Added 4 GitHub A records (185.199.108.153, 109.153, 110.153, 111.153)
- [ ] Added www CNAME record (optional)
- [ ] Disabled "Parked Domain" or "Coming Soon" page
- [ ] Saved all changes
- [ ] Configured custom domain in GitHub Pages settings
- [ ] Uploaded CNAME file to GitHub repository
- [ ] Waiting for DNS propagation (check at whatsmydns.net)

## Testing

**After 1-2 hours:**
1. Check DNS propagation: https://www.whatsmydns.net/#A/xinzhouvoice.com
   - Should show: 185.199.108.153, 185.199.109.153, etc.

2. Visit your site: https://xinzhouvoice.com
   - Should show your GitHub Pages website (not "Launching Soon")

3. If still showing placeholder:
   - Double-check DNS records in GoDaddy
   - Make sure "Parked Domain" is disabled
   - Wait longer (up to 48 hours)

## Need Help?

If you're stuck:
1. Take a screenshot of your GoDaddy DNS records page
2. Verify CNAME file is uploaded to GitHub
3. Check GitHub Pages settings have custom domain configured
4. Contact GoDaddy support if DNS records aren't saving

