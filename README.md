# 📈 30-Day 25% Trading Plan Tracker

A clean, interactive HTML dashboard for tracking a 30-day trading challenge with a **25% daily compound growth target**. Built with a dark, terminal-inspired aesthetic and mobile-friendly interface.

![Version](https://img.shields.io/badge/version-1.0.0-blue)
![License](https://img.shields.io/badge/license-MIT-green)

---

## 🎯 Overview

This tool helps traders visualize and track a 30-day growth plan starting from **$5.00** with a **25% daily target**, using **1:2000 leverage**. It provides:

- **Day-by-day balance tracking** with compound interest calculation
- **Interactive checkboxes** to mark days as achieved or missed
- **Milestone indicators** at key profit levels ($10, $50, $100, $500, $1K)
- **Persistent progress** via browser localStorage
- **Progress bar** and statistics dashboard

---

## ✨ Features

### 📊 Auto-Calculated Table
- Pre-calculated balances, daily profits, and expected values for all 30 days
- Compound growth from $5.00 to ~$4,038 by Day 30
- Milestone days highlighted with gold tags

### ✅ Interactive Tracking
- Tap/click any checkbox to cycle through states:
  - **Empty** → Not yet marked
  - **✓ (green)** → Achieved
  - **✗ (red)** → Missed
- State persists even after page refresh

### 📈 Progress Dashboard
- **Start Capital**: $5.00
- **Daily Target**: 25%
- **Day 30 Target**: Automatically calculated
- **Days Done**: Running count of achieved days
- **Progress Bar**: Visual representation of completion

### 🎨 Visual Design
- Dark, trader-friendly theme
- Monospace numbers for financial data
- Gold accent color (#c9a84c) for key metrics
- Hover effects and smooth transitions

---

## 🚀 Quick Start

### Option 1: Direct Use
1. Download the `index.html` file
2. Open it in any modern web browser
3. Start tracking your trades!

### Option 2: Host Online
Upload the file to any static hosting service:
- GitHub Pages
- Netlify
- Vercel
- Cloudflare Pages

---

## 📊 How It Works

### Calculation Logic
```javascript
// Day 1: $5.00 × 1.25 = $6.25
// Day 2: $6.25 × 1.25 = $7.81
// ... compounds daily until Day 30: ~$4,038
```

### Milestone Days
| Day | Target Balance |
|-----|----------------|
| 4   | $10            |
| 11  | $50            |
| 13  | $100           |
| 21  | $500           |
| 24  | $1,000         |

---

## 🎮 Usage Guide

1. **Mark a Day Complete** → Tap the checkbox (✓ appears in green)
2. **Mark a Day Missed** → Tap again (✗ appears in red)
3. **Reset a Day** → Tap a third time (checkbox clears)
4. **Track Progress** → Watch the progress bar and stats update automatically

---

## 🛠️ Technical Details

### Built With
- Pure HTML5, CSS3, and Vanilla JavaScript
- Google Fonts: Barlow + Share Tech Mono
- localStorage for state persistence

### Browser Support
- Works on all modern browsers (Chrome, Firefox, Safari, Edge)
- Mobile-optimized with responsive design

---

## 📁 File Structure

```
/
├── index.html          # Complete single-page application
└── README.md           # Documentation
```

---

## 💾 Data Persistence

Your progress is automatically saved in your browser's `localStorage` using the key `msnr_state`. No data is sent anywhere—it stays entirely on your device.

```javascript
// State structure
{
  "1": 1,  // 0=empty, 1=done, 2=failed
  "2": 0,
  // ... up to day 30
}
```

---

## 🎨 Customization

### Change Starting Capital
```javascript
// Line ~133 in index.html
let bal = 5.00;  // Change to any amount
```

### Modify Daily Target
```javascript
// Line ~134 in index.html
const profit = bal * 0.25;  // Change 0.25 to any decimal
```

### Add/Remove Milestones
```javascript
// Line ~130 in index.html
const milestones = { 
  4: '$10', 
  11: '$50', 
  13: '$100', 
  21: '$500', 
  24: '$1K' 
};
```

---

## 📱 Mobile Support

The interface is fully responsive and optimized for:
- Smartphones (portrait & landscape)
- Tablets
- Desktop screens
- Touch interactions (tap to toggle)

---

## 🤝 Contributing

Feel free to fork and customize for your own trading plans!

### Suggested Improvements
- [ ] Add export/import of progress data
- [ ] Support multiple trading plans
- [ ] Add notes/comments per day
- [ ] Visual charts for performance
- [ ] Sound effects for milestones

---

## 📄 License

MIT License - Free to use, modify, and distribute.

---

## ⚠️ Disclaimer

**This tool is for educational and tracking purposes only.** Trading with leverage carries significant risk. Past performance does not guarantee future results. Always consult with a qualified financial advisor before making investment decisions.

---

## 📞 Support

For issues or questions:
- Open an issue on GitHub
- Check browser console for errors
- Ensure JavaScript is enabled in your browser

---

**Happy Trading! 🚀**
