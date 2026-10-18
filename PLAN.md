# RJ Code Craft Website: Plan & Progress

Goal: turn the "RJ Code Craft Website" design into a static site, host it on GitHub Pages, and link it from Google Play Console.

- Design source: https://claude.ai/artifact/9YktRogdYRj7DH8mnr7w1M
- Live site URL: _TBD_
- GitHub repo: _TBD_

**Status legend:** `[x]` done · `[ ]` to do · `[~]` in progress

---

## Phase 0: Planning
- [x] Review the design (header, hero, Prank Sounds app card, About, Contact, footer)
- [x] Write the plan
- [ ] Answer the open questions (below)

## Phase 1: Build the static website
- [x] Create `index.html` with the same layout, copy, fonts (Space Grotesk + DM Sans) and colours (accent `#FFD23F`)
- [x] Create `styles.css` that works at phone width (checked at 1440px and 390px)
- [x] Create `privacy-policy.html` (copied word for word from the Google Sites page)
- [x] Add `assets/favicon.svg`; keep the drawn phone mockup (decided 2026-10-19)
- [~] Add SEO and share tags: title, description and Open Graph text are done; still need `og:image`, `og:url` and canonical URL once the live URL is known
- [x] Add `404.html`
- [ ] Add `app-ads.txt`: the privacy policy says the app uses AdMob, so this is needed; waiting for the AdMob publisher ID (`pub-…`)
- [x] Add `README.md` and `.nojekyll`
- [ ] Review locally and get approval (`python3 -m http.server 8000` → http://localhost:8000)

Target structure:
```
rj-code-craft-web/
├── index.html
├── privacy-policy.html
├── styles.css
├── assets/
├── app-ads.txt      (if AdMob)
├── 404.html
├── .nojekyll
└── README.md
```

## Phase 2: Publish on GitHub Pages
- [~] `git init` (done; branch is `master`, rename to `main` or deploy from `master`) and first commit
- [ ] Create the GitHub repo (`<username>.github.io` recommended)
- [ ] Push to `main`
- [ ] Turn on Pages: Settings → Pages → deploy from `main` / root
- [ ] (Optional) Custom domain: `CNAME` file + DNS records + enforce HTTPS
- [ ] Check that the home page, privacy policy and all Play links open

> Note: `app-ads.txt` must sit at the **domain root**. A project repo (`username.github.io/repo/`) won't work for it; use a user-site repo or a custom domain.

## Phase 3: Add to Google Play Console
- [ ] Website: Grow users → Store presence → Store settings → Store listing contact details
- [ ] Privacy policy: Policy and programs → App content → Privacy policy (for each app)
- [ ] (Optional) Developer page → website
- [ ] (If AdMob) Same developer website in Play, `app-ads.txt` live, then "Check for updates" in AdMob
- [ ] Confirm the changes appear after review (hours to a few days)

---

## Open questions
| # | Question | Answer |
|---|----------|--------|
| 1 | GitHub username, and repo type (`username.github.io` or project repo)? | |
| 2 | Do you use AdMob or other ads? AdMob publisher ID (`pub-…`)? | The privacy policy lists AdMob; need the publisher ID |
| 3 | Privacy policy: copy into the site, or keep the Google Sites link? | Copied into the site (`privacy-policy.html`) |
| 4 | Custom domain, or `github.io` for now? | |
| 5 | Real app icon and screenshots, or keep the drawn mockup? | Keep the drawn mockup |
| 6 | App name: the site says "Prank Sounds: Air Horn & Taser" but the privacy policy says "Prank Sounds - Prank Unlimited". Which matches the Play listing? | |

## Apps
| App | Package | Play link |
|-----|---------|-----------|
| Prank Sounds: Air Horn & Taser | `prank.airhornfarthaircutclippersound.hiprank.funnysound` | https://play.google.com/store/apps/details?id=prank.airhornfarthaircutclippersound.hiprank.funnysound |

## Progress log
| Date | Update |
|------|--------|
| 2026-10-19 | Reviewed the design and wrote the plan (Phases 0–3). |
| 2026-10-19 | Phase 1 built: `index.html`, `styles.css`, `privacy-policy.html`, `404.html`, `assets/favicon.svg`, `README.md`, `.nojekyll`. Checked in Chrome at desktop and phone widths. Privacy links now point to the local page instead of Google Sites. |
