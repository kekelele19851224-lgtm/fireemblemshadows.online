# Fire Emblem Shadows Fan Hub

**Live site:** [fire emblem shadows](https://fireemblemshadows.online)

A fast, mobile-first, unofficial fan hub for *Fire Emblem Shadows*. This repository contains a lightweight multi-page static site with a Hub-and-Spoke architecture, dark/light theme, accessible components, and SEO-ready markup.

> **Disclaimer:** This is a fan-made site and is **not affiliated** with Nintendo or Intelligent Systems. No official logos, key art, or copyrighted assets are used.

---

## 📁 Project structure

```
index.html                # Hub: overview + intent router
download.html             # Download & install (iOS/Android) + troubleshooting
what-is.html              # What is + trailer overview + disambiguation
deduction-guide.html      # Social deduction & voting guide
teams-gear.html           # Characters, team comps & real-time tactics
bazaar.html               # Bazaar trading, currencies & value tips
updates.html              # Updates & events timeline
faq.html                  # Extended FAQ (optional if kept on home)
robots.txt
sitemap.xml
```

Each page is a **single, self-contained HTML file** (inline CSS/JS, semantic HTML5, SVG illustrations).

---

## 🚀 Run locally

Choose one of the following:

**Python**
```bash
python3 -m http.server 5500
# open http://localhost:5500
```

**Node (serve)**
```bash
npx serve -l 5500 .
# or: npx http-server -p 5500 .
```

**VS Code Live Server**
```
Right-click index.html → "Open with Live Server".
```

---

## 🔗 Internal linking (how pages connect)

**Home → Spokes:**  
Download · What is · Guides (Voting / Teams & Gear / Bazaar) · FAQ · Updates

**Context links inside articles:**

- "download on iOS/Android" → /download.html
- "voting / social deduction / Disciple of Shadow" → /deduction-guide.html  
- "characters / team comps / roles" → /teams-gear.html
- "bazaar / trading / in-game gold" → /bazaar.html
- "updates / events" → /updates.html · "FAQ / troubleshooting" → /faq.html

**Page footer "Next steps" cards:** each spoke page links to 2–3 related pages.

**Breadcrumbs:** every non-home page shows *Home › Guides › Current Page*.

**Tip:** headings (`<h2>`/`<h3>`) auto-generate anchors, enabling deep links like `/download.html#troubleshoot`.

---

## 🧭 SEO checklist (per indexable page)

- `<title>` & `<meta name="description">` include the core keyword **"fire emblem shadows"** plus the page's intent (e.g., download, voting guide).
- **H1** contains *fire emblem shadows*; **H2/H3** use long-tail variants naturally.
- Natural keyword density (~1–2%); avoid stuffing.
- **Structured data:**  
  WebSite (home), Article (long-form pages), FAQPage (FAQ & download fixes), HowTo (install steps), BreadcrumbList (all pages), ImageObject (hero illustration).
- `robots.txt` allows crawling; `sitemap.xml` lists all HTML pages.
- LCP < 2.5s on mobile; images are inline SVG or optimized `<picture>`.

---

## 🎨 Accessibility & design

- Dark/light theme toggle, respects `prefers-color-scheme`.
- Interactive targets ≥ 44×44px; visible focus styles.
- SVGs use `<figure>` + `<figcaption>` with descriptive alt (no keyword stuffing).

---

## 🛠️ Editing guide

- Each page is standalone—open the HTML file you need and edit copy/sections.
- Keep internal anchors stable (e.g., `#ios`, `#android`, `#troubleshoot`, `#disambiguation`).
- Use consistent link text variants (e.g., "voting guide", "team comps", "bazaar basics").

---

## 🌐 Deployment

Any static host works (GitHub Pages, Netlify, Vercel, S3, etc.):

1. Push the repository.
2. Point your host to the project root.
3. Ensure the live domain is set to `https://fireemblemshadows.online`.
4. Verify `sitemap.xml` and `robots.txt` are served at the root.

---

## 🧾 License & attribution

- Content © respective authors.
- This project is for educational and community purposes only.

**Visit the live site:** [fire emblem shadows](https://fireemblemshadows.online)
