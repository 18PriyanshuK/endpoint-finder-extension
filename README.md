<div align="center">

```
███████╗███╗   ██╗██████╗ ██████╗  ██████╗ ██╗███╗   ██╗████████╗
██╔════╝████╗  ██║██╔══██╗██╔══██╗██╔═══██╗██║████╗  ██║╚══██╔══╝
█████╗  ██╔██╗ ██║██║  ██║██████╔╝██║   ██║██║██╔██╗ ██║   ██║   
██╔══╝  ██║╚██╗██║██║  ██║██╔═══╝ ██║   ██║██║██║╚██╗██║   ██║   
███████╗██║ ╚████║██████╔╝██║     ╚██████╔╝██║██║ ╚████║   ██║   
╚══════╝╚═╝  ╚═══╝╚═════╝ ╚═╝      ╚═════╝ ╚═╝╚═╝  ╚═══╝   ╚═╝   
███████╗██╗███╗   ██╗██████╗ ███████╗██████╗ 
██╔════╝██║████╗  ██║██╔══██╗██╔════╝██╔══██╗
█████╗  ██║██╔██╗ ██║██║  ██║█████╗  ██████╔╝
██╔══╝  ██║██║╚██╗██║██║  ██║██╔══╝  ██╔══██╗
██║     ██║██║ ╚████║██████╔╝███████╗██║  ██║
╚═╝     ╚═╝╚═╝  ╚═══╝╚═════╝ ╚══════╝╚═╝  ╚═╝
```

### Automatic URL and API Endpoint Discovery — Chrome Extension

*Instantly surface every URL, API endpoint, and resource link on any website — right from your browser toolbar.*

<br/>

<img src="https://img.shields.io/badge/JavaScript-ES6-f7df1e?style=for-the-badge&logo=javascript&logoColor=black&labelColor=1a1a2e"/>
<img src="https://img.shields.io/badge/HTML5-Structure-e34f26?style=for-the-badge&logo=html5&logoColor=white&labelColor=1a1a2e"/>
<img src="https://img.shields.io/badge/CSS3-Styles-1572b6?style=for-the-badge&logo=css3&logoColor=white&labelColor=1a1a2e"/>
<img src="https://img.shields.io/badge/Chrome-Extension-4285f4?style=for-the-badge&logo=googlechrome&logoColor=white&labelColor=1a1a2e"/>
<img src="https://img.shields.io/badge/No%20Dependencies-Zero%20External%20Libs-10b981?style=for-the-badge&logoColor=white&labelColor=1a1a2e"/>

<br/><br/>

</div>

---

## 📸 Demo

<img width="1919" height="1014" alt="Endpoint Finder Demo" src="https://github.com/user-attachments/assets/22c818dd-54f4-4786-9ee3-ace8707a9e30" />

---

## 📖 What is Endpoint Finder?

**Endpoint Finder** is a lightweight Chrome browser extension that automatically discovers and lists every URL, API endpoint, and resource link present on any website you visit — all in a clean, searchable popup. No configuration, no external tools, no command line required.

Whether you are a bug bounty hunter mapping attack surface, a developer exploring a third-party site's structure, a security researcher doing reconnaissance, or just curious about what endpoints a website exposes, Endpoint Finder gives you instant visibility with a single click.

---

## ✨ Features

- 🔍 **Automatic Discovery** — Detects all URLs and endpoints loaded on the current page instantly
- 🔗 **Clickable Links** — Every discovered endpoint opens in a new tab on click
- 🔎 **Real-Time Search** — Filter endpoints by keyword — find `api`, `login`, `admin`, `user` in seconds
- 🧹 **Deduplication** — Filters out repeated URLs so you see a clean, unique list
- 📦 **Zero Dependencies** — No external libraries, no API keys, no permissions beyond the active tab
- ⚡ **Instant Results** — No page reload needed — works on the currently open page
- 🎨 **Clean UI** — Sleek popup interface designed for fast, distraction-free usage

---

## 🛠️ Tech Stack

| Technology | Purpose |
|------------|---------|
| JavaScript (ES6) | DOM parsing, URL extraction, search and dedup logic |
| HTML5 | Popup interface structure |
| CSS3 | Popup styling and layout |
| Chrome Extensions API | Browser tab access and popup rendering |

---

## 📁 Project Structure

```
endpoint-finder-extension/
│
├── manifest.json         # Extension manifest — permissions and metadata
├── popup.html            # Popup UI shown on icon click
├── popup.js              # Core logic — DOM parsing, URL extraction, search
├── styles.css            # Popup styling
├── README.md             # Project documentation
│
└── icons/                # Extension icons
    ├── icon16.png
    ├── icon48.png
    └── icon128.png
```

---

## 🧠 How It Works

```
User clicks Endpoint Finder icon
            │
            ▼
Extension accesses current tab's DOM
            │
            ▼
Parser scans for endpoint sources:
  ├── <a href="...">          →  Hyperlinks
  ├── <script src="...">      →  JavaScript files
  ├── <link href="...">       →  Stylesheets and resources
  ├── <form action="...">     →  Form submission endpoints
  └── XHR / fetch requests    →  API calls (where accessible)
            │
            ▼
URLs filtered and deduplicated
            │
            ▼
Clean list rendered in popup
            │
            ├── Click any URL  →  Opens in new tab
            └── Type in search →  Filters list in real time
```

---

## 📦 Installation

### Developer Mode (From Source)

**1. Clone the repository:**
```bash
git clone https://github.com/18PriyanshuK/endpoint-finder-extension.git
cd endpoint-finder-extension
```

**2. Open Chrome and navigate to:**
```
chrome://extensions/
```

**3. Enable Developer Mode:**
Toggle the **Developer mode** switch in the top-right corner.

**4. Load the extension:**
Click **Load unpacked** → Select the `endpoint-finder-extension` folder.

**5. Pin the extension:**
Click the puzzle icon in the Chrome toolbar → Pin **Endpoint Finder**.

✅ The extension is now active on every tab you visit.

---

## ▶️ Usage

**1.** Navigate to any website you want to analyse.

**2.** Click the **Endpoint Finder** icon in the Chrome toolbar.

**3.** The popup instantly displays all discovered URLs and endpoints.

**4.** Use the **search bar** to filter results:

| Search term | Finds |
|-------------|-------|
| `api` | All API endpoint URLs |
| `login` | Authentication endpoints |
| `admin` | Admin panel paths |
| `user` | User-related routes |
| `.json` | JSON data endpoints |
| `v1` / `v2` | API versioned routes |

**5.** Click any URL in the list to open it in a new tab.

---

## 🎯 Use Cases

| Use Case | How Endpoint Finder Helps |
|----------|--------------------------|
| 🐛 Bug Bounty Hunting | Rapidly map all endpoints for attack surface analysis |
| 🔐 Security Reconnaissance | Discover hidden or undocumented API routes |
| 👨‍💻 Developer Exploration | Understand how a third-party site is structured |
| 📚 Learning Web Security | See what a real-world site exposes in its DOM |
| 🧪 API Testing | Quickly find API base URLs and endpoints to test |

---

## 🔮 Future Enhancements

- [ ] Export discovered endpoints as `.txt` or `.json`
- [ ] Copy all URLs to clipboard with one click
- [ ] Categorise endpoints by type (API, static, forms, scripts)
- [ ] WebSocket and dynamic XHR request capture
- [ ] Integration with OWASP ZAP for automated scanning
- [ ] Firefox and Edge browser support
- [ ] Severity tagging for sensitive endpoint patterns

---

## 🤝 Contributing

Contributions and feature suggestions are welcome.

```bash
# Fork the repository
git fork https://github.com/18PriyanshuK/endpoint-finder-extension.git

# Create a feature branch
git checkout -b feature/your-feature-name

# Commit your changes
git commit -m "Add: your feature description"

# Push and open a Pull Request
git push origin feature/your-feature-name
```

Ideas for contribution:
- Exporting URLs as `.txt` or `.json`
- WebSocket and dynamic request support
- OWASP ZAP integration
- Multi-browser support

---

## 📜 License

This project is licensed under the [MIT License](https://github.com/PriyanshuKhambalkar/Endpoint-finder-extension/blob/da84db5d420f7a525549e71859883932f3adb9f1/LICENSE) - see the LICENSE file for details.<br/>
For commercial use or redistribution, please contact the author.

---

## 👤 Author

**Priyanshu Khambalkar**


---

<div align="center">

*Built with JavaScript · Chrome Extensions API · Zero Dependencies*

⭐ **Star this repo if it saved you time on recon**

</div>
