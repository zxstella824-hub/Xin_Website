# Upload to GitHub Using GitHub Desktop

## Step-by-Step Instructions

### Step 1: Open GitHub Desktop
1. Launch GitHub Desktop application
2. Sign in with your GitHub account if prompted

### Step 2: Add Your Local Repository
1. Click **File** → **Add Local Repository**
2. Click **Choose...** button
3. Navigate to and select your website folder: `D:\Stella\website`
4. Click **Add Repository**

### Step 3: Connect to Your GitHub Repository
1. If GitHub Desktop asks to publish the repository:
   - Repository name: `Xin_Website`
   - Description: (optional) "Professional website for Xin Zhou"
   - Make sure **"Keep this code private"** is **UNCHECKED** (must be public for free GitHub Pages)
   - Click **Publish Repository**

2. If it doesn't ask to publish, or if you need to connect manually:
   - Click **Repository** → **Repository Settings** → **Remote**
   - Add remote: `origin`
   - Remote URL: `https://github.com/zxstella824-hub/Xin_Website.git`
   - Click **Save**
   - Then click **Repository** → **Push** (or use the Push button in the top toolbar)

### Step 4: Commit Your Changes
1. You'll see all your files listed on the left side
2. At the bottom left, write a commit message: **"Update website: Changed About to Bio"**
3. Click **Commit to main** button

### Step 5: Push to GitHub
1. Click the **Push origin** button (top right, or **Repository** → **Push**)
2. Wait for the upload to complete

### Step 6: Verify Upload
1. Go to https://github.com/zxstella824-hub/Xin_Website
2. You should see all your files including `bio.html` (not `about.html`)

### Step 7: Enable GitHub Pages (Important!)
1. On your GitHub repository page, click **Settings**
2. Scroll down to **Pages** in the left sidebar
3. Under **Source**, select:
   - Branch: **main**
   - Folder: **/ (root)**
4. Click **Save**
5. Wait 2-5 minutes, then visit: **https://zxstella824-hub.github.io/Xin_Website/**

## Troubleshooting

### If GitHub Desktop doesn't recognize your folder as a Git repository:
1. Click **File** → **New Repository**
2. Name: `Xin_Website`
3. Local Path: `D:\Stella\website`
4. Click **Create Repository**
5. Then follow Step 3 above to connect to GitHub

### If you get authentication errors:
- Make sure you're signed in to GitHub Desktop
- You may need to authenticate through your browser

### Files to Upload:
Make sure these files are in your folder:
- ✅ `bio.html` (NEW - replaces about.html)
- ✅ `index.html`
- ✅ `look.html`
- ✅ `listen.html`
- ✅ `calendar.html`
- ✅ `voice-studio.html`
- ✅ `contact.html`
- ✅ `styles.css`
- ✅ `script.js`
- ✅ `README.md`
- ✅ `images/` folder
- ❌ `about.html` (should be deleted - we changed it to bio.html)

## Your Website URL
After enabling GitHub Pages, your site will be live at:
**https://zxstella824-hub.github.io/Xin_Website/**


