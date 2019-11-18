#### Anmerkungen SB 15.11. (bitte nach Bearbeitung löschen)
* Domain Vision Statement: 
    * Wenn Sie Begriffe dort verwenden, bitte verlinken Sie immer auf das Glossar. 

# Tracking der aufgewendeten Zeit

Zu klären

# Domäne Knopf-Hilferuf Vision-Statement

Die Domäne Knopf-Hilferuf hält die Aufgabe, auf das Drücken eines Knopfes zu reagieren.
Nach einem Knopfdruck wird der zugehörige Alarmknopf ermittelt und die sich darum befindlichen
dementiell erkrankten Personen. Für diese wird dann ein Knopf-Hilferuf erzeugt.

# Lokales Datenmodell

* Knopf - Id, Position
* DementiellErkranktePerson - Id, GpsSenderId, LetzteErfasstePosition
* KnopfHilferuf - DementiellErkranktePersonId

# Mapping der Events auf lokales Datenmodell

* CRUD eines Knopfes -> Update der Knopf-Entity
* CRUD eines Dementiell erkrankten Person -> Update der DementiellErkranktePerson-Entity
* Neue Position -> Update der letzten erfassten Position in DementiellErkranktePerson-Entity
* Knopfdruck -> Ausführung der Business-Logik und ggf. Erstellung eines KnopfHilferuf.