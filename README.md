# Rozprávková krajina

Statická landing page pre [GitHub Pages](https://pages.github.com/).

## Doména (mapovanie na GitHub Pages)

1. V repozitári: **Settings → Pages** — zdroj: vetva `main`, priečinok `/ (root)`.
2. V sekcii **Custom domain** zadaj `www.rozpravkovakrajina.sk` a ulož (súbor `CNAME` je už v repozitári).
3. U registrátora domény v DNS nastav **obe** časti:

   **Subdoména `www`**
   - **CNAME**: host `www` → `branobielik.github.io`

   **Apex `rozpravkovakrajina.sk` (bez `www`)** — inak GitHub hlási *NotServedByPagesError* / „Domain does not resolve to the GitHub Pages server“.
   - Štyri **A** záznamy pre host `@` (alebo názov domény podľa panelu registrátora), každý na jednu IP:
     - `185.199.108.153`
     - `185.199.109.153`
     - `185.199.110.153`
     - `185.199.111.153`

   Aktuálne hodnoty sú v [dokumentácii GitHub](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/managing-a-custom-domain-for-your-github-pages-site#configuring-an-apex-domain). Ak registrátor podporuje len jeden A záznam, použij presmerovanie apex → `www` alebo ALIAS/ANAME podľa návodu u registrátora.

4. Po propagácii DNS v Pages klikni **Check again**, potom zapni **Enforce HTTPS**.

## Akin's Adventures — samostatná stránka a doména

Doména **`www.akinsadventures.com`** patrí **samostatnému** GitHub repozitáru (nie tomuto). V priečinku **`akins-adventures-site/`** v tomto repozitári je pripravený statický web s vlastným `CNAME` (nahraj ho ako koreň nového repa).

1. Vytvor nový repozitár na GitHube a nahraj doň obsah `akins-adventures-site` (postup v jeho **README.md**).
2. Zapni **GitHub Pages** z vetvy `main`, priečinok `/ (root)`.
3. V **Custom domain** zadaj `www.akinsadventures.com` a u registrátora nastav **CNAME** `www` → `tvoj-ucet.github.io` (presný tvar podľa nového repa).
4. Na hlavnej stránke *Rozprávka krajina* je obálka knihy *Akin's Adventures* odkazom na `https://www.akinsadventures.com`.

## Lokálny vývoj

Otvor `index.html` v prehliadači alebo spusti jednoduchý server v koreňovom priečinku projektu.
