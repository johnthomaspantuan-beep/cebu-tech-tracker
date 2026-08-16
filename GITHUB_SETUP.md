# Complete GitHub Setup Guide

This guide will walk you through uploading your tracker to GitHub and making it live online.

## Prerequisites

- GitHub account (free at https://github.com)
- Git installed on your computer (https://git-scm.com/download)
- All your tracker files ready

## Step-by-Step Setup

### Phase 1: Prepare Your Local Files

#### 1.1 Create a Project Folder
```bash
# Create and navigate to project folder
mkdir cebu-tech-tracker
cd cebu-tech-tracker
```

#### 1.2 Add All Files
Copy these files to your folder:
- `index.html`
- `lanyards.html`
- `merchandise.html`
- `data.json`
- `README.md`
- `.gitignore`

#### 1.3 Test Locally
Open `index.html` in your browser to make sure everything works

---

### Phase 2: Create GitHub Repository

#### 2.1 Create Repository on GitHub
1. Go to https://github.com/new
2. Fill in:
   - **Repository name**: `cebu-tech-tracker`
   - **Description**: `Merchandise and lanyard tracking for Cebu Tech`
   - **Public** or **Private**: Choose based on your needs
     - **Public**: Anyone can view online (recommended for easy sharing)
     - **Private**: Only invited people can view (more secure)
   - Uncheck "Add a README.md" (you already have one)
3. Click "Create repository"

#### 2.2 Copy Your Repository URL
After creating, you'll see a green "Code" button with a URL like:
```
https://github.com/YOUR-USERNAME/cebu-tech-tracker.git
```
Copy this URL - you'll need it next.

---

### Phase 3: Connect Local Folder to GitHub

#### 3.1 Initialize Git
In your terminal (in your project folder):
```bash
# Initialize git
git init

# Show hidden files to verify
git status
```

#### 3.2 Add Your Remote Repository
```bash
# Replace the URL with your copied URL
git remote add origin https://github.com/YOUR-USERNAME/cebu-tech-tracker.git

# Verify it worked
git remote -v
```

#### 3.3 Make First Commit
```bash
# Add all files to git
git add .

# Create commit with message
git commit -m "Initial commit: Add merchandise trackers"

# Show what will be uploaded
git status
```

#### 3.4 Upload to GitHub
```bash
# Set main branch
git branch -M main

# Push to GitHub
git push -u origin main

# After this, use just:
# git push
```

If you get an authentication error:
- GitHub will prompt for credentials
- Use your username and a Personal Access Token (not password)
- Get token at: https://github.com/settings/tokens
  - Click "Generate new token"
  - Select `repo` scope
  - Copy the token and paste when prompted

---

### Phase 4: Enable GitHub Pages (Make It Live)

#### 4.1 Go to Repository Settings
1. Open your repo on GitHub: https://github.com/YOUR-USERNAME/cebu-tech-tracker
2. Click the "Settings" tab (top right)
3. Click "Pages" in left sidebar

#### 4.2 Configure GitHub Pages
1. Under "Build and deployment":
   - **Source**: Select "Deploy from a branch"
   - **Branch**: Select `main`
   - **Folder**: Select `/ (root)`
2. Click "Save"

#### 4.3 Wait for Deployment
- GitHub will show a banner: "Your site is live at..."
- URL will be: `https://YOUR-USERNAME.github.io/cebu-tech-tracker`
- This takes ~1-2 minutes
- Keep refreshing until you see the green checkmark

#### 4.4 Test Your Site
Visit your new URL! You should see your tracker dashboard.

---

## Updating Your Orders

### Method 1: Edit on GitHub (Web)
1. Go to your repo
2. Click on `data.json`
3. Click the pencil icon to edit
4. Make changes
5. Click "Commit changes"
6. Changes live in ~1 minute

### Method 2: Edit Locally (Recommended)
```bash
# Edit data.json with your favorite editor
# Then upload changes:

git add data.json
git commit -m "Update: Add new orders"
git push

# Changes live in ~1 minute
```

### Method 3: Bulk Import
1. Export your Excel file as CSV
2. Use online converter: https://www.convertcsv.com/csv-to-json.htm
3. Update `data.json` with converted data
4. Commit and push

---

## Common Git Commands

```bash
# Check status
git status

# Add specific file
git add data.json

# Add all changed files
git add .

# Commit with message
git commit -m "Your message here"

# Upload to GitHub
git push

# Download latest changes
git pull

# View commit history
git log

# Create backup branch
git branch backup-$(date +%Y-%m-%d)
git push origin backup-$(date +%Y-%m-%d)

# Undo last commit (keeps changes)
git reset --soft HEAD~1

# Undo last commit (deletes changes)
git reset --hard HEAD~1
```

---

## Troubleshooting

### GitHub Pages Not Working
- Wait 2-3 minutes after enabling
- Hard refresh browser (Ctrl+Shift+R or Cmd+Shift+R)
- Check under Settings → Pages for any errors

### Can't Push to GitHub
```bash
# Reset authentication
git remote remove origin
git remote add origin https://github.com/YOUR-USERNAME/cebu-tech-tracker.git
git push -u origin main
```

### JSON Errors After Editing
- Use https://jsonlint.com to validate your JSON
- Common mistakes:
  - Missing commas between objects
  - Quotes around keys
  - Trailing commas at end of arrays

### Data Not Updating on Site
- Changes take 1-2 minutes to show
- Check your browser cache (Ctrl+Shift+Delete)
- Verify your `data.json` has valid JSON format

---

## Security Tips

### Keep Data Safe
- Don't put passwords or sensitive info in data.json
- Use **Private** repository if data should be confidential
- GitHub Pages only works for public files anyway

### Collaborate Safely
1. Give people the GitHub link only
2. If you want others to edit:
   - Add them as collaborators (Repo Settings → Collaborators)
   - Or make it public and they can suggest changes via pull requests

---

## Next Steps

1. **Share Your Tracker**
   - Share the GitHub Pages URL with your team
   - They can view live data anytime

2. **Automate Updates**
   - Set reminders to update `data.json` weekly
   - Keep orders current

3. **Add More Features**
   - Duplicate trackers for new projects
   - Customize colors in HTML files
   - Add new columns to JSON

4. **Backup Regularly**
   - Create backup branches with dates
   - You can revert if needed

---

## Questions?

- GitHub Docs: https://docs.github.com
- Git Help: https://git-scm.com/doc
- My Issues: Ask in your local group

---

**You're all set!** Your tracker is now live and ready to use. 🎉
