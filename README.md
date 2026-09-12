# PFC Website — Diamond Membership

Standalone site for **`diamond.painfreeclub.in`** — the Pain Free Club
**Diamond Membership** landing/sales page.

## Contents
- `index.html` — the Diamond Membership page (self-contained: all styles and
  most images are inline; conversion happens via the external Cashfree payment
  form, WhatsApp, and email — no backend or form handler needed).
- `manan-photo.jpg`, `manan-portrait.jpg` — the two photos referenced by the page.
- `vercel.json` — minimal static config (`cleanUrls`).

## Deploy (Vercel)
1. **vercel.com → Add New → Project → Import** this repo (`PFCwebsite`).
   - Framework preset: **Other**. Root Directory: repo root. Click **Deploy**.
   - You get a free `*.vercel.app` URL — test the page there first.
2. **Settings → Domains → Add** `diamond.painfreeclub.in`. Vercel shows the DNS
   record to create (a CNAME: host `diamond` → `cname.vercel-dns.com`).
3. **In DNS (GoDaddy → painfreeclub.in → Manage DNS):** change the existing
   `diamond` record (currently pointing to Netlify) to the CNAME Vercel shows.
4. Vercel auto-issues SSL. Once "Valid Configuration" shows, the page is live at
   `https://diamond.painfreeclub.in/`. The old Netlify site can then be retired.

## History
Migrated off Netlify (Sept 2026). The previous host had no build step or
Netlify-specific features, so this is a straight static copy.
