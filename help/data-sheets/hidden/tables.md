---
title: Tabellen
description: Arbeiten mit Markdown-Tabellen und HTML-Tabellen
hide: true
hidefromtoc: true
exl-id: 5ce746fc-6835-4bee-85c5-5ad5176baca0
source-git-commit: 6893d1e41c3899c3ab6a9b02b305161eb3f7e049
workflow-type: tm+mt
source-wordcount: '1421'
ht-degree: 17%

---

# Tabellen

Matt war immer wieder hier -

EDS

Standard-Markdown unterstützt nur einfache Tabellen. Für AdobeDocs Markdown haben Sie die folgenden Optionen:

* Grundlegende Markdown-Tabellen
* HTML-Tabellen
* Markdown-Tabellen mit begrenzter HTML-Syntax für Absatzumbrüche (`<p>`), Zeilenumbrüche (`<br>`) und Basislisten (`<ul>`, `<ol>`).

## Konvertieren von HTML-Tabellen in Markdown-Tabellen

In einigen Fällen empfiehlt es sich, eine HTML-Tabelle in eine Markdown-Tabelle oder in Markdown-Text zu konvertieren. Vielleicht müssen Sie das Erscheinungsbild verbessern, einen Validierungsfehler beheben oder die Bearbeitung in Zukunft erleichtern.

Leider konnten wir kein einziges Tool finden, das HTML-Tabellen gut konvertiert. Normalerweise verwenden wir eine Kombination von Tools, um eine anständige Markdown-Tabelle zusammenzuzimmern.

| Tool | Funktion |
|--- |--- |
| [Markdown-Tabellen-Generator](https://www.tablesgenerator.com/markdown_tables) | Ideal zum Erstellen von Markdown-Tabellen von Grund auf. |
| [Erweiterter Tabellenkonverter](https://tableconvert.com/html-to-markdown) | Konvertieren von Tabellen beliebiger Formate in beliebige Formate <p>**Hinweis:** Links und Bilder werden bei der Konvertierung reduziert. |
| [Grundlegende Tabelle HTML > Markdown-Konverter](https://jmalarcon.github.io/markdowntables/) | Einfacher HTML-Konverter <p>**Hinweis:** Links und Bilder werden bei der Konvertierung reduziert. |
| [Nicht-Tabellen-HTML > Markdown-Konverter](https://codebeautify.org/html-to-markdown) | Konvertiert HTML-Tabellen in Nicht-Tabellen-Markdown-Syntax. Verwenden Sie diese Option in Kombination mit den oben genannten Tools zum Kopieren von Links, Bildern und anderen reduzierten Elementen. |

## Grundlegende Markdown-Tabellen

* Achten Sie darauf, dass Sie mindestens drei Bindestriche in der zweiten Zeile hinzufügen, die die Tabelleneigenschaften bestimmt. Beispiel: `|--- |--- |--- |` für eine 3-spaltige Tabelle.
* Markdown-Tabellen müssen mindestens eine Kopfzeile und eine Textzeile haben. Eine einzeilige oder eine einzellige Markdown-Tabelle kann nicht erstellt werden (stattdessen HTML verwenden).
* Stellen Sie sicher, dass jede Zeile über dieselbe Anzahl von senkrechten Strichen ( &vert; ) verfügt. Wenn Sie ein Pipe-Zeichen in eine Tabellenzelle einschließen müssen, escapen Sie es, indem Sie ihm einen umgekehrten Schrägstrich (`\|`) voranstellen oder den HTML-Entitätscode (`&vert;`) verwenden.
* Achten Sie auf die Verwendung von Codeblöcken in Tabellen. Inline-Code-Blöcke können zu unverhältnismäßigen Spaltenbreiten führen.
* Sie können ändern, wie die Tabelle gerendert wird, indem Sie Auto oder Fest angeben. Siehe [Ändern der Darstellung von Tabellen](#table-rendering).

## Erstellen von Markdown-Tabellen mit Bonus-HTML

Um die Migration zu erleichtern, haben wir Markdown-Tabellen erweitert, um HTML-Absatzumbrüche (`<p>`), Zeilenumbrüche (`<br>`) und einfache HTML-Listen (`<ul>` und `<ol>`) in Markdown-Tabellen zu unterstützen.

**Markdown-Tabelle mit Zeilenumbrüchen und Listen**

```
| Header 1 | Header 2 | Header 3 |
|--- |--- |--- |
| Normal row | row 1 column 2 | row 1 column 3 |
| Line break | first line in cell<br>second line in cell | row 1 column 3 |
| Bullet list | Bullet list:<ul><li>Item 1</li><li>Item 2</li><li>Item 3</li></ul> | row 2 column 3 |
| Bullet list with line break | Bullet list:<ul><li>Item 1</li><li>Item 2</li><li>Item 3</li></ul><br>This is a new line after the bullet list | row 2 column 3 |
```

**Beispiel**

| Kopfzeile 1 | Kopfzeile 2 | Kopfzeile 3 |
|--- |--- |--- |
| Normale Zeile | row 1 column 2 | row 1 column 3 |
| Zeilenumbruch | Erste Zeile in Zelle<br>Zweite Zeile in Zelle | row 1 column 3 |
| Aufzählungsliste | Aufzählungsliste:<ul><li>Element 1</li><li>Element 2</li><li>Element 3</li></ul> | row 2 column 3 |
| Aufzählungsliste mit Zeilenumbruch | Aufzählungsliste:<ul><li>Element 1</li><li>Element 2</li><li>Element 3</li></ul><br>Dies ist eine neue Zeile nach dem Aufzählungszeichen. | row 2 column 3 |

>[!IMPORTANT]
>
>Wenn Sie sich für die Verwendung von HTML in nativen Tabellen entscheiden, stellen Sie sicher, dass Sie die richtige HTML-Syntax verwenden. Fehler beim HTML der Syntax führen zu schwer verständlichen Validierungsfehlern. Überprüfen Sie Ihre Arbeit.

## Arbeiten mit HTML-Tabellen

Das Migrations-Tool hat versucht, so viel Formatierung wie möglich aus der ursprünglichen Tabelle beizubehalten. Der Großteil dieser HTML-Syntax wird ignoriert, während ein Teil dieser Syntax zu Validierungsfehlern führt.

**Beispiel für migrierte HTML-Tabelle**

```
<table> 
 <tbody>
  <tr>
   <th>Property</th> 
   <th>Type</th> 
   <th>Value Description</th> 
  </tr>
  <tr>
   <td>badgingPath</td> 
   <td>String[]</td> 
   <td><p><i>(Required)</i> A multi-value string of badge images up to the number of badgingLevels. The badge image paths must be ordered so the first is awarded to the highest expert. If there are less badges than indicated by badgingLevels, the last badge in the array fills out the rest of the array. Example entry:</p><p> <code>/etc/community/badging/images/expert-badge/jcr:content/expert.png</code></p></td> 
  </tr>
  <tr>
   <td>badgingLevels</td> 
   <td>Long</td> 
   <td><i><p>(Optional)</i> Specifies the levels of expertise to be awarded. For example, if there should be an <code>expert </code>and an <code>almost expert</code> (two badges), then the value should be set to 2. The badgingLevel should correspond with the number of expert-related badge images listed for the badgingPath property. Default is 1.</p></td> 
  </tr>
  <tr>
   <td>badgingType</td> 
   <td>String</td> 
   <td><p><i>(Required)</i> Identifies the scoring engine as either "basic" or "advanced". Set to "advanced" else the default is "basic".</p></td> 
  </tr>
 </tbody>
</table>
```

**gerendert**

<table> 
 <tbody>
  <tr>
   <th>Eigenschaft</th> 
   <th>Typ</th> 
   <th>Beschreibung des Werts</th> 
  </tr>
  <tr>
   <td>badgingPath</td> 
   <td>String[]</td> 
   <td><p><i>(Erforderlich)</i> Eine Zeichenfolge mit mehreren Werten aus Badge-Bildern bis zur Anzahl der badgingLevels. Die Abzeichen-Bildpfade müssen bestellt werden, damit der erste an den höchsten Experten vergeben wird. Wenn es weniger Badges gibt als durch badgingLevels angegeben, füllt das letzte Badge im Array den Rest des Arrays aus. Beispieleintrag:</p><p> <code>/etc/community/badging/images/expert-badge/jcr:content/expert.png</code></p></td> 
  </tr>
  <tr>
   <td>BadgingLevels</td> 
   <td>Lang</td> 
   <td><p><i>(Optional)</i> Gibt den Grad des Fachwissens an, das verliehen werden soll. Wenn beispielsweise ein (<code>expert </code> und ein <code>almost expert</code> (zwei Badges) vorhanden sein sollen, sollte der Wert auf 2 gesetzt werden. Die BadgingLevel sollte mit der Anzahl der fachkundigen Badge-Bilder übereinstimmen, die für die badgingPath-Eigenschaft aufgeführt sind. Der Standardwert ist 1.</p></td> 
  </tr>
  <tr>
   <td>badgingType</td> 
   <td>String</td> 
   <td><p><i>(Erforderlich)</i> Gibt die Scoring-Engine als „Standard“ oder „Erweitert“ an. Auf „Erweitert“ gesetzt, andernfalls ist der Standard „Einfach“.</p></td> 
  </tr>
 </tbody>
</table>

**Verwendung von HTML-Tabellen**

* Spalten ausgleichen.
* So lassen Sie Tabellenkopfzeilen weg (Markdown-Tabellen müssen über eine Kopfzeile verfügen).
* So entfernen Sie den Rahmen einer einzeiligen Tabelle (`<tr style="border: 0;">`).
* So fügen Sie Spalten- oder Zeilenspannen hinzu.
* Ausrichten von Text in einer Tabellenzelle.

**Hinweise zum Arbeiten mit HTML-Tabellen**

* Verwenden Sie keine Markdown-Syntax in HTML-Tabellen. Wenn Sie beispielsweise `[!NOTE]` zu einer HTML-Tabelle hinzufügen, wird sie wie vorliegend gerendert (`[!NOTE]`). Verwenden Sie stattdessen die HTML-Syntax für Dinge wie Notizen und Bilder.

  Sperren-Tags bilden eine Ausnahme von dieser Regel, da UICONTROL- und DNL-Tags entfernt werden, bevor die Seiten gerendert werden.

* Nicht die gesamte HTML-Syntax wird in Tabellen unterstützt. width, height, color und andere HTML-Syntaxelemente werden beim Rendern in EXL ignoriert. Sie können diese Werte in lassen, es sei denn, sie führen zu Validierungsfehlern.
* Verwenden Sie zum Ausrichten von Text `align: "left|center|right"` HTML. Um beispielsweise den Inhalt einer Tabellenzelle zu zentrieren, verwenden Sie `<td align="center">`.
* HTML-Tabellen dürfen keine verschachtelten Tabellen enthalten.

>[!TIP]
>
>Wenn Sie einen Rahmen für eine einzeilige HTML-Tabelle deaktivieren möchten, verwenden Sie diese Syntax:
>
>```
><table>
><tr style="border: 0;">
>```

## Festlegen, wie Tabellen gerendert werden {#table-rendering}

Wir haben zwei Möglichkeiten, Tabellen zu rendern:

* **Behoben** (derzeit der Standard) - Enthält benutzerdefinierte Regeln zum Rendern von Tabellen, einschließlich des HTML von Tabellen mit Bildern. Tabellen werden als volle Breite ohne Scrollen gerendert, was manchmal zu überlappendem Text führt.
* **Auto** - Ähnlich wie Git-Markdown (GFM). Tabellen dürfen scrollen, sodass sich der Text nicht überschneidet.

In den meisten Fällen werden die Tabellen mit demselben Erscheinungsbild gerendert. Wenn Ihre Tabelle jedoch überlappenden Text enthält, sollten Sie das `auto`-Tag anwenden. Falls Ihre HTML-Tabelle mit Grafikkarten nicht ordnungsgemäß gerendert wird, können Sie das `fixed`-Tag anwenden.

Wir erwägen, den Standardwert von `fixed` in `auto` zu ändern.

## Bearbeiten von Markdown-Tabellen

Wenn Sie angeben möchten, wie eine native Markdown-Tabelle gerendert wird, fügen Sie eine der folgenden Syntaxzeilen NACH der Tabelle hinzu, wobei leere Zeilen vor und nach der Tabelle stehen:

* `{style="table-layout:auto"}`
* `{style="table-layout:fixed"}`

![table-rendering](assets/table-render.png)

### Bearbeiten von HTML-Tabellen

Wenn Sie angeben möchten, wie eine HTML-Tabelle gerendert wird, verwenden Sie eine der folgenden Syntaxzeilen in der ersten Zeile der Tabelle:

* `<table style="table-layout:auto">`
* `<table style="table-layout:fixed">`

```
<table style="table-layout:fixed">
  <tr>
    <th>Month</th>
    <th>Savings</th>
  </tr>
  <tr>
    <td>January</td>
    <td>$100</td>
  </tr>
</table>
```

### Verwendung von „Automatisch“ oder „Behoben“

**Überlappender Text**

Verwenden Sie `auto` für Tabellen mit langen Codeblöcken oder Text, der zu überlappendem Text führt, wenn `fixed` (Standard) ausgewählt ist.

*Behoben (Standard)*

| Insights-Metrik | Beschreibung | ID-Abfrageparameter |
| ---- | ---- | ---- |
| **timeseries.data.collection.validation.category.type.count** | Gesamtanzahl ungültiger Meldungen vom Typ „Typ“ für einen Datensatz oder für alle Datensätze. | Datensatz-ID |
| **timeseries.data.collection.validation.category.range.count** | Gesamtanzahl ungültiger Meldungen vom Typ „Bereich“ für einen Datensatz oder für alle Datensätze. | Datensatz-ID |
| **timeseries.data.collection.validation.category.format.count** | Gesamtanzahl ungültiger Meldungen vom Typ „Format“ für einen Datensatz oder für alle Datensätze. | Datensatz-ID |
| **timeseries.data.collection.validation.category.pattern.count** | Gesamtanzahl ungültiger Meldungen vom Typ „Muster“ für einen Datensatz oder für alle Datensätze. | Datensatz-ID |
| **timeseries.data.collection.validation.category.presence.count** | Gesamtanzahl ungültiger Meldungen vom Typ „Präsenz“ für einen Datensatz oder für alle Datensätze. | Datensatz-ID |
| **timeseries.data.collection.validation.category.enum.count** | Gesamtanzahl ungültiger Meldungen vom Typ „Aufzählung“ für einen Datensatz oder für alle Datensätze. | Datensatz-ID |

{style="table-layout:fixed"}

*Auto*

| Insights-Metrik | Beschreibung | ID-Abfrageparameter |
| ---- | ---- | ---- |
| **timeseries.data.collection.validation.category.type.count** | Gesamtanzahl ungültiger Meldungen vom Typ „Typ“ für einen Datensatz oder für alle Datensätze. | Datensatz-ID |
| **timeseries.data.collection.validation.category.range.count** | Gesamtanzahl ungültiger Meldungen vom Typ „Bereich“ für einen Datensatz oder für alle Datensätze. | Datensatz-ID |
| **timeseries.data.collection.validation.category.format.count** | Gesamtanzahl ungültiger Meldungen vom Typ „Format“ für einen Datensatz oder für alle Datensätze. | Datensatz-ID |
| **timeseries.data.collection.validation.category.pattern.count** | Gesamtanzahl ungültiger Meldungen vom Typ „Muster“ für einen Datensatz oder für alle Datensätze. | Datensatz-ID |
| **timeseries.data.collection.validation.category.presence.count** | Gesamtanzahl ungültiger Meldungen vom Typ „Präsenz“ für einen Datensatz oder für alle Datensätze. | Datensatz-ID |
| **timeseries.data.collection.validation.category.enum.count** | Gesamtanzahl ungültiger Meldungen vom Typ „Aufzählung“ für einen Datensatz oder für alle Datensätze. | Datensatz-ID |

{style="table-layout:auto"}

**HTML-Tabellen mit ausgeglichenen Bildern**

Verwenden Sie `fixed` für das HTML von Tabellen, für die ausgewogene Bilder erforderlich sind, die bei Auswahl von `auto` unausgeglichen werden. In diesem Beispiel haben die Bilder identische Größen, aber es gibt mehr Text in der mittleren Spalte.

*Auto*

<table style="table-layout:auto">
<tr>
  <td>
    <a href="note-test.md">
    <img alt="Lead" src="assets/leads-home.png"/>
    </a>
    <div>
    <a href="note-test.md"><strong>Workflow zum Adobe von Leads</strong></a>
    </div>
    <em>Hauptbearbeitungs-Workflow für Lead-Writer.</em>
    <br>
  </td>
  <td>
    <a href="syntax-style-guide.md">
      <img alt="Gelegentlich" src="assets/infrequent.png">
    </a>
    <div>
    <a href="syntax-style-guide.md"><strong>Workflow für selten verwendete Benutzer</strong></a>
    </div>
    <em>Kein leitender Autor? Erfahren Sie, wie Sie am einfachsten Beiträge leisten können. Kein leitender Autor? Erfahren Sie, wie Sie am einfachsten Beiträge leisten können. Kein leitender Autor? Erfahren Sie, wie Sie am einfachsten Beiträge leisten können. Kein leitender Autor? Erfahren Sie, wie Sie am einfachsten Beiträge leisten können. Kein leitender Autor? Erfahren Sie, wie Sie am einfachsten Beiträge leisten können. Kein leitender Autor? Erfahren Sie, wie Sie am einfachsten Beiträge leisten können.</em>
    <br>
  </td>
  <td>
    <a href="note-test.md">
      <img alt="Validierung" src="assets/validation.png">
    </a>
    <div>
    <a href="note-test.md"><strong>Validierung</strong></a>
    </div>
    <em>Erfahren Sie, wie Sie Validierungsfehler beheben können.</em>
    <br>
  </td>
</tr>
</table>

*Behoben (auf mehrere Arten)*

<table style="table-layout:fixed">
<tr>
  <td>
    <a href="note-test.md">
    <img alt="Lead" src="assets/leads-home.png"/>
    </a>
    <div>
    <a href="note-test.md"><strong>Workflow zum Adobe von Leads</strong></a>
    </div>
    <em>Hauptbearbeitungs-Workflow für Lead-Writer.</em>
    <br>
  </td>
  <td>
    <a href="syntax-style-guide.md">
      <img alt="Gelegentlich" src="assets/infrequent.png">
    </a>
    <div>
    <a href="syntax-style-guide.md"><strong>Workflow für selten verwendete Benutzer</strong></a>
    </div>
    <em>Kein leitender Autor? Erfahren Sie, wie Sie am einfachsten Beiträge leisten können. Kein leitender Autor? Erfahren Sie, wie Sie am einfachsten Beiträge leisten können. Kein leitender Autor? Erfahren Sie, wie Sie am einfachsten Beiträge leisten können. Kein leitender Autor? Erfahren Sie, wie Sie am einfachsten Beiträge leisten können. Kein leitender Autor? Erfahren Sie, wie Sie am einfachsten Beiträge leisten können. Kein leitender Autor? Erfahren Sie, wie Sie am einfachsten Beiträge leisten können.</em>
    <br>
  </td>
  <td>
    <a href="note-test.md">
      <img alt="Validierung" src="assets/validation.png">
    </a>
    <div>
    <a href="note-test.md"><strong>Validierung</strong></a>
    </div>
    <em>Erfahren Sie, wie Sie Validierungsfehler beheben können.</em>
    <br>
  </td>
</tr>
</table>
