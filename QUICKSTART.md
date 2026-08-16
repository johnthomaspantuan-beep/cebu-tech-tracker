# Quick Start Guide - Cebu Tech Tracker

## 🚀 Get Started in 5 Minutes

### Option A: Use Immediately (Offline)
1. Download all 7 files to a folder
2. Open `index.html` in your browser
3. Done! Use right now.

### Option B: Host on GitHub (Online, Free)
Follow the **GitHub Deployment** section below.

---

## 📂 What You Got

### 7 Files Ready to Use:

| File | Purpose |
|------|---------|
| `index.html` | Main dashboard - links to both trackers |
| `lanyards.html` | Cebu Tech Lanyards tracker |
| `merchandise.html` | BSCpE merchandise tracker |
| `data.json` | Your order data - EDIT THIS to update |
| `README.md` | Full documentation |
| `GITHUB_SETUP.md` | How to deploy to GitHub Pages |
| `.gitignore` | Git configuration |

---

## ✅ What It Does

### Dashboard (index.html)
- Shows quick stats for both projects
- Links to detailed trackers
- Live total calculations

### Lanyard Tracker (lanyards.html)
- All 7 lanyard orders
- Total amount: ₱1,050
- Toggle paid status with checkboxes
- Search and filter options
- Real-time calculations

### Merchandise Tracker (merchandise.html)
- All 14 merchandise orders
- Track polos, t-shirts, lanyards, pins
- Filter by product type
- See who ordered what
- Payment tracking

---

## 💾 Update Your Orders

### Edit data.json (Easiest Method)

Open `data.json` in any text editor. It contains:

```json
{
  "lanyards": [
    {
      "id": 0,
      "name": "Customer Name",
      "lanyard": "Design",
      "price": 150,
      "discount": 0,
      "paid": false
    }
  ],
  "merchandise": [
    {
      "id": 0,
      "name": "Customer Name",
      "polo": "Design B",
      "poloSize": "L",
      "tshirt": null,
      "tshirtSize": null,
      "lanyard": "Design",
      "pins": "5",
      "paid": false
    }
  ]
}
```

### To Add New Orders:
1. Copy a similar object
2. Change the `id` (increment by 1)
3. Update all fields
4. Make sure commas are correct
5. Save file
6. Refresh browser

### Example - Add a Lanyard:
```json
{
  "id": 7,
  "name": "Juan Dela Cruz",
  "lanyard": "COE Design C",
  "price": 150,
  "discount": 0,
  "paid": false
}
```

---

## 🌐 Deploy to GitHub (Free Hosting)

### Step 1: Create GitHub Account
Go to https://github.com and sign up (free)

### Step 2: Create Repository
1. Click "+" → "New repository"
2. Name: `cebu-tech-tracker`
3. Description: "Merchandise and lanyard tracking"
4. Choose "Public" (for easy sharing)
5. Click "Create repository"

### Step 3: Upload Files
Option A - Drag & Drop (Easiest):
1. Click "Add file" → "Upload files"
2. Drag your 7 files to upload
3. Click "Commit changes"

Option B - Use Command Line (More Control):
```bash
# Open terminal/command prompt in your project folder
cd path/to/cebu-tech-tracker

# Initialize git
git init

# Add files
git add .

# Commit
git commit -m "Initial commit: Add trackers"

# Add remote (replace YOUR-USERNAME)
git remote add origin https://github.com/YOUR-USERNAME/cebu-tech-tracker.git

# Upload
git push -u origin main
```

### Step 4: Enable GitHub Pages
1. Go to your repo Settings
2. Click "Pages" in left sidebar
3. Source: "Deploy from branch"
4. Branch: "main"
5. Folder: "/ (root)"
6. Click "Save"

### Step 5: Get Your Live URL
Wait 1-2 minutes, then visit:
```
https://YOUR-USERNAME.github.io/cebu-tech-tracker
```

Your tracker is now LIVE! 🎉

---

## 📝 Daily Usage

### Offline (Local File)
1. Open `index.html` in browser
2. Click tracker you need
3. Use normally
4. Close browser

### Online (GitHub Pages)
1. Visit your URL anytime
2. View from anywhere
3. Share the link with team

### Update Orders
1. Edit `data.json`
2. **If offline**: Refresh browser
3. **If on GitHub**: 
   - Edit on GitHub website, OR
   - Edit locally + git push + wait 1-2 min

---

## 🎨 Customize

### Change Colors
Edit the `<style>` section in HTML files:
```css
body { background: #f5f5f5; }  /* Page background */
h1 { color: #0b0b0b; }         /* Text color */
```

### Change Lanyard Price
In `data.json`, update:
```json
"settings": {
  "lanyardPrice": 200  /* Change from 150 to 200 */
}
```

### Change Currency
```json
"settings": {
  "currency": "PHP",
  "currencySymbol": "₱"  /* Change to $ or € */
}
```

---

## ❓ Common Questions

**Q: Will my data be lost if I close the browser?**
A: Payment status (checked/unchecked) is saved locally. Order data stays in `data.json`.

**Q: Can I use this offline?**
A: Yes! Just download files and open `index.html`. Works perfectly offline.

**Q: Can my team edit orders?**
A: 
- **Offline**: Share files, everyone edits `data.json`
- **GitHub Public**: Anyone can suggest edits via pull requests
- **GitHub Private**: Invite collaborators only

**Q: How do I backup my data?**
A: 
- If on GitHub: Data is auto-backed up
- If local: Copy the folder to another location

**Q: How often should I update?**
A: As needed. Update whenever someone pays or orders something.

---

## 🆘 Troubleshooting

### Files not loading on GitHub
- Wait 2-3 minutes after uploading
- Hard refresh browser (Ctrl+Shift+R)

### JSON format errors
- Use https://jsonlint.com to check
- Common mistake: Missing commas

### Can't upload to GitHub
- Use Personal Access Token instead of password
- Get one at: https://github.com/settings/tokens

---

## 📞 Need Help?

Read the full docs:
- `README.md` - Complete documentation
- `GITHUB_SETUP.md` - Detailed GitHub guide

---

**You're ready to go!** 🚀

Start with Option A (offline) to test, then move to Option B (GitHub) for team access.
