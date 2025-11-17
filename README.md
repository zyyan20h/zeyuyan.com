# Personal + Lab Website Template with Subpaths

Single repo that serves:
- root index for personal homepage
- /repo for related work
- /lab for lab landing

## Local dev
```bash
bundle exec jekyll serve
# visit http://localhost:4000
```

## Deploy on GitHub Pages
- Repo name: zyyan20h.github.io
- Settings → Pages → Deploy from a branch → main → /

## Split later into separate repos or domains
- Copy the /lab folder into a new repo when ready
- Set custom domain for that repo, for example lab.zeyuyan.com
- Keep this repo serving the root and /repo paths
