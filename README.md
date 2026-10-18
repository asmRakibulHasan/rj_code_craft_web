# RJ Code Craft Website

Developer website for **RJ Code Craft**, an indie Android studio. It's a plain static site (HTML + CSS, no build step) hosted on GitHub Pages and linked from Google Play Console.

## Pages
| File | Purpose |
|------|---------|
| `index.html` | Home: hero, apps, about, contact |
| `404.html` | Page shown by GitHub Pages for missing URLs |
| `styles.css` | All styles |
| `assets/` | Favicon and images |

The privacy policy is hosted on Google Sites: https://sites.google.com/view/rj-code-craft/privacy-policy

## Preview locally
```sh
python3 -m http.server 8000
```
Then open http://localhost:8000

## Deploy
Push to `main`. GitHub Pages (Settings → Pages → Deploy from branch → `main` / root) publishes it automatically.

## Adding a new app
Copy the `<article class="app-card">` block in `index.html`, then change the name, description, features and Play link. Each app also needs a privacy policy that names it (on Google Sites).

See `PLAN.md` for progress.
