# Rajkumar PN — Portfolio

Static, production-built site. Ready to deploy directly on GitHub Pages.

## Deploy on GitHub Pages

1. Create a new repository on GitHub (e.g. `portfolio`).
2. Upload **all files in this folder** (including the hidden `.nojekyll` file) to the root of that repository — either via "Add file → Upload files" on github.com, or:
   ```bash
   git init
   git add .
   git commit -m "Initial deploy"
   git branch -M main
   git remote add origin https://github.com/<your-username>/<your-repo>.git
   git push -u origin main
   ```
3. In the repository, go to **Settings → Pages**.
4. Under **Build and deployment → Source**, choose **Deploy from a branch**.
5. Under **Branch**, choose `main` and folder `/ (root)`, then **Save**.
6. Wait a minute or two — GitHub will show your live URL at the top of the Pages settings page:
   `https://<your-username>.github.io/<your-repo>/`

That's it — no build step needed on GitHub's side, this folder is already the compiled output.

## Notes
- All asset paths (`static/`, `projects/`, `profile.png`, `resume.pdf`) are relative, so the site works correctly whether it's served at the root of a domain or under a `/repo-name/` subpath — no config changes needed either way.
- The `.nojekyll` file tells GitHub Pages to skip Jekyll processing (its default static site generator), which otherwise ignores files/folders starting with `_` and can interfere with the build output.
- The contact form posts directly to Formspree — no backend server is required for this site to work.
