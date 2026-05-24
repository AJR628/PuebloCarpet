# Pueblo Carpet Pros

Static HTML landing page for pueblocarpetpros.com. Deployed via Netlify with Netlify Forms for lead capture.

## Stack

- Pure HTML/CSS — no build step
- Google Fonts (Bricolage Grotesque + Inter) via CDN
- Inline SVG icons + favicon
- JSON-LD `ProfessionalService` schema for SEO
- Netlify Forms for the contact form

## Files

| File | Purpose |
|---|---|
| `index.html` | The single landing page |
| `sitemap.xml` | Submitted to Google Search Console for indexing |
| `robots.txt` | Allows all crawlers, references the sitemap |

## Deployment

### One-time setup

1. Push this repo to GitHub
2. Sign in to [Netlify](https://app.netlify.com) and click "Add new site" → "Import an existing project"
3. Connect GitHub and pick the `PuebloCarpet` repo
4. Build settings: leave **Build command** empty, set **Publish directory** to `/` (root)
5. Click Deploy — Netlify gives you a temporary URL like `pueblocarpetpros.netlify.app`

### Custom domain

1. In Netlify: Site settings → Domain management → Add custom domain → `pueblocarpetpros.com`
2. Update DNS at your domain registrar:
   - Add a CNAME record for `www` pointing to `pueblocarpetpros.netlify.app`
   - Or update A records to Netlify's load balancer (Netlify shows you the exact values)
3. Enable HTTPS in Netlify (automatic via Let's Encrypt, free)

### Form submissions

The contact form uses Netlify Forms (no external service needed). Submissions appear in:

- Netlify dashboard → Forms → `quote-request`
- Configure email notifications: Site settings → Forms → Form notifications → Add notification → Email notification

Set the notification email to your real inbox so you get pinged on each lead.

## What's intentionally NOT here yet

- **Phone number** — Will be added when Google Voice (719) number is set up. Add a phone button back to the header and a "Call Us" CTA to the hero when ready.
- **Google Business Profile** — Not pursuing for v1. Re-evaluate at month 3 once organic traffic is materializing and operator partner is identified.
- **Additional content pages** — Cost guide, dedicated commercial page, pet stain page, and neighborhood pages are all planned but not yet built.

## Updating the site

Static HTML, so just edit `index.html` and push to GitHub. Netlify auto-deploys on push to main.

## TODOs (in priority order)

1. Add phone number once Google Voice (719) is set up — search and replace `contact@pueblocarpetpros.com` references with phone where appropriate
2. Build the cost guide page (`/carpet-cleaning-cost-pueblo/`) — high-volume informational query, weak Map Pack pressure
3. Build the dedicated commercial page (`/commercial-carpet-cleaning-pueblo/`) — Pueblo commercial competition is 1/10
4. Build the pet stain removal page (`/pet-stain-removal-pueblo/`)
5. Build neighborhood pages for Bessemer, Pueblo West, Belmont, Mesa Junction
6. Submit to local citation directories: Yelp, Yellow Pages, BBB, Hotfrog, Citysearch, MerchantCircle, Bing Places
7. Submit sitemap to Google Search Console and Bing Webmaster Tools
8. Identify and reach out to 1-2 Pueblo carpet operators for lead-handoff partnership

## SEO baseline

- Primary keyword: `carpet cleaning pueblo`
- Secondary: `pueblo carpet cleaner`, `carpet cleaning pueblo co`, `commercial carpet cleaning pueblo`
- SEO Difficulty: 4/10 (Ubersuggest) for residential primary
- Estimated monthly volume: 590-800 for primary keyword

## Notes

- All copy avoids fabricated pricing, fabricated testimonials, fabricated certifications, or specific operational claims that would be verifiable
- "We" pronouns retained but applied to generic service language
- Schema uses `ProfessionalService` (not `LocalBusiness`) to avoid fake physical address claims
- Email-only contact for v1; phone added when real number is in place
