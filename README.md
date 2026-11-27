# Zvert website

Zvert, Halal Ads for Bangladesh. A static, mobile-first one-page site with an English / Bangla switch.
No build step, no frameworks, no tracking. Total size is about 160 KB.

## Files

| Path | What it is |
| --- | --- |
| `index.html` | All page text (English and Bangla side by side in `.en` / `.bn` spans) |
| `css/style.css` | Brand colours, layout and animations |
| `js/main.js` | Services, halal rules, steps, sample ads, packages, FAQ, language switch, brief form, scroll reveals |
| `assets/` | Zvert logos (from the brand kit) and the link-preview image |
| `favicon.svg` | Browser tab icon |

### Common edits

- **Prices and package contents:** in `js/main.js`, find `const plans=`. Each plan has its English name, Bangla name, English price, Bangla price, a 1 for "Most popular", and its feature list.
- **Services, FAQ, halal rules, steps:** the arrays `svc`, `faqs`, `never` / `always` and `steps` in `js/main.js`. Every entry has an English and a Bangla version.
- **Sample ads:** `const ads=` in `js/main.js`. Replace them with real client work when you have it.
- **Headings and section text:** in `index.html`. Edit both the `class="en"` and `class="bn"` versions.
- **Email and Facebook link:** search for `zvert.bd@gmail.com` and `facebook.com/zvert.bd` in `index.html` and `js/main.js`.

Halal rules for anything you add: no music or autoplay audio or video, no women, no human or animal faces (including AI-generated ones, cartoons and silhouettes), and truthful claims only.

## Put it on GitHub

1. Create a new repository on GitHub, for example `zvert-website` (Public is needed for free GitHub Pages).
2. Click **Add file > Upload files**, drag in everything from this folder (keep the `css`, `js` and `assets` folders), and commit.

## Deploy option A: GitHub Pages (simplest, free)

1. In the repository, open **Settings > Pages**.
2. Under **Build and deployment**, choose **Deploy from a branch**, branch `main`, folder `/ (root)`, and save.
3. After a minute the site is live at `https://<your-username>.github.io/zvert-website/`.
4. Every time you commit a change on GitHub, the site updates automatically.

## Deploy option B: Vercel (free, nicer default address)

1. Sign in at vercel.com with your GitHub account.
2. Click **Add New > Project**, import the `zvert-website` repository.
3. Framework preset: **Other**. Leave the build command and output directory empty, and click **Deploy**.
4. The site is live at `https://zvert-website.vercel.app` (or similar). Every commit to `main` redeploys it.

## Custom domain (for example zvert.com.bd)

Both options support a custom domain for free; you only pay for the domain itself.

- GitHub Pages: **Settings > Pages > Custom domain**, then add the DNS records GitHub shows you.
- Vercel: **Project > Settings > Domains**, then add the DNS records Vercel shows you.

HTTPS is free and automatic on both.
