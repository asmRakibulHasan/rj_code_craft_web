# RJ Code Craft Website: Plan & Progress

Goal: turn the "RJ Code Craft Website" design into a static site, host it on GitHub Pages, and link it from Google Play Console.

- Design source: https://claude.ai/artifact/9YktRogdYRj7DH8mnr7w1M
- Live site URL: https://asmrakibulhasan.github.io/rj_code_craft_web/
- app-ads.txt URL: https://asmrakibulhasan.github.io/app-ads.txt (repo `asmRakibulHasan/asmRakibulHasan.github.io`)
- GitHub repo: https://github.com/asmRakibulHasan/rj_code_craft_web

**Status legend:** `[x]` done · `[ ]` to do · `[~]` in progress

---

## Phase 0: Planning
- [x] Review the design (header, hero, Prank Sounds app card, About, Contact, footer)
- [x] Write the plan
- [ ] Answer the open questions (below)

## Phase 1: Build the static website
- [x] Create `index.html` with the same layout, copy, fonts (Space Grotesk + DM Sans) and colours (accent `#FFD23F`)
- [x] Create `styles.css` that works at phone width (checked at 1440px and 390px)
- [x] Privacy policy: link to the Google Sites page (decided 2026-10-19; local `privacy-policy.html` removed)
- [ ] Fix the app name in the Google Sites policy: "Prank Sounds - Prank Unlimited" → "Prank Sounds: Air Horn & Taser" (**you do this on Google Sites**)
- [x] Add `assets/favicon.svg`; keep the drawn phone mockup (decided 2026-10-19)
- [~] Add SEO and share tags: title, description and Open Graph text are done; still need `og:image`, `og:url` and canonical URL once the live URL is known
- [x] Add `404.html`
- [x] Add `app-ads.txt` (AdMob `pub-5915419200767915`)
- [x] Serve `app-ads.txt` at the domain root: https://asmrakibulhasan.github.io/app-ads.txt (repo `asmRakibulHasan.github.io`, `63b51a4`)
- [x] Add `README.md` and `.nojekyll`
- [ ] Review locally and get approval (`python3 -m http.server 8000` → http://localhost:8000)

Target structure:
```
rj-code-craft-web/
├── index.html
├── styles.css
├── assets/
├── app-ads.txt      (if AdMob)
├── 404.html
├── .nojekyll
└── README.md
```

## Phase 2: Publish on GitHub Pages
- [x] `git init` and first commit (`f0d4f2a`)
- [x] Create the GitHub repo: `asmRakibulHasan/rj_code_craft_web` (project repo, so `app-ads.txt` needs a custom domain or a user-site repo)
- [x] Push to `main`
- [x] Make the repo public and turn on Pages: Settings → Pages → deploy from `main` / root
- [ ] (Optional) Custom domain: `CNAME` file + DNS records + enforce HTTPS
- [x] Check that the home page, privacy policy link and all Play links open (all 200)

> Note: `app-ads.txt` must sit at the **domain root**. A project repo (`username.github.io/repo/`) won't work for it; use a user-site repo or a custom domain.

## Phase 3: Add to Google Play Console
- [x] Website: Grow users → Store presence → Store settings → Store listing contact details (live on the Play listing)
- [x] Privacy policy: already set to the Google Sites page in Play Console (no change needed)
- [ ] (Optional) Developer page → website
- [x] (AdMob) Developer website set in Play and `app-ads.txt` live
- [ ] In AdMob: Apps → app-ads.txt → "Check for updates" (verification can take up to 24h)
- [x] Confirm the changes appear on the Play listing

---

## Open questions
| # | Question | Answer |
|---|----------|--------|
| 1 | GitHub username, and repo type (`username.github.io` or project repo)? | `asmRakibulHasan`, project repo `rj_code_craft_web` |
| 2 | Do you use AdMob or other ads? AdMob publisher ID (`pub-…`)? | Yes, AdMob `pub-5915419200767915` |
| 3 | Privacy policy: copy into the site, or keep the Google Sites link? | Keep using Google Sites; the website links there |
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
| 2026-10-19 | Website added in Play Console; it now shows on the Play listing. |
| 2026-10-19 | Website live on GitHub Pages; all links checked. Created the `asmRakibulHasan.github.io` repo; `app-ads.txt` is live at the domain root. |
| 2026-10-19 | Added `app-ads.txt` (AdMob `pub-5915419200767915`). |
| 2026-10-19 | Privacy policy: switched to the Google Sites link and removed the local copy. Checked the Play listing: title "Prank Sounds: Air Horn & Taser", privacy policy = Google Sites. |
| 2026-10-19 | Pushed to GitHub (`asmRakibulHasan/rj_code_craft_web`, branch `main`). |
| 2026-10-19 | Phase 1 built: `index.html`, `styles.css`, `privacy-policy.html`, `404.html`, `assets/favicon.svg`, `README.md`, `.nojekyll`. Checked in Chrome at desktop and phone widths. Privacy links now point to the local page instead of Google Sites. |
