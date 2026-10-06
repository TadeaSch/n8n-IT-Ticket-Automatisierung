# n8n-IT-Ticket-Automatisierung

## Projektziel

Ziel des Projekts ist die Automatisierung und Unterstützung bei der Bearbeitung interner IT-Support-Anfragen mithilfe eines KI-gestützten Workflows. Die KI übernimmt insbesondere wiederkehrende Aufgaben wie das Lesen, Verstehen, Kategorisieren, Priorisieren und Zuordnen von Support-Anfragen. Bei bekannten Problemen kann der KI-Agent eine automatische Antwort erstellen. Nur die IT-Fachkraft kann ein Ticket schließen. Die fachliche Kontrolle und die finale Entscheidung bleiben beim Menschen.


## Verwendete Tools

- n8n
- LLM: OpenAI - gpt-oss-20b
- Email (SMTP)


## Workflow

1. Anfragen Eingang (hier im Pilot über n8n Forms, später gesammelt über E-Mail, Microsoft Teams und Ticketsystem)
2. automatische Eingangsbestätigung und Vergabe von Ticket-ID
3. KI-Analyse: Lesen, Verstehen, Kategorisieren, Priorisieren und Zuordnen
4. KI-Archiv-Vergleich: Suche nach gleichen oder ähnlichen bereits gelösten Problemen
5. Weiterleitung an zuständiges IT-Support-Personal mit KI-Lösungsvorschlag aus ähnlichen Problemen oder automatischer Antwort bei bekannten Problemen
6. Bearbeitung durch IT-Support-Personal mit anschließender Ticketschließung per Lösungsweg Angabe
7. Archivierung duch KI

<img width="2513" height="1183" alt="n8n_Workflow_Screenshot" src="https://github.com/user-attachments/assets/33dbf687-68f1-492e-8d43-b76ed30b1eac" />

## Herausforderungen

- Priorisierung: Für eine nachvollziehbare KI-generierte Priorisierung muss der Priorisierungsscore gemeinsam mit den IT-Fachkräften genau definiert werden.
- bekannte Anfragen: Nicht jede ähnliche Anfrage eignet sich für eine automatische Antwort, besonders bei: Passwort-Zurücksetzungen und Zugriffsrechten. Lösung (für Erweiterung): Die Archivsuche soll nur bei geeigneten IT-Problemen durchgeführt werden, anderen Anfragen werden direkt an die zuständige Person weitergeleitet.
- Datenschutz: Da Support-Anfragen personenbezogene oder andere sensible Informationen enthalten können, sollte ein lokal aufgesetztes LLM verwendet werden.


## Erweiterungen

- Anfragen Eingang gesammelt über mehrere Wege (E-Mail, Microsoft Teams und Ticketsystem)
- Archivsuche nur bei IT-Problemen
