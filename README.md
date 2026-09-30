# products-site

Static landing pages and privacy policies for Header Tool, AI Chat Exporter and the FDA Recalls Monitor
Apify actor. Plain HTML plus one CSS file (`style.css`); no build step, no JavaScript, no analytics.

## Before publishing

Search for `TODO(owner)` and fix each hit:

- `header-tool/index.html`, `ai-chat-exporter/index.html`: Chrome Web Store link (after the listing exists).
- `fda-recalls/index.html`: Apify Store URL (also contains `YOUR_APIFY_USERNAME`).
- `header-tool/privacy.html`, `ai-chat-exporter/privacy.html`: contact email (`YOUR_EMAIL@example.com`).

```sh
rg "TODO\(owner\)|YOUR_EMAIL|YOUR_APIFY" .
```

## Publish on GitHub Pages (free)

1. On github.com create a new **public** repository named `products-site` (no README, no .gitignore).
2. From this folder:
   ```sh
   git remote add origin git@github.com:<username>/products-site.git
   git push -u origin main
   ```
3. In the repo go to Settings, Pages. Under "Build and deployment" set Source to "Deploy from a branch",
   Branch `main`, folder `/ (root)`, then Save.
4. After a minute the site is live at `https://<username>.github.io/products-site/`.

Preview locally: `python3 -m http.server` in this folder, then open http://localhost:8000.

## URLs

| Page | URL |
|---|---|
| Home | `https://<username>.github.io/products-site/` |
| Header Tool | `https://<username>.github.io/products-site/header-tool/` |
| Header Tool privacy | `https://<username>.github.io/products-site/header-tool/privacy.html` |
| AI Chat Exporter | `https://<username>.github.io/products-site/ai-chat-exporter/` |
| AI Chat Exporter privacy | `https://<username>.github.io/products-site/ai-chat-exporter/privacy.html` |
| FDA Recalls | `https://<username>.github.io/products-site/fda-recalls/` |

## Which URL goes where

- Chrome Web Store, Header Tool listing, Privacy policy field: `.../header-tool/privacy.html`
- Chrome Web Store, AI Chat Exporter listing, Privacy policy field: `.../ai-chat-exporter/privacy.html`
- Each Chrome Web Store listing's Homepage URL (optional): the product landing page.
- Support link: both extensions open `.../support.html`; fill in the `TODO(owner)` payment placeholders there first.
- Apify Store: the actor does not need a privacy policy URL; the landing page can be used as the website link.
- Both extensions have a `TODO(owner)` privacy URL in `src/config.ts`; replace `YOUR_GITHUB_USERNAME` with `whitel1ght` and rebuild.
