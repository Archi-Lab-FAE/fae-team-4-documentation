---
layout: post
title: Team4 Entity Decision
author: team4
categories: team4
---

| Entity                    | Eigenschaft  | Erlärung                                                                                                    |
|---------------------------|--------------|-------------------------------------------------------------------------------------------------------------|
| DementiellErkranktePerson |              | Wird für die Alarmierung der Angehörigen benötigt                                                           |
|                           | id           | Mapping Hilferuf auf Person                                                                                 |
|                           | trackerId    | Wird von Service, der tracker anlegt, erstellt. Deshalb einfacher String                                    |
|                           | position     | Die zuletzt über Kafka übermittlete Position                                                                |
| Alarmknopf                |              | Bei unserem Service ankommende Meldung                                                                      |
|                           | id           | Von Service, der Registrierung des Knopfes vornimmt, erstllt. Deswegen einfacher String                     |
|                           | position     | Position des Knopfes                                                                                        |
| Alarmknopfdruck           |              | Bei unserem Service ankommende Meldung                                                                      |
|                           | alarmknopfId | eindeutige id für Knopf. Wird vom Controller zugewiesen. String, weil nicht von uns erstellt oder überprüft |
| Position                  |              | Einbettbare Klasse, die Eigenschaften einer Position enthält                                                |
|                           | id           | von uns zugewiesene id. Deshalb UUID.                                                                       |
|                           | laengengrad  | Eigenschaft einer Position                                                                                  |
|                           | breitengrad  | Eigenschaft einer Position                                                                                  |
| Laengengrad               |              | Kapsel für den Laengengrad                                                                                  |
|                           | laengengrad  |                                                                                                             |
| Breitengrad               |              | Kapsel für den Breitengrad                                                                                  |
|                           | breitengrad  |                                                                                                             |
|                           |              |                                                                                                             |
|                           |              |                                                                                                             |

	

## Kommentar SB 29.11. (bitte nach Bearbeitung löschen)
* hier draus sollten Sie eher eine Grundsatzentscheidung machen: "Wie sehen unsere IDs aus"
* Bitte fügen Sie noch eine neue Decision für Ihr Time-Tracking ein: 
   * welche Daten erfassen Sie bei der Eingabe und wieso?
   * zeitliche Granularität, in der Sie Ihre Aktivitäten erfassen (15min, 1h, ...) und wieso
* es wäre hilfreich, wenn Sie schon einmal eine Beispiel-Auswertung, basierend auf Ihrer bis hierhin aufgewendeten Zeit, in Ihre Dokumentation aufnehmen würden.
* gibt es keine weiteren Entscheidungen bis jetzt?	
