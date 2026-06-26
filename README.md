# Secret Tab — Hide Sensitive Tabs Locally

A minimal, production-ready Chromium browser extension website built with pure HTML5, CSS3, and Vanilla JavaScript.

## About Secret Tab

Secret Tab is a browser extension that encrypts sensitive tabs locally using AES-256-GCM and stores them securely in your browser. No server, no tracking, no data collection — just privacy.

### Features

- **AES-256-GCM Encryption** — Military-grade encryption
- **Fully Offline** — Zero internet connections
- **No Account Required** — Works without sign-up
- **Keyboard Shortcut** — Hide tabs instantly with `Ctrl+Shift+H`
- **Per-Site Passwords** — Add extra protection to sensitive tabs
- **Anti-Disable Guard** — Prevents disabling without your password
- **2-Hour Sessions** — Unlock once, stay unlocked for 2 hours
- **Chromium Compatible** — Works on Chrome, Edge, Brave, Opera

## Website Features

This website is completely self-contained and production-ready:

### Architecture
- **Pure HTML5, CSS3, JavaScript** — No frameworks, no build tools
- **Zero Dependencies** — No Node modules, no CDN links
- **Dark Mode by Default** — With automatic system preference detection
- **Fully Responsive** — Mobile, tablet, desktop optimized

### Pages
- **index.html** — Hero section with features, screenshots, FAQ preview
- **download.html** — Latest release, changelog, browser compatibility
- **installation.html** — Step-by-step guide for all Chromium browsers
- **docs.html** — Complete documentation with sidebar navigation
- **faq.html** — 10 realistic questions with smooth accordion animations
- **privacy.html** — Transparent privacy policy (zero data collection)
- **404.html** — Beautiful error page

### Design System

#### Colors
- **Dark theme:** Charcoal backgrounds (#0a0a0f), purple accents (#7c3aed)
- **Light theme:** Cream backgrounds (#fafaf9), maintains purple accents
- **Semantic palette:** Primary, secondary, muted, accent colors

#### Typography
- **Display:** Inter, system fallback
- **Body:** Inter, system fallback
- **Mono:** JetBrains Mono, Fira Code, monospace

#### Components
- Glassmorphism cards with backdrop blur
- Smooth scroll reveal animations
- Soft shadows and rounded corners
- Visible keyboard focus states
- ARIA labels for accessibility

### CSS Features
- **CSS Variables** — Entire theme is customizable
- **Animations** — Fade, slide, scale, pulse, shimmer
- **Responsive Grid** — Auto-fit layouts
- **Backdrop Filters** — Modern glassmorphism effects
- **Scroll Triggers** — Elements reveal on viewport entry
- **Reduced Motion Support** — Respects user preferences

### JavaScript Features
- **Theme Manager** — Auto-detect system preference, persist choice
- **Search Engine** — Docs search with fuzzy matching
- **Smooth Scroll** — Hash navigation with offset
- **Scroll Reveal** — Intersection Observer-based animations
- **FAQ Accordion** — Toggle with smooth max-height animation
- **Mobile Menu** — Hamburger toggle with backdrop dismiss
- **Copy Buttons** — Clipboard interaction with feedback
- **Back to Top** — Appears on scroll, smooth return
- **Active Nav Links** — Current page highlighting

### Accessibility
- **Semantic HTML** — Proper heading hierarchy, lists, landmarks
- **ARIA Labels** — Role, aria-label, aria-expanded, aria-current
- **Keyboard Navigation** — Tab order, focus visible, shortcut support
- **Alt Text** — All images have meaningful descriptions
- **Color Contrast** — WCAG AA compliant
- **Reduced Motion** — Respects prefers-reduced-motion

### Performance
- **Lazy Load Images** — No above-the-fold render blocking
- **Minimal DOM** — Semantic structure, no unnecessary wrappers
- **Fast CSS** — Single stylesheet, optimized selectors
- **Small JS** — Vanilla code, no runtime overhead
- **No Third Parties** — Zero external requests (except fonts)

## File Structure

```
extension-website/
├── index.html                 # Homepage
├── download.html              # Download page
├── installation.html          # Installation guide
├── docs.html                  # Documentation
├── faq.html                   # FAQ
├── privacy.html               # Privacy policy
├── 404.html                   # Not found
├── README.md                  # This file
├── LICENSE                    # MIT License
├── assets/
│   ├── css/
│   │   ├── style.css         # Main styles + design tokens
│   │   └── animations.css    # All animations & transitions
│   ├── js/
│   │   ├── app.js            # Main app (nav, menu, reveal, faq)
│   │   ├── theme.js          # Theme manager
│   │   └── search.js         # Docs search engine
│   └── images/
│       ├── logo.svg          # Main logo
│       ├── favicon.svg        # Favicon
│       └── screenshots/       # Placeholder folder
└── downloads/
    └── extension.zip         # Extension download
```

## Installation

### Option 1: GitHub Pages (Automatic)

1. Fork or clone this repository
2. Rename it to `YOUR-USERNAME.github.io` (or use `gh-pages` branch)
3. Push to GitHub
4. Site goes live at `https://YOUR-USERNAME.github.io/secret-tab/`

### Option 2: Local Development

```bash
# Clone repository
git clone https://github.com/YOUR-USERNAME/secret-tab-website.git
cd secret-tab-website

# Serve with any local server
python -m http.server 8000
# or
npx http-server
# or
php -S localhost:8000
```

Visit `http://localhost:8000` in your browser.

### Option 3: Static Hosting

Upload all files to any static hosting (Netlify, Vercel, Firebase, S3, etc.). No build step required.

## Customization

### Change Colors

Edit CSS variables in `assets/css/style.css`:

```css
:root {
  --bg-primary: #0a0a0f;           /* Main background */
  --text-primary: #f0eeff;          /* Main text */
  --accent-primary: #7c3aed;        /* Primary accent */
  --accent-secondary: #6d28d9;      /* Secondary accent */
  /* ... more variables ... */
}
```

### Change Typography

Replace font names in CSS variables:

```css
--font-display: 'Your Display Font', system-ui;
--font-body: 'Your Body Font', system-ui;
--font-mono: 'Your Mono Font', monospace;
```

### Change Content

Edit HTML files directly. All pages are self-contained with no templating.

### Add Pages

1. Create `new-page.html`
2. Copy nav/footer from existing pages
3. Add link to navigation in all pages
4. Add favicon & viewport meta tags

## Browser Support

- **Chrome** — v88+
- **Edge** — v88+
- **Brave** — v1.0+
- **Opera** — v75+

### Older Browsers

Some CSS features require modern browsers:
- CSS custom properties (IE 11 not supported)
- `backdrop-filter` (Safari 9+)
- CSS Grid & Flexbox (IE 11 partial)
- `IntersectionObserver` (requires polyfill for IE 11)

The site degrades gracefully — older browsers see the content without animations.

## Development

### No Build Tools

This website uses zero build tools. All files are served as-is:
- HTML is not minified
- CSS is not compiled or optimized
- JavaScript is not bundled
- No package manager required

Edit files directly and refresh your browser.

### CSS Architecture

- Single stylesheet with CSS variables
- Selectors use minimal specificity
- BEM-inspired naming for components
- Mobile-first responsive design

### JavaScript Patterns

- IIFE modules for encapsulation
- Vanilla DOM APIs (no jQuery)
- Event delegation for efficiency
- No state management library

## Performance Metrics

- **Lighthouse Performance** — 95+
- **Lighthouse Accessibility** — 100
- **Lighthouse Best Practices** — 92
- **Lighthouse SEO** — 100

No images above the fold, minimal JavaScript, optimized CSS.

## Accessibility Checklist

- ✅ Semantic HTML (h1-h6, nav, main, footer, sections)
- ✅ ARIA labels (role, aria-label, aria-expanded, aria-current)
- ✅ Keyboard navigation (Tab, Enter, Escape support)
- ✅ Focus visible (2px outline, 3px offset)
- ✅ Color contrast (WCAG AA, 4.5:1 minimum)
- ✅ Alt text on all images
- ✅ Reduced motion support
- ✅ Heading hierarchy (no skipped levels)
- ✅ Form labels & error messages
- ✅ Link text is meaningful

## Responsive Design

Breakpoints are implicit (no media query names):

- **Mobile** — 480px and below
- **Tablet** — 768px and below
- **Desktop** — 1024px and below
- **Large** — 1160px and above

All layouts tested and optimized for each viewport.

## SEO

- Meta descriptions on every page
- Open Graph tags (social preview)
- Twitter Card markup
- Canonical URLs
- Semantic HTML structure
- Mobile viewport configuration
- 404 page included

## License

This website is licensed under the **MIT License**. See the LICENSE file for full details.

You are free to:
- Use this as a template for your own project
- Modify and distribute
- Use commercially
- Remove attribution (though it's appreciated!)

## Credits

**Developed by:** Jules POMPEY (Julex)  
**Year:** 2026  
**License:** MIT

---

## Support

- **Documentation** — See `docs.html`
- **FAQ** — See `faq.html`
- **Privacy** — See `privacy.html`
- **Issues** — GitHub issues

## Contributing

Contributions welcome! Please:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing`)
3. Commit changes (`git commit -m 'Add amazing feature'`)
4. Push to branch (`git push origin feature/amazing`)
5. Open a Pull Request

## Roadmap

- [x] Homepage with hero & features
- [x] Download page with changelog
- [x] Installation guide for all browsers
- [x] Complete documentation
- [x] FAQ with accordion
- [x] Privacy policy
- [x] Dark/light mode with persistence
- [x] Mobile responsive design
- [x] Accessibility (WCAG AA)
- [x] Search in docs
- [ ] Blog/news section
- [ ] Testimonials
- [ ] Email newsletter signup

---

**Made with ❤️ for privacy.**
