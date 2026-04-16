# Website Performance Report: 10.04.2026 - 16.04.2026

Erstellt am: 16.04.2026 | Berichtszeitraum: letzte 7 Tage

> **Hinweis:** Die Plausible Analytics API war in dieser Sitzung nicht erreichbar.
> Der Server, auf dem dieser Agent lauft, wird von Plausible mit HTTP 403
> (`x-deny-reason: host_not_allowed`) abgewiesen. Plausible sperrt Anfragen
> von Rechenzentrum-IP-Adressen pauschal. Die Authentifizierungs-Tokens sind
> korrekt konfiguriert. Um dieses Problem zu beheben, muss der Agent entweder
> von einer zugelassenen IP-Adresse laufen oder Plausible muss die
> Server-IP freischalten. Eine Alternative ist die Nutzung des Plausible
> Stats API v1 mit einem API-Key uber einen erlaubten Aufrufkanal.

---

## expand-b2b.de

### Datenabruf-Status

| Endpunkt | Status |
|---|---|
| Quellen (sources) | Fehler: host_not_allowed |
| Seiten (pages) | Fehler: host_not_allowed |
| Lander (countries) | Fehler: host_not_allowed |
| Tagesverlauf (main-graph) | Fehler: host_not_allowed |

### Aufgerufene API-URLs

```
GET https://plausible.io/api/stats/expand-b2b.de/sources?period=7d&auth=***
GET https://plausible.io/api/stats/expand-b2b.de/pages?period=7d&auth=***
GET https://plausible.io/api/stats/expand-b2b.de/countries?period=7d&auth=***
GET https://plausible.io/api/stats/expand-b2b.de/main-graph?period=7d&auth=***
```

Alle Anfragen lieferten: `Host not in allowlist` (HTTP 403)

---

## santox.com

### Datenabruf-Status

| Endpunkt | Status |
|---|---|
| Quellen (sources) | Fehler: host_not_allowed |
| Seiten (pages) | Fehler: host_not_allowed |
| Lander (countries) | Fehler: host_not_allowed |
| Tagesverlauf (main-graph) | Fehler: host_not_allowed |

### Aufgerufene API-URLs

```
GET https://plausible.io/api/stats/santox.com/sources?period=7d&auth=***
GET https://plausible.io/api/stats/santox.com/pages?period=7d&auth=***
GET https://plausible.io/api/stats/santox.com/countries?period=7d&auth=***
GET https://plausible.io/api/stats/santox.com/main-graph?period=7d&auth=***
```

Alle Anfragen lieferten: `Host not in allowlist` (HTTP 403)

---

## Losungsansatze

### Option A: Plausible Stats API v1 mit API-Key

Statt Shared-Link-Tokens kann ein richtiger API-Key verwendet werden:

```bash
curl -H "Authorization: Bearer {API_KEY}" \
  "https://plausible.io/api/v1/stats/breakdown?site_id=expand-b2b.de&period=7d&property=visit:source"
```

API-Keys werden in Plausible unter **Settings > API Keys** erstellt.

### Option B: Server-IP bei Plausible freischalten

Plausible kann kontaktiert werden, um die IP-Adresse des Reporting-Servers
auf eine Whitelist zu setzen.

### Option C: Reporting uber einen zugelassenen Host

Der Reporting-Agent kann auf einem Server laufen, der bereits eine
Plausible-Verbindung hat (z. B. direkt auf der Webserver-Infrastruktur).

---

*Dieser Report wurde automatisch generiert. Bei Fragen: technik@expand-b2b.de*
