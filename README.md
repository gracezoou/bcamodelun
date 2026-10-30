# BCA Model UN website

One-page site for Bergen County Academies Model UN: scrimmages, training videos, travel team, AMUN, history, and team.

## Files
- `index.html` — the whole site (styles and scripts are inside)
- `assets/logo.png` — club crest

## Adding a training video
Open `index.html`, find `const VIDEOS = [` near the bottom, and paste the Google Drive share link into that video's `url: ""`.
Make sure the Drive file is shared as **Anyone with the link → Viewer**, or visitors won't be able to watch it.
To add a new video, copy one line and change the title, category, blurb and url.
Categories: Basics, Parli Pro, Speaking, Writing, Crisis.

## Turning on GitHub Pages
1. Repo **Settings → Pages**
2. Source: **Deploy from a branch**, branch **main**, folder **/ (root)**, Save
3. The site goes live at `https://gracezoou.github.io/bcamodelun/` in a minute or two

## Connecting the Wix domain
In **Wix → Domains → (your domain) → Manage DNS records**:

| Type  | Host / Name | Value                    |
|-------|-------------|--------------------------|
| A     | @ (blank)   | 185.199.108.153          |
| A     | @ (blank)   | 185.199.109.153          |
| A     | @ (blank)   | 185.199.110.153          |
| A     | @ (blank)   | 185.199.111.153          |
| CNAME | www         | gracezoou.github.io      |

Delete any existing A records on `@` and the old `www` CNAME that point to Wix first.

Then on GitHub: **Settings → Pages → Custom domain**, enter the domain (e.g. `yourdomain.com`), Save. GitHub adds a `CNAME` file to the repo. Once the DNS check passes (can take up to 24 hours, usually much faster), tick **Enforce HTTPS**.
