# compare-palme3 — project guide

Static HTML site served at **compare.palme3.dk**.

## Dev & deploy (git-pull flow, same model as ecDocs)
- **This is the local working copy** on DEVBOX2 (`C:\Users\devbox2\projects\compare-palme3`). Edit here, commit, and push to GitHub (`Palmegg/compare-palme3`, branch `main`). **GitHub is the single source of truth.**
- **Deploy:** run the **"Deploy compare-palme3"** desktop shortcut (= `C:\Users\devbox2\bin\deploy-compare-palme3.ps1`). It pushes to GitHub, then websites-lxc runs `git pull` in the webroot. Live within seconds.
- **Never edit on the server.** `/var/www/sites/compare-palme3` on websites-lxc is a read-only puller (read-only GitHub deploy key). Anything edited there is overwritten on the next deploy.

## Hosting
- Server: **websites-lxc** (10.10.20.27), webroot `/var/www/sites/compare-palme3`, nginx → exposed via Nginx Proxy Manager. `.git` is denied in the nginx config (not web-exposed).
