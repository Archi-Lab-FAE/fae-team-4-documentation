---
layout: post
title: Nur Put für Alarmknöpfe
author: team4
categories: team4
requirement level: must
---

Wir verwenden Put statt Post für Alarmknöpfe, da wir davon ausgehen, dass die ID des jeweiligen Alarmknopfes hart in der Hardware des Buzzers verbaut ist.
Würden wir Knöpfe abbauen und neu anmelden müssten wir die ID in der Hardware bei neu Aufstellen ändern. Durch die Verwendung von Put registrieren wir die Knopf Id einfach mit.