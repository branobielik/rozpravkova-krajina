# Rozprávková krajina

Statická landing page pre [GitHub Pages](https://pages.github.com/).

## Doména (mapovanie na GitHub Pages)

1. V repozitári: **Settings → Pages** — zdroj: vetva `main`, priečinok `/ (root)`.
2. V sekcii **Custom domain** zadaj `www.rozpravkovakrajina.sk` a ulož (súbor `CNAME` je už v repozitári).
3. U registrátora domény v DNS nastav:
   - **CNAME** pre host `www` → `branobielik.github.io` (presný cieľ uvidíš v GitHub Pages po uložení domény).
4. Po propagácii DNS zapni **Enforce HTTPS** v nastaveniach Pages.

_Apex doména_ (`rozpravkovakrajina.sk` bez `www`): v DNS pridaj A záznamy podľa [dokumentácie GitHub](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/managing-a-custom-domain-for-your-github-pages-site#configuring-an-apex-domain), alebo presmerovanie z apex na `www` u registrátora.

## Lokálny vývoj

Otvor `index.html` v prehliadači alebo spusti jednoduchý server v koreňovom priečinku projektu.
