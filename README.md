# haseenxdesign — Personal Portfolio Website

A single-file academic portfolio for **Dr. Md Haseen Akhtar**, Design Researcher and Assistant Professor at IIT Hyderabad. Built with pure HTML and CSS — no frameworks, no build step, no dependencies beyond a Google Fonts import.

---

## Live Sections

| Section | Description |
|---|---|
| **Hero** | Introduction, role, and research tags |
| **About / Philosophy** | Research philosophy cards |
| **Research** | Active projects and emerging ideas |
| **Publications** | Selected peer-reviewed works with DOI links |
| **Teaching** | Courses taught at IIT Hyderabad, UC Berkeley, IIT Kanpur, and NIFT Hyderabad |
| **Education** | Academic credentials, fellowships, and grants |
| **Contact** | Email, phone, and IIT Hyderabad faculty profile link |

---

## File Structure

```
haseenxdesign.html   ← entire site (HTML + CSS, self-contained)
README.md
```

No JavaScript. No build tooling. Everything lives in one file.

---

## Customisation

### Add your photo
Find the `.hero-photo` div and replace the placeholder content with an `<img>` tag:

```html
<div class="hero-photo">
  <img src="your-photo.jpg" alt="Md Haseen Akhtar" style="width:100%; height:100%; object-fit:cover; border-radius:4px;" />
</div>
```

### Add student work images
Replace the `.work-placeholder` divs in the Teaching section:

```html
<div class="work-strip">
  <img src="student-work-1.jpg" alt="Open-Interact-Birth" style="aspect-ratio:4/3; object-fit:cover; border-radius:4px;" />
  <!-- repeat for each image -->
</div>
```

### Update contact details or links
All contact information is in the `#contact` section near the bottom of the file. Email links, phone numbers, and the IIT Hyderabad faculty profile URL can be edited directly.

### Colours
Design tokens are defined as CSS custom properties at the top of the `<style>` block:

```css
:root {
  --cream:   #F8F5F0;
  --fog:     #EDE8E1;
  --blush:   #E8D9CE;
  --sage:    #C8D5C5;
  --accent:  #8FA68C;   /* muted sage green */
  --ink:     #2C2B28;
  --mid:     #6B6760;
}
```

Change `--accent` to shift the brand colour throughout the entire page.

---

## Deployment

### GitHub Pages (recommended)

1. Push this repo to GitHub.
2. Go to **Settings → Pages**.
3. Set source to `main` branch, `/ (root)`.
4. Rename `haseenxdesign.html` to `index.html` so it loads at the root URL.

```bash
mv haseenxdesign.html index.html
git add .
git commit -m "rename to index.html for GitHub Pages"
git push
```

Your site will be live at `https://<your-username>.github.io/<repo-name>/`.

### Netlify / Vercel

Drag and drop the file (renamed `index.html`) into the Netlify drop zone or connect the repo directly — both platforms will serve it immediately with no configuration required.

---

## Typography

- **Cormorant Garamond** (serif) — headings and display text
- **Inter** (sans-serif) — body copy and UI labels

Both loaded via Google Fonts. To use system fonts offline, remove the `<link>` tags and update the `--serif` and `--sans` variables.

---

## Browser Support

Works in all modern browsers. No polyfills required. CSS Grid and custom properties are used throughout; IE is not supported.

---

## License

© 2025 Md Haseen Akhtar · IIT Hyderabad. All rights reserved.
