# Unified Jiu-Jitsu: website

Plain HTML, CSS and JavaScript. No build step and no dependencies.

## Files
- `index.html`: home (hero, programs, first class, instructors)
- `schedule.html`: weekly schedule with program filters and today highlighted
- `instructors.html`: instructor profiles
- `contact.html`: free trial form, location and map, FAQ
- `thanks.html`: shown after the form is submitted
- `styles.css`, `main.js`, `favicon.svg`, `robots.txt`, `sitemap.xml`
- `images/`: put your photos here

## Before launch: fill in the placeholders
Search all files for `[`, `example.com` and `000-0000`:
- Street address, ZIP, phone and email (footer on every page, contact page, and JSON-LD in `index.html`)
- Belt rank, lineage and bios for Damon and Raphael (`instructors.html`, plus the home page cards)
- Pricing answer in the FAQ (`contact.html`)
- Instagram and Facebook links
- Your real domain in place of `https://www.example.com` (canonical tags, og tags, `robots.txt`, `sitemap.xml`)
- Map: in `contact.html`, replace `West+Jordan,+UT` in the iframe with your full address

## Adding photos
- **Hero:** in `index.html`, change `<section class="hero">` to
  `<section class="hero" style="--hero-img: url('images/hero.jpg')">`
- **Instructors:** replace the initials inside `.portrait` with
  `<img src="images/damon.jpg" alt="Damon Morgan">`
- **Social preview:** add `images/og-image.jpg` (1200×630)

Compress images before uploading (squoosh.app). Aim for under 300 KB each.

## Deploy (Netlify, free)
1. Go to app.netlify.com and drag this folder onto the deploy area.
2. The trial form works automatically. Submissions appear under **Forms** in the Netlify dashboard, and you can turn on email notifications there.
3. Add your custom domain under **Domain settings**.

On a host other than Netlify, sign up at formspree.io and set the form's `action` to your Formspree URL.

## Changing the schedule
Edit the `<li class="session">` items in `schedule.html`. The `data-program` value controls the colour and the filter:
`fundamentals`, `all-levels`, `advanced`, `competition`, `open-mat`.
If you change times, also update the program cards in `index.html` and the "23 sessions per week" figure.

## Colours and fonts
Every colour lives at the top of `styles.css` under `:root`. Change `--accent` to restyle the red throughout the site.
