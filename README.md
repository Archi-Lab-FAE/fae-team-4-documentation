# Tracking der aufgewendeten Zeit

Zu klären

# Domäne Alarmknopf-Hilferuf Vision-Statement

Die Domäne Alarmknopf-Hilferuf hält die Aufgabe, auf das Drücken eines [Alarmknopfes](https://github.com/Archi-Lab-FAE/fae-global-documentation/blob/master/2019-11-15-Glossary-Alarmknopf.md) zu reagieren.
Nach einem Knopfdruck wird der zugehörige [Alarmknopf](https://github.com/Archi-Lab-FAE/fae-global-documentation/blob/master/2019-11-15-Glossary-Alarmknopf.md) ermittelt und die sich darum befindlichen
[dementiell erkrankten Personen](https://github.com/Archi-Lab-FAE/fae-global-documentation/blob/master/2019-11-15-Glossary-Dementiell%20erkrankter.md). Für diese wird dann ein [Alarmknopf-Hilferuf](https://github.com/Archi-Lab-FAE/fae-global-documentation/blob/master/2019-11-18-Glossary-Alarmknopf-Hilferuf.md) erzeugt.

# Lokales Datenmodell

* [Alarmknopf](https://github.com/Archi-Lab-FAE/fae-global-documentation/blob/master/2019-11-15-Glossary-Alarmknopf.md) - Id, Position
* [DementiellErkranktePerson](https://github.com/Archi-Lab-FAE/fae-global-documentation/blob/master/2019-11-15-Glossary-Dementiell%20erkrankter.md) - Id, GpsSenderId, LetzteErfasstePosition
* [AlarmknopfHilferuf](https://github.com/Archi-Lab-FAE/fae-global-documentation/blob/master/2019-11-18-Glossary-Alarmknopf-Hilferuf.md) - DementiellErkranktePersonId

# Mapping der Events auf lokales Datenmodell

* CRUD eines [Alarmknopfes](https://github.com/Archi-Lab-FAE/fae-global-documentation/blob/master/2019-11-15-Glossary-Alarmknopf.md) -> Update der Knopf-Entity
* CRUD einer [DementiellErkranktenPerson](https://github.com/Archi-Lab-FAE/fae-global-documentation/blob/master/2019-11-15-Glossary-Dementiell%20erkrankter.md) -> Update der DementiellErkranktePerson-Entity
* Neue Position -> Update der letzten erfassten Position in DementiellErkranktePerson-Entity
* Knopfdruck -> Ausführung der Business-Logik und ggf. Erstellung eines [AlarmknopfHilferuf](https://github.com/Archi-Lab-FAE/fae-global-documentation/blob/master/2019-11-18-Glossary-Alarmknopf-Hilferuf.md).
