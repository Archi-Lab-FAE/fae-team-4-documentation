#### Anmerkungen SB 29.11. (bitte nach Bearbeitung löschen)
* Das README sollte die "Eintrittskarte" in das Repo bieten. Hierhin gehört:
   * das Domain Vision Statement - in einer Form, dass ein **Außenstehender** versteht, worum es geht.
   * Hinweise auf Weiterlesen (Wiki)	
* die Elemente unten gehören aus meiner Sicht teilweise in die Decisions, teils ins Glossar, teils in Wiki

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

* CUD eines [Alarmknopfes](https://github.com/Archi-Lab-FAE/fae-global-documentation/blob/master/2019-11-15-Glossary-Alarmknopf.md) -> Update der Knopf-Entity
* CUD einer [DementiellErkranktenPerson](https://github.com/Archi-Lab-FAE/fae-global-documentation/blob/master/2019-11-15-Glossary-Dementiell%20erkrankter.md) -> Update der DementiellErkranktePerson-Entity
* Neue Position -> Update der letzten erfassten Position in DementiellErkranktePerson-Entity
* Knopfdruck -> Ausführung der Business-Logik und ggf. Erstellung eines [AlarmknopfHilferuf](https://github.com/Archi-Lab-FAE/fae-global-documentation/blob/master/2019-11-18-Glossary-Alarmknopf-Hilferuf.md).
