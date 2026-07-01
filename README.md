# Domino Websites

Beautiful static websites for local small businesses. One great website sets everything in motion.

## What's here

`index.html` — the complete site. Single file, zero dependencies, no build step. Dark premium design with gold accents, domino-effect branding, and animation throughout (preloader, staggered hero reveal, parallax tiles, scroll reveals, animated counters, 3D tilt showcase cards, magnetic buttons, cascading process timeline). Fully responsive and respects reduced-motion preferences.

## Preview locally

Double-click `index.html` — it opens in any browser.

## Go live at dominowebsites.com (GitHub Pages + Porkbun)

### 1. Push to GitHub

From this folder, in Terminal:

```bash
cd "$HOME/Library/Mobile Documents/com~apple~CloudDocs/1. Gold Lion Mortgages - Working Brain/Domino Websites"
git init
git add index.html README.md CNAME
git commit -m "Domino Websites landing page"
git branch -M main
git remote add origin https://github.com/surinder-oss/Domino-Websites.git
git push -u origin main
```

### 2. Enable GitHub Pages

On github.com/surinder-oss/Domino-Websites: **Settings → Pages → Source: Deploy from a branch → main / (root) → Save.**

Then in the same Pages screen, under **Custom domain**, enter `dominowebsites.com` and Save. Tick **Enforce HTTPS** once it becomes available (can take up to an hour after DNS is set).

### 3. Point Porkbun DNS at GitHub

Porkbun → Domain Management → dominowebsites.com → **DNS Records**. Delete Porkbun's default ALIAS/CNAME parking records, then add:

| Type | Host | Answer |
|------|------|--------|
| A | (leave blank) | 185.199.108.153 |
| A | (leave blank) | 185.199.109.153 |
| A | (leave blank) | 185.199.110.153 |
| A | (leave blank) | 185.199.111.153 |
| CNAME | www | surinder-oss.github.io |

DNS usually propagates in 15–60 minutes. Then https://dominowebsites.com is live, and www redirects to it.

## Customize

- **WhatsApp**: quote form sends leads to WhatsApp 403-629-4003. To change, edit `WHATSAPP_NUMBER` in index.html (digits only, with country code).
- **Colors**: edit the CSS variables at the top of the `<style>` block (`--gold`, `--bg`, etc.).
- **Copy**: all text is plain HTML — edit directly.
- **Custom domain**: GitHub Settings → Pages → Custom domain (e.g. dominowebsites.com).
