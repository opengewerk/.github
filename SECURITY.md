# Sicherheitslücken melden

Danke, dass du dir die Mühe machst. Melde eine Sicherheitslücke bitte **nicht** als öffentliches Issue und nicht in den Discussions, sondern über das private Meldeformular von GitHub.

## So geht es

1. Öffne im betroffenen Repository den Reiter **Security**.
2. Wähle **Report a vulnerability** (Private Vulnerability Reporting).
3. Beschreibe die Lücke, die betroffene Stelle und, wenn möglich, wie sie sich nachvollziehen lässt.

Direktlinks:

- [opengewerk](https://github.com/opengewerk/opengewerk/security/advisories/new)
- [opengewerk-kanzlei](https://github.com/opengewerk/opengewerk-kanzlei/security/advisories/new)
- [opengewerk-api-spec](https://github.com/opengewerk/opengewerk-api-spec/security/advisories/new)

Auf diesem Weg sind Meldung und Diskussion privat, bis eine Behebung vorliegt. Eine eigene E-Mail-Adresse für Sicherheitsmeldungen gibt es bewusst nicht, weil ein Postfach ohne verlässliche Bearbeitung schlechter ist als gar keines.

## Was danach passiert

Das Projekt wird in der Freizeit entwickelt und befindet sich in der Planungsphase. Es gibt daher keine zugesicherte Reaktionszeit. Realistisch ist eine erste Rückmeldung innerhalb von zwei Wochen. Bleibt eine Antwort länger aus, ist eine freundliche Erinnerung im selben Advisory willkommen.

Ist die Lücke bestätigt und behoben, wird das Advisory veröffentlicht. Wer meldet, wird dort genannt, sofern er das möchte.

## Was in den Geltungsbereich fällt

Derzeit besteht das Projekt aus Konzeptdokumenten, einer API-Spezifikation und Repository-Gerüsten. Eine lauffähige Anwendung gibt es noch nicht.

Sinnvolle Meldungen betreffen deshalb aktuell vor allem:

- Fehler im Sicherheitsmodell der Spezifikation, etwa ein Endpunkt, der Daten außerhalb des dafür vorgesehenen Scopes freigäbe
- Schwächen im beschriebenen Verbindungsaufbau zwischen Mandant und Kanzlei-Hub
- Angaben in den Konzeptdokumenten, die zu einer unsicheren Umsetzung verleiten würden
- Probleme an der GitHub-Konfiguration der Organisation selbst

Sobald es Code gibt, kommen die üblichen Punkte dazu. Diese Datei wird dann ergänzt.

## Was nicht in den Geltungsbereich fällt

- Ergebnisse automatischer Scanner ohne nachvollziehbare Auswirkung
- Schwächen in Diensten Dritter, etwa GitHub selbst. Diese bitte direkt dort melden.
