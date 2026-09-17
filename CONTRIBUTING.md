# Mitwirken an OpenGewerk

Schön, dass du hier bist. Diese Regeln gelten für alle Repositories der Organisation `opengewerk`.

Das Projekt ist in der Planungsphase. Es gibt noch keinen lauffähigen Code, nur ausgearbeitete Konzepte, eine API-Spezifikation und die Repository-Gerüste. Deshalb ist fachliche Rückmeldung aus dem Betriebsalltag gerade mehr wert als jeder Pull Request: Was fehlt in der Belegkette? Welche Frist überwacht heute niemand? Welche Prüfung im Elektrohandwerk läuft noch auf Papier, weil keine Software sie abbildet?

## Wo was hingehört

| Anliegen | Ort |
| --- | --- |
| Frage, Idee, Erfahrungsbericht, noch kein konkreter Vorschlag | Discussions des passenden Repositories |
| Konkreter Fehler | Issue mit der Vorlage *Fehlerbericht* |
| Konkreter Funktionswunsch oder Konzeptänderung | Issue mit der Vorlage *Funktionswunsch* |
| Sicherheitslücke | **Nicht** öffentlich, siehe [SECURITY.md](SECURITY.md) |
| Änderung an Dokument, Spezifikation oder Code | Pull Request |

Welches Repository das richtige ist:

- [`opengewerk`](https://github.com/opengewerk/opengewerk) für alles, was der Handwerksbetrieb benutzt.
- [`opengewerk-kanzlei`](https://github.com/opengewerk/opengewerk-kanzlei) für alles, was die Steuerberaterkanzlei benutzt.
- [`opengewerk-api-spec`](https://github.com/opengewerk/opengewerk-api-spec) für alles, was zwischen beiden über die Leitung geht.

Im Zweifel reicht ein Issue im Hauptrepository, es wird dann verschoben.

## Sprache

- Dokumente, Issues, Pull-Request-Beschreibungen, Labels und Oberflächentexte sind auf **Deutsch**.
- Eingebürgerte Fachbegriffe bleiben englisch: Pull Request, Issue, Commit, Branch, Repository, Scope, Webhook.
- Feldnamen in Datenstrukturen und JSON-Schemas sind englisch, ihre Beschreibungen deutsch.
- Lizenztexte werden nicht übersetzt.

## Dateien

Das gilt für jede Datei in jedem Repository der Organisation, und die CI prüft es bei jedem Push:

- **UTF-8 ohne BOM.** Umlaute stehen direkt im Text, ä ö ü ß, kein HTML-Escaping.
- **LF als Zeilenende**, geregelt über `.gitattributes`. Unter Windows nichts an `core.autocrlf` drehen, das erledigt die Datei.
- Einrückung und Leerzeichen richten sich nach `.editorconfig`.
- Keine Platzhalter wie TODO, TBD oder Beispieltext in committeten Dateien. Was noch nicht existiert, wird in einem Satz beschrieben.

## Commits

- Eine Commit-Nachricht sagt auf Deutsch, was sich ändert, in der Gegenwartsform: `Scope-Tabelle um Zuordnung zu Endpunkten ergänzt`.
- Erste Zeile kurz, danach Leerzeile, dann bei Bedarf die Begründung. Das Warum gehört in den Text, nicht in den Code.
- Ein Commit ist eine Änderung. Aufräumen und Inhalt nicht mischen.

## Pull Requests

1. Fork anlegen oder, mit Schreibrechten, einen Branch von `main` abzweigen.
2. Änderung umsetzen und `CHANGELOG.md` unter `## [Unreleased]` ergänzen, wenn die Änderung für Anwender sichtbar ist.
3. Pull Request eröffnen, die Vorlage ausfüllen und auf das zugehörige Issue verweisen.
4. Auf die Prüfung warten. `main` ist geschützt, direkte Pushes gibt es nicht.

Große Änderungen bitte vorher als Issue oder Discussion abstimmen. Ein fertiger Pull Request, dessen Richtung nicht passt, ist für beide Seiten ärgerlich.

## Änderungen an den Konzeptdokumenten

Die Konzepte unter `docs/konzept/` sind die verbindliche Quelle, solange es keinen Code gibt. Für sie gilt zusätzlich:

- Versionsnummer in der Kopfzeile anheben und das Änderungsprotokoll am Dateiende ergänzen.
- Falsches wird an der Stelle selbst korrigiert, an der es steht. Eine Richtigstellung 400 Zeilen weiter unten liest niemand rechtzeitig.
- Betrifft die Änderung mehrere Repositories, im Pull Request darauf hinweisen.
- Rechtliche Aussagen brauchen eine Fundstelle: Paragraf, Norm oder Frist. Eine allgemeine Einschätzung reicht nicht.

## Änderungen an der API-Spezifikation

- Erst den Vertrag ändern, dann die Implementierungen. Nie umgekehrt.
- Prüfen, ob die Änderung ein Breaking Change ist. Die Kriterien stehen in der README von `opengewerk-api-spec`.
- Scopes, Endpunkte und Webhooks müssen zwischen Spezifikation und Konzeptdokumenten übereinstimmen.

## Architekturentscheidungen

Entscheidungen, die schwer umkehrbar sind oder mehrere Module betreffen, werden als Architecture Decision Record festgehalten, siehe `docs/adr/` im Hauptrepository. Wer eine bestehende Entscheidung umstoßen will, schreibt ein neues Record und setzt das alte auf `überholt durch`.

## Lizenz deiner Beiträge

Mit einem Pull Request stellst du deinen Beitrag unter die Lizenz des jeweiligen Repositories: AGPL-3.0 für `opengewerk` und `opengewerk-kanzlei`, Apache-2.0 für `opengewerk-api-spec`. Ein Contributor License Agreement gibt es nicht.

## Umgang miteinander

Es gilt der [Verhaltenskodex](CODE_OF_CONDUCT.md) der Organisation.
