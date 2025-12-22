# How to Upload Your Website to GitHub

There are several ways to upload your website to GitHub. Choose the method that works best for you:

## Method 1: Using GitHub Website (Easiest - No Git Required)

### Step 1: Create a GitHub Account
1. Go to [github.com](https://github.com) and sign up if you don't have an account

### Step 2: Create a New Repository
1. Click the "+" icon in the top right corner
2. Select "New repository"
3. Name your repository (e.g., `xinzhou-website` or `xinzhou.github.io`)
4. Choose **Public** (required for free GitHub Pages)
5. **DO NOT** check "Initialize this repository with a README"
6. Click "Create repository"

### Step 3: Upload Files
1. On the new repository page, click "uploading an existing file"
2. Drag and drop ALL files from your `website` folder:
   - `index.html`
   - `about.html`
   - `look.html`
   - `listen.html`
   - `calendar.html`
   - `voice-studio.html`
   - `contact.html`
   - `styles.css`
   - `script.js`
   - `README.md`
   - `.gitignore`
   - `images` folder (drag the entire folder)
3. Scroll down and click "Commit changes"

### Step 4: Enable GitHub Pages
1. Go to your repository on GitHub
2. Click **Settings** (top menu)
3. Scroll down to **Pages** in the left sidebar
4. Under **Source**, select:
   - Branch: **main**
   - Folder: **/ (root)**
5. Click **Save**
6. Wait a few minutes, then your site will be live at:
   `https://yourusername.github.io/repository-name/`

---

## Method 2: Using GitHub Desktop (Easy GUI Method)

### Step 1: Install GitHub Desktop
1. Download from [desktop.github.com](https://desktop.github.com)
2. Install and sign in with your GitHub account

### Step 2: Create Repository
1. In GitHub Desktop, click "File" → "New Repository"
2. Name: `xinzhou-website`
3. Local Path: Choose your `D:\Stella\website` folder
4. Click "Create Repository"

### Step 3: Commit and Push
1. You'll see all your files listed
2. Write a commit message: "Initial website upload"
3. Click "Commit to main"
4. Click "Publish repository" (top right)
5. Choose to make it Public
6. Click "Publish repository"

### Step 4: Enable GitHub Pages
1. Go to your repository on GitHub.com
2. Settings → Pages
3. Source: main branch, / (root)
4. Save

---

## Method 3: Using Command Line (If Git is Installed)

If you install Git, you can use these commands in PowerShell:

```powershell
# Navigate to your website folder
cd D:\Stella\website

# Initialize git repository
git init

# Add all files
git add .

# Create first commit
git commit -m "Initial website upload"

# Add remote repository (replace YOUR_USERNAME and REPO_NAME)
git remote add origin https://github.com/YOUR_USERNAME/REPO_NAME.git

# Push to GitHub
git branch -M main
git push -u origin main
```

---

## After Uploading: Enable GitHub Pages

**Important:** After uploading, you MUST enable GitHub Pages:

1. Go to your repository on GitHub
2. Click **Settings** → **Pages**
3. Under **Source**:
   - Branch: **main**
   - Folder: **/ (root)**
4. Click **Save**

Your website will be available at:
- `https://yourusername.github.io/repository-name/`

---

## Troubleshooting

### If your site doesn't load:
- Wait 5-10 minutes after enabling Pages
- Check that `index.html` is in the root folder
- Make sure the repository is Public (not Private)
- Check Settings → Pages for any error messages

### If images don't show:
- Make sure images are in the `images/` folder
- Check file names match exactly (case-sensitive)
- Use `.jpg` or `.png` extensions

### Custom Domain (Optional):
If you want to use your own domain (e.g., `xinzhou.com`):
1. Create a file named `CNAME` (no extension) in the root
2. Add your domain name inside: `xinzhou.com`
3. Configure your domain's DNS settings

---

## Recommended: Method 1 (GitHub Website)

For beginners, **Method 1** is the easiest - just drag and drop your files!


