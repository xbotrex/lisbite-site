# LISBITE website deploy guide

This is a plain static website for GitHub Pages.

## Files

- `index.html` — website content
- `styles.css` — visual design
- `script.js` — mobile navigation and footer year
- `CNAME` — tells GitHub Pages to use `lisbite.com`
- `.nojekyll` — prevents GitHub from trying to process the site with Jekyll

## Upload to GitHub

1. Create a new public repository, for example `lisbite-site`.
2. Upload all files in this folder to the repository root.
3. Go to repository `Settings` → `Pages`.
4. Set source to `Deploy from a branch`.
5. Select branch `main` and folder `/root`.
6. Save.
7. Under `Custom domain`, enter `lisbite.com` and save.
8. Once DNS is correct, enable `Enforce HTTPS`.

## DNS records for the domain

At your domain registrar, set these records.

A records for the root/apex domain:

| Type | Host | Value |
| --- | --- | --- |
| A | @ | 185.199.108.153 |
| A | @ | 185.199.109.153 |
| A | @ | 185.199.110.153 |
| A | @ | 185.199.111.153 |

CNAME record for www:

| Type | Host | Value |
| --- | --- | --- |
| CNAME | www | YOUR-GITHUB-USERNAME.github.io |

Replace `YOUR-GITHUB-USERNAME` with your actual GitHub username.

## Edit the site

Replace placeholder text in `index.html`, especially:

- project names
- contact email
- social links
- descriptions
- update posts
