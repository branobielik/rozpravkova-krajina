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

## Lokálny vývoj

Otvor `index.html` v prehliadači alebo spusti jednoduchý server v koreňovom priečinku projektu.
