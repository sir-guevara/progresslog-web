# ProgressLog · website

Static pages for `progresslog.org` — landing, privacy policy, terms of service.

## Files

- `index.html` — marketing landing page
- `privacy.html` — privacy policy (linked from in-app About + required by App Review)
- `terms.html` — terms of service (linked from in-app About)

Each file is self-contained: no shared CSS, no JS bundles, no build step. Drop them on any static host.

## Quick deploy

### Option A · GitHub Pages (free, easiest)
1. Create a public GitHub repo named `progresslog-web`.
2. Drop these three files in the repo root.
3. Settings → Pages → Source: `main` branch, `/ (root)`.
4. Point `progresslog.org` at the Pages URL with a CNAME record.

### Option B · Cloudflare Pages
1. Create a Cloudflare account, connect the repo above.
2. Build command: *(leave blank)*. Output directory: `/`.
3. Custom domain: `progresslog.org`.

### Option C · Apple-friendly any-host
The pages are static HTML and don't need a server. Any S3 bucket + CloudFront, Netlify, or Vercel will serve them in seconds.

## Email · support@progresslog.org

Make sure `support@progresslog.org` is a real inbox before submitting the app — Apple Review checks it. Cheapest options:

- iCloud Custom Email Domain (free with iCloud+, ~$1/mo)
- Cloudflare Email Routing (free, forwards to your existing inbox)
- Google Workspace ($6/mo)

## Brand tokens

If you spin up new pages, copy these values to match the app:

| Token | Value |
| --- | --- |
| Background | `#f7f7f9` |
| Surface | `#ffffff` |
| Soft accent | `#f0eefe` |
| Text primary | `#121217` |
| Text secondary | `#5a5a64` |
| Accent (violet) | `#735BEF` |
| Accent dark | `#5a44c9` |
| Radius (large) | `18px` |
| Font | system-ui / SF Pro |

## Before submitting to the App Store

- [ ] `progresslog.org/` returns 200
- [ ] `progresslog.org/privacy` returns 200
- [ ] `progresslog.org/terms` returns 200
- [ ] `support@progresslog.org` receives a test email and forwards correctly
- [ ] Update `index.html`'s "Coming soon" CTA to a real App Store link after launch
