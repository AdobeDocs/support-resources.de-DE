---
title: Tabellen
description: Arbeiten mit Markdown-Tabellen und HTML-Tabellen.
hide: true
hidefromtoc: true
source-git-commit: 3779d588f21da83928bf0c71357afa90fd5f7179
workflow-type: tm+mt
source-wordcount: '1421'
ht-degree: 18%

---

# Tabellen

Matt war immer wieder hier -

EDS

Standard Markdown unterstützt nur einfache Tabellen. Für AdobeDocs Markdown stehen Ihnen die folgenden Optionen zur Verfügung:

* Grundlegende Markdown-Tabellen
* HTML-Tabellen
* Markdown-Tabellen mit begrenzter HTML-Syntax für Absatzumbrüche (`<p>`), Zeilenumbrüche (`<br>`) und einfachen Listen (`<ul>`, `<ol>`).

## Konvertieren von HTML-Tabellen in Markdown-Tabellen

In einigen Fällen möchten Sie eine HTML-Tabelle in eine Markdown-Tabelle oder in Markdown-Text konvertieren. Möglicherweise müssen Sie das Erscheinungsbild verbessern, einen Validierungsfehler beheben oder die Bearbeitung in Zukunft vereinfachen.

Leider konnten wir kein einziges Tool finden, das HTML-Tabellen gut konvertiert. Normalerweise verwenden wir eine Kombination von Tools, um eine anständige Markdown-Tabelle zusammenzufügen.

| Tool | Funktion |
|--- |--- |
| [Markdown Tables Generator](https://www.tablesgenerator.com/markdown_tables) | Gut geeignet zum Erstellen von Markdown-Tabellen von Grund auf. |
| [Erweiterter Tabellenkonverter](https://tableconvert.com/html-to-markdown) | Konvertieren Sie Tabellen aus beliebigen Formaten in beliebige Formate. <p>**Hinweis:** Links und Bilder werden beim Konvertieren reduziert. |
| [Grundlegende Tabellen-HTML > Markdown-Konverter](https://jmalarcon.github.io/markdowntables/) | Einfacher HTML-Konverter <p>**Hinweis:** Links und Bilder werden beim Konvertieren reduziert. |
| [Nicht tabellarische HTML > Markdown-Konverter](https://codebeautify.org/html-to-markdown) | Konvertiert HTML-Tabellen in Tabellen-Markdown-Syntax ohne Tabelle. Verwenden Sie in Kombination mit den oben genannten Tools zum Kopieren von Links, Bildern und anderen reduzierten Elementen. |

## Grundlegende Markdown-Tabellen

* Stellen Sie sicher, dass Sie in der zweiten Zeile, die die Tabelleneigenschaften bestimmt, mindestens drei Bindestriche hinzufügen. Beispiel: `|--- |--- |--- |` für eine Tabelle mit drei Spalten.
* Markdown-Tabellen müssen mindestens eine Kopfzeile und eine Textzeile enthalten. Sie können keine einzeilige oder einzellige Markdown-Tabelle erstellen (verwenden Sie stattdessen HTML).
* Stellen Sie sicher, dass jede Zeile dieselbe Anzahl von Pipe-Zeichen ( &amp;vert; ) enthält. Wenn Sie in eine Tabellenzelle einen senkrechten Strich (Pipe) einfügen müssen, führen Sie eine Escape-Sequenz durch, indem Sie ihm einen umgekehrten Schrägstrich (`\|`) oder unter Verwendung des HTML-Entitätscodes (`&vert;`).
* Achten Sie darauf, Codeblöcke in Tabellen zu verwenden. Inline-Codeblöcke können zu unverhältnismäßigen Spaltenbreiten führen.
* Sie können die Darstellung der Tabelle ändern, indem Sie Auto oder Fixed angeben. Siehe [Ändern der Darstellung von Tabellen](#table-rendering).

## Erstellen von Markdown-Tabellen mit Bonus-HTML

Zur Erleichterung der Migration haben wir Markdown-Tabellen erweitert, um HTML-Absatzumbrüche zu unterstützen (`<p>`), Zeilenumbrüche (`<br>`) und grundlegende HTML-Listen (`<ul>` und `<ol>`) in Markdown-Tabellen.

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
| Zeilenumbruch | erste Zeile in Zelle<br>zweite Zeile in Zelle | row 1 column 3 |
| Aufzählungsliste | Aufzählungsliste:<ul><li>Element 1</li><li>Element 2</li><li>Element 3</li></ul> | row 2 column 3 |
| Aufzählungsliste mit Zeilenumbruch | Aufzählungsliste:<ul><li>Element 1</li><li>Element 2</li><li>Element 3</li></ul><br>Dies ist eine neue Zeile nach der Aufzählungsliste | row 2 column 3 |

>[!IMPORTANT]
>
>Wenn Sie sich für die Verwendung von HTML in nativen Tabellen entscheiden, stellen Sie sicher, dass Sie die richtige HTML-Syntax verwenden. Fehler in der HTML-Syntax führen zu Überprüfungsfehlern, die schwer zu verstehen sind. Überprüfen Sie Ihre Arbeit.

## Arbeiten mit HTML-Tabellen

Das Migrationstool versuchte, so viele Formatierungen wie möglich von der ursprünglichen Tabelle beizubehalten. Der Großteil dieser HTML-Syntax wird ignoriert, während einige dieser Syntax zu Validierungsfehlern führt.

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

**Gerendert**

<table> 
 <tbody>
  <tr>
   <th>Eigenschaft</th> 
   <th>Typ</th> 
   <th>Wertbeschreibung</th> 
  </tr>
  <tr>
   <td>badgingPath</td> 
   <td>Zeichenfolge[]</td> 
   <td><p><i>(Erforderlich)</i> Eine mehrwertige Zeichenfolge von Badge-Bildern bis zur Anzahl der badgingLevels. Die Badge-Bildpfade müssen so angeordnet sein, dass der erste an den höchsten Fachmann vergeben wird. Wenn es weniger Abzeichen gibt, als durch badgingLevels angegeben, füllt das letzte Abzeichen im Array den Rest des Arrays aus. Beispieleintrag:</p><p> <code>/etc/community/badging/images/expert-badge/jcr:content/expert.png</code></p></td> 
  </tr>
  <tr>
   <td>badgingLevels</td> 
   <td>Lang</td> 
   <td><p><i>(Optional)</i> Gibt den Umfang des zu vergebenden Fachwissens an. Wenn beispielsweise eine <code>expert </code>und <code>almost expert</code> (zwei Abzeichen), sollte der Wert auf 2 gesetzt werden. BadgingLevel sollte mit der Anzahl der von Experten verwendeten Badge-Bilder übereinstimmen, die für die badgingPath -Eigenschaft aufgelistet sind. Der Standardwert ist 1.</p></td> 
  </tr>
  <tr>
   <td>badgingType</td> 
   <td>Zeichenfolge</td> 
   <td><p><i>(Erforderlich)</i> Identifiziert die Scoring-Engine entweder als "Standard"oder als "erweitert". Auf "Erweitert"gesetzt, andernfalls ist der Standardwert "Einfach".</p></td> 
  </tr>
 </tbody>
</table>

**Verwendung von HTML-Tabellen**

* Zum Ausgleichen von Spalten.
* Zum Auslassen von Tabellenüberschriften (Markdown-Tabellen müssen über eine Kopfzeile verfügen).
* So entfernen Sie den Rand einer einzeiligen Tabelle (`<tr style="border: 0;">`).
* So fügen Sie Spalten- oder Zeilenbereiche hinzu.
* So richten Sie Text in einer Tabellenzelle aus.

**Hinweise zum Arbeiten mit HTML-Tabellen**

* Verwenden Sie keine Markdown-Syntax in HTML-Tabellen. Wenn Sie beispielsweise `[!NOTE]` auf eine HTML-Tabelle verweist, wird sie wie folgt gerendert: (`[!NOTE]`). Verwenden Sie stattdessen die HTML-Syntax für Anmerkungen und Bilder.

  Loc-Tags bilden eine Ausnahme zu dieser Regel, da UICONTROL und DNL-Tags entfernt werden, bevor die Seiten gerendert werden.

* Nicht die gesamte HTML-Syntax wird in Tabellen unterstützt. Breite, Höhe, Farbe und andere HTML-Syntaxelemente werden bei der Wiedergabe in EXL ignoriert. Sie können diese Werte in lassen, es sei denn, sie führen zu Überprüfungsfehlern.
* Um Text auszurichten, verwenden Sie `align: "left|center|right"` in HTML. Um beispielsweise den Inhalt einer Tabellenzelle zu zentrieren, verwenden Sie `<td align="center">`.
* HTML-Tabellen können keine verschachtelten Tabellen enthalten.

>[!TIP]
>
>Wenn Sie einen Rahmen für eine einzeilige HTML-Tabelle deaktivieren möchten, verwenden Sie folgende Syntax:
>
>```
><table>
><tr style="border: 0;">
>```

## Festlegen der Darstellung von Tabellen {#table-rendering}

Tabellen können auf zwei Arten gerendert werden:

* **Fest** (derzeit Standardeinstellung) - Umfasst benutzerdefinierte Regeln für das Rendering von Tabellen, einschließlich HTML-Tabellen mit Bildern. Tabellen werden in voller Breite ohne Bildlauf dargestellt, was manchmal zu überlappendem Text führt.
* **Auto** - Ähnlich wie Git-aromatisiertes Markdown (GFM). Tabellen dürfen scrollen, sodass sich der Text nicht überschneidet.

In den meisten Fällen werden die Tabellen mit dem gleichen Erscheinungsbild gerendert. Wenn Ihre Tabelle jedoch überlappenden Text enthält, sollten Sie die `auto` -Tag. Oder wenn Ihre HTML-Tabelle mit Grafikkarten nicht richtig dargestellt wird, sollten Sie die `fixed` -Tag.

Wir erwägen, die Standardeinstellung von `fixed` nach `auto`.

## Bearbeiten von Markdown-Tabellen

Wenn Sie angeben möchten, wie eine native Markdown-Tabelle gerendert wird, fügen Sie NACH der Tabelle eine der folgenden Syntaxzeilen mit leeren Zeilen vor und nach:

* `{style="table-layout:auto"}`
* `{style="table-layout:fixed"}`

![table-rendering](assets/table-render.png)

### Bearbeiten von HTML-Tabellen

Wenn Sie angeben möchten, wie eine HTML-Tabelle dargestellt wird, verwenden Sie eine der folgenden Syntaxzeilen in der ersten Zeile der Tabelle:

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

### Verwendung von &quot;Auto&quot;oder &quot;Fest&quot;

**Überschneidender Text**

Verwendung `auto` für Tabellen mit langen Codeblöcken oder Text, der überlappenden Text verursacht, wenn `fixed` (Standard) ausgewählt ist.

*Korrigiert (Standard)*

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

**HTML von Tabellen mit ausgeglichenen Bildern**

Verwendung `fixed` für HTML-Tabellen, für die bei `auto` ausgewählt ist. In diesem Beispiel haben die Bilder identische Größen, aber es gibt mehr Text in der mittleren Spalte.

*Auto*

<table style="table-layout:auto">
<tr>
  <td>
    <a href="table-breaks.md">
    <img alt="Lead" src="assets/leads-home.png"/>
    </a>
    <div>
    <a href="table-breaks.md"><strong>Workflow für Adobe-Leads</strong></a>
    </div>
    <em>Hauptarbeitsablauf für Lead-Autoren.</em>
    <br>
  </td>
  <td>
    <a href="syntax-style-guide.md">
      <img alt="Gelegentlich" src="assets/infrequent.png">
    </a>
    <div>
    <a href="syntax-style-guide.md"><strong>Workflow für seltene Benutzer</strong></a>
    </div>
    <em>Kein Lead-Autor? Lernen Sie die einfachsten Möglichkeiten kennen, Beiträge zu leisten. Kein Lead-Autor? Lernen Sie die einfachsten Möglichkeiten kennen, Beiträge zu leisten. Kein Lead-Autor? Lernen Sie die einfachsten Möglichkeiten kennen, Beiträge zu leisten. Kein Lead-Autor? Lernen Sie die einfachsten Möglichkeiten kennen, Beiträge zu leisten. Kein Lead-Autor? Lernen Sie die einfachsten Möglichkeiten kennen, Beiträge zu leisten. Kein Lead-Autor? Lernen Sie die einfachsten Möglichkeiten kennen, Beiträge zu leisten.</em>
    <br>
  </td>
  <td>
    <a href="note-test.md">
      <img alt="Validierung" src="assets/validation.png">
    </a>
    <div>
    <a href="note-test.md"><strong>Validierung</strong></a>
    </div>
    <em>Erfahren Sie, wie Sie Überprüfungsfehler beheben können.</em>
    <br>
  </td>
</tr>
</table>

*Korrigiert (in mehr als einer Richtung)*

<table style="table-layout:fixed">
<tr>
  <td>
    <a href="table-breaks.md">
    <img alt="Lead" src="assets/leads-home.png"/>
    </a>
    <div>
    <a href="table-breaks.md"><strong>Workflow für Adobe-Leads</strong></a>
    </div>
    <em>Hauptarbeitsablauf für Lead-Autoren.</em>
    <br>
  </td>
  <td>
    <a href="syntax-style-guide.md">
      <img alt="Gelegentlich" src="assets/infrequent.png">
    </a>
    <div>
    <a href="syntax-style-guide.md"><strong>Workflow für seltene Benutzer</strong></a>
    </div>
    <em>Kein Lead-Autor? Lernen Sie die einfachsten Möglichkeiten kennen, Beiträge zu leisten. Kein Lead-Autor? Lernen Sie die einfachsten Möglichkeiten kennen, Beiträge zu leisten. Kein Lead-Autor? Lernen Sie die einfachsten Möglichkeiten kennen, Beiträge zu leisten. Kein Lead-Autor? Lernen Sie die einfachsten Möglichkeiten kennen, Beiträge zu leisten. Kein Lead-Autor? Lernen Sie die einfachsten Möglichkeiten kennen, Beiträge zu leisten. Kein Lead-Autor? Lernen Sie die einfachsten Möglichkeiten kennen, Beiträge zu leisten.</em>
    <br>
  </td>
  <td>
    <a href="note-test.md">
      <img alt="Validierung" src="assets/validation.png">
    </a>
    <div>
    <a href="note-test.md"><strong>Validierung</strong></a>
    </div>
    <em>Erfahren Sie, wie Sie Überprüfungsfehler beheben können.</em>
    <br>
  </td>
</tr>
</table>
