# UFAG Job Feed (GitHub Pages)

Dette repo hoster en JSON-fil med ufaglærte job til din web-app.

## Filer
- `ufag_jobs.json` – selve feedet (kan opdateres dagligt)
- `index.html` – en lille informations-/preview-side
- `.nojekyll` – sikrer at JSON serves korrekt på GitHub Pages

## Kom i gang (2 minutter)
1. Opret et nyt public repository på GitHub, fx **ufag-job-feed**.
2. Upload disse tre filer til repoet.
3. Gå til **Settings → Pages** og vælg **Deploy from branch**. Vælg **Branch: main**, **/ (root)**. Gem.
4. Vent 1–2 minutter. Din side vil få en URL i stil med:  
   `https://<dit-brugernavn>.github.io/ufag-job-feed/`
5. Feed-URL’en bliver:  
   `https://<dit-brugernavn>.github.io/ufag-job-feed/ufag_jobs.json`

## Brug i appen
Sæt miljøvariablen i frontend:
```bash
NEXT_PUBLIC_FEED_URL="https://<dit-brugernavn>.github.io/ufag-job-feed/ufag_jobs.json"
```
Appen vil nu læse data direkte fra dit hostede JSON.

## Opdatering af data
- Erstat blot indholdet i `ufag_jobs.json` og commit/push.
- GitHub Pages opdaterer automatisk (normalt inden for 1–2 min).

## JSON-format
Eksempel på en post:
```json
{
  "id": "pelican-studentconsulting-2025-07-17-rodovre",
  "title": "Butiksmedarbejder (deltid, 28 t/uge)",
  "company": "Pelican Self Storage (via StudentConsulting)",
  "location": "Rødovre/København",
  "source": "StudentConsulting",
  "url": "https://www.studentconsulting.com/",
  "posted_at": "2025-07-17",
  "deadline": "2025-09-12",
  "is_new": false
}
```

> Tip: Læg den daglige liste ind her (kun nye i forhold til i går), så matcher det din agent-logik.

---
*Senest genereret: 2025-08-09T10:55:35*
