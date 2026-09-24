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
- [opengewerk-website](https://github.com/opengewerk/opengewerk-website/security/advisories/new)

Auf diesem Weg sind Meldung und Diskussion privat, bis eine Behebung vorliegt. Eine eigene E-Mail-Adresse für Sicherheitsmeldungen gibt es bewusst nicht, weil ein Postfach ohne verlässliche Bearbeitung schlechter ist als gar keines.

## Welche Fassungen unterstützt werden

**Die Anwendung, `opengewerk`,** erscheint in Releases mit einer Fassungsnummer (`v0.x.y`). Eine Sicherheitskorrektur bekommt nur die jeweils neueste Fassung. Das genügt, weil ein Update jede Fassung überspringen darf: die Migrationen ziehen jeden älteren Stand hoch, wer also noch auf einer alten Fassung steht, geht mit der Korrektur direkt auf die neueste. Die Regel gilt für die Reihe 0.x und wird mit 1.0 neu entschieden.

Die Korrektur geht sofort nach der Behebung als neues Release von `main` hinaus, einen eigenen Zweig je Fassung gibt es nicht. Ihre Nummer folgt dem Inhalt: eine Patch-Fassung, wenn seit dem letzten Release nur Korrekturen dazugekommen sind, sonst eine neue Nebenversion, die dann auch neue Funktionen mitbringt. Eine Installation aus dem Quelltext bekommt die Behebung schon vorher, sobald sie auf `main` steht. Bis zum ersten Release gilt nur dieser zweite Weg.

**Die Spezifikation, `opengewerk-api-spec`,** unterstützt ihre neueste Fassung. Eine Lücke im Sicherheitsmodell wird mit einer neuen Fassung des Vertrags behoben; bricht die Behebung bestehende Implementierungen, ist es eine neue Hauptversion, wie bei jedem Bruch des Vertrags.

**Der Kanzlei-Hub und die Website** haben keine Releases. Unterstützt wird der Stand auf `main`, und die Website ist mit jedem Merge ausgeliefert.

## Was danach passiert

Das Projekt wird in der Freizeit entwickelt. Die Anwendung läuft und steht vor dem ersten Pilotbetrieb, der Kanzlei-Hub ist noch ein Konzept. Es gibt keine zugesicherte Reaktionszeit. Realistisch ist eine erste Rückmeldung innerhalb von zwei Wochen. Bleibt eine Antwort länger aus, ist eine freundliche Erinnerung im selben Advisory willkommen.

Ist die Lücke bestätigt und behoben, wird das Advisory veröffentlicht. Es nennt die betroffenen Fassungen und die Fassung, die die Korrektur enthält; ein Advisory aus der Zeit vor dem ersten Release nennt statt einer Fassung den Commit auf `main`, mit dem die Lücke behoben wurde. Wer meldet, wird dort genannt, wenn gewünscht.

## Wie Betreiber davon erfahren

An drei Stellen: im veröffentlichten Advisory, auf der Release-Seite der Fassung mit der Korrektur, die mit einem Hinweis darauf beginnt, und im Kanal `#ankündigungen` des [Discord-Servers](https://discord.gg/NRrEvbQdxz). Wer eine Instanz betreibt, abonniert am besten die Releases von [opengewerk](https://github.com/opengewerk/opengewerk) auf GitHub (Watch, Custom, Releases). Dann kommt jede neue Fassung als Benachrichtigung, eine Korrektur eingeschlossen.

## Was in den Geltungsbereich fällt

Die Handwerkersoftware in `opengewerk` ist lauffähig, mit Anmeldung, Mandantentrennung, Offline-Abgleich, Belegen und E-Mail-Versand. Dort interessieren vor allem:

- Anmeldung und Sitzungen, der zweite Faktor, Einladungslinks und die Ersteinrichtung einer leeren Instanz
- die Mandantentrennung: ein Betrieb, der Daten eines anderen lesen oder ändern kann, über die API, den Abgleich oder an der Row-Level Security der Datenbank vorbei
- Rechte und Rollen: eine Rolle, die mehr darf, als ihre Rechte sagen, etwa ein Monteur, der Belege festschreibt
- der Offline-Abgleich: ein Gerät, das etwas schreibt, das es nicht schreiben darf, oder einen festgeschriebenen Beleg ändert
- Belege und Dateien: PDF, E-Rechnung, Unterschrift, der Dateispeicher und die Dokumentenablage mit Fotos von der Baustelle
- die Zeiterfassung, vor allem der Standort, den es nur mit Einwilligung gibt, und dass niemand die Zeiten anderer sieht, der sie nicht sehen darf
- die E-Mail-Einstellungen eines Betriebs und die dort versiegelten Zugangsdaten
- Schutz gegen fremde Seiten: Herkunftsprüfung, Cookies, Sicherheits-Header
- Sicherung, Rückspielen und Update, die Docker-Konfiguration und die Voreinstellungen einer neuen Installation

Außerdem weiterhin:

- Fehler im Sicherheitsmodell der API-Spezifikation, etwa ein Endpunkt, der Daten außerhalb des dafür vorgesehenen Scopes freigäbe
- Schwächen im beschriebenen Verbindungsaufbau zwischen Mandant und Kanzlei-Hub
- Angaben in den Konzeptdokumenten, die zu einer unsicheren Umsetzung verleiten würden
- die Website unter opengewerk.de und der Weg, auf dem sie ausgespielt wird
- Probleme an der GitHub-Konfiguration der Organisation selbst

## Was nicht in den Geltungsbereich fällt

- Ergebnisse automatischer Scanner ohne nachvollziehbare Auswirkung
- Angriffe, die schon Zugang zum Server, zur `.env` oder zur Datenbank einer Instanz voraussetzen
- eine Installation, die gegen die Anleitung betrieben wird, etwa ohne TLS vor der Anwendung
- Schwächen in Diensten Dritter, etwa GitHub selbst. Diese bitte direkt dort melden.
