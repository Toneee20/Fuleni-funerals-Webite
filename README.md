# Fuleni Funerals G — Website

A single-page, scrollable HTML site for Fuleni Funerals G, serving Vereeniging and Meyerton, South Africa. Built as a static site with embedded CSS/JS — no build tooling required.

## Files in this repo

| File | Purpose |
|---|---|
| `index.html` | The full site (all 10 sections, nav, styles, scripts) |
| `vercel.json` | Vercel routing/security headers config |
| `package.json` | Project metadata (no real build step needed) |
| `robots.txt` | Allows all crawlers, points to sitemap |
| `sitemap.xml` | SEO sitemap for the homepage |
| `.gitignore` | Standard ignores |

## Deploy: GitHub → Vercel

1. **Create the GitHub repo**
   ```bash
   git init
   git add .
   git commit -m "Initial commit: Fuleni Funerals G site"
   git branch -M main
   git remote add origin https://github.com/<your-username>/fuleni-funerals-website.git
   git push -u origin main
   ```

2. **Import into Vercel**
   - Go to https://vercel.com/new
   - Select "Import Git Repository" and choose this repo
   - Framework Preset: **Other** (static site — Vercel will auto-detect `index.html`)
   - Build Command: leave blank (or `npm run build`, which just echoes)
   - Output Directory: leave as root (`.`)
   - Click **Deploy**

3. **Custom domain**
   - In the Vercel project → Settings → Domains, add `fulenifunerals.co.za` (and `www.`)
   - Update your DNS with the records Vercel provides
   - Update `sitemap.xml`, `robots.txt`, and the canonical/OG tags in `index.html` if the final domain differs from `fulenifunerals.co.za`

## After deployment — SEO checklist

- [ ] Submit `sitemap.xml` to Google Search Console and Bing Webmaster Tools
- [ ] Verify the site in Google Search Console (domain or URL-prefix property)
- [ ] Replace placeholder stock photography with real, licensed images of the branches/team
- [ ] Confirm the canonical URL and Open Graph URLs match the live domain exactly
- [ ] Test social sharing previews (Facebook Sharing Debugger, Twitter Card Validator)

## Notes on content

- The "Insights" section on the page currently shows three teaser cards (grief support, funeral policy planning, ceremony guidance) that link back to the contact/assistance section rather than to standalone articles. This is fine for a single-page site, but if full blog articles are wanted later for SEO depth, each would need its own page/route.
- All internal navigation links, the mobile menu, and all "Request Immediate Assistance" CTAs were checked and correctly point to matching section IDs.
- Contact details (Vereeniging: 016 422 0099 / 072 904 9300 / WhatsApp 067 215 2800; Meyerton: 016 362 1278 / 082 927 9264) are consistent across the header, footer, and contact section.
