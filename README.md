<div align="center">

# ⚡ rasel.dev

### A code-editor-themed developer portfolio, built to look like VS Code itself.

[![Live Demo](https://img.shields.io/badge/demo-live-7FDBB6?style=for-the-badge&logo=vercel&logoColor=white)](https://rasel.dev)
[![HTML5](https://img.shields.io/badge/HTML5-E44D26?style=for-the-badge&logo=html5&logoColor=white)](#)
[![CSS3](https://img.shields.io/badge/CSS3-264DE4?style=for-the-badge&logo=css3&logoColor=white)](#)
[![JavaScript](https://img.shields.io/badge/JavaScript-F1E05A?style=for-the-badge&logo=javascript&logoColor=black)](#)
[![GitHub API](https://img.shields.io/badge/GitHub_API-live_data-181717?style=for-the-badge&logo=github&logoColor=white)](#)

<br>

<img src="https://img.shields.io/badge/status-actively%20maintained-brightgreen?style=flat-square" alt="status">
<img src="https://img.shields.io/badge/license-MIT-blue?style=flat-square" alt="license">
<img src="https://img.shields.io/badge/no%20frameworks-vanilla%20JS-orange?style=flat-square" alt="vanilla js">

</div>

---

## 📸 Preview

> Add a screenshot or GIF here — it's the single biggest thing that sells a portfolio repo.
>
> ```md
> ![preview](./preview.png)
> ```

## ✨ Overview

**rasel.dev** isn't your typical portfolio template — it's a fully interactive recreation of a **VS Code-style code editor**, rendered entirely in the browser. Every section of the site — Hero, About, Skills, Experience, Projects, GitHub Stats, Certifications, and Contact — is styled as a "file" that opens in an editor pane, complete with:

- A working title bar, activity bar, file explorer sidebar, and status bar
- Syntax-highlighted "code" as real content
- A tab strip for navigating between sections, synced to scroll position
- A live terminal-style footer and a real-time clock in the status bar
- **Live GitHub stats** pulled directly from the GitHub REST API — no backend required

The result feels less like a static page and more like a tool developers will instantly recognize and enjoy exploring.

## 🧩 Features

| Feature | Description |
|---|---|
| 🖥️ **Editor Chrome** | Title bar with traffic-light dots, activity bar, collapsible file-explorer sidebar, and status bar — all functional UI, not just decoration |
| 📁 **File-Based Sections** | Hero, About, Skills, Experience, Projects, GitHub Stats, Certifications, and Contact are each modeled as an open "file" |
| 🧭 **Synced Navigation** | Sidebar files and the top tab strip stay in sync with scroll position via `IntersectionObserver` |
| 📊 **Live GitHub Integration** | Fetches real repo count, stars, forks, followers, top languages, recently pushed repos, and recent commit activity straight from `api.github.com` — cached per session |
| 🏆 **Certifications Grid** | Auto-laid-out grid of clickable, verifiable credentials |
| 📬 **Contact Section** | Styled "form" plus quick-link cards for email, Fiverr, Upwork, phone, GitHub, and LinkedIn |
| 📱 **Fully Responsive** | Sidebar becomes a slide-out drawer, tab strip collapses to icons, and typography scales fluidly on mobile |
| 🎨 **Editor-Accurate Theming** | Custom color tokens for keywords, strings, functions, tags, and comments — styled like a real syntax-highlighted theme (JetBrains Mono + Inter) |
| ⚡ **Zero Dependencies** | No frameworks, no build step, no bundler — just HTML, CSS, and vanilla JavaScript in a single file |

## 🛠️ Tech Stack

- **Markup/Styling:** Semantic HTML5 + hand-written CSS (custom properties, `clamp()`, CSS Grid & Flexbox)
- **Scripting:** Vanilla JavaScript (`IntersectionObserver`, `fetch`, `sessionStorage`)
- **Fonts:** [JetBrains Mono](https://www.jetbrains.com/lp/mono/) & [Inter](https://rsms.me/inter/) via Google Fonts
- **Data:** [GitHub REST API](https://docs.github.com/en/rest) (`/users/{user}`, `/users/{user}/repos`, `/users/{user}/events/public`)

No React, no Tailwind, no build tools — just a single, portable `.html` file.

## 📂 Project Structure

```
.
├── main_3.html      # Everything: markup, styles, and scripts in one file
└── README.md        # You're here
```

Because the entire site lives in one file, it's trivially easy to fork, host, or drop into any static file server.

## 🚀 Getting Started

### Run it locally

No build step, no dependencies — just open it:

```bash
git clone https://github.com/iamraselmolla/rasel.dev.git
cd rasel.dev
open main_3.html   # or double-click the file / drag into a browser
```

Or serve it locally to avoid any `fetch` / CORS quirks:

```bash
python3 -m http.server 8000
# then visit http://localhost:8000/main_3.html
```

### Deploy it

Since it's a static file, it deploys anywhere in seconds:

- **Vercel / Netlify:** drag-and-drop the file or connect the repo
- **GitHub Pages:** rename to `index.html`, push to `main`, enable Pages in repo settings
- **Any static host:** it's just HTML — upload and go

## ⚙️ Customization

All personal content lives inline in the HTML, organized by section ID:

| Section | Element ID | What to edit |
|---|---|---|
| Hero | `#hero` | Name, tagline, intro copy |
| About | `#about` | Bio paragraphs, key-value facts |
| Skills | `#skills` | Skill categories and tags (`.skill-cat`) |
| Experience | `#work` | Timeline entries (`.log-line`) |
| Projects | `#projects` | Project cards (`.proj`) |
| GitHub Stats | `#github` | Set `GH_USER` near the bottom of the `<script>` tag |
| Certifications | `#certs` | Credential cards (`.cert-card`) |
| Contact | `#contact` | Contact links (`.contact-card`) |

To point the live GitHub panel at your own account, update this line in the script:

```js
const GH_USER = 'iamraselmolla'; // 👈 change to your GitHub username
```

All colors, fonts, and spacing are controlled by CSS custom properties at the top of the `<style>` block (`:root { --bg, --func, --string, --keyword, ... }`) — tweak these to reskin the whole theme in one place.

## 🌐 Browser Support

Works in all modern evergreen browsers (Chrome, Firefox, Safari, Edge). Uses `IntersectionObserver` and `fetch`, both broadly supported — no polyfills needed for current browser versions.

## 🤝 Connect

<div align="center">

[![Email](https://img.shields.io/badge/Email-raselmolla6336%40gmail.com-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:raselmolla6336@gmail.com)
[![GitHub](https://img.shields.io/badge/GitHub-iamraselmolla-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/iamraselmolla)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-iamraselmolla-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/iamraselmolla)
[![Fiverr](https://img.shields.io/badge/Fiverr-raselmolla6336-1DBF73?style=for-the-badge&logo=fiverr&logoColor=white)](https://www.fiverr.com/raselmolla6336)

</div>

## 📄 License

This project is licensed under the [MIT License](LICENSE) — feel free to fork it, reskin it, and make it your own. A star ⭐ is always appreciated if it helped you build your own portfolio.

---

<div align="center">
<sub>Built with ☕ and way too many hours in an actual code editor, by <a href="https://github.com/iamraselmolla">Md Rasel Molla</a>.</sub>
</div>