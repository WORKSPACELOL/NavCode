# NAVCODE — Quick publish to GitHub Pages

This repository holds a simple static site. Follow the steps below to publish it on GitHub Pages (free) and get a shareable URL.

## 1) Create a GitHub repository
- Go to https://github.com and sign in / create an account.
- Click **New** and create a repository (e.g. `navcode-site`).
- You can leave it public and *do not* initialize with a README (we already have files locally).

## 2) Push your local `WEBSITE` folder to GitHub
Open a terminal (Git Bash or Command Prompt) in this folder (`WEBSITE`) and run:

```bash
git init
git add .
git commit -m "Initial site"
git branch -M main
# Replace <YOUR-USERNAME> with your GitHub username before running:
git remote add origin https://github.com/WORKSPACELOL/navecode-prototype.git
git push -u origin main
```

## 3) Enable GitHub Pages
- In GitHub, open the repository page > Settings > Pages.
- Under "Source", choose branch `main` and folder `/ (root)`, then Save.
- After a minute or two your site will be available at `https://WORKSPACELOL.github.io/navecode-prototype/`.

## Notes & suggestions
- Filenames with spaces (like `WEB BG.png`) can cause issues. Rename to `web-bg.png` for reliability and update CSS:

```css
background: url('web-bg.png') center/cover no-repeat fixed;
```

- If you want the site at `https://<YOUR-USERNAME>.github.io/` (no repo segment), name the repository exactly `<YOUR-USERNAME>.github.io` and push there.

If you'd like, I can also commit these changes for you and produce the exact `git remote add` command with your GitHub username. Provide your GitHub username (so I can fill it in), or run the commands above yourself after replacing `<YOUR-USERNAME>`.
