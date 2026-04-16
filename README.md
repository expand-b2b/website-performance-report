# Website Performance Report

Automatisierter woechentlicher Report fuer die Plausible Analytics Daten von:
- **expand-b2b.de** (EXPAND B2B)
- **santox.com** (SANTOX)

## Ablauf

Ein Claude Code Scheduled Agent laeuft jeden Montag um 7:00 Uhr (Berlin):
1. Ruft die Plausible Stats API ab (Quellen, Seiten, Laender, Tagesverlauf)
2. Generiert einen Markdown-Report
3. Committet den Report in dieses Repo

## Reports

Reports werden als `YYYY-MM-DD-website-report.md` im Root-Verzeichnis abgelegt.

## Lokaler Zugriff

```bash
cd /c/tmp/website-performance-report
git pull origin main
```
