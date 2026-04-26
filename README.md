# Vybhav Reddy KC — Portfolio

Personal portfolio site. Single-page, zero dependencies, no build step.

🌐 **Live:** [vybhavk.github.io/portfolio](https://vybhavk.github.io/portfolio/)

---

## About

A static portfolio for [Vybhav Reddy KC](https://www.linkedin.com/in/vybhavreddykc/) — Staff Data Scientist with 10+ years across FinTech, identity verification, fraud detection, and agentic AI systems.

The site is one HTML file. No frameworks, no bundler, no `node_modules`. It loads instantly and is trivial to edit.

---

## Stack

| | |
|---|---|
| **Hosting** | GitHub Pages |
| **Markup** | Single-file HTML |
| **Styling** | Vanilla CSS (variables, grid, flexbox) |
| **Fonts** | Fraunces · Manrope · JetBrains Mono (Google Fonts) |
| **JS** | One IntersectionObserver for scroll-reveal |
| **Build step** | None |

---

## Project structure

```
.
├── index.html       # the entire site
├── favicon.svg      # VK monogram favicon
├── og-image.png     # 1200×630 social-share preview
├── og-image.svg     # editable source for the OG image
├── resume.pdf       # downloadable resume (add your own)
├── .nojekyll        # tells GitHub Pages to skip Jekyll
└── README.md
```

---

## Sections

1. **Hero** — name, tagline, key stats, CTA bar
2. **About** — bio + scope of role + sidebar metadata
3. **Experience** — Socure → Conduent → Cognizant
4. **Selected Work** — 6 production projects with metrics and external links
5. **Voices** — testimonials + LinkedIn recommendations link
6. **Press** — featured-in strip (BusinessWire, Gartner, Finovate, etc.)
7. **Stack** — areas of expertise, languages, platforms
8. **Contact** — email, Calendly, resume, LinkedIn, GitHub

---

## Local preview

Open `index.html` directly in a browser:

```bash
open index.html        # macOS
xdg-open index.html    # Linux
start index.html       # Windows
```

Or run a tiny dev server (better for testing relative links):

```bash
python3 -m http.server 8000
# → http://localhost:8000
```

---

## Deploying changes

The site auto-deploys from the `main` branch via GitHub Pages.

```bash
git add .
git commit -m "Update content"
git push
```

Changes are live in 30–60 seconds at [vybhavk.github.io/portfolio](https://vybhavk.github.io/portfolio/).

To check deploy status: **Settings → Pages** in the repo.

---

## Editing content

Everything lives in `index.html`. Each section is wrapped in a clearly commented block:

```html
<!-- ============ HERO ============ -->
<!-- ============ ABOUT ============ -->
<!-- ============ EXPERIENCE ============ -->
<!-- ============ PROJECTS ============ -->
<!-- ============ TESTIMONIALS ============ -->
<!-- ============ PRESS STRIP ============ -->
<!-- ============ SKILLS ============ -->
<!-- ============ CONTACT ============ -->
```

Just search for the section you want to update and edit the HTML directly.

### Update colors

CSS variables live at the top of the `<style>` block:

```css
:root {
  --bg: #0f1010;          /* page background */
  --ink: #ededea;         /* primary text */
  --accent: #d4ff3a;      /* lime — main accent */
  --serif: 'Fraunces', serif;
  --sans:  'Manrope', sans-serif;
  --mono:  'JetBrains Mono', monospace;
}
```

Change `--accent` to recolor the entire site.

### Add a new project

Find the **Selected Work** section and copy any `<article class="project">` block. Update:

- `project-num` → `/ 07`
- `project-title` → name of the project
- `project-desc` → 1–2 sentence description
- `project-metrics` → key impact numbers
- `project-stack` → tech used
- `project-links` → case study / repo / demo links

### Add a new testimonial

In the **Voices** section, copy any `<figure class="testimonial">` block and replace the quote, name, and role. Use real LinkedIn recommendations whenever possible.

---

## Open Graph / social preview

`og-image.png` is the 1200×630 image that appears when the site is shared on LinkedIn, Twitter, Slack, etc.

To regenerate after editing `og-image.svg`:

```bash
pip install cairosvg
python3 -c "import cairosvg; cairosvg.svg2png(url='og-image.svg', write_to='og-image.png', output_width=1200, output_height=630)"
```

Test the preview after deploy:

- LinkedIn — [Post Inspector](https://www.linkedin.com/post-inspector/)
- Generic — [opengraph.xyz](https://www.opengraph.xyz/)

---

## Custom domain (optional)

To point a domain like `vybhavreddy.com` at this site:

1. Create a `CNAME` file in the repo root with the domain on a single line:

   ```
   vybhavreddy.com
   ```

2. At your registrar, add DNS records:

   - **A records** for `@` →
     ```
     185.199.108.153
     185.199.109.153
     185.199.110.153
     185.199.111.153
     ```
   - **CNAME** for `www` → `vybhavk.github.io`

3. In **Settings → Pages**, add the custom domain and enable **Enforce HTTPS**.

---

## Performance

| Metric | Value |
|---|---|
| Page weight (HTML) | ~30 KB |
| OG image | ~88 KB (loaded only by social crawlers) |
| HTTP requests | 4 (HTML, fonts CSS, fonts WOFF2, favicon) |
| JavaScript | ~250 bytes |
| Build time | 0 ms (no build) |

---

## License

Content (resume copy, project descriptions, testimonials) © Vybhav Reddy KC.

Code (HTML / CSS structure) is freely usable as a template — credit appreciated, not required.

---

## Contact

- 📧 [vybhav19@gmail.com](mailto:vybhav19@gmail.com)
- 💼 [LinkedIn](https://www.linkedin.com/in/vybhavreddykc/)
- 🐙 [GitHub](https://github.com/vybhavk)
- 📅 [Book a 15-min chat](https://calendly.com/vykc19/quick-chat)

---

<sub>Built in Seattle, WA · 2026</sub>
