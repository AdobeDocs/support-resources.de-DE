---
title: Tabellenumbrüche
description: Test verschiedener Tabellenumbrüche
hide: true
hidefromtoc: true
source-git-commit: cd9f841a3f720ee366b33f3a78f7ca731c0b865a
workflow-type: tm+mt
source-wordcount: '265'
ht-degree: 12%

---

# Tabellenumbrüche

## Standard-Markdown-Tabelle mit `<br>`

**FIXED`Green<br>Red<br>Blue`**

|  | Zahl | Farben |
|---|---|---|
| Juanya | 17 | Grün<br>Rot<br>Blau |
| Maria | 23 | Gelb<br>Braun |

{style="table-layout:fixed"}

**AUTO`Green<br>Red<br>Blue`**

|  | Zahl | Farben |
|---|---|---|
| Juanya | 17 | Grün<br>Rot<br>Blau |
| Maria | 23 | Gelb<br>Braun |

{style="table-layout:auto"}

## Markdown-Tabelle mit zweifacher `<br>`s

**FIXED`Green<br><br>Red<br><br>Blue`**

|  | Zahl | Farben |
|---|---|---|
| Juanya | 17 | Grün<br><br>Rot<br><br>Blau |
| Maria | 23 | Gelb<br><br>Braun |

{style="table-layout:fixed"}

**AUTO`Green<br><br>Red<br><br>Blue`**

|  | Zahl | Farben |
|---|---|---|
| Juanya | 17 | Grün<br><br>Rot<br><br>Blau |
| Maria | 23 | Gelb<br><br>Braun |

{style="table-layout:auto"}

## Markdown-Tabelle mit `<p>`

**FIXED`Green<p>Red<p>Blue`**

|  | Zahl | Farben |
|---|---|---|
| Juanya | 17 | Grün<p>Rot<p>Blau |
| Maria | 23 | Gelb<p>Braun |

{style="table-layout:fixed"}

**AUTO`Green<p>Red<p>Blue`**

|  | Zahl | Farben |
|---|---|---|
| Juanya | 17 | Grün<p>Rot<p>Blau |
| Maria | 23 | Gelb<p>Braun |

{style="table-layout:auto"}

|  | Zahl | Farben |
|---|---|---|
| Juanya | 17 | Die Farbe **grün** und es soll in eine andere Zeile umbrechen, wenn es um eine Sache und oder um Mittel zur Prüfung der oben genannten Absatzunterbrechungen geht. <p>Die Farbe **red** und es soll in eine andere Zeile umbrechen, wenn es um eine Sache und oder um Mittel zur Prüfung der oben genannten Absatzunterbrechungen geht. <p>Die Farbe **blau** und es soll in eine andere Zeile umbrechen, wenn es um eine Sache und oder um Mittel zur Prüfung der oben genannten Absatzunterbrechungen geht. |
| Maria | 23 | Gelb<p>Braun |

{style="table-layout:fixed"}

|  | Zahl | Farben |
|---|---|---|
| Juanya | 17 | Die Farbe **grün** und es soll in eine andere Zeile umbrechen, wenn es um eine Sache und oder um Mittel zur Prüfung der oben genannten Absatzunterbrechungen geht. <p>Die Farbe **red** und es soll in eine andere Zeile umbrechen, wenn es um eine Sache und oder um Mittel zur Prüfung der oben genannten Absatzunterbrechungen geht. <p>Die Farbe **blau** und es soll in eine andere Zeile umbrechen, wenn es um eine Sache und oder um Mittel zur Prüfung der oben genannten Absatzunterbrechungen geht. |
| Maria | 23 | Gelb<p>Braun |

{style="table-layout:auto"}
