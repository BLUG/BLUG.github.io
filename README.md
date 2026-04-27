# BLUG – Bergen Linux User Group

Nettside for Bergen Linux (and BSD) User Group, bygget med [Hugo](https://gohugo.io/) og [Hugo Blox](https://hugoblox.com/).

## Komme i gang

### Installer mise

Vi bruker [mise](https://mise.jdx.dev/) for å håndtere verktøy (Hugo, Go, Node.js). Installer mise først:

```bash
curl https://mise.run | sh
```

Følg instruksjonene for å aktivere mise i shellet ditt. Se [mise.jdx.dev](https://mise.jdx.dev/getting-started.html) for detaljer.

### Sett opp prosjektet

```bash
git clone git@github.com:BLUG/BLUG.github.io.git
cd BLUG.github.io
mise install       # Installerer Hugo, Go og Node.js
```

### Kjør utviklingsserver

```bash
mise run serve
```

Siden er nå tilgjengelig på [http://localhost:1313](http://localhost:1313).

### Bygg for produksjon

```bash
mise run build
```

## Legge til et nytt møte

Møter ligger i `content/event/`. Lag en ny fil med navn etter mønsteret `YYYY-MM-tema.md`:

```bash
cp content/event/2021-11-nextcloud.md content/event/2025-05-mittforedrag.md
```

Rediger frontmatteren (YAML mellom `---`) i den nye filen:

```yaml
---
title: "Tittel på foredraget"
date: "2025-05-29T18:30:00+02:00"
date_end: "2025-05-29T20:30:00+02:00"
summary: "Kort beskrivelse som vises på forsiden"
event: "BLUG"
event_url: "https://www.meetup.com/Bergen-Linux-and-BSD-User-Group/events/..."
location: "Media City Bergen - 'Pressekonferanse-rommet'"
authors:
  - "Navn på foredragsholder"
featured: true
links:
  - name: MeetUp
    url: "https://www.meetup.com/..."
---

Brødtekst med beskrivelse av foredraget i Markdown.

Dersom foredraget filmes, legg til video etter at den er lastet opp:

{{</* youtube VIDEO_ID */>}}
```

### Tips

- **Video**: Bruk `{{</* youtube VIDEO_ID */>}}` for å legge inn YouTube-video.
- **Bilder**: Legg bildefiler i `assets/media/` og referer til dem med `image: filename: "filnavn.jpg"` i frontmatteren.
- **Lenker**: Bruk `links:`-arrayet for MeetUp, Facebook og andre lenker.

## Publisering

Pushing til `master` trigger automatisk bygging og publisering til GitHub Pages via GitHub Actions. Siden blir tilgjengelig på [blug.linux.no](https://blug.linux.no).
