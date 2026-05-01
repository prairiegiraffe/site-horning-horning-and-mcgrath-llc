# Horning, Horning and McGrath, LLC — Site Rebuild

## What This Is

This repo contains a captured copy of hhmattorneys.com. The HTML was cloned from the
live site — it works but it's full of builder cruft (WordPress/Elementor/Squarespace/etc.
markup, inline styles, unnecessary divs, broken class names, etc.).

**Your job: rebuild each page as clean, semantic HTML + Tailwind CSS that looks identical
to the original.** This is a code cleanup, not a redesign.

## Rules

### DO
- **Match the original design exactly** — same layout, same colors, same fonts, same spacing
- **Keep all original content** — every heading, paragraph, image, link, testimonial, phone number
- **Keep the same page structure** — same pages, same sections in the same order
- **Keep the same navigation** — same menu items, same order, same links
- **Use Tailwind CSS** for styling — replace inline styles and builder classes with Tailwind utilities
- **Use semantic HTML** — proper heading hierarchy (h1→h2→h3), `<nav>`, `<main>`, `<section>`, `<footer>`
- **Keep all images** — use the same image URLs from the original HTML (they're hosted on our CDN)
- **Make it responsive** — the original probably is, match the breakpoints
- **Add `data-content` attributes** to editable text elements (headings, paragraphs, images)
- **Add `data-block-id` attributes** to each `<section>` for the platform editor

### DON'T
- **Don't redesign** — if the original has a dark header, keep a dark header. If it has a sidebar, keep the sidebar.
- **Don't rewrite copy** — use the exact text from the original pages. Fix obvious typos only.
- **Don't change the color scheme** — extract the exact colors from the original CSS and use them
- **Don't add sections that aren't in the original** — no new testimonials, no new CTAs
- **Don't remove sections** — if the original has it, the rebuild has it
- **Don't use a CSS framework's component library** — use Tailwind utilities to match the original design
- **Don't invent content** — if something is in the original, keep it. If it's not, don't add it.

## How to Work

1. **Read the original HTML file** for the page you're building
2. **Identify the visual structure** — what sections exist, what order, what layout
3. **Extract the design tokens** — colors, fonts, spacing from the original CSS/styles
4. **Rebuild it** as clean HTML + Tailwind, matching the original pixel-for-pixel
5. **Test it** — `npx serve .` and compare side-by-side with the original

### Tailwind Setup
Add the Tailwind CDN to each page's `<head>`:
```html
<script src="https://cdn.tailwindcss.com"></script>
<script>
tailwind.config = {
  theme: {
    extend: {
      // Extract these from the original site's CSS:
      colors: {
        // primary: '#...', secondary: '#...', accent: '#...'
      },
      fontFamily: {
        // heading: ['...', 'serif'], body: ['...', 'sans-serif']
      }
    }
  }
}
</script>
```

Extract the actual brand colors and fonts from the original page CSS. Don't guess — read the
`<style>` blocks and inline styles in the original HTML to find the exact values.

## Pages

- `index.html` — Horning Horning and McGrath - Horning, Horning and McGrath, LLC
- `about-us.html` — About Us - Horning, Horning and McGrath, LLC
- `cassie-lewis.html` — Cassie Lewis - Horning, Horning and McGrath, LLC
- `contact-us.html` — Contact Us - Horning, Horning and McGrath, LLC
- `j-david-horning.html` — J. David Horning - Horning, Horning and McGrath, LLC
- `karena-kase.html` — Karena Kase - Horning, Horning and McGrath, LLC
- `practice-areas.html` — Practice Areas - Horning, Horning and McGrath, LLC
- `richard-horning.html` — Richard Horning - Horning, Horning and McGrath, LLC
- `ryan-mcgrath.html` — Ryan McGrath - Horning, Horning and McGrath, LLC
- `sarah-weerstra.html` — Sarah Weerstra - Horning, Horning and McGrath, LLC
- `savannah-kramer.html` — Savannah Kramer - Horning, Horning and McGrath, LLC

Each page is already in the repo as an HTML file. Read it, understand the structure,
then rewrite it in place with clean code.

## Images (already on CDN)

These images are from the original site and are already hosted. Use these URLs directly:
- https://devtools.prairiegiraffe.com/api/files/sites/proj_r99yrv9s/1773341263119/assets/mmntlnx725372g.svg
- https://devtools.prairiegiraffe.com/api/files/sites/proj_r99yrv9s/1773341263119/assets/mmntlnx552l1u7.webp
- https://devtools.prairiegiraffe.com/api/files/sites/proj_r99yrv9s/1773341263119/assets/mmntlnzsub7kuw.webp
- https://devtools.prairiegiraffe.com/api/files/sites/proj_r99yrv9s/1773341263119/assets/mmntloc7cfc5kg.gif
- https://devtools.prairiegiraffe.com/api/files/sites/proj_r99yrv9s/1773341263119/assets/mmntloc8xjxk99.svg
- https://devtools.prairiegiraffe.com/api/files/sites/proj_r99yrv9s/1773341263119/assets/mmntloa1wlmzsr.webp
- https://devtools.prairiegiraffe.com/api/files/sites/proj_r99yrv9s/1773341263119/assets/mmntlocyly4eam.svg
- https://devtools.prairiegiraffe.com/api/files/sites/proj_r99yrv9s/1773341263119/assets/mmntlocirn98tw.svg
- https://devtools.prairiegiraffe.com/api/files/sites/proj_r99yrv9s/1773341263119/assets/mmntloexy3i5bo.svg
- https://devtools.prairiegiraffe.com/api/files/sites/proj_r99yrv9s/1773341263119/assets/mmntmjs4b5kcp7.svg
- https://devtools.prairiegiraffe.com/api/files/sites/proj_r99yrv9s/1773341263119/assets/mmntmjs4tt8f9f.jpg
- https://devtools.prairiegiraffe.com/api/files/sites/proj_r99yrv9s/1773341263119/assets/mmntmjwqg3mg89.jpg
- https://devtools.prairiegiraffe.com/api/files/sites/proj_r99yrv9s/1773341263119/assets/mmntmjv27pp2o5.jpg
- https://devtools.prairiegiraffe.com/api/files/sites/proj_r99yrv9s/1773341263119/assets/mmntmjwjxjpa64.jpg
- https://devtools.prairiegiraffe.com/api/files/sites/proj_r99yrv9s/1773341263119/assets/mmntmjvsc6y5jb.jpg
- https://devtools.prairiegiraffe.com/api/files/sites/proj_r99yrv9s/1773341263119/assets/mmntmwcat6oclx.jpg
- https://devtools.prairiegiraffe.com/api/files/sites/proj_r99yrv9s/1773341263119/assets/mmntmwf9sktkqh.jpg
- https://devtools.prairiegiraffe.com/api/files/sites/proj_r99yrv9s/1773341263119/assets/mmntmwg66e8qoy.jpg
- https://devtools.prairiegiraffe.com/api/files/sites/proj_r99yrv9s/1773341263119/assets/mmntmwgwvw64xn.jpg
- https://devtools.prairiegiraffe.com/api/files/sites/proj_r99yrv9s/1773341263119/assets/mmntmwg3e9enjh.jpg
- https://devtools.prairiegiraffe.com/api/files/sites/proj_r99yrv9s/1773341263119/assets/mmntn2h1xpzac3.jpg
- https://devtools.prairiegiraffe.com/api/files/sites/proj_r99yrv9s/1773341263119/assets/mmntn2kni0jimj.jpg
- https://devtools.prairiegiraffe.com/api/files/sites/proj_r99yrv9s/1773341263119/assets/mmntn2m7bx7nvh.jpg
- https://devtools.prairiegiraffe.com/api/files/sites/proj_r99yrv9s/1773341263119/assets/mmntn2lvcf571p.jpg
- https://devtools.prairiegiraffe.com/api/files/sites/proj_r99yrv9s/1773341263119/assets/mmntn2m22weh81.jpg
- https://devtools.prairiegiraffe.com/api/files/sites/proj_r99yrv9s/1773341263119/assets/mmntn93i1p0fun.jpg
- https://devtools.prairiegiraffe.com/api/files/sites/proj_r99yrv9s/1773341263119/assets/mmntnfee1y0rpc.jpg
- https://devtools.prairiegiraffe.com/api/files/sites/proj_r99yrv9s/1773341263119/assets/mmntnfde3w0oyn.jpg
- https://devtools.prairiegiraffe.com/api/files/sites/proj_r99yrv9s/1773341263119/assets/mmntnfehiyag1c.jpg
- https://devtools.prairiegiraffe.com/api/files/sites/proj_r99yrv9s/1773341263119/assets/mmntnfarbukv7a.jpg

## Business Facts (extracted from the site)

| Field | Value |
|-------|-------|
| **Business Name** | Horning, Horning and McGrath, LLC |
| **Industry** | legal |
| **Phone** | 3076863736 |
| **Email** | N/A |
| **Address** | N/A |

### Services
- Business formation and planning
- Mergers and acquisitions
- Commercial and business litigation
- Real estate transactions and land use
- Estate planning
- Probate
- Oil and gas law and mineral royalties
- Ranching and agriculture law
- Employment law
- Contract law

### Service Areas
- Gillette, WY

## Platform Integration

### Editable Attributes
Add these so the platform editor can modify content:
- `data-content="hero-title"` on editable headings
- `data-content="hero-image"` on `<img>` tags
- `data-block-id="page:section-name"` on each `<section>`
- `data-devtools-partial="header"` on the header wrapper
- `data-devtools-partial="footer"` on the footer wrapper

### Forms
If the site has contact/quote forms, wire them to the platform:

```bash
curl -X POST "https://devtools.prairiegiraffe.com/api/projects/proj_r99yrv9s/forms" \
  -H "Content-Type: application/json" \
  -H "Authorization: Bearer dtk_1cfa4ada57ca17ec56ca9e4b47b73b7585edab352d788b24731d900e58b4788c" \
  -d '{
    "name": "Contact Form",
    "fields": [
      { "label": "Name", "type": "text", "required": true },
      { "label": "Email", "type": "email", "required": true },
      { "label": "Phone", "type": "phone", "required": false },
      { "label": "Message", "type": "textarea", "required": true }
    ],
    "settings": { "submit_button_text": "Send Message", "form_type": "contact" }
  }'
```

Then in the HTML form: add `data-devtools-form` and `data-form-type="contact"`.
Use `name="name"`, `name="email"`, `name="phone"`, `name="message"` for standard fields.
Use `name="custom_fields[field_name]"` for anything else.

## Deployment

- **Repo**: https://github.com/prairiegiraffe/site-horning-horning-and-mcgrath-llc
- **Live URL**: https://site-horning-horning-and-mcgrath-llc.pages.dev
- Push to `main` → auto-deploys via Cloudflare Pages
- No build step — static HTML served directly
