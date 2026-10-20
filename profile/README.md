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
| [opengewerk-haustechnik](https://github.com/opengewerk/opengewerk-haustechnik) | Software für Betreiber von Gebäuden und ihre Haustechnik: Liegenschaften, Räume und Anlagen in einem Datenmodell, Betreiberpflichten als überwachte Fristen, Rundgänge und Prüfungen auch ohne Netz, unveränderliche Nachweise. Steht auf demselben Fundament wie die Handwerkersoftware. |
| [opengewerk-kanzlei](https://github.com/opengewerk/opengewerk-kanzlei) | Der Hub für Steuerberater, der alle OpenGewerk-Mandanten in einer Anwendung bündelt. Föderiert statt zentral, die Daten bleiben beim Mandanten. |
| [opengewerk-api-spec](https://github.com/opengewerk/opengewerk-api-spec) | Der gemeinsame API-Vertrag zwischen beiden: OpenAPI-Definition, JSON-Schemas und Konformitätstests, versioniert nach SemVer. |
| [opengewerk-website](https://github.com/opengewerk/opengewerk-website) | Die Website unter [opengewerk.de](https://opengewerk.de), als statisches HTML mit Astro gebaut. |
| [.github](https://github.com/opengewerk/.github) | Dieses Profil, die Beitragsregeln, der Verhaltenskodex, die Sicherheitsrichtlinie und die Marke. |

## Stand der Dinge

**Handwerkersoftware.** Das Fundament und Phase 1, der MVP für den Pilotbetrieb, sind gebaut; die neueste Fassung ist [OpenGewerk 0.6.0](https://github.com/opengewerk/opengewerk/releases) vom 20.10.2026. Eine Installation läuft über Docker Compose auf eigener Hardware, auf x86_64 wie auf ARM64, kommt als Release mit signierten Abbildern, wird im Browser eingerichtet und sichert sich jede Nacht selbst. Sie führt Kunden, Objekte, Anlagen und Aufträge, im Büro wie auf der Baustelle und dort auch ohne Netz. Dazu gibt es:

- Belege von Angebot und Kostenvoranschlag über die Auftragsbestätigung bis zur Rechnung, mit Abschlägen, Schlussrechnung und Storno, als PDF, per E-Mail und an Unternehmen als E-Rechnung im Format XRechnung oder ZUGFeRD. An jedem Angebot an einen Verbraucher hängt die Widerrufsbelehrung.
- Den Regiebericht, auf der Baustelle geschrieben und vom Kunden auf dem Gerät unterschrieben, dazu Zeiterfassung, Fotos, Dateien und Aufgaben.
- Für Elektro die Struktur einer Anlage mit Verteilern und Stromkreisen, das Stromkreisverzeichnis als PDF und das Prüfprotokoll der Erstprüfung nach DIN VDE 0100-600, je Stromkreis gemessen, jeder Wert mit Grenzwert und Fundstelle, vom Prüfer auf dem Gerät unterschrieben.
- Aus Phase 2 bereits: Fristen, die von selbst entstehen, Push-Nachrichten auf die Geräte, das Änderungsprotokoll im Büro, Passkeys, mehrere Betriebe auf einer Instanz, die PV-Struktur einer Anlage, QR-Etiketten und Artikel mit Lieferanten.

Vor dem produktiven Einsatz stehen noch die fachliche Abnahme der Regelpakete und ein Praxistest der E-Rechnung bei einem echten Empfänger. Der Rest von Phase 2, dem Kern für Elektro und PV, ruht, solange die Haustechnik Vorrang hat; die Reihenfolge danach steht im Fahrplan in Abschnitt 10 der Feature-Gliederung.

**OpenGewerk Haustechnik** ist am 01.10.2026 dazugekommen: Software für alle, die Gebäude betreiben und dafür eigene Haustechniker haben. Sie steht auf demselben Fundament wie die Handwerkersoftware, das dafür in eigene Pakete herausgelöst wurde ([ADR 0010](https://github.com/opengewerk/opengewerk/blob/main/docs/adr/0010-fundament-als-pakete.md)). Am 15.10.2026 ist Phase 1, der MVP für den Pilotbetrieb, als erste Fassung erschienen, die neueste ist [OpenGewerk Haustechnik 0.1.9](https://github.com/opengewerk/opengewerk-haustechnik/releases) vom 20.10.2026. Ein Betreiber führt damit seine Liegenschaften bis zum Raum, seine Anlagen mit Akte, Etikett und Zählern, das Pflichtenverzeichnis mit Vorschlägen aus offenen Pflichtenpaketen, Nachweise mit Unterschrift und Festschreibung, Rundgänge vor Ort auch ohne Netz, Mängel, Aufträge und Dokumente; an Fristen erinnert sie per E-Mail und Push. Der Pilotbetrieb, ein Träger mit rund zwanzig Liegenschaften, betreibt sie seitdem parallel zu seiner bisherigen Anwendung. Version 1 ist erreicht, wenn er diese abschalten kann, und darauf arbeitet Phase 2 hin. Was davon fertig ist, erscheint in Zwischenfassungen: Störmeldungen mit und ohne Konto, Lager, Fremdfirmen und Verträge, die Pflichtenübertragung, die Pakete Raumluft und Kälte, Heizung sowie Förderanlagen und Arbeitsmittel, eigene Rollen und die Funktionen der DSGVO. Mit 0.1.9 kamen die Elektro-Struktur einer Anlage bis zum Stromkreis, mit Messwerten je Stromkreis, deren Grenzwerte als Regeln mit Fundstelle im Paket Elektro stehen, die PV-Struktur mit Wechselrichtern, Strings und Modulen und die Korrekturen aus der externen Sicherheitsprüfung. Offen sind noch deren Abschluss und die Fassung, die Phase 2 abschließt.

Der Kanzlei-Hub ist noch in der Planung. Er baut auf der Buchhaltung der Handwerkersoftware auf, die dort mit Phase 3 kommt; bis dahin wird der gemeinsame API-Vertrag weitergeführt.

Den vollständigen Funktionsumfang beschreiben die drei Konzepte:

- [Feature-Gliederung der Handwerkersoftware](https://github.com/opengewerk/opengewerk/blob/main/docs/konzept/Feature-Gliederung.md)
- [Planungskonzept von OpenGewerk Haustechnik](https://github.com/opengewerk/opengewerk-haustechnik/blob/main/docs/konzept/Planungskonzept.md)
- [Planungskonzept des Kanzlei-Hubs](https://github.com/opengewerk/opengewerk-kanzlei/blob/main/docs/konzept/Planungskonzept.md)

Einen Überblick, auch im Vergleich mit anderen Lösungen, gibt [opengewerk.de](https://opengewerk.de). Fachliche Rückmeldung aus dem Betriebs- oder Kanzleialltag ist gerade wertvoller als Code.

## Mitmachen

Die [Beitragsregeln](https://github.com/opengewerk/.github/blob/main/CONTRIBUTING.md) und der [Verhaltenskodex](https://github.com/opengewerk/.github/blob/main/CODE_OF_CONDUCT.md) gelten für alle Repositories der Organisation. Sicherheitslücken bitte über den Weg in [SECURITY.md](https://github.com/opengewerk/.github/blob/main/SECURITY.md) melden, nicht als öffentliches Issue.

Für kurze Fragen gibt es einen [Discord-Server](https://discord.gg/NRrEvbQdxz), für den Austausch unter Betrieben das Subreddit [r/OpenGewerk](https://www.reddit.com/r/OpenGewerk/). Beide ersetzen die Discussions nicht: was dort geklärt wird und für andere zählt, gehört hinterher in eine Discussion oder ein Issue.

## Branding

Logo, Bildmarke, App-Icons und Banner liegen in diesem Repository unter [`brand/`](https://github.com/opengewerk/.github/tree/main/brand). Das ist die einzige Quelle; die anderen Repositories binden die Dateien per Raw-URL ein, damit es keine Kopien gibt. Farben, Dateizuordnung und Schutzraum stehen in [`brand/README.md`](https://github.com/opengewerk/.github/blob/main/brand/README.md).
