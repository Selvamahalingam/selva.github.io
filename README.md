# Mechanical Design Engineer Portfolio Website

A professional, conversion-focused portfolio website for a Freelance Mechanical Design Engineer specializing in SolidWorks, conveyor systems, engineering calculations, and manufacturing drawings.

## 🗂️ Project Structure

```
portfolio/
├── index.html                    ← Main landing page (all sections)
├── css/
│   └── style.css                 ← All styles (variables, layout, components)
├── js/
│   └── main.js                   ← Interactions, animations, form handling
├── pages/
│   ├── blog-roller-conveyor.html ← Blog post: Conveyor capacity calculations
│   ├── blog-parametric-design.html (template — duplicate & edit)
│   └── blog-shaft-design.html   (template — duplicate & edit)
├── assets/
│   ├── cv-mechanical-engineer.pdf   ← Add your CV here
│   └── og-image.jpg                 ← Add social share image (1200×630px)
└── README.md
```

## 📄 Website Sections (All on index.html)

| Section | ID | Description |
|---|---|---|
| Hero | `#hero` | Headline, stats, CTAs |
| Services | `#services` | 6 engineering service cards |
| Portfolio | `#portfolio` | 6 project cards with filter |
| Engineering Capabilities | `#skills` | Skill bars + capability badges |
| Process | `#process` | 6-step project workflow |
| Testimonials | *(inline)* | 3 client reviews |
| Blog | `#blog` | 3 engineering articles |
| About | `#about` | Engineer bio + details |
| Contact | `#contact` | Info + project inquiry form |

## 🎨 Design System

- **Color Palette**: Dark steel (`#0a0c0f`) + Amber accent (`#f59e0b`) + Cyan highlights
- **Fonts**: Syne (headings) · DM Mono (labels/code) · Lato (body)
- **Theme**: Industrial Precision — blueprint-inspired dark aesthetic

## ⚙️ Customization Guide

### 1. Personal Details
Edit `index.html` and replace:
- `hello@mechdesign.pro` → your email
- `MechDesign.pro` → your brand/name
- `Your Name` → your actual name
- Stats (50+ projects, 7+ years, etc.) → your real numbers
- About section text → your real bio

### 2. Projects
Each project card in the `#portfolio` section follows this pattern:
```html
<div class="card project-card" data-category="conveyor|modeling|calculations|drawings">
  <!-- Replace SVG with screenshot/image of your actual work -->
  <div class="project-thumb">
    <img src="../assets/project-name.jpg" alt="Project description" />
  </div>
  ...
</div>
```

Replace the inline SVG illustrations with actual screenshots from your SolidWorks projects.

### 3. Contact Form
The form currently simulates submission. To connect it to a real backend:

**Option A — Formspree (free):**
```html
<form action="https://formspree.io/f/YOUR_FORM_ID" method="POST">
```

**Option B — EmailJS:**
Replace the setTimeout in `main.js` with an EmailJS call.

**Option C — PHP backend:**
```php
// contact.php
mail($to, $subject, $message, $headers);
```

### 4. SEO Meta Tags
Update in `<head>` of index.html:
- `<title>` — include your real name + specializations
- `<meta name="description">` — 150-160 chars, keyword-rich
- `og:url` — your actual domain
- Schema.org JSON-LD — fill in your real details

### 5. CV / Resume
Place your CV PDF at `assets/cv-mechanical-engineer.pdf` to enable the download button.

### 6. Blog Posts
To add more blog posts:
1. Duplicate `pages/blog-roller-conveyor.html`
2. Edit content
3. Update the links in `index.html` blog section

## 🚀 Deployment (GitHub Pages)

```bash
# 1. Create a repository on GitHub named: yourusername.github.io
#    OR any repo name (will deploy to yourusername.github.io/repo-name)

# 2. Initialize and push
git init
git add .
git commit -m "Initial portfolio deploy"
git remote add origin https://github.com/yourusername/your-repo.git
git push -u origin main

# 3. Enable GitHub Pages:
#    Repository Settings → Pages → Source: main branch / root
#    Site will be live at: https://yourusername.github.io
```

### Custom Domain (optional)
1. Add a `CNAME` file in root: `echo "yourdomain.com" > CNAME`
2. Configure your domain DNS to point to GitHub Pages IPs

## 📱 Browser Support
- Chrome, Firefox, Safari, Edge (last 2 versions)
- Mobile: iOS Safari 14+, Android Chrome 90+
- IE11: Not supported (uses CSS custom properties)

## ✅ SEO Checklist
- [x] Meta title and description on all pages
- [x] Keywords: "Mechanical Design Engineer", "SolidWorks Designer", "Conveyor System Design", "Freelance Mechanical Engineering Services"
- [x] Schema.org Person structured data
- [x] Open Graph tags for social sharing
- [x] Semantic HTML5 (`section`, `article`, `nav`, `footer`)
- [x] `aria-label` and `role` attributes for accessibility
- [x] Canonical URLs
- [ ] Add Google Search Console verification meta tag
- [ ] Submit sitemap.xml (create manually or generate)
- [ ] Add Google Analytics or Plausible tracking

## 🔧 Performance Tips
- Compress your project images to WebP format before using
- Host fonts locally for faster loading (download from Google Fonts)
- Add `loading="lazy"` to any `<img>` tags you add
- Consider using a CDN for static assets

---

Built with pure HTML, CSS, and vanilla JavaScript — no frameworks, no build tools needed.
Ready to upload and run on any static hosting provider.
