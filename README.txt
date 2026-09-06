ADS THAT CONVERT — Multi-page site (split from the single-page version)
======================================================================
Same design & CSS as before, now as separate HTML files.

PAGES
  index.html     → Home
  services.html  → Services
  results.html   → Results
  about.html     → About
  contact.html   → Contact
  privacy.html   → Privacy Policy   (linked from the footer)
  terms.html     → Terms of Service (linked from the footer)
  assets/        → logo + favicon (used by the og:image social-preview tag)

WHAT CHANGED vs the single-page file
  • The nav (and all in-page buttons/footer links) now point to real .html files
    instead of #anchors — each page is its own document with a normal reload.
  • Each page has its OWN <title>, <meta name="description">, and a self-referencing
    <link rel="canonical"> (plus matching Open Graph / Twitter tags) for SEO.
  • The active nav item is highlighted per page.
  • Everything else is identical: same styles, animations, Calendly, WhatsApp button,
    cookie banner, lightbox on the Results page, and the tracking settings block.

CANONICAL DOMAIN
  Canonicals currently use https://adsthatconvert.co/ . If your live domain is
  different, do a find-and-replace of "https://adsthatconvert.co/" across the files.

DEPLOY
  Upload ALL files + the assets folder to GitHub (keep index.html at the top level).
  Vercel will serve index.html as the homepage and /services.html, /results.html, etc.
