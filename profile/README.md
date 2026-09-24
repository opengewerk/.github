<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/opengewerk/.github/main/brand/banner/opengewerk-banner-1280x640-dark.png">
  <img alt="OpenGewerk: Self-hosted CRM &amp; ERP für Handwerksbetriebe" src="https://raw.githubusercontent.com/opengewerk/.github/main/brand/banner/opengewerk-banner-1280x640-light.png" width="100%">
</picture>

# OpenGewerk

OpenGewerk ist eine Open-Source-Software für Handwerksbetriebe, die CRM und ERP in einem einzigen Datenmodell zusammenführt: Kunde, Objekt, Anlage, Auftrag, Beleg, Buchung. Kernmodul ist Elektro und PV, von Prüfprotokollen über den Messgeräte-Import bis zur PV-Dokumentation, und die Buchhaltung gehört dazu statt an einen Exportknopf zu enden. Alles läuft auf eigener Hardware, die Daten bleiben im Betrieb.

**Self-hosted · Open Source · Deutsch**

## Kein Tarifmodell

OpenGewerk ist nicht die kostenlose Alternative zu den etablierten Systemen. Es ist die Software, in der niemand eine Funktion zurückhält, um einen höheren Tarif zu verkaufen. Keine Tarifstufen, keine Nutzerlimits, keine Schnittstelle, die erst ab einem Paket freigeschaltet wird, und keine Auswertung, die von der gebuchten Stufe abhängt. Der Funktionsumfang ist der, der im Repository liegt.

Geld kann später neben der Software entstehen, nicht in ihr: Hosting für Betriebe, die nicht selbst hosten wollen, Installation und Migration, Support und Wartung, Schulungen, Anbindungen an Messgeräte und Fremdsysteme als Auftragsarbeit. Jede dieser Leistungen ist ein Angebot und keine Voraussetzung. Ein Betrieb muss OpenGewerk ohne fremde Hilfe betreiben können, sonst wäre die Beschränkung nur an eine andere Stelle gewandert.

Daraus folgt zweierlei: Es wird keine kommerzielle Fassung und keine bezahlten Erweiterungen geben, auch nicht vom Projekt selbst, und es gibt kein Contributor License Agreement. Ausführlich steht das in [Leitentscheidung 9 der Feature-Gliederung](https://github.com/opengewerk/opengewerk/blob/main/docs/konzept/Feature-Gliederung.md#0-leitentscheidungen).

## Die Repositories

| Repository | Wofür |
| --- | --- |
| [opengewerk](https://github.com/opengewerk/opengewerk) | Die Handwerkersoftware selbst: Angebot, Regiebericht, Rechnung, Plantafel, Zeiterfassung, Prüfprotokolle für Elektro und PV, vollständige Buchhaltung, GoBD-konform und als offline-fähige PWA. |
| [opengewerk-kanzlei](https://github.com/opengewerk/opengewerk-kanzlei) | Der Hub für Steuerberater, der alle OpenGewerk-Mandanten in einer Anwendung bündelt. Föderiert statt zentral, die Daten bleiben beim Mandanten. |
| [opengewerk-api-spec](https://github.com/opengewerk/opengewerk-api-spec) | Der gemeinsame API-Vertrag zwischen beiden: OpenAPI-Definition, JSON-Schemas und Konformitätstests, versioniert nach SemVer. |
| [opengewerk-website](https://github.com/opengewerk/opengewerk-website) | Die Website unter [opengewerk.de](https://opengewerk.de), als statisches HTML mit Astro gebaut. |
| [.github](https://github.com/opengewerk/.github) | Dieses Profil, die Beitragsregeln, der Verhaltenskodex, die Sicherheitsrichtlinie und die Marke. |

## Stand der Dinge

Das Fundament der Handwerkersoftware ist gebaut, und seit September 2026 entsteht Phase 1, der MVP für den Pilotbetrieb. Eine Installation läuft über Docker Compose auf eigener Hardware, wird im Browser eingerichtet, sichert sich jede Nacht selbst und führt Kunden mit ihren Ansprechpartnern, Objekte, Anlagen und Aufträge mit Nummer und Folgeaufträgen, im Büro wie auf der Baustelle und dort auch ohne Netz. Auf der Baustelle kommen Zeiterfassung, Fotos und Dateien, Aufgaben und die Elektro-Struktur einer Anlage mit Verteilern und Stromkreisen dazu, samt Stromkreisverzeichnis als PDF. Aus Angebot oder Kostenvoranschlag werden Auftragsbestätigung und Rechnung, mit Widerrufsbelehrung an jedem Angebot an einen Verbraucher; einen Regiebericht unterschreibt der Kunde auf dem Gerät. Rechnungen gibt es mit kumulierten Abschlägen, einer Schlussrechnung, die abzieht, was eingegangen ist, und Storno, als PDF und an Unternehmen als E-Rechnung, als XRechnung oder ZUGFeRD-PDF, und jeder Beleg geht auf Wunsch direkt per E-Mail an den Kunden. Was noch fehlt und in welcher Reihenfolge es kommt, steht im Fahrplan in Abschnitt 10 der Feature-Gliederung, was davon offen ist, im [Meilenstein Phase 1](https://github.com/opengewerk/opengewerk/milestone/2).

Der Kanzlei-Hub ist noch in der Planung. Er baut auf der Buchhaltung der Handwerkersoftware auf, die dort mit Phase 3 kommt; bis dahin wird der gemeinsame API-Vertrag weitergeführt.

Den vollständigen Funktionsumfang beschreiben die beiden Konzepte:

- [Feature-Gliederung der Handwerkersoftware](https://github.com/opengewerk/opengewerk/blob/main/docs/konzept/Feature-Gliederung.md)
- [Planungskonzept des Kanzlei-Hubs](https://github.com/opengewerk/opengewerk-kanzlei/blob/main/docs/konzept/Planungskonzept.md)

Einen Überblick, auch im Vergleich mit anderen Lösungen, gibt [opengewerk.de](https://opengewerk.de). Fachliche Rückmeldung aus dem Betriebs- oder Kanzleialltag ist gerade wertvoller als Code.

## Mitmachen

Die [Beitragsregeln](https://github.com/opengewerk/.github/blob/main/CONTRIBUTING.md) und der [Verhaltenskodex](https://github.com/opengewerk/.github/blob/main/CODE_OF_CONDUCT.md) gelten für alle Repositories der Organisation. Sicherheitslücken bitte über den Weg in [SECURITY.md](https://github.com/opengewerk/.github/blob/main/SECURITY.md) melden, nicht als öffentliches Issue.

Für kurze Fragen gibt es einen [Discord-Server](https://discord.gg/NRrEvbQdxz). Er ersetzt die Discussions nicht: was dort geklärt wird und für andere zählt, gehört hinterher in eine Discussion oder ein Issue.

## Branding

Logo, Bildmarke, App-Icons und Banner liegen in diesem Repository unter [`brand/`](https://github.com/opengewerk/.github/tree/main/brand). Das ist die einzige Quelle; die anderen Repositories binden die Dateien per Raw-URL ein, damit es keine Kopien gibt. Farben, Dateizuordnung und Schutzraum stehen in [`brand/README.md`](https://github.com/opengewerk/.github/blob/main/brand/README.md).
