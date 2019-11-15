---
layout: post
title: Team4 Entity Decision
author: team4
categories: team4
---
* Person          | wird für die Alarmierung der Angehörigen benötigt
	* id              | Mapping Hilferuf auf Person
	* trackerId       | wird von Service, der tracker anlegt, erstellt. Deshalb einfacher String

* Knopfdruck      | bei unserem Service ankommende Meldung
	* id              | eindeutige id für Knopf. Wird vom Controller zugewiesen. String, weil nicht von uns erstellt oder überprüft

* Knopf           | ausgegebener Knopf 
	* id              | von Service, der Registrierung des Knopfes vornimmt, erstllt. Deswegen einfacher String
	* Position        | Position des Knopfes

* Position        | einbettbare Klasse, die Eigenschaften einer Position enthält
	* id              | von uns zugewiesene id. Deshalb UUID.
	* laengengrad     | Eigenschaft einer Position
	* breitengrad     | Eigenschaft einer Position

* Laengengrad     | Kapsel für den Laengengrad
	* laengengrad 

* Breitengrad     | Kapsel für den Breitengrad
	* breitengrad

* PersonPosition  | enhält die aktuelle Position einer Person
	* trackerId       | von Service, der Tracker registriert, erstellte ID. Deshalb einfacher String
	* position        | von Service, der Positionen der Personen verwaltet, übermittelte Position der Person
