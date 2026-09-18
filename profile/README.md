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

## Die drei Repositories

| Repository | Wofür |
| --- | --- |
| [opengewerk](https://github.com/opengewerk/opengewerk) | Die Handwerkersoftware selbst: Angebot, Regiebericht, Rechnung, Plantafel, Zeiterfassung, Prüfprotokolle für Elektro und PV, vollständige Buchhaltung, GoBD-konform und als offline-fähige PWA. |
| [opengewerk-kanzlei](https://github.com/opengewerk/opengewerk-kanzlei) | Der Hub für Steuerberater, der alle OpenGewerk-Mandanten in einer Anwendung bündelt. Föderiert statt zentral, die Daten bleiben beim Mandanten. |
| [opengewerk-api-spec](https://github.com/opengewerk/opengewerk-api-spec) | Der gemeinsame API-Vertrag zwischen beiden: OpenAPI-Definition, JSON-Schemas und Konformitätstests, versioniert nach SemVer. |

## Stand der Dinge

Das Projekt ist in der **Planungsphase**. Es gibt noch keinen lauffähigen Code, wohl aber zwei ausgearbeitete Konzepte, die den Funktionsumfang vollständig beschreiben:

- [Feature-Gliederung der Handwerkersoftware](https://github.com/opengewerk/opengewerk/blob/main/docs/konzept/Feature-Gliederung.md)
- [Planungskonzept des Kanzlei-Hubs](https://github.com/opengewerk/opengewerk-kanzlei/blob/main/docs/konzept/Planungskonzept.md)

Wer mitreden will, fängt dort an. Fachliche Rückmeldung aus dem Betriebs- oder Kanzleialltag ist gerade wertvoller als Code.

## Mitmachen

Die [Beitragsregeln](https://github.com/opengewerk/.github/blob/main/CONTRIBUTING.md) und der [Verhaltenskodex](https://github.com/opengewerk/.github/blob/main/CODE_OF_CONDUCT.md) gelten für alle Repositories der Organisation. Sicherheitslücken bitte über den Weg in [SECURITY.md](https://github.com/opengewerk/.github/blob/main/SECURITY.md) melden, nicht als öffentliches Issue.

## Branding

Logo, Bildmarke, App-Icons und Banner liegen in diesem Repository unter [`brand/`](https://github.com/opengewerk/.github/tree/main/brand). Das ist die einzige Quelle; die anderen Repositories binden die Dateien per Raw-URL ein, damit es keine Kopien gibt. Farben, Dateizuordnung und Schutzraum stehen in [`brand/README.md`](https://github.com/opengewerk/.github/blob/main/brand/README.md).
