# Portfolio — Hari Charan Boddu

A single-file, scroll-driven 3D portfolio built with Three.js. No build step — `index.html` is the entire site.

## Deploy to GitHub Pages

1. Create a new repo on GitHub. If you want it at `https://<username>.github.io`, name the repo exactly `<username>.github.io`. Otherwise any name works and it'll deploy to `https://<username>.github.io/<repo-name>`.

2. From this folder:
   ```bash
   git init
   git add .
   git commit -m "Initial portfolio"
   git branch -M main
   git remote add origin https://github.com/<username>/<repo-name>.git
   git push -u origin main
   ```

3. On GitHub: go to the repo → **Settings → Pages** → under "Build and deployment", set **Source** to "Deploy from a branch" → branch `main`, folder `/ (root)` → **Save**.

4. Wait a minute or two, then visit the URL GitHub shows on that same Pages settings screen (either `https://<username>.github.io` or `https://<username>.github.io/<repo-name>`).

## Updating the resume links

Once your site is live, update the "Portfolio" and "GitHub" links in `Hari_Charan_Boddu_Resume_DevOps.docx` to point to the real URL instead of the placeholders.

## Editing content

Everything lives in `index.html`:
- Section text (About, Experience, Projects, Skills, Contact) is plain HTML — edit directly.
- The 3D scene logic is in the `<script>` block near the bottom. Each "station" (hero, experience, projects, skills, contact) is its own `THREE.Group` positioned along the z-axis; scrolling moves the camera through them.
