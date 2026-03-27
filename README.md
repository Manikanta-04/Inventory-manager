<div align="center">

<img src="https://img.shields.io/badge/STOCKR-Inventory%20Dashboard-7c3aed?style=for-the-badge&logo=javascript&logoColor=white" alt="STOCKR Banner"/>

# 📦 STOCKR — Inventory Management Dashboard

### *Sleek Dark-Themed Inventory Dashboard — All in One HTML File*

<br/>

[![Live Demo](https://img.shields.io/badge/🌐%20Live%20Demo-GitHub%20Pages-7c3aed?style=for-the-badge)](https://manikanta-04.github.io/stockr/)

<br/>

[![HTML5](https://img.shields.io/badge/HTML5-Structure-E34F26?style=flat-square&logo=html5&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/HTML)
[![CSS3](https://img.shields.io/badge/CSS3-Dark%20Theme-1572B6?style=flat-square&logo=css3)](https://developer.mozilla.org/en-US/docs/Web/CSS)
[![JavaScript](https://img.shields.io/badge/Vanilla%20JS-ES6+-F7DF1E?style=flat-square&logo=javascript&logoColor=black)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
[![Chart.js](https://img.shields.io/badge/Chart.js-Live%20Charts-FF6384?style=flat-square)](https://chartjs.org)
[![License: MIT](https://img.shields.io/badge/License-MIT-green?style=flat-square)](LICENSE)
[![Status](https://img.shields.io/badge/Status-Active-brightgreen?style=flat-square)]()

</div>

---

## 🚀 Live Demo

| Service | URL |
|---|---|
| 🌐 **STOCKR Dashboard** | [manikanta-04.github.io/stockr](https://manikanta-04.github.io/stockr/) |

> ⚡ No login. No install. Open and manage your inventory instantly.
> *(Update with your actual deployed URL)*

---

## 🎥 Demo Video

> 📽️ *(Add a Loom / YouTube demo walkthrough here)*
>
> [![Watch Demo](https://img.shields.io/badge/▶%20Watch%20Demo-YouTube-red?style=for-the-badge&logo=youtube)](https://youtube.com)

---

## 🧠 Problem Statement

Small businesses and individuals managing inventory are forced to choose between:

- 📊 Heavyweight ERP systems (SAP, Zoho) — expensive, complex, overkill for small teams
- 📋 Static spreadsheets — no alerts, no charts, no real-time filtering
- 🌐 Cloud-based dashboards — require accounts, subscriptions, and internet dependence
- ⚙️ No zero-install option exists — every tool requires setup, frameworks, or a backend

**Small teams need a powerful inventory tool they can just open and use — instantly.**

---

## 💡 Solution

**STOCKR** is a fully client-side inventory management dashboard packed into a single `index.html` file. Full CRUD operations, live Chart.js visualizations, smart stock alerts, real-time search, and a category donut chart — all with zero installs, zero backend, zero frameworks.

> *"Stock smarter. Ship faster."*

---

## 🖼️ Screenshots

| Main Dashboard | Live Charts |
|---|---|
| ![Dashboard](screenshots/dashboard.png) | ![Charts](screenshots/charts.png) |

| Smart Stock Alerts | Category Donut Chart |
|---|---|
| ![Alerts](screenshots/alerts.png) | ![Donut](screenshots/donut.png) |

| Add Item Modal | Real-Time Search |
|---|---|
| ![Add](screenshots/add-item.png) | ![Search](screenshots/search.png) |

> 📌 *(Replace with actual screenshots from your deployed app)*

---

## 🏗️ Architecture

```
┌──────────────────────────────────────────────────────────┐
│              SINGLE FILE APP — index.html                 │
│                                                           │
│  ┌──────────────────────────────────────────────────┐     │
│  │              CSS LAYER                            │     │
│  │  Dark theme design system | Animated stat cards   │     │
│  │  Color-coded alert badges | Responsive grid       │     │
│  └──────────────────────────────────────────────────┘     │
│                                                           │
│  ┌──────────────────────────────────────────────────┐     │
│  │              JAVASCRIPT MODULES                   │     │
│  │  inventoryStore[]    → in-memory data array       │     │
│  │  renderTable()       → DOM table from store       │     │
│  │  addItem()           → push to store + re-render  │     │
│  │  editItem()          → update store entry         │     │
│  │  deleteItem()        → splice + re-render         │     │
│  │  searchFilter()      → live filter on input       │     │
│  │  stockAlerts()       → auto flag low/zero qty     │     │
│  │  updateCharts()      → Chart.js refresh on change │     │
│  │  animateStats()      → count-up on load           │     │
│  └──────────────────────────────────────────────────┘     │
│                                                           │
│  CDN: Chart.js (live charts + donut visualization)        │
└──────────────────────────────────────────────────────────┘
```

---

## ⚙️ Tech Stack

| Layer | Technology | Purpose |
|---|---|---|
| **Structure** | HTML5 | Semantic page markup |
| **Styling** | CSS3 | Dark theme, animations, responsive grid |
| **Logic** | Vanilla JavaScript ES6+ | CRUD, search, alerts, stat animations |
| **Charts** | Chart.js (CDN) | Live bar chart + category donut |
| **Data** | In-memory JS Array | Client-side inventory store |
| **Hosting** | GitHub Pages | Free static hosting |

---

## ✨ Features

### 📊 Live Charts (Chart.js)
- Real-time bar and line charts update as inventory changes
- Reflects current stock levels instantly after every CRUD operation

### 🍩 Category Donut Visualization
- Visual breakdown of inventory percentage per category
- Updates live as items are added, edited, or removed

### 🎯 Animated Stat Cards
- Dynamic count-up animation on dashboard load
- Total Items, Total Value, Low Stock Count, Categories

### 🛠️ Full CRUD Operations
- **Create** — Add new inventory items via modal form
- **Read** — View all items in sortable table
- **Update** — Edit any field inline or via modal
- **Delete** — Remove items with confirmation

### 🚨 Smart Stock Alerts
Color-coded automatic warnings:
| Status | Color | Condition |
|---|---|---|
| ✅ In Stock | 🟢 Green | Quantity above threshold |
| ⚠️ Low Stock | 🟡 Yellow | Quantity below minimum |
| ❌ Out of Stock | 🔴 Red | Quantity is zero |

### 🔍 Real-Time Search
- Instant filtering across all inventory items
- Searches by name and category simultaneously
- No delay — filters on every keystroke

### 🌑 Dark Theme UI
- Eye-friendly dark palette — looks great day and night
- Consistent glassmorphism surface cards
- Clean typography with clear data hierarchy

### 📁 Single File
- Everything — HTML, CSS, JS, charts — in one `index.html`
- Download and double-click to run. No setup ever.

---

## 📊 System Design

```
Data Flow:

[User Action]  (Add / Edit / Delete / Search)
       │
       ▼
[inventoryStore[]]   ← in-memory JavaScript array
       │
       ├── renderTable()     → rebuilds DOM table from store
       ├── stockAlerts()     → scans each item, applies badge class
       ├── updateCharts()    → pushes new data to Chart.js instances
       └── animateStats()    → recalculates totals → count-up display
```

```
CRUD Flow:

ADD ITEM:
  [Form submit] → validate fields → push to inventoryStore[]
              → renderTable() → updateCharts() → animateStats()

EDIT ITEM:
  [Edit click] → populate modal with item data → on save
              → update inventoryStore[index] → re-render all

DELETE ITEM:
  [Delete click] → confirm → splice inventoryStore[index]
               → renderTable() → updateCharts() → animateStats()

SEARCH:
  [Input event] → filter inventoryStore[] by name/category
              → renderTable() with filtered subset (store unchanged)
```

**Inventory Item Schema:**

```javascript
{
  id:         unique identifier,
  name:       "Product Name",
  category:   "Electronics / Clothing / Food / etc.",
  quantity:   number,
  price:      number (₹),
  minStock:   number (alert threshold),
  status:     "in-stock" | "low-stock" | "out-of-stock"
}
```

---

## 🔄 Workflow

```
1. User opens index.html        →  Dashboard renders with sample data
2. Stat cards animate up        →  Total items, value, alerts counted
3. Charts render                →  Bar chart + donut chart from store
4. User searches                →  Table filters live on keystroke
5. User adds item               →  Modal opens → form submit → store updated
6. Charts + stats refresh       →  Instant visual update across all panels
7. Low stock triggers           →  Alert badge auto-applied on threshold breach
8. User edits item              →  Modal pre-filled → save → re-render
9. User deletes item            →  Confirm → splice → all panels update
```

---

## 📈 Performance & Metrics

| Metric | Value |
|---|---|
| Total files | 1 (single `index.html`) |
| External CDN | 1 (Chart.js only) |
| CRUD operations | Full (Create, Read, Update, Delete) |
| Alert tiers | 3 (In Stock / Low / Out of Stock) |
| Chart types | 2 (Bar + Donut) |
| Search scope | Name + Category (simultaneous) |
| Build step required | None |
| Framework required | None |
| Time to load | < 1s (static HTML + CDN) |

---

## 🧪 Testing

```bash
# Open directly in browser
open index.html

# Or serve locally
npx serve .
# Visit: http://localhost:3000

# Manual test checklist:
# ✅ Dashboard loads with sample inventory data
# ✅ Stat cards animate (count-up) on page load
# ✅ Bar chart and donut chart render correctly
# ✅ Add item → table + charts + stats update
# ✅ Edit item → values update across all panels
# ✅ Delete item → row removed, charts refresh
# ✅ Search filters table in real time (no delay)
# ✅ Low stock alert badge auto-appears when below threshold
# ✅ Out of stock badge shows when quantity = 0
# ✅ Fully responsive at 375px (mobile)
# ✅ Works on Chrome, Firefox, Safari, Edge
```

### Browser Compatibility

| Browser | Support |
|---|---|
| Chrome 90+ | ✅ Full |
| Firefox 88+ | ✅ Full |
| Safari 14+ | ✅ Full |
| Edge 90+ | ✅ Full |
| Mobile Chrome | ✅ Full |

---

## 📁 Project Structure

```
stockr/
│
├── index.html      # Entire app — HTML + CSS + JS + Chart.js integration
└── README.md       # Project documentation
```

> Everything — dashboard, CRUD logic, live charts, alerts, search — lives in **one self-contained `index.html` file.**

---

## 🎨 Design System

| Token | Value |
|---|---|
| Primary (Purple) | `#7c3aed` |
| Background | `#1a1a2e` (Deep Dark) |
| Surface | `rgba(255,255,255,0.05)` (Glassmorphism) |
| In Stock | `#22c55e` (Green) |
| Low Stock | `#eab308` (Yellow) |
| Out of Stock | `#ef4444` (Red) |
| Layout | CSS Grid + Flexbox |

---

## 🔐 Security

- **No user data sent anywhere** — fully client-side, nothing leaves the browser
- **No backend** — zero server-side attack surface
- **No eval()** — all JS is safe DOM manipulation
- **No auth required** — local-only tool, no credentials stored
- **GitHub Pages HTTPS** — all traffic served over SSL

---

## ⚙️ Local Development Setup

### Prerequisites

- Any modern browser
- No Node.js, Python, or runtime required

### 1️⃣ Clone the Repository

```bash
git clone https://github.com/manikanta-04/stockr.git
cd stockr
```

### 2️⃣ Open in Browser

```bash
# Direct open
open index.html

# Or serve locally
npx serve .
# Visit: http://localhost:3000
```

---

## 🔑 Environment Variables

No environment variables required — fully static, client-side app.

---

## 🚀 Deployment

### GitHub Pages *(Recommended)*

1. Push `index.html` to `main` branch
2. Go to **Settings → Pages**
3. Source: `main` branch → `/ (root)`
4. Live at: `https://manikanta-04.github.io/stockr/`

### Vercel / Netlify

```bash
# Drag & drop the project folder OR connect GitHub repo
# No build command needed
```

| Setting | Value |
|---|---|
| Framework | Other / Static |
| Build Command | *(leave empty)* |
| Output Directory | `./` |

---

## 🔮 Future Improvements

- [ ] 💾 `localStorage` persistence — data survives page refresh
- [ ] 📤 CSV export — download inventory as spreadsheet
- [ ] 📥 CSV import — bulk upload from Excel/Sheets
- [ ] 🔔 Push notifications for low-stock alerts
- [ ] 🗂️ Multi-category filter panel (checkbox filter)
- [ ] 📅 Expiry date tracking per item
- [ ] 🖨️ Print-ready inventory report
- [ ] 🌐 Multi-user mode with Supabase Realtime backend

---

## 🤝 Contributing

Contributions are welcome and appreciated!

```bash
# 1. Fork this repository
# 2. Create your feature branch
git checkout -b feature/your-feature-name

# 3. Commit with conventional commits
git commit -m "feat: describe your change"

# 4. Push and open a Pull Request
git push origin feature/your-feature-name
```

---

## 👨‍💻 Author

**Manikanta Naripeddi** — Full Stack Developer

[![GitHub](https://img.shields.io/badge/GitHub-Manikanta--04-181717?style=flat-square&logo=github)](https://github.com/manikanta-04)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Manikanta%20Naripeddi-0077b5?style=flat-square&logo=linkedin)](https://www.linkedin.com/in/manikanta-naripeddi-4326232a5/)
[![Email](https://img.shields.io/badge/Email-manikantachowdary296@gmail.com-D14836?style=flat-square&logo=gmail)](mailto:manikantachowdary296@gmail.com)

---

## 📜 License

This project is licensed under the **MIT License** — see the [LICENSE](LICENSE) file for details.

---

## 🙌 Acknowledgements

- [Chart.js](https://www.chartjs.org/) — Live charts and donut visualization
- [GitHub Pages](https://pages.github.com/) — Free static hosting
- [MDN Web Docs](https://developer.mozilla.org/) — JS + CSS reference

---

<div align="center">

**Built with ❤️ for small businesses and solo operators who just need it to work**

⭐ **Star this repo** if STOCKR saved you from a spreadsheet!

[![GitHub Stars](https://img.shields.io/github/stars/manikanta-04/stockr?style=social)](https://github.com/manikanta-04/stockr)

---

*📦 Stock smarter. Ship faster.*

</div>
