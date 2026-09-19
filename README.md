# KHH Analytics — Website

Static marketing site for KHH Analytics. Plain HTML, CSS, and JavaScript — no build
step, no dependencies, no framework. Deployable directly to GitHub Pages.

## Files

| File | Purpose |
| --- | --- |
| `index.html` | The entire site (single page, anchored sections) |
| `styles.css` | Design system + layout |
| `script.js` | Mobile nav, scroll reveal, footer year |
| `favicon.svg` | Monogram mark |
| `.nojekyll` | Tells GitHub Pages to serve files as-is |
| `robots.txt` | Crawler directives |

## Local preview

Open `index.html` in a browser, or serve it:

    python -m http.server 8000

Then visit <http://localhost:8000>.

## Deploying to GitHub Pages

1. Push this directory to a GitHub repository.
2. In the repo: **Settings → Pages → Source → Deploy from a branch**.
3. Choose branch `main`, folder `/ (root)`, then **Save**.
4. The site publishes in 1–2 minutes.

**URL depends on the repo name:**

- Repo named `<username>.github.io` → `https://<username>.github.io`
- Any other repo name → `https://<username>.github.io/<repo-name>`

All asset paths in this site are relative, so either option works without edits.

### Custom domain (khhanalytics.com)

1. Add a file named `CNAME` at the repo root containing one line: `khhanalytics.com`
2. At your DNS registrar, create four `A` records for the apex domain pointing to
   `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`,
   and a `CNAME` record for `www` pointing to `<username>.github.io`.
3. In **Settings → Pages**, enter the domain and tick **Enforce HTTPS** once the
   certificate has been provisioned.

Do not add the `CNAME` file before DNS is configured — Pages will fail to serve
the site until the records resolve.

## Editing content

All copy lives in `index.html` as ordinary markup. Section order is controlled by
the `<section>` elements; the nav links to their `id` attributes.

Brand colors are CSS custom properties at the top of `styles.css` (`:root`).
Changing `--accent` restyles the whole site.

## Legal note

The footer contains a general-purpose disclaimer. Investment-related marketing is
regulated — if KHH Analytics is or becomes a registered investment adviser, have
securities counsel review this page before publishing, particularly any language
describing expected or comparative performance.
