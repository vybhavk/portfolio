# Vybhav Reddy KC — Portfolio

Personal portfolio site. Single-page, no build step, ready for GitHub Pages.

---

## 🚀 Deploy to GitHub Pages (5 minutes)

### Option A — User site at `vybhavreddykc.github.io` (recommended)

This gives you the cleanest URL.

1. **Create the repo on GitHub**
   - Repo name **must** be exactly: `<your-username>.github.io`
   - Example: if your username is `vybhavreddykc`, name it `vybhavreddykc.github.io`
   - Make it **Public**

2. **Push this folder to the repo**
   ```bash
   cd portfolio
   git init
   git add .
   git commit -m "Initial portfolio"
   git branch -M main
   git remote add origin https://github.com/<your-username>/<your-username>.github.io.git
   git push -u origin main
   ```

3. **Enable Pages**
   - Go to repo → **Settings** → **Pages**
   - Source: **Deploy from a branch**
   - Branch: **main** · Folder: **/ (root)** → Save

4. **Done.** Site live at `https://<your-username>.github.io` in ~1 minute.

### Option B — Project site (e.g. `username.github.io/portfolio`)

1. Create any public repo (e.g. `portfolio`).
2. Push these files to `main`.
3. **Settings → Pages** → Source: **main / root** → Save.
4. Site live at `https://<your-username>.github.io/portfolio/`.

---

## 🌐 Add a custom domain (optional)

1. Buy a domain (Namecheap, Cloudflare, Google Domains).
2. Create a file named `CNAME` in this repo with your domain on a single line:
   ```
   vybhavreddy.com
   ```
3. At your domain registrar, add DNS records pointing to GitHub Pages:
   - **A records** for `@`:
     ```
     185.199.108.153
     185.199.109.153
     185.199.110.153
     185.199.111.153
     ```
   - **CNAME record** for `www` → `<your-username>.github.io`
4. In repo **Settings → Pages**, add the custom domain and check "Enforce HTTPS".

---

## ✏️ Editing content

Everything lives in **`index.html`** — no frameworks, no build. Just open in any editor and change text directly.

Sections (search for these comments to jump):
- `<!-- ============ HERO ============ -->` — Name, tagline, stats
- `<!-- ============ ABOUT ============ -->` — Bio paragraphs and side metadata
- `<!-- ============ EXPERIENCE ============ -->` — Job history
- `<!-- ============ PROJECTS ============ -->` — Featured work cards
- `<!-- ============ SKILLS ============ -->` — Stack
- `<!-- ============ CONTACT ============ -->` — Email + links

### Customize colors
At the top of the `<style>` block, edit CSS variables:
```css
--bg: #0f1010;          /* page background */
--accent: #d4ff3a;      /* electric lime accent */
--accent-warm: #ff7a3d; /* secondary accent */
```

### Update social links
In the **Contact** section near the bottom, replace:
- LinkedIn URL ✅ already set to your profile
- `https://github.com/` ← add your GitHub username
- Email ✅ already set
- Phone ✅ already set

---

## 🧪 Preview locally

Just open the file:
```bash
open index.html       # macOS
xdg-open index.html   # Linux
start index.html      # Windows
```

Or run a tiny dev server:
```bash
python3 -m http.server 8000
# → http://localhost:8000
```

---

## 📁 Files

```
portfolio/
├── index.html       ← the entire site
├── README.md        ← this file
└── .nojekyll        ← tells GitHub Pages to skip Jekyll processing
```

Built clean: zero dependencies, ~1 file, instant load.
