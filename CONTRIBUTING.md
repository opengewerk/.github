# Mitwirken an OpenGewerk

Schön, dass du hier bist. Diese Regeln gelten für alle Repositories der Organisation `opengewerk`.

Die Handwerkersoftware läuft und steht vor dem ersten Pilotbetrieb: Kunden, Objekte und Aufträge, Angebot bis Rechnung mit E-Rechnung, der Regiebericht mit Unterschrift und die Zeiterfassung auf der Baustelle, auch ohne Netz. Der Kanzlei-Hub ist noch ein Konzept mit einer API-Spezifikation. Fachliche Rückmeldung aus dem Betriebsalltag ist deshalb weiter mehr wert als jeder Pull Request: Was fehlt in der Belegkette? Welche Frist überwacht heute niemand? Welche Prüfung im Elektrohandwerk läuft noch auf Papier, weil keine Software sie abbildet?

## Wo was hingehört

| Anliegen | Ort |
| --- | --- |
| Frage, Idee, Erfahrungsbericht, noch kein konkreter Vorschlag | Discussions des passenden Repositories |
| Kurze Frage, Zuruf, jemanden erreichen | [Discord](https://discord.gg/NRrEvbQdxz) |
| Konkreter Fehler | Issue mit der Vorlage *Fehlerbericht* |
| Konkreter Funktionswunsch oder Konzeptänderung | Issue mit der Vorlage *Funktionswunsch* |
| Sicherheitslücke | **Nicht** öffentlich, siehe [SECURITY.md](SECURITY.md) |
| Änderung an Dokument, Spezifikation oder Code | Pull Request |

Welches Repository das richtige ist:

- [`opengewerk`](https://github.com/opengewerk/opengewerk) für alles, was der Handwerksbetrieb benutzt.
- [`opengewerk-kanzlei`](https://github.com/opengewerk/opengewerk-kanzlei) für alles, was die Steuerberaterkanzlei benutzt.
- [`opengewerk-api-spec`](https://github.com/opengewerk/opengewerk-api-spec) für alles, was zwischen beiden über die Leitung geht.
- [`opengewerk-website`](https://github.com/opengewerk/opengewerk-website) für die Seite unter opengewerk.de.

Im Zweifel reicht ein Issue im Hauptrepository, es wird dann verschoben.

Der [Discord-Server](https://discord.gg/NRrEvbQdxz) ist für das Dazwischen: eine kurze Frage, ein Zuruf, jemanden erreichen. Er ersetzt die Discussions nicht, denn ein Chatverlauf ist nicht durchsuchbar. Was dort geklärt wird und für andere zählt, gehört hinterher in eine Discussion oder ein Issue, sonst findet es in einem halben Jahr niemand wieder.

## Labels und Vorlagen

Alle Repositories haben dieselben sechs Labels: *Fehler*, *Funktionswunsch*, *Dokumentation*, *Konzept*, *Gute erste Aufgabe* und *Hilfe gesucht*, mit denselben Farben und Beschreibungen. `opengewerk` hat dazu je ein Label für seine Module und Bereiche. Ein neues Repository bekommt die sechs mit `gh label clone opengewerk/opengewerk-api-spec --repo opengewerk/<neues-repository>`, danach werden die englischen Vorgaben von GitHub gelöscht.

Die Vorlagen für Issues in diesem Repository unter `.github/ISSUE_TEMPLATE` gelten für jedes Repository der Organisation ohne eigene, heute für die Website und für dieses Repository selbst. Die Anwendung, der Kanzlei-Hub und die Spezifikation haben eigene.

## Sprache

- Dokumente, Issues, Pull-Request-Beschreibungen, Labels und Oberflächentexte sind auf **Deutsch**.
- Eingebürgerte Fachbegriffe bleiben englisch: Pull Request, Issue, Commit, Branch, Repository, Scope, Webhook.
- **Code ist Englisch**, ohne Ausnahme: Bezeichner, Kommentare, Testnamen und die Namen von Code-Dateien, auch in Migrationen und in den Skripten der Workflows. Deutsch bleibt, was ein Mensch in einer Oberfläche liest, etwa ein `name:` eines Workflows oder die Meldung einer Prüfung.
- Feldnamen in Datenstrukturen und JSON-Schemas sind englisch, ihre Beschreibungen deutsch.
- Lizenztexte werden nicht übersetzt.

## Dateien

Das gilt für jede Datei in jedem Repository der Organisation, und die CI prüft es bei jedem Push:

- **UTF-8 ohne BOM.** Umlaute stehen direkt im Text, ä ö ü ß, kein HTML-Escaping.
- **LF als Zeilenende**, geregelt über `.gitattributes`. Unter Windows nichts an `core.autocrlf` drehen, das erledigt die Datei.
- Einrückung und Leerzeichen richten sich nach `.editorconfig`.
- Keine Platzhalter wie TODO, TBD oder Beispieltext in committeten Dateien. Was noch nicht existiert, wird in einem Satz beschrieben.
- Im Hauptrepository ist die Formatierung Teil der Prüfung: vor dem Commit `pnpm run format`, sonst wird der Job "Typprüfung, Lint und Tests" rot. Markdown, Workflows und Migrationen nimmt `.prettierignore` aus.

## Commits

- Eine Commit-Nachricht sagt auf Deutsch, was sich ändert, in der Gegenwartsform: `Scope-Tabelle um Zuordnung zu Endpunkten ergänzt`.
- Erste Zeile kurz, danach Leerzeile, dann bei Bedarf die Begründung. Das Warum gehört in den Text, nicht in den Code.
- Ein Commit ist eine Änderung. Aufräumen und Inhalt nicht mischen.

## Pull Requests

1. Fork anlegen oder, mit Schreibrechten, einen Branch von `main` abzweigen.
2. Änderung umsetzen und `CHANGELOG.md` unter `## [Unreleased]` ergänzen, im passenden Abschnitt und mit einem Satz, warum. Das gehört zu jedem Pull Request in einem Repository mit CHANGELOG; `.github` und `opengewerk-website` haben keines.
3. Pull Request eröffnen, die Vorlage ausfüllen und auf das zugehörige Issue verweisen. Soll der Pull Request ein Issue schließen, gehört unter den deutschen Text eine englische Zeile `Closes #<Nummer>`: GitHub erkennt nur die englischen Schlüsselwörter, ein „Schließt #12“ bewirkt nichts.
4. Auf die Prüfung warten. `main` ist geschützt, direkte Pushes gibt es nicht.

Große Änderungen bitte vorher als Issue oder Discussion abstimmen. Ein fertiger Pull Request, dessen Richtung nicht passt, ist für beide Seiten ärgerlich.

## Änderungen an den Konzeptdokumenten

Die Konzepte unter `docs/konzept/` sind die verbindliche Quelle für den Funktionsumfang, auch jetzt, wo es Code gibt: was gebaut wird, steht zuerst dort. Für sie gilt zusätzlich:

- Versionsnummer in der Kopfzeile anheben und das Änderungsprotokoll am Dateiende ergänzen.
- Falsches wird an der Stelle selbst korrigiert, an der es steht. Eine Richtigstellung 400 Zeilen weiter unten liest niemand rechtzeitig.
- Betrifft die Änderung mehrere Repositories, im Pull Request darauf hinweisen.
- Rechtliche Aussagen brauchen eine Fundstelle: Paragraf, Norm oder Frist. Eine allgemeine Einschätzung reicht nicht.
- Jeder Punkt der Feature-Gliederung hat eine Phase in Abschnitt 10. Wer einen Punkt einträgt, trägt seine Phase im selben Zug ein.

## Änderungen an der API-Spezifikation

- Erst den Vertrag ändern, dann die Implementierungen. Nie umgekehrt.
- Prüfen, ob die Änderung ein Breaking Change ist. Die Kriterien stehen in der README von `opengewerk-api-spec`.
- Scopes, Endpunkte und Webhooks müssen zwischen Spezifikation und Konzeptdokumenten übereinstimmen.

## Architekturentscheidungen

Entscheidungen, die schwer umkehrbar sind oder mehrere Module betreffen, werden als Architecture Decision Record festgehalten, siehe `docs/adr/` im Hauptrepository. Wer eine bestehende Entscheidung umstoßen will, schreibt ein neues Record und setzt das alte auf `überholt durch`. Weicht der Code in einem Punkt ab, ohne die Entscheidung umzustoßen, bekommt das Record einen datierten Nachtrag mit Grund; umgeschrieben wird ein angenommenes Record nicht.

## Lizenz deiner Beiträge

Mit einem Pull Request stellst du deinen Beitrag unter die Lizenz des jeweiligen Repositories: AGPL-3.0 für `opengewerk`, `opengewerk-kanzlei` und `opengewerk-website`, Apache-2.0 für `opengewerk-api-spec`. Ein Contributor License Agreement gibt es nicht, und das ist eine Festlegung, keine Lücke: Ein CLA bräuchte das Projekt nur, um seinen eigenen Code später zusätzlich unter eine geschlossene Lizenz stellen zu können. Genau das soll es nicht geben. Siehe Leitentscheidung 9 der Feature-Gliederung.

## Umgang miteinander

Es gilt der [Verhaltenskodex](CODE_OF_CONDUCT.md) der Organisation.
