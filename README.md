# Transformation Control Tower (sample)

A single-page prototype of a portfolio view for a transformation office. Each initiative has a baseline, target, owner and next milestone, with change readiness and continuity exposure beside the benefits. A "supply shock" toggle delays route-dependent initiatives by 4 weeks, and a Board note is drafted from the data.

**All data is invented for illustration. It is not from any real organisation.**

No build step and no dependencies: one `index.html` (it loads two fonts from Google Fonts and falls back to system fonts without them).

## Run it locally
Open `index.html` in a browser, or serve the folder:

```bash
python3 -m http.server 8000   # then open http://localhost:8000
```

## Put it on GitHub and publish it (GitHub Pages)
1. Create a free account at github.com if you do not have one.
2. Click **New repository**. Name it `transformation-control-tower`, choose **Public** (free Pages needs a public repo on a free plan), and do **not** tick "Add a README". Click **Create repository**.
3. On your computer, open a terminal in this folder and run (replace `YOUR-USERNAME`):
   ```bash
   git remote add origin https://github.com/YOUR-USERNAME/transformation-control-tower.git
   git branch -M main
   git push -u origin main
   ```
   GitHub will ask you to sign in. Use a personal access token as the password if it asks for one (GitHub: Settings, Developer settings, Personal access tokens).
4. In the repository, open **Settings**, then **Pages**.
5. Under **Build and deployment**, set **Source** to **Deploy from a branch**, **Branch** to `main`, folder `/ (root)`, then **Save**.
6. Wait one to two minutes and refresh the Pages screen. It shows your link: `https://YOUR-USERNAME.github.io/transformation-control-tower/`.
7. To change it later, edit `index.html`, then run `git add . && git commit -m "Update" && git push`. The site updates in a minute or two.

### No terminal? Upload in the browser
On the new repository page click **uploading an existing file**, drag in `index.html` and `README.md`, click **Commit changes**, then do steps 4 to 6.

### Other free hosts
- **Netlify:** go to app.netlify.com/drop and drag the folder in. You get a link immediately.
- **Cloudflare Pages or Vercel:** connect the GitHub repository and choose "no framework, no build command".

## Make it your own
The data is the `DATA` array near the bottom of `index.html`. Change names, baselines, targets and dates, and keep the "sample data" badge unless the data is real.

## 3D view

The page loads three.js r128 from cdnjs and fonts from Google Fonts, so it needs internet access. If WebGL or the CDN is blocked, the 3D panel shows a short message and the charts, list and Board note still work. To edit the data, change the `DATA` array in `index.html`; tower heights, charts and the note all follow it.
