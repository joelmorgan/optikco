# optikco landing page

Static HTML/CSS, no build step. Matches the Figma design (node 3832-1345) — dark hero with gradient headline, 4-item services grid, and OPTIK watermark CTA section.

## Run locally
Open `index.html` in a browser, or:
```
npx serve .
```

## Push to GitHub (from Cursor's terminal)
```
git init
git add .
git commit -m "Landing page"
git branch -M main
gh repo create optikco --public --source=. --push
```
(No `gh` CLI? Create an empty repo named `optikco` on github.com, then:)
```
git remote add origin https://github.com/<your-username>/optikco.git
git push -u origin main
```

## Deploy on Vercel
1. vercel.com → **Add New > Project** → import the `optikco` GitHub repo.
2. Framework preset: **Other** (it's static, no build command needed).
3. Deploy.
4. Project Settings → Domains → add `optikco.com` and follow the DNS instructions Vercel gives you (usually an A record to `76.76.21.21` or a CNAME to `cname.vercel-dns.com`, set at your domain registrar).

## Notes / next steps
- Hero background image lives at `assets/hero_bg.jpg`, referenced in `styles.css` under `.hero2-bg`.
- Service icons are inline SVGs (compass, layout, camera, pen).
- Contact button links to `mailto:hello@optikco.com` — update to your real address.
- Custom "OXIDATION" logotype font from the design isn't used (fell back to Inter Bold); add it to `styles.css` via `@font-face` if you have the license.
