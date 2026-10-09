# Raul S Freitas Landscapes (RSFL)

One-page website for www.rsfl.je, for GitHub Pages. Same look as the old site: navy background, Oswald font, white labels and yellow links. Plain HTML and CSS. No build step.

## Before you go live: add facts if you have them

These help Google a lot. Add them to `index.html` (page text and JSON-LD) and `llms.txt`:

- Skip sizes (for example mini, midi, builders) and what fits through a gate.
- Yard or office address and postcode (add to `address` in the JSON-LD).
- Opening hours (add `openingHoursSpecification` to the JSON-LD).
- Years in business, insurance, waste carrier licence.

## Files

| File | What it does |
| --- | --- |
| `index.html` | The page, all meta tags and the JSON-LD schema |
| `css/main.css` | All styles. Colours are at the top. |
| `fonts/` | Oswald font, on your site. No calls to Google. Licence: SIL OFL. |
| `images/logo.png` | The logo, from the live site. Made smaller with no change to the image. |
| `images/og-image.jpg` | Picture shown when the link is shared (1200 x 630) |
| `favicon.ico`, `favicon-32.png` | Browser tab icons (the star from the logo) |
| `apple-touch-icon.png` | iPhone home screen icon |
| `icon-192.png`, `icon-512.png`, `icon-maskable-512.png` | Android icons |
| `site.webmanifest` | Tells phones which icons and colours to use |
| `sitemap.xml`, `robots.txt` | Help search engines find the page |
| `llms.txt` | Short plain-text summary for AI search tools |
| `404.html` | "Page not found" page |
| `.nojekyll` | Tells GitHub Pages not to run Jekyll |

## SEO in this page

- Title and description use "skip hire", "landscaping", "block paving", "slab laying" and "Jersey".
- One `h1`, then `h2` and `h3` headings with the service names.
- JSON-LD: `HomeAndConstructionBusiness`, 4 `Service` items, `WebSite` and `WebPage`.
- Open Graph and X (Twitter) tags, so shared links show the logo.
- Canonical URL, sitemap, robots.txt.

## Email links

- The email link at the top opens an email with the subject "Enquiry from rsfl.je".
- The "Email raul@rsfl.je" button at the end opens an email with 3 prompts: what, where and when.
- On phones, a "Call" and "Email" bar shows at the bottom of the screen between the top and the end of the page.

## The most important step for local search

Set up a **Google Business Profile** for RSFL (business.google.com). For local searches like "skip hire Jersey", this has more effect than the website. Use the same name, phone number and website on the profile and on this page.

Also check listings on Jersey Insight and Bing Places. Use the same name and phone number everywhere.

## Domain

All URLs in the meta tags, schema, sitemap and robots.txt use `https://www.rsfl.je/`. If you use a different address, search and replace `https://www.rsfl.je/` in these files.

## 1. Put it on GitHub

```bash
cd rsfl-site
git init
git add .
git commit -m "RSFL website"
git branch -M main
git remote add origin https://github.com/YOUR-NAME/rsfl-site.git
git push -u origin main
```

## 2. Turn on GitHub Pages

1. In the repo, go to **Settings > Pages**.
2. Source: **Deploy from a branch**.
3. Branch: **main**, folder: **/ (root)**. Click **Save**.

## 3. Use the www.rsfl.je domain

1. In **Settings > Pages > Custom domain**, type `www.rsfl.je`. Click **Save**.
2. At the DNS provider for `rsfl.je`, add:
   - `CNAME` record: `www` to `YOUR-NAME.github.io`
   - For the bare domain `rsfl.je`, add `A` records to `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
3. When the check passes, tick **Enforce HTTPS**.

Check the current GitHub IP addresses before you change DNS:
https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site

## 4. After it is live

1. Test the schema: https://search.google.com/test/rich-results and https://validator.schema.org
2. Test the share image: paste the URL in a WhatsApp or LinkedIn message.
3. Add the site in Google Search Console and submit `https://www.rsfl.je/sitemap.xml`.

## Test on your computer

```bash
cd rsfl-site
python3 -m http.server 8000
```

Open `http://localhost:8000`.
