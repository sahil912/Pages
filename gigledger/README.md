# GigLedger Website

Static website for GigLedger app - deploys to Cloudflare Pages, GitHub Pages, Netlify, or Vercel.

## Structure

```
website/
├── index.html          # Home/landing page
├── privacy/
│   └── index.html      # Privacy policy
├── support/
│   └── index.html      # Support & FAQ
├── terms/
│   └── index.html      # Terms of service
├── 404.html            # Error page
├── styles.css          # Global styles
├── robots.txt          # SEO
├── sitemap.xml         # SEO
├── _headers            # Security headers (Cloudflare/Netlify)
├── _redirects          # URL redirects
└── assets/             # Favicon & icons (add your own)
```

## Deployment

### Cloudflare Pages (Recommended)
1. Push this folder to a GitHub repo
2. Go to [Cloudflare Pages](https://pages.cloudflare.com)
3. Connect your GitHub repo
4. Set build output directory to `website` (or repo root if website folder is the repo)
5. Deploy

### GitHub Pages
1. Push to GitHub
2. Go to repo Settings → Pages
3. Select branch and folder (`/website` or `/docs`)
4. Your site will be at `username.github.io/repo-name`

### Vercel
1. Push to GitHub
2. Import project on [Vercel](https://vercel.com)
3. Set root directory to `website`
4. Deploy

## Custom Domain

Update these files when you have your domain:
- `sitemap.xml` - Replace `gigledger.app` with your domain
- `robots.txt` - Update sitemap URL

## Assets Needed

Add to the `assets/` folder:
- `apple-touch-icon.png` (180x180)
- `favicon-32x32.png` (32x32)
- `favicon-16x16.png` (16x16)
- `favicon.ico`

## Customization

If you rename the app, find and replace:
- "GigLedger" → "YourAppName"
- "gigledger.app" → "yourapp.com"
- Email addresses (support@, privacy@, legal@, feedback@)
