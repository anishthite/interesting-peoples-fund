# The Side Project Fund

Not a fund. A few hours a week, given to whoever reaches out with a
side project or a startup they're stuck on.

A single-page static site in the thite.site style: et-book serif, warm
paper background, no build step, no frameworks.

## Run locally

```sh
python3 -m http.server
```

Then open <http://localhost:8000>.

## Files

- `index.html` — the entire site (self-contained HTML/CSS, no JS)
- `assets/fonts/` — et-book webfonts
- `.github/workflows/deploy.yml` — Cloudflare Pages deployment

## Deployment

Deployed to [Cloudflare Pages](https://pages.cloudflare.com/) via GitHub
Actions on every push to `main`. The workflow uses
`cloudflare/wrangler-action` and requires two repository secrets:

- `CLOUDFLARE_API_TOKEN`
- `CLOUDFLARE_ACCOUNT_ID`

The Cloudflare Pages project name is `interesting-peoples-fund`.
