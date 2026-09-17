# OpenGewerk

OpenGewerk ist eine Open-Source-Software für Handwerksbetriebe, die CRM und ERP in einem einzigen Datenmodell zusammenführt: Kunde, Objekt, Anlage, Auftrag, Beleg, Buchung. Kernmodul ist Elektro und PV, von Prüfprotokollen über den Messgeräte-Import bis zur PV-Dokumentation, und die Buchhaltung gehört dazu statt an einen Exportknopf zu enden. Alles läuft auf eigener Hardware, die Daten bleiben im Betrieb.

**Self-hosted · Open Source · Deutsch**

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
