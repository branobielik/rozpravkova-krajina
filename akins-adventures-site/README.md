# Akin's Adventures — samostatná stránka (GitHub Pages)

Tento priečinok je **samostatný** statický web pre doménu **www.akinsadventures.com**. V gite žije ako podpriečinok v *rozpravkova-krajina*, ale na GitHube ide do **vlastného nového repozitára** (nie do toho istého ako Rozprávková krajina).

## Nasadenie na GitHub

1. Na GitHube vytvor **nový repozitár** (napr. `akins-adventures`).
2. Skopíruj do nového repa **iba obsah** tohto priečinka (`index.html`, `styles.css`, `CNAME`, `.nojekyll`, tento `README.md`).

   ```bash
   cd cesta/k/akins-adventures-site
   git init
   git add .
   git commit -m "Initial site for Akin's Adventures"
   git branch -M main
   git remote add origin https://github.com/TVOJ-UCET/akins-adventures.git
   git push -u origin main
   ```

3. **Settings → Pages**: zdroj **Deploy from a branch**, vetva **main**, priečinok **/ (root)**.
4. **Settings → Pages → Custom domain**: `www.akinsadventures.com` (súbor `CNAME` je pripravený).
5. U registrátora **akinsadventures.com**: **CNAME** `www` → `TVOJ-UCET.github.io` (alebo podľa presného cieľa, ktorý GitHub zobrazí).
6. Po overení DNS zapni **Enforce HTTPS**.

Hlavná stránka projektu *Rozprávková krajina* má na obálke knihy odkaz na `https://www.akinsadventures.com`.

## Formulár „Subscribe via email“

Používa [FormSubmit](https://formsubmit.co/) (`formsubmit.co`) — odosiela na **akinthebook@gmail.com** bez vlastného servera. Pri **prvom** odoslaní môže FormSubmit poslať na túto adresu **potvrdzovací e-mail**; treba ho odkliknúť, aby formulár začal fungovať.
