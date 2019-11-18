# Tracking der aufgewendeten Zeit

Zu klären

# Domäne AlarmKnopf-Hilferuf Vision-Statement

Die Domäne AlarmKnopf-Hilferuf hält die Aufgabe, auf das Drücken eines [AlarmKnopfes](https://github.com/Archi-Lab-FAE/fae-global-documentation/blob/master/2019-11-15-Glossary-Alarmknopf.md) zu reagieren.
Nach einem Knopfdruck wird der zugehörige [AlarmKnopf](https://github.com/Archi-Lab-FAE/fae-global-documentation/blob/master/2019-11-15-Glossary-Alarmknopf.md) ermittelt und die sich darum befindlichen
[dementiell erkrankten Personen](https://github.com/Archi-Lab-FAE/fae-global-documentation/blob/master/2019-11-15-Glossary-Dementiell%20erkrankter.md). Für diese wird dann ein [Knopf-Hilferuf](https://github.com/Archi-Lab-FAE/fae-global-documentation/blob/master/2019-11-18-Glossary-Knopf-Hilferuf.md) erzeugt.

# Lokales Datenmodell

* [AlarmKnopf](https://github.com/Archi-Lab-FAE/fae-global-documentation/blob/master/2019-11-15-Glossary-Alarmknopf.md) - Id, Position
* [DementiellErkranktePerson](https://github.com/Archi-Lab-FAE/fae-global-documentation/blob/master/2019-11-15-Glossary-Dementiell%20erkrankter.md) - Id, GpsSenderId, LetzteErfasstePosition
* [KnopfHilferuf](https://github.com/Archi-Lab-FAE/fae-global-documentation/blob/master/2019-11-18-Glossary-Knopf-Hilferuf.md) - DementiellErkranktePersonId

# Mapping der Events auf lokales Datenmodell

* CRUD eines [AlarmKnopfes](https://github.com/Archi-Lab-FAE/fae-global-documentation/blob/master/2019-11-15-Glossary-Alarmknopf.md) -> Update der Knopf-Entity
* CRUD einer [DementiellErkranktenPerson](https://github.com/Archi-Lab-FAE/fae-global-documentation/blob/master/2019-11-15-Glossary-Dementiell%20erkrankter.md) -> Update der DementiellErkranktePerson-Entity
* Neue Position -> Update der letzten erfassten Position in DementiellErkranktePerson-Entity
* Knopfdruck -> Ausführung der Business-Logik und ggf. Erstellung eines [KnopfHilferuf](https://github.com/Archi-Lab-FAE/fae-global-documentation/blob/master/2019-11-18-Glossary-Knopf-Hilferuf.md).
