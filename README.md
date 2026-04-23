# aidvokat.cz – web Ondřeje Hanáka

## Struktura souborů

```
/
├── index.html          ← hlavní stránka
├── content.json        ← CELÝ OBSAH WEBU – edituj zde nebo přes CMS
├── admin/
│   ├── index.html      ← Netlify CMS panel
│   └── config.yml      ← konfigurace CMS
└── images/             ← sem nahraj obrázky (vytvoří Netlify CMS)
```

## Jak nasadit na Netlify + aidvokat.cz

### 1. GitHub
1. Vytvoř nový repozitář na github.com (např. `aidvokat`)
2. Nahraj všechny soubory do repozitáře

### 2. Netlify
1. Jdi na netlify.com → **Add new site → Import an existing project**
2. Vyber GitHub a vyber repozitář `aidvokat`
3. Build command: *nechat prázdné*
4. Publish directory: `.` (tečka)
5. Klikni **Deploy site**

### 3. Doména aidvokat.cz
1. V Netlify: **Domain settings → Add custom domain** → zadej `aidvokat.cz`
2. Netlify ti ukáže DNS záznamy – nastav je u svého registrátora domény
3. Počkej pár minut na propagaci

### 4. Netlify CMS (admin rozhraní)
1. V Netlify: **Identity → Enable Identity**
2. **Identity → Registration → Invite only**
3. **Identity → Services → Git Gateway → Enable**
4. Pozvi sebe: **Identity → Invite users** → zadej svůj email
5. V souboru `admin/config.yml` nahraď `TVOJE_GITHUB_USERNAME` svým GitHub username

### 5. Přihlášení do CMS
- Jdi na `https://aidvokat.cz/admin`
- Přijmi pozvánku z emailu a nastav heslo
- Hotovo – obsah edituj přes vizuální rozhraní

## Ruční úprava obsahu
Pokud nechceš používat CMS, stačí otevřít `content.json` v libovolném textovém editoru a upravit texty. Po uložení a pushnutí na GitHub se Netlify automaticky aktualizuje.
