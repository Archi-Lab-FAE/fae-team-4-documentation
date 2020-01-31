---
layout: post
title: Verwendung von DTOs
author: team4
categories: team4
requirement level: should
---

Wir wollen DTOs in den IO Schichten (api, eventing) verwenden, wenn es sinnvoll ist. Dies ermöglicht uns, Jsons zu flatten oder erspart uns, die Domain anzupassen, wenn sich eine Schnittstelle ändern soll.