---
layout: post
title: Team4 Entity Decision
author: team4
categories: team4
---

| Entity                    | Eigenschaft  | Erlärung                                                                                                    |
|---------------------------|--------------|-------------------------------------------------------------------------------------------------------------|                                                                                                     |
| Alarmknopf                |              | Bei unserem Service ankommende Meldung                                                                      |
|                           | id           | Von Service, der Registrierung des Knopfes vornimmt, erstllt. Deswegen einfacher String                     |
|                           | position     | Position des Knopfes                                                                                        |
|                	    | radius       | Radius, in welchem der Knopf getriggert wird.                                                               |
|			    | name         | Name des Ortes, an dem der Knopf sich befindet                                                              |
|                           |              |                                                                                                             |
| Alarmknopfdruck           |              | Bei unserem Service ankommende Meldung                                                                      |
|                           | alarmknopfId | eindeutige id für Knopf. Wird vom Controller zugewiesen. String, weil nicht von uns erstellt oder überprüft |
|                           |              |                                                                                                             |
| Position                  |              | Einbettbare Klasse, die Eigenschaften einer Position enthält                                                |                                                                       |
|                           | laengengrad  | Eigenschaft einer Position                                                                                  |
|                           | breitengrad  | Eigenschaft einer Position                                                                                  |
|                           |              |                                                                                                             |
| Laengengrad               |              | Kapsel für den Laengengrad                                                                                  |
|                           | laengengrad  |                                                                                                             |
|                           |              |                                                                                                             |
| Breitengrad               |              | Kapsel für den Breitengrad                                                                                  |
|                           | breitengrad  |       
|			    |              |
| Tracker                   | id           | Id aus Registrierungs service
|                           | Position     | letzte position des trackers                                                                                                   