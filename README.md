# Cebu Tech Merchandise & Lanyards Tracker

A complete web-based tracking system for managing merchandise orders and lanyards. Includes support for Cebu Tech Official Lanyards and BSCpE 1C Evening merchandise (polos, t-shirts, lanyards, pins).

## 🚀 Quick Start

### Option 1: Use Locally (No Internet Required)
1. Download all files to a folder
2. Open `index.html` in your browser
3. Use immediately - no installation needed!

### Option 2: Deploy to GitHub Pages (Free Hosting)
Follow the instructions in `index.html` under "Setup Instructions for GitHub"

## 📁 File Structure

```
cebu-tech-tracker/
├── index.html          # Main dashboard with project links
├── lanyards.html       # Lanyard tracker page
├── merchandise.html    # Merchandise tracker page
├── data.json          # All order data (edit this to update)
├── README.md          # This file
└── .gitignore         # Git ignore file
```

## 💾 Data Format

Edit `data.json` to update your orders. Structure:

### Lanyards
```json
{
  "lanyards": [
    {
      "id": 0,
      "name": "Customer Name",
      "lanyard": "Design Description",
      "price": 150,
      "discount": 0,
      "paid": false
    }
  ]
}
```

### Merchandise
```json
{
  "merchandise": [
    {
      "id": 0,
      "name": "Customer Name",
      "polo": "Design B",
      "poloSize": "L",
      "tshirt": "Design A",
      "tshirtSize": "M",
      "lanyard": "Design B",
      "pins": "5",
      "paid": false
    }
  ]
}
```

## 🔧 Converting Excel to JSON

### Step 1: Copy from Excel
Open your Excel file and select all data

### Step 2: Use Online Converter
Visit: https://www.convertcsv.com/csv-to-json.htm
1. Paste Excel data as TSV (Tab-Separated Values)
2. Convert to JSON
3. Copy the result

### Step 3: Update data.json
Replace the arrays in `data.json` with your new data, keeping the outer structure intact

## 📝 How to Use

### Tracking Orders
1. Open the tracker (lanyards.html or merchandise.html)
2. View summary metrics at the top
3. Search by name or filter by status
4. Click checkboxes to mark items as paid
5. Status updates automatically

### Saving Payment Status
- Payment status is saved locally in your browser
- Close and reopen the page - your data stays
- Status doesn't affect the JSON file (local storage only)

### Updating Order Data
1. Edit `data.json` with new orders
2. Refresh the page
3. New orders appear automatically

## 🌐 GitHub Setup (Recommended)

### Step 1: Create Repository
```bash
# Go to https://github.com/new
# Create repository named: cebu-tech-tracker
# Choose "Public" for free hosting
```

### Step 2: Initialize Locally
```bash
cd path/to/your/project
git init
git add .
git commit -m "Initial commit: Add trackers"
git remote add origin https://github.com/YOUR-USERNAME/cebu-tech-tracker.git
git branch -M main
git push -u origin main
```

### Step 3: Enable GitHub Pages
1. Go to your repo settings: https://github.com/YOUR-USERNAME/cebu-tech-tracker/settings
2. Click "Pages" in the left sidebar
3. Select "Deploy from branch"
4. Choose branch: `main`, folder: `/ (root)`
5. Click "Save"

### Step 4: Access Your Site
Wait ~1 minute, then visit:
```
https://YOUR-USERNAME.github.io/cebu-tech-tracker
```

### Step 5: Update Orders (via Git)
```bash
# Edit data.json with new orders
git add data.json
git commit -m "Update orders"
git push origin main
# Wait ~1 minute for changes to appear online
```

## 💡 Tips

### Bulk Add Orders
Instead of editing JSON manually, you can:
1. Copy all data from Excel
2. Use a CSV to JSON converter
3. Update the array in `data.json`
4. Push to GitHub

### Backup Your Data
```bash
# Create a backup branch
git branch backup-$(date +%Y-%m-%d)
git push origin backup-$(date +%Y-%m-%d)
```

### Collaborate
- Share the GitHub link with team members
- They can view orders online
- Only you can edit (if private) or anyone can help (if public)

## 🔐 Privacy

- **Local Storage**: Payment status saved in browser only
- **Data.json**: Keep it public (no sensitive data) or private (GitHub Private repo)
- **GitHub Pages**: Free public hosting for static sites

## ⚙️ Customization

### Change Lanyard Price
Edit in `data.json`:
```json
"settings": {
  "lanyardPrice": 200,  // Change this
  "lanyardDiscount": 10,
  "currency": "PHP",
  "currencySymbol": "₱"
}
```

### Add More Projects
Copy `lanyards.html` to `newproject.html` and edit the data-loading logic

### Change Colors
Edit the CSS in the HTML files (look for `background:`, `color:`, etc.)

## 🆘 Troubleshooting

### Data not loading
- Check browser console (F12)
- Ensure `data.json` is valid JSON
- Use https://jsonlint.com to validate

### Changes not showing on GitHub Pages
- Wait 1-2 minutes after pushing
- Hard refresh browser (Ctrl+Shift+R)
- Check that files are in the `main` branch

### Can't push to GitHub
```bash
# If authentication fails:
# Use Personal Access Token instead of password
# https://github.com/settings/tokens
```

## 📧 Support

Need help? Check:
- GitHub Pages docs: https://pages.github.com
- Git commands: https://git-scm.com/docs
- JSON format: https://www.json.org

## 📄 License

Free to use and modify. No restrictions.

---

**Last Updated**: August 2026
**Version**: 1.0
