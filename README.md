# rangolideeksha.github.io

Personal portfolio of **Deeksha Dadhich** — built on the [al-folio](https://github.com/alshedivat/al-folio) Jekyll theme (gem `al_folio_core`), deployed via GitHub Pages.

## Structure
- `_pages/` — about, projects, cv, publications
- `_projects/` — one markdown file per project, grouped into pillars via the `category` field
- `_bibliography/papers.bib` — publications
- `_data/socials.yml` — contact & social links
- `assets/pdf/` — CV PDFs (master + role-targeted)
- `CNAME` — custom domain (rangolideeksha.com)

## Add a project (your extensibility workflow)
1. Copy `_projects/TEMPLATE.md` to a new file, e.g. `_projects/my-new-thing.md`.
2. Fill in title / description / result; set `category` to one of the pillars listed in `_pages/projects.md`.
3. Delete the `published: false` line.
4. `git add . && git commit -m "add project" && git push` — the site rebuilds automatically.

## Deploy
1. Create a **public** repo named `rangolideeksha.github.io` on GitHub.
2. `git remote add origin https://github.com/rangolideeksha/rangolideeksha.github.io.git`
3. `git push -u origin main`
4. Repo → **Settings → Pages → Build and deployment → Source: GitHub Actions** (this repo ships `.github/workflows/deploy.yml`). The first push triggers the build.
5. **Custom domain:** at your DNS provider point `rangolideeksha.com` to GitHub Pages (A records to GitHub's IPs + a `CNAME` record for `www` → `rangolideeksha.github.io`). The `CNAME` file here is already set.

## Run locally (optional)
```
bundle install
bundle exec jekyll serve
# http://localhost:4000
```

## TODO before launch
- Replace `assets/img/prof_pic.jpg` with your photo.
- Confirm `github_username` in `_data/socials.yml` (currently `rangolideeksha`).
- Add Google Scholar / ORCID in `_data/socials.yml` when ready.
