# Kwasi Adi-Dako — Portfolio

Personal portfolio site. Single-file build: `index.html` + a portrait image + a resume PDF.

## What gets published

Three files make up the public site:

- `index.html`
- `kwasi-portrait.jpg`
- `Kwasi AD Resumé Portfolio.pdf`

Everything else in this folder (source decks, write-ups, JDs) is excluded by `.gitignore`.

## Publish to GitHub Pages

### Option A — Personal site at `<username>.github.io`

1. Create a new repo on GitHub named **exactly** `<your-username>.github.io` (e.g. `kwasiadidako.github.io`).
2. From this folder, in a terminal:
   ```bash
   git init
   git add .
   git commit -m "Initial portfolio"
   git branch -M main
   git remote add origin https://github.com/<your-username>/<your-username>.github.io.git
   git push -u origin main
   ```
3. The site will be live at `https://<your-username>.github.io` within a minute or two.

### Option B — Project repo (lives at `<username>.github.io/portfolio`)

1. Create a repo on GitHub (any name, e.g. `portfolio`).
2. Push the same way as above, with the matching repo URL.
3. In the repo's **Settings → Pages**, set **Source** to "Deploy from a branch" → `main` → `/ (root)`.
4. The site goes live at `https://<your-username>.github.io/<repo-name>`.

## Custom domain (kwasiadidako.com)

If you want the site at `kwasiadidako.com` instead:

1. Create a `CNAME` file in this folder containing just `kwasiadidako.com` (no protocol, no path).
2. In your domain registrar, point the DNS:
   - `A` records for the apex domain → `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
   - `CNAME` for `www` → `<your-username>.github.io`
3. In the GitHub repo's **Settings → Pages**, enter `kwasiadidako.com` as the custom domain and tick **Enforce HTTPS** once it's available.

## Editing later

The whole site is in `index.html`. Open it directly in a browser (`file://…/index.html`) to preview changes, or push and let GitHub Pages rebuild.
