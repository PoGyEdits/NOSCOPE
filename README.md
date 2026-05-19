# NOSCOPE Post Generator

Moderní webový nástroj pro generování grafik pro Instagram posty a stories týmu NOSCOPE.

## Klíčové vlastnosti
* **Předvolby textu (slide 2)**: Rychlý výběr hotových textů a sloganů s automatickým fialovým zvýrazněním.
* **Vrstvy na pozadí**: Podpora až 4 různých obrázků/vrstev. Každá vrstva má vlastní posun X/Y a možnost přiblížení (zoom).
* **Jednoduchá správa vrstev**: Změna pořadí vrstev (▲/▼) a mazání vrstev přímo v ovládacím panelu.
* **Export**: Stažení výsledného PNG obrázku v rozlišení 1440×1800 px připraveného pro Instagram.

---

## Návod na zprovoznění a nasazení (Cloudflare Pages)

Tento projekt je čistě statická webová stránka (HTML + JS), takže nepotřebuje žádný build ani speciální hosting.

### 1. Inicializace Git repozitáře a upload na GitHub
1. Otevřete terminál (PowerShell nebo Bash) ve složce s projektem.
2. Inicializujte Git:
   ```bash
   git init
   ```
3. Přidejte soubory a udělejte první commit:
   ```bash
   git add .
   git commit -m "feat: pridany vrstvy a textove predvolby"
   ```
4. Vytvořte nové repozitář na Vašem **GitHubu** (může být soukromý/private).
5. Propojte lokální složku s GitHubem a odešlete změny:
   ```bash
   git remote add origin URL_VASEHO_GIT_REPOZITARE
   git branch -M main
   git push -u origin main
   ```

### 2. Nasazení na Cloudflare Pages
1. Přihlaste se do administrace **Cloudflare**.
2. V levém menu přejděte na **Workers & Pages** -> **Create application** -> záložka **Pages** -> klikněte na **Connect to Git**.
3. Vyberte svůj GitHub účet a vyhledejte repozitář `Noscopepostgenerator`.
4. V nastavení buildu (**Build settings**):
   * **Framework preset**: Ponechte prázdné nebo vyberte `None`.
   * **Build command**: Ponechte prázdné.
   * **Build output directory**: Ponechte prázdné (nebo `/` - značí kořenový adresář).
5. Klikněte na **Save and Deploy**.
6. Cloudflare Pages web automaticky nasadí a vygeneruje Vám unikátní subdoménu (např. `noscopepostgenerator.pages.dev`). Jakmile nahrajete nový kód na GitHub, web se sám aktualizuje.
