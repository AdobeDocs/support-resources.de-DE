---
title: Tabellenumbrüche
description: Testen verschiedener Tabellenumbrüche
hide: true
hidefromtoc: true
exl-id: a769fcb7-f8d3-419b-bdd4-98b71bdf3b5d
source-git-commit: 972704990172c966a27744b49b9f7af5626e9f3e
workflow-type: tm+mt
source-wordcount: '270'
ht-degree: 8%

---

# Tabellenumbrüche

Nicht viel zu sehen hier.

## Standard-Markdown-Tabelle mit `<br>`

**FESTE`Green<br>Red<br>Blue`**

|  | Zahl | Farben |
|---|---|---|
| Juanya | 17 | Grün<br>Rot<br>Blau |
| Maria | 23 | gelb<br>braun |

{style="table-layout:fixed"}

**AUTOMATISCHE`Green<br>Red<br>Blue`**

|  | Zahl | Farben |
|---|---|---|
| Juanya | 17 | Grün<br>Rot<br>Blau |
| Maria | 23 | gelb<br>braun |

{style="table-layout:auto"}

## Markdown-Tabelle mit doppelten `<br>`

**FESTE`Green<br><br>Red<br><br>Blue`**

|  | Zahl | Farben |
|---|---|---|
| Juanya | 17 | Grün<br><br>Rot<br><br>Blau |
| Maria | 23 | gelb<br><br>braun |

{style="table-layout:fixed"}

**AUTOMATISCHE`Green<br><br>Red<br><br>Blue`**

|  | Zahl | Farben |
|---|---|---|
| Juanya | 17 | Grün<br><br>Rot<br><br>Blau |
| Maria | 23 | gelb<br><br>braun |

{style="table-layout:auto"}

## Markdown-Tabelle mit `<p>`

**FESTE`Green<p>Red<p>Blue`**

|  | Zahl | Farben |
|---|---|---|
| Juanya | 17 | Grün<p>Rot<p>Blau |
| Maria | 23 | Gelb<p>Braun |

{style="table-layout:fixed"}

**AUTOMATISCHE`Green<p>Red<p>Blue`**

|  | Zahl | Farben |
|---|---|---|
| Juanya | 17 | Grün<p>Rot<p>Blau |
| Maria | 23 | Gelb<p>Braun |

{style="table-layout:auto"}

|  | Zahl | Farben |
|---|---|---|
| Juanya | 17 | Dies ist die Farbe **grün** und soll als Materie und/oder Mittel zum Testen der oben genannten Absatzumbrüche in eine andere Zeile umgebrochen werden. <p>Dies ist die Farbe **rot** und es soll in eine andere Zeile umgebrochen werden, als eine Angelegenheit und/oder Mittel zum Testen der oben genannten Absatzumbrüche. <p>Dies ist die Farbe **blau** und es soll in eine andere Zeile als eine Materie und/oder Mittel zum Testen der oben genannten Absatzumbrüche umgebrochen werden. |
| Maria | 23 | Gelb<p>Braun |

{style="table-layout:fixed"}

|  | Zahl | Farben |
|---|---|---|
| Juanya | 17 | Dies ist die Farbe **grün** und soll als Materie und/oder Mittel zum Testen der oben genannten Absatzumbrüche in eine andere Zeile umgebrochen werden. <p>Dies ist die Farbe **rot** und es soll in eine andere Zeile umgebrochen werden, als eine Angelegenheit und/oder Mittel zum Testen der oben genannten Absatzumbrüche. <p>Dies ist die Farbe **blau** und es soll in eine andere Zeile als eine Materie und/oder Mittel zum Testen der oben genannten Absatzumbrüche umgebrochen werden. |
| Maria | 23 | Gelb<p>Braun |

{style="table-layout:auto"}
