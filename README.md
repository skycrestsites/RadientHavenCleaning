# Radiant Haven Cleaning Services website

A fast, mobile-first site (home page + 8 service pages) for Radiant Haven Cleaning Services (Rancho Cucamonga, CA).

## Files
- `index.html` - all page content and SEO metadata
- `css/styles.css` - styles (Style 3 editorial look: navy #1a365d + warm gold #c5a059, Playfair Display headings, Inter body)
- `js/main.js` - mobile nav, scroll effects, and the quote form handler
- `assets/` - images and favicon
- `robots.txt`, `sitemap.xml` - search engine files

## Clean URLs (no .html)
The site is a single page served from `index.html`. On any standard static host
(Netlify, Vercel, Cloudflare Pages, GitHub Pages, or Apache/Nginx), `index.html`
is served automatically at the root, so visitors only ever see:

    https://slcpremiercleaning.com/

No `.html` ever appears in the address bar. Just deploy the whole folder and point
the domain at it.

## Before you go live
0. IMPORTANT - domain, email and booking still point at the SLC Premier project this
   site was duplicated from (kept on purpose until Radiant Haven's details arrive).
   Search the whole folder for `slcpremiercleaning` and replace:
   - `https://slcpremiercleaning.com` (canonicals, Open Graph, JSON-LD, `sitemap.xml`, `robots.txt`)
   - `hello@slcpremiercleaning.com` (all pages + `js/main.js`)
   - `slcpremiercleaning.bookingkoala.com` (the booking iframe + preconnect in `index.html`).
     Until this is swapped, bookings made on this site go to SLC Premier's BookingKoala account.
1. Phone number: replace the placeholder `(909) 000-0000` in `index.html`
   (contact section + footer, and the `tel:` links).
2. Email: `hello@slcpremiercleaning.com` is set as the contact address. Create that
   inbox on the domain, or change it in `index.html` and `js/main.js`.
3. Quote form: it currently opens the visitor's email app pre-filled. To collect
   submissions automatically, create a free form at formspree.io and add
   `action="https://formspree.io/f/XXXXXXX" method="POST"` to the `<form id="quoteForm">`.
4. Photos: swap the stock images in `assets/` with real job photos when available.
5. Add the site to Google Business Profile and Google Search Console for local SEO.

## SEO included
- Location-focused title, description, and keywords for Rancho Cucamonga
- Open Graph + Twitter cards
- Geo meta tags and `HouseCleaningService` JSON-LD structured data (services,
  service areas, reviews, hours, geo)
- `robots.txt` and `sitemap.xml`
