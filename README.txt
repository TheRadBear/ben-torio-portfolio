# Kael Wright — Creative Developer Portfolio Template

## Quick Start

1. Open `portfolio.html` in a code editor (VS Code, Sublime Text, etc.)
2. Replace placeholder content with your own
3. Upload the single file to any web host
4. Done — no build step required

---

## File Structure

```
kael-wright-portfolio/
  portfolio.html    ← The complete template (single file)
  README.txt        ← This documentation
  LICENSE.txt       ← Usage license
```

---

## Customization Guide

### Changing Your Name & Title

Find the hero section (around line 305-314) and update:

```html
<h1 class="hero-name">
  <span class="line"><span class="line-inner">YOUR FIRST NAME</span></span>
  <span class="line"><span class="line-inner"><em>YOUR LAST NAME</em></span></span>
</h1>
```

Also update the nav logo (line ~286):
```html
<a href="#" class="nav-logo">Y.N.</a>
```

And the page title (line ~6):
```html
<title>YOUR NAME — Creative Developer & Designer</title>
```

### Changing Colors

All colors are CSS custom properties at the top of the `<style>` block (lines 14-31). Simply change the hex values:

```css
:root {
  --bg: #08070c;        /* Main background */
  --cream: #ede8e0;     /* Primary text */
  --coral: #e8764b;     /* Accent 1 */
  --teal: #4ecdc4;      /* Accent 2 */
  --lavender: #c4a8e0;  /* Accent 3 */
  --gold: #e8c55a;      /* Accent 4 */
  --rose: #e07888;      /* Accent 5 */
  /* ...and more */
}
```

### Updating Projects

Each project is an `<article class="p-card">` element (lines ~348-352). Update the title, category tag, year, and link:

```html
<article class="p-card r-up">
  <div class="p-img"><div class="p-bg"><div class="p-deco"></div></div></div>
  <div class="p-info">
    <div>
      <div class="p-meta">
        <span class="p-tag">YOUR CATEGORY</span>
        <span class="p-year">2025</span>
      </div>
      <h3 class="p-title">Your Project Title</h3>
    </div>
    <a href="YOUR_URL" class="p-link">View Project ...</a>
  </div>
</article>
```

To add your own project images, replace the gradient `<div class="p-bg">` with an actual image:

```html
<div class="p-img">
  <img src="your-image.jpg" alt="Project" class="p-bg"
       style="width:100%;height:100%;object-fit:cover">
</div>
```

### Updating the About Section

Find the about section (lines ~317-338):
- Update the heading, paragraphs, and stats
- The abstract visual (`.about-vis`) can be replaced with your photo

### Updating Skills

The skills marquee (lines ~358-361) contains two rows of scrolling items. Update the `<span class="mq-item">` text:

```html
<span class="mq-item"><em>Your Skill</em></span>
<span class="mq-dot"></span>
```

Use `<em>` for italic display font treatment, plain text for regular.

### Updating Testimonials

Find the testimonials section (lines ~364-371). Each `.test-card` contains a quote, name, and role. Simply update the text.

### Updating Contact & Social Links

Find the contact section (lines ~374-386):
- Update the email in the `mailto:` link
- Update the social link `href` attributes (GitHub, X, LinkedIn, Dribbble)
- SVG icons are inline — to swap platforms, replace the SVG `<path>` data

### Updating Footer

Line ~390: Update the copyright year and name.

---

## Changing Fonts

The template uses Google Fonts loaded via CDN (line ~9). To change fonts:

1. Go to fonts.google.com and choose your fonts
2. Replace the `<link>` tag with your new Google Fonts embed code
3. Update the CSS variables:

```css
--ff: 'YourBodyFont', sans-serif;
--fd: 'YourDisplayFont', serif;
--fm: 'YourMonoFont', monospace;
```

---

## Adding More Projects

To add a 6th project card:

1. Copy an existing `<article class="p-card">` block
2. Paste it inside the `.p-grid` container
3. Add a unique gradient background by adding CSS like:
   ```css
   .p-card:nth-child(6) .p-bg { background: linear-gradient(...) }
   ```
4. Update the project count text ("05 Works" → "06 Works")

---

## Deployment

This template works with any static hosting:

- **Netlify** — Drag and drop the HTML file
- **Vercel** — Upload via CLI or dashboard
- **GitHub Pages** — Push to a repo, enable Pages
- **Cloudflare Pages** — Connect to your repo
- **Any traditional hosting** — Upload via FTP

No server-side rendering, no build step, no environment variables needed.

---

## Browser Support

- Chrome 90+ (recommended)
- Firefox 90+
- Safari 15+
- Edge 90+

The custom cursor is automatically disabled on touch devices and screens below 768px.

---

## Libraries Used (loaded via CDN)

| Library | Version | Purpose |
|---------|---------|---------|
| GSAP | 3.12.5 | Scroll animations, parallax, reveals |
| ScrollTrigger | 3.12.5 | Scroll-based animation triggers |
| Lenis | 1.1.18 | Smooth scroll behavior |

All libraries are loaded from CDN — no local files needed.

---

## Performance Notes

- All animations use GPU-accelerated `transform` and `opacity` properties
- Will-change hints are used sparingly for smooth 60fps animation
- Images are lazy-loaded by default in modern browsers
- CSS is minified inline for minimal file size
- Total file size: ~30KB (before external CDN resources)

---

## License

This template is licensed for personal and commercial use.

You MAY:
- Use it for your own portfolio
- Use it for client projects
- Modify it freely

You MAY NOT:
- Resell the template as-is
- Include it in other template collections for sale
- Claim it as your own creation for sale

---

## Support

If you need help customizing the template, please reach out through the Gumroad message system on the product page.

---

## Changelog

### v1.0 (March 2025)
- Initial release
- 7 sections: Hero, About, Projects, Skills, Testimonials, Contact, Footer
- GSAP ScrollTrigger animations
- Custom cursor with hover effects
- Lenis smooth scroll
- Responsive design (desktop, tablet, mobile)
- 10-color warm palette with CSS custom properties
