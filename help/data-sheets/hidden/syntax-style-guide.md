---
title: Handbuch zur Syntax und Formatierung der gemeinsamen Dokumentation für Self-Service-Excellence
description: Eine grundlegende Einführung in den Markdown-Stil
mini-toc-levels: 1
hide: true
hidefromtoc: true
exl-id: 9f15436b-156a-4c07-bfaf-8557cd948197
source-git-commit: 637c13cb347add1da3a37aac5ce333b4926e074f
workflow-type: tm+mt
source-wordcount: '4300'
ht-degree: 13%

---

# Stilhandbuch zur Markdown-Syntax

Auf dieser Seite wird die Markdown-Komponente für das Authoring der technischen Dokumentation für digitale Erlebnisse mit dem Markdown-Format (.md) erläutert. Diese Seite enthält Details für Adobe-Mitarbeiter.

EDS

Siehe hier: [Adobe.com](https://www.adobe.com){rel=nofollow}

<!--
* You can [view a basic sample file](sample.md) or [view a sample file with advanced syntax examples](sample-full.md)
-->

>[!TIP]
>
>Sehen Sie sich dieses [AdobeDocs Markdown-Video](https://video.tv.adobe.com/v/26165) an.

Zum größten Teil folgen wir der Git-Flavored Markdown-Syntax (GFM) für die Formatierung von Text. Einige Syntax (wie horizontale Linien) wird jedoch nicht unterstützt, und wir haben Markdown auf verschiedene Arten erweitert, um unsere Dokumentationsanforderungen zu erfüllen.

## Grundlegende Textformatierung

Für einen Absatz ist keine spezielle Syntax in Markdown erforderlich. Fügen Sie zwischen jedem Absatz eine leere Zeile hinzu.

Um Text als **fett** zu formatieren, schließen Sie ihn in zwei Sternchen ein:

```
This text is **bold**.
```

Um Text *kursiv* zu formatieren, schließen Sie ihn in einfache Sternchen ein:

```
This text is *italic*.
```

Um Text sowohl als ***fett als auch kursiv*** zu formatieren, fügen Sie ihn in drei Sternchen ein:

```
This is text is both ***bold and italic***.
```

Um Markdown-Formatierungszeichen zu ignorieren, verwenden Sie vor dem -Zeichen `\`:

`This is not \*italicized\* type.`

Rendered: Dies ist nicht vom Typ \*italicized\*.

## Badges

Gestartet. Warten auf &quot;Lokal&quot;.

<!--

See the [dev version of this article](https://experienceleague-dev.corp.adobe.com/docs/authoring-guide-exl/using/markdown/syntax-style-guide.html#badges) for an example. Or [this one](https://experienceleague-dev.corp.adobe.com/docs/internal-test/test/badge.html).

There are two ways to create badges:

* **Metadata badge** - Specify the badge information in metadata so that the badge appears above the title in the article. This is especially useful for adding a badge to all articles in a guide or repo via the TOC.md or metadata.me files.
* **Inline badge** - Specify the badge information on its own line or in a heading, table, or other page element.

![badge examples](assets/badge-examples.png)

**Badge syntax**

*Metadata*: `badge: "Beta Content" type="Informative" url="https://www.example.com" tooltip="Go to example.com"`

*Inline*: `[!BADGE Beta Content]{type=Informative url="https://www.example.com" tooltip="Go to example.com"}`

**Examples**

```
|Type|Badge|
|---|---|
|Informative (default)|[!BADGE Beta]{type=Informative url="https://www.example.com"}|
|Positive|[!BADGE New Feature]{type=Positive url="https://www.example.com" tooltip="Go to example.com"}|
|Negative|[!BADGE Discontinued]{type=negative tooltip="This feature is now end of life"}|
|Neutral|[!BADGE Maybe]{type=Neutral tooltip="A rider fell off his horse..."}|
|Caution|[!BADGE Attention]{type=Caution tooltip="Yellow status"}|
```

**Rendered**

|Type|Badge|
|---|---|
|Informative (default)|[!BADGE Beta]{type=Informative url="https://www.example.com"}|
|Positive|[!BADGE New Feature]{type=Positive url="https://www.example.com" tooltip="Go to example.com"}|
|Negative|[!BADGE Discontinued]{type=negative tooltip="This feature is now end of life"}|
|Neutral|[!BADGE Maybe]{type=Neutral tooltip="A rider fell off his horse..."}|
|Caution|[!BADGE Attention]{type=Caution tooltip="Yellow status"}|

**More details**

* Only the badge label is required. The `type`, `url`, and `tooltip` parameters are optional. The `type` parameter determines the color. The `url` parameter lets users click the badge to open an article. The `tooltip` parameter displays the tooltip text on mouseover.
* If you want multiple badges to appear at the top of the page, use different badge names. For example, you can create badge names such as `badgeBeta` or `badgeWeb`. Example:

  ```
  badge1: "Beta"
  badge2: "Campaign Web"
  ```

* For metadata badges, make sure that all values are wrapped in quotes. For inline badges, make sure that `url` and `tooltip` are wrapped in quotes.
* Valid type values include *Informative* (default, blue), *Positive* (green), *Negative* (red), *Neutral* (dark gray), and *Caution* (yellow). 

-->

## Blockzitate

Unser Authoring-System verwendet die Blockierungsquotensyntax (`>` am Anfang von Zeilen), um benutzerdefinierte Markdown-Erweiterungen für Tipps, Hinweise und Videos zu identifizieren. Sie können tatsächliche Blockzitate erstellen, indem Sie vor einem Absatz ein `>` -Zeichen hinzufügen.

>Dies ist ein Blockzitat.

```
>This is a blockquote quotation.
```

## Codeblock (in Zeile){#code-block}

**Verwendungszeitpunkt**

Wird verwendet, um einen Code in einer Zeile in einem Satz wiederzugeben. Ideal, um einen Cookie-Namen, Dateinamen, Wert oder Befehl abzurufen, für den kein vollständiger Codeblock erforderlich ist.

Inhalte in Codeblöcken in werden wie besehen und nicht lokalisiert gerendert. (Eine Ausnahme von dieser Regel ist die Syntax `!UICONTROL` und `!DNL`, die während der Verpackung zur Veröffentlichung entfernt wird.)

Verwenden Sie auch Codeblöcke für Beispiel-URLs, die nicht validiert werden sollen: `https://www.example.com`

**Syntax**

Ein Codeblock verwendet einzelne Backticks, um das Codeelement einzuschließen, das Sie hervorheben möchten.

```
This is `inline code` within a paragraph of text.
```

**Beispiel**

This is `inline code` within a paragraph of text.

>[!TIP]
>
>Sie können Text auch mit dreifachen Backticks (&grave;&grave;&amp;;grave;) umbrechen, um einen Inline-Codeblock zu erstellen. Dies ist besonders nützlich, wenn Sie auf ein Zeichen mit der Rücktaste in einem Inline-Codeblock verweisen müssen. Beispiel:
>
&grave;&grave;&grave;`Use a back tick (`&grave;`) for formatting`&grave;&grave;&amp;&amp;grave

## Codeblock (abgegrenzt)

**Verwendungszeitpunkt**

Verwenden Sie einen Codeblock, um die Codesyntax anzuzeigen. Ein abgegrenzter Codeblock verwendet drei Backticks, um das Codeelement einzuschließen, das Sie hervorheben möchten. Fügen Sie leere Zeilen über und unter dem abgegrenzten Codeblock hinzu.

Codeblöcke werden nicht lokalisiert.

>[!TIP]
>
Geben Sie eine Sprache an, wenn Sie einen abgegrenzten Codeblock erstellen. Wenn Sie eine Sprache angeben, kann die Syntax speziell für diese Sprache hervorgehoben werden. Außerdem wird für die Benutzer die Schaltfläche **Kopieren** angezeigt. Wenn Sie eine Sprache angeben, können Sie auch Zeilennummern anzeigen.

**Syntax**

Verwenden Sie drei Backticks ( &grave;&grave;&grave; ) vor und nach den Codezeilen. Achten Sie darauf, dass die Zecken zum Öffnen und Schließen der Rückseite mit der gleichen Anzahl von Leerzeichen eingerückt sind. Geben Sie für eine optimale Darstellung eine Codesprache an.

&grave;&grave;&grave;`javascript`

**Beispiel**

```javascript
var visitor = Visitor.getInstance("INSERT-MARKETING-CLOUD-ORGANIZATION ID-HERE", {
     trackingServer: "INSERT-TRACKING-SERVER-HERE", // same as s.trackingServer
     trackingServerSecure: "INSERT-SECURE-TRACKING-SERVER-HERE", // same as s.trackingServerSecure

     // To enable CNAME support, add the following configuration variables
     // If you are not using CNAME, DO NOT include these variables
     marketingCloudServer: "INSERT-TRACKING-SERVER-HERE",
     marketingCloudServerSecure: "INSERT-SECURE-TRACKING-SERVER-HERE" // same as s.trackingServerSecure
});
```

### Syntaxhervorhebung für Code-Blöcke

Experience League unterstützt die Syntaxhervorhebung für Code-Blöcke. Achten Sie darauf, eine Sprache wie `java` nach der öffnenden Reihe von Backticks anzugeben, um sicherzustellen, dass die Syntax richtig hervorgehoben wird. Eine Liste der gültigen Sprachen finden Sie unter [https://prismjs.com](https://prismjs.com/#supported-languages). Wenn Sprachen fehlen, senden Sie bitte ein Jira-Ticket.

### Zeilennummerierung in Code-Blöcken

Fügen Sie `{line-numbers="true"}` nach der Sprache hinzu, um die Zeilennummerierung zu aktivieren.

Beispiel mit Zeilennummern (&grave;&grave;&grave;`html {line-numbers="true"}`):

```html {line-numbers="true"}
<!DOCTYPE html>
<html>
<body>

<h1>My First Heading</h1>
<p>My first paragraph.</p>

</body>
</html>
```

**Beginnen der Nummerierung in Zeile _**

Fügen Sie `start-number="n"` nach der Zeilennummernsyntax hinzu, um die Nummerierung mit einer anderen Zahl als 1 zu beginnen.

Beispiel mit neuer Startzeile (&grave;&grave;&grave;`html {line-numbers="true" start-line="7"}`):

```html {line-numbers="true" start-line="7"}
<!DOCTYPE html>
<html>
<body>

<h1>My First Heading</h1>
<p>My first paragraph.</p>
<p>My second paragraph.</p>

</body>
</html>
```

### Zeilenhervorhebung in Code-Blöcken

Fügen Sie `highlight="n"` nach der Zeilennummernsyntax hinzu, um Zeilen in einem Code-Block hervorzuheben. Die Angabe von `11-13, 16` markiert die Zeilen 11 bis 13 und 16.

Beispiel mit Zeilenhervorhebung (&grave;&grave;&grave;`html {line-numbers="true" start-line="7" highlight="11-13, 16"}`):

```html {line-numbers="true" start-line="7" highlight="11-13, 16"}
<!DOCTYPE html>
<html>
<body>

<h1>My First Heading</h1>
<p>My first paragraph.</p>
<p>My second paragraph.</p>

</body>
</html>
```

### Variablenformatierung in Codeblöcken

Die Variablensyntax wie `<i>italic</i>` wird in Codeblöcken nicht unterstützt. Um Variablentext anzugeben, ist eine Option die Verwendung von spitzen Klammern `< >`.

## Reduzierbare Abschnitte

Sie können einen ausblendbaren Abschnitt (manchmal auch als **Accordion** bezeichnet) erstellen, der standardmäßig ausgeblendet ist. Der Benutzer kann auf den Titel klicken, um den Abschnitt zu erweitern oder zu reduzieren.

Reduzierbarer Text kann verwendet werden, um komplexe Inhalte zu vereinfachen, z. B. das Rationalisieren einer FAQ-Seite oder das Deklarieren eines komplexen Verfahrens mit verschachtelten Listen. Anstatt beispielsweise eine Reihe von Unterschritten anzuzeigen, können Sie die Unterschritte in einen Abschnitt &quot;Details anzeigen&quot;reduzieren.

**Syntax**

```
+++See details
This is text inside a collapsible section.

* Bullet one
* Bullet two
* Bullet three

+++
```

**Beispiel**

++ + Siehe Details
Dies ist Text in einem ausblendbaren Abschnitt.

* Aufzählungszeichen eins
* Aufzählungszeichen 2
* Aufzählungszeichen drei

+++

**Hinweise**

* Verschachteln Sie nicht ausblendbare Abschnitte in ausblendbaren Abschnitten. Verschachtelte reduzierbare Abschnitte werden nicht ordnungsgemäß dargestellt. Sie führen jedoch nicht dazu, dass die Validierung fehlschlägt, sodass Benutzer die Syntax `+++` des verschachtelten Abschnitts sehen.
* Stellen Sie sicher, dass Sie im ausblendbaren Abschnitt leere Zeilen über und unter Elementen wie Aufzählungslisten und Codeblöcke hinzufügen. Andernfalls wird ein Überprüfungsfehler ausgegeben.
* Sie können Überschriften in ausblendbaren Abschnitten hinzufügen. Dies wird jedoch nicht empfohlen.
* [Akkordeons sind nicht immer die Antwort für komplexe Inhalte auf Desktops](https://www.nngroup.com/articles/accordions-complex-content/)
* Ein historischer Nachteil ausblendbarer Abschnitte ist, dass **In Seite finden** (Strg/Befehl+F) ausgeblendeten Text ignoriert. Dies trifft zwar weiterhin in Safari zu, gilt jedoch nicht mehr für Chrome. &quot;Suchen in Seite&quot;erkennt ausgeblendeten Text in Chrome.
* Beispiel einer [Wartungsaktualisierung](https://experienceleague.adobe.com/docs/workfront-known-issues/releases/current-updates.html?lang=en) -Seite mit ausblendbaren Abschnitten.

## Kommentare und Bemerkungen

Kommentare werden nicht im wiedergegebenen Hilfesystem angezeigt. Verwenden Sie Kommentare, um Notizen für sich selbst oder andere Autoren zu hinterlassen. Sie können auch Kommentare für Textentwürfe verwenden.

Beachten Sie bei Kommentaren, dass sie zwar nicht im Hilfesystem gerendert werden, aber für Benutzer sichtbar sind, die Markdown-Dateien unter GitHub.com bearbeiten. Schließen Sie keine vertraulichen Informationen in Kommentare ein.

```
<!-- standard comment code -->

DO NOT USE the following:
<!--> bad comment syntax <-->
```

Sie sollten Text unter diesem nicht sehen können (&quot;Sie können mich nicht sehen&quot;), es sei denn, Sie bearbeiten das Dokument.

<!--
You can't see me (unless you're editing in Git).
-->

**Erinnerung:** Kommentare (Anmerkungen) werden nicht in den öffentlichen Hilfeartikeln angezeigt. Kommentare werden jedoch in den öffentlichen Markdown-Dateien angezeigt, die Benutzer sehen und bearbeiten können.

>[!IMPORTANT]
>
Vermeiden Sie das Hinzufügen von Kommentaren innerhalb von Blockkomponenten wie Aufzählungslisten, insbesondere verschachtelten Aufzählungslisten. Der Kommentar kann die Darstellung der Aufzählungsliste ändern.
>
Kommentieren Sie in der Datei TOC.md keine Zeilen in der Mitte der TOC-Liste aus. Dies kann die Liste der Inhaltsverzeichnisse zerbrechen und Überprüfungsfehler verursachen. Verschieben Sie stattdessen Kommentare im Inhaltsverzeichnis an das Ende der Datei.

## KONTEXTBEZOGENE HILFE

Autoren können mit Produktteams zusammenarbeiten, um in der Experience Cloud- oder Experience Platform-Produktoberfläche Hilfeaufrufe hinzuzufügen. Beispiel:

```markdown
>[!CONTEXTUALHELP]
>id="platform_destinations_activate_mandatorykey_4"
>title="About mandatory attributes"
>abstract="Select the XDM schema attributes that all exported profiles should include. Profiles without the mandatory key are not exported to the destination. Not selecting a mandatory key exports all qualified profiles regardless of their attributes."
>additional-url="http://www.adobe.com/go/destinations-mandatory-attributes-en" text="Learn more in documentation"
```

## Definitionslisten

Für Definitionslisten wird die Markdown-Standardsyntax noch nicht unterstützt. Verwenden Sie stattdessen eine manuelle Formatierung wie die folgende:

```
**Frog** - An amphibious green creature. Likes flies.
```

Gerendert:

**Frosch** - Eine amphibische grüne Kreatur. Fliegen mag es.

<!--
A definition list is a Markdown extension that supports the Definition List component in AEM. A definition list consists of a term and its definition.

**When to use**

Using a definition list is optional. To define lists of features or options, you can use either the definition list syntax or use basic Markdown formatting, such as applying bold to option names.

**Syntax**

```
Frog
: An amphibious green creature. Likes flies.

Cat
: A less amphibious creature than frogs.
```

**Example**

Frog
: An amphibious green creature. Likes flies.

Cat
: A less amphibious creature than frogs.
-->

## Herunterladen von Dateien

Laden Sie die ZIP-Datei oder eine andere herunterladbare Datei in das Asset-Verzeichnis hoch und verknüpfen Sie sie dann. Wenn es sich um eine ZIP-Datei handelt, wird durch Klicken auf den Link die Datei heruntergeladen. Wenn es sich um einen Dateityp wie PDF oder PNG handelt, der in einem Browser geöffnet werden kann, wird durch Klicken auf den Link eine neue Registerkarte geöffnet. Für solche Dateien sollten Sie sie komprimieren oder Anweisungen zum Rechtsklick auf den Link und zum Herunterladen bereitstellen.

`Download` &amp;lbrack;`download-test.zip`&amp;rbrack;`(assets/download-test.zip)`

Gerendert:

Laden Sie die ZIP-Datei [Download-Test herunter](assets/download-test.zip)

>[!NOTE]
>
Die maximale Dateigröße für Download-Dateien und Bilder beträgt 100 MB. Das ist die github.com Grenze. Die git.corp.adobe.com -Grenze ist höher (250 MB), aber wir müssen in der Lage sein, Dateien in den github.com -Spiegel zu kopieren.

## Überschriften {#headings}

In Markdown verwenden Sie Pfund-Zeichen (`#`) zur Identifizierung von Überschriftenebenen. Die erste Ebene (`#`) ist der Artikeltitel, der auch im Metadaten-Header angegeben ist. Behalten Sie diese bei. Die zweite Ebene (`##`) stellt die Hauptüberschriften auf der Seite dar, die im Mini-Inhaltsverzeichnis enthalten sein werden. Wenn Sie es gewohnt sind, in AEM (chl-author) zu schreiben, werden die Überschriften der Stufe 2 (`##`) in AEM der Komponente &quot;Überschrift 1&quot;zugeordnet.

Maximale Zeichenanzahl für Überschriften: 69 Zeichen (Englisch) / 120 Zeichen (LOC).

```
# This is level 1 (article title)

## This is level 2
   
### This is level 3
```

**Best Practices für Überschriften**

* Stellen Sie sicher, dass eine Überschrift der Stufe 1 (`#`) nach den Metadaten in jedem Artikel eine leere Zeile folgt.
* Überspringen Sie keine Ebenen, z. B. von Ebene 2 (`##`) zu Ebene 4 (`####`).
* Fügen Sie für jede Überschrift eine leere Zeile *vor* und *nach* ein.
* Wenn eine Überschrift Ziffern enthält, geben Sie eine explizite Überschriften-ID an, die nicht mit einer Zahl beginnt, z. B. `## Release notes for 2016 {#release-notes-2016}`.
* Wir empfehlen nur drei Überschriftenebenen. Die Ebenen 4 und höher werden derzeit nicht ordnungsgemäß dargestellt.
* Überschriften werden in der rechten Navigationsleiste angezeigt, sodass Benutzer klicken können, um zu einem Abschnitt zu springen. Standardmäßig werden in der rechten Navigationsleiste zwei Ebenen von Überschriften angezeigt. Wenn Sie die Anzahl der Ebenen ändern möchten, verwenden Sie `mini-toc-levels` -Metadaten, z. B. `mini-toc-levels: 3`.

**Überschriften-IDs**

Überschriften-IDs (auch *Anker-IDs* genannt) werden zum Erstellen benutzerdefinierter Deep-Links zu Abschnitten in Artikeln verwendet. Verwenden Sie das folgende Format, um eine Überschriften-ID anzugeben:

```
## Creating processing rules {#processing-rules}
```

Überschriften-IDs sollten in Kleinbuchstaben und getrennt werden.

Wenn Sie keine Überschriften-ID für eine Überschrift angeben, lautet die standardmäßige Überschriften-ID die Überschrift &quot;gelogifiziert&quot;(Kleinbuchstaben und Silbentrennung). Beispielsweise verfügt die Überschrift `## Creating widgets and Such` über einen `#creating-widgets-and-such` -Anker.

## HTML-Syntax {#html}

Aus verschiedenen Gründen, einschließlich Sicherheit und Barrierefreiheit, begrenzen wir die HTML-Syntax, die in Markdown verwendet werden kann. Die folgende Liste zeigt die unterstützte HTML-Syntax. Jede HTML-Syntax, die nicht auf dieser Liste steht, führt zu einem Validierungsfehler.

```html
<table>
<tbody>
<td>
<tfoot>
<thead>
<th>
<tr>
<col>
<colgroup>
<p> (paragraph break)
<ul> (unordered list / numbered list)
<ol> (ordered list / bullet list)
<li> (list item)
<br> (line break)
<b>
<caption>
<i>
<strong> (bold)
<u> (underline)
<s> (strikethrough)
<span>
<sub> (subscript)
<sup> (superscript)
<a>
<img>
<div>
<em> (emphasis, italics)
<pre> (codeblock)
<code>
<codeblock>
```

<!--
Bob: Check above no space char. (ignore the space; I can't add a codeblock inside this codeblock)
-->

Wenn Sie möchten, dass dieser Liste eine HTML-Syntax hinzugefügt wird, melden Sie sich bitte ein Ticket an oder kontaktieren Sie das SSE-Team.

## Bilder {#images}

Verwenden Sie die Syntax `![]()` für Bilder. Die Klammern `[ ]` enthalten ALT-Text und die Klammern `( )` enthalten die Bildposition und optional den Mauszeiger über Text (QuickInfo). Das Ausrufezeichen unterscheidet ein Bild von einem Link.

```
![alt text](assets/logo.png "Hover text")
```

![alt text](assets/logo.png "hover text")

Bei freigegebenen Bildern können Sie die Bilder in einem Stammordner für Assets platzieren und dann einen Stammlink verwenden, der von einer beliebigen Datei in einem Repository aus funktioniert:

```
/help/assets/imagename.png
```

### Ändern und Ausrichten von Bildern

**Bildeigenschaften (mit rechts ausgerichtetem Bild)** ![ALT-Text](assets/premium.png "Premium-Hover-Text"){align="right"}

Verwenden Sie die folgende Syntax, um die standardmäßige Bildbreite zu ändern oder das Bild in der Seitenansicht oder Tabellenzelle rechts auszurichten.

```
![Dive image alt text](assets/maui-dive.jpg "Hover text - Maui dive width is 300 pixels and centered"){width="300" align="center"}
```

Gerendert:

![Alternativtext für Bild tauchen](assets/maui-dive.jpg "Hover text - Maui-Tauchbreite ist 300 Pixel und zentriert"){width="300" align="center"}

* Bei großen Bildern empfehlen wir, Bilder zu erstellen, die groß genug sind, um skaliert und an die Seitenbreite angepasst zu werden (mindestens 640 Pixel breit). Die empfohlene Breite beträgt 1500 Pixel. Es müssen keine Bilder erstellt werden, die größer als 2500 Pixel oder 500 KB sind. Die maximale Dateigröße für Bilder beträgt 100 MB.
* Erstellen Sie bei kleinen Bildern Bilder mit der gewünschten Breite in Pixel oder verwenden Sie den Breitenparameter, z. B. `{width="250"}` (Pixel) oder `{width="50%"}` (Prozentsatz des Ansichtsbereichs, nicht die Originalbildgröße). Bilder werden proportional skaliert. Beachten Sie, dass Bilder vergrößert oder verkleinert werden können. Achten Sie daher auf die Verpixelung.
* In einigen Fällen sehen Bilder aus derselben Benutzeroberfläche auf der Seite nicht proportional aus, da breitere Bilder (z. B. eine Symbolleiste) herunterskaliert werden, während schmale Bilder (z. B. ein Bedienfeld) nicht herunterskaliert werden. In solchen Fällen sollten Sie die größeren Bilder herabsetzen, um die visuelle Konsistenz zu verbessern.
* Sie können die Ausrichtung eines Bildes innerhalb des Ansichtsbereichs ändern. Verwenden Sie entweder `{align="center"}` oder `{align="right"}`. Der Parameter `valign` wird nicht unterstützt.

>[!NOTE]
>
Die maximale Dateigröße für Bilder beträgt 100 MB. Das ist die github.com Grenze. Die git.corp.adobe.com -Grenze ist höher (250 MB), aber wir müssen in der Lage sein, Dateien in den github.com -Spiegel zu kopieren.

### Bildlinks

Wenn Sie Benutzern erlauben möchten, auf ein Bild zu klicken, um zu einer anderen Seite zu springen, verwenden Sie dieses Format.

**Syntax**

```
[![image](assets/core-services_96.png)](https://www.adobe.com)
```

**Beispiel**

Klicken Sie auf dieses Bild, um zur Adobe-Website zu gelangen.

[![Bild](assets/core-services_96.png)](https://www.adobe.com)

### Zoom-Bild durch Klicken

Verwenden Sie den Parameter `zoomable` , damit Benutzer auf ein Bild klicken können, um eine vergrößerte Version des Bildes anzuzeigen. Wenn der Mauszeiger über ein vergrößerbares Bild bewegt, wird der Zeiger zu einem Lupensymbol. Wenn auf geklickt wird, wird das Bild auf die volle Breite des Browsers erweitert. Es kann mit einem Schließen-Knopf verworfen werden.

**Beispiel**

![Tauchbild](/help/data-sheets/hidden/assets/maui-dive.jpg "Tauchen in Maui"){width="100" zoomable="yes"}

**Syntax**

```
![Diving image](/help/data-sheets/hidden/assets/maui-dive.jpg "Diving in Maui"){width="100" zoomable="yes"}
```

## Links und Querverweise {#links-and-cross-references}

Externe Links sind direkt vorwärts und können als verknüpfte Beschriftung oder reine URL gerendert werden.

```
[Adobe](https://www.adobe.com)
```

Gerendert:

[Adobe](https://www.adobe.com)

Wenn Sie eine URL direkt zu Text hinzufügen, wird sie nicht automatisch in einen Link konvertiert. Wenn eine URL als Link angezeigt werden soll, fügen Sie die Syntax `< >` hinzu. Beispiele:

```
https://www.adobe.com

<https://www.adobe.com>
```

Gerendert:

https://www.adobe.com

<https://www.adobe.com>

Links zu Artikeln (Querverweise) können etwas komplexer sein.

**Option 1: Standardmäßiger relativer Link**

So sieht ein standardmäßiger relativer Link aus:

```
See [Overview example article](collaborative-doc-instructions/overview.md)
```

Der Pfadname muss sowohl den Speicherort der Quelldatei als auch die Zieldatei berücksichtigen. Sie können alle relativen Link-Operanden verwenden, z. B. `./` (aktuelles Verzeichnis), `../` (vorheriges Verzeichnis) und `../../` (zwei Ordner zurück).

**Option 2: Root relative link**

Der Vorteil dieses Linktyps besteht darin, dass nur die Zieldatei berücksichtigt werden muss. Sie funktioniert aus jeder Quelldatei im Repository, unabhängig vom Speicherort der Quelldatei.

```
/help/using/docile-rules/introduction.md
```

**Deep-Linking**

Um eine Verknüpfung zu einer Überschrift innerhalb eines Artikels herzustellen, muss die Zielüberschrift über eine explizite Überschriften-ID verfügen (auch als &quot;Anker-ID&quot;bezeichnet). Beispiel:

`## Creating audience segments {#creating-audience-segments}`

Verwenden Sie die Überschriften-ID als Link, um innerhalb derselben Seite auf diese Überschrift zu verweisen:

`See [Creating audience segments](#creating-audience-segments)`

Um von einem anderen Artikel im Repo aus auf diese Überschrift zu verweisen, fügen Sie das Suffix für die Überschriften-ID am Ende des Links hinzu:

`See [Audiences: Creating audience segments](audiences.md#creating-audience-segments)`

**In neuer Registerkarte öffnen**

Wenn Sie möchten, dass ein Link eine neue Registerkarte öffnet, z. B. wenn Sie zu einem anderen Handbuch springen, verwenden Sie die Eigenschaft `{target="_blank"}` im Link.

Beispiel:

`[See What's new](whats-new.md){target="_blank"}`

## Metadaten

Fügen Sie oben in der Markdown-Datei Metadaten hinzu. Die nächste Zeile nach der Metadatenzeile (und leere Zeile) MUSS der Artikeltitel (# Titel) sein.

```
---
title: Title for search optimization
description: This is the article description used for search optimization. Use common search keywords and synonyms.
---

# Article title
```

## Lokalisierungstags: UICONTROL, DNL und DONOTLOCALIZE

Alle unsere Markdown-Hilfeinhalte werden zunächst durch maschinelle Übersetzung lokalisiert. Wenn die Hilfe noch nie lokalisiert wurde, behalten wir die maschinelle Übersetzung bei. Wenn der Hilfeinhalt jedoch in der Vergangenheit lokalisiert wurde, fungiert der maschinell übersetzte Inhalt als Platzhalter, während der Inhalt manuell übersetzt wird.

## Mehr wie dieses

Verwenden Sie die Komponente &quot;Mehr wie dieses&quot;zum Anzeigen verwandter Links am Ende eines Artikels. Nach der Wiedergabe wird die Komponente MORELIKETHIS als &quot;Related Articles&quot;gerendert (und in anderen Sprachen lokalisiert).

**Syntax**

![ Mehr wie diese Syntax](assets/morelikethis.png)

**Beispiel**

>[!MORELIKETHIS]
>
* [Article 1](https://helpx.adobe.com/de/support/analytics.html)
* [Article 2](https://helpx.adobe.com/de/support/audience-manager.html)

## Hinweise/Empfehlungen

Wir haben Markdown erweitert, um verschiedene Arten von Notizen zu formatieren: Hinweis, Tipp, Wichtig und Warnung.

**Syntax**

```
>[!NOTE]
>
>This is a standard NOTE block.
```

**Beispiel**

>[!NOTE]
>
Dies ist ein standardmäßiger HINWEIS-Block.

**Syntax**

```
>[!TIP]
>
>This is a standard tip.
```

**Beispiel**

>[!TIP]
>
Dies ist ein Standardtipp.

**Syntax**

```
>[!WARNING]
>
>This is a standard warning block.
```

**Beispiel**

>[!WARNING]
>
Dies ist ein Standardwarnblock.

**Syntax**

```
>[!IMPORTANT]
>
>This is a standard important block.
```

**Beispiel**

>[!IMPORTANT]
>
Dies ist ein wichtiger Standardblock.

**Syntax**

```
>[!NOTE]
>
>This is a standard NOTE block.
>
>It includes multiple paragraphs.
```

**Beispiel**

>[!NOTE]
>
Dies ist ein standardmäßiger HINWEIS-Block.
>
Es enthält mehrere Absätze.

Neue unterstützte Hinweistypen:

>[!ADMIN]
>
Dies ist eine Administratornote. Nur EXL.

>[!AVAILABILITY]
>
Dies ist ein Hinweis zur Verfügbarkeit. Nur EXL.

>[!PREREQUISITES]
>
Dies ist ein Hinweis zu den Voraussetzungen. Nur EXL.

>[!INFO]
>
Dies ist ein Informationshinweis. Nur EXL.

>[!ERROR]
>
Dies ist ein Fehlerhinweis. Nur EXL.

>[!SUCCESS]
>
Dies ist ein Erfolgshinweis. Nur EXL.

## Nummerierte Listen und Aufzählungslisten {#lists}

Um nummerierte Listen zu erstellen, beginnen Sie eine Zeile mit `1.` oder `1)`, wählen Sie jedoch eine Methode aus und verwenden Sie sie konsistent im Artikel. Sie müssen die Zahlen nicht speziell angeben. GitHub erledigt das für Sie.

Verwenden Sie die Zahl &quot;`1`&quot; für jeden Schritt in der nummerierten Liste.

Fügen Sie vor und nach Listen leere Zeilen hinzu.

**Syntax**

```
1. This is step 1.

1. This is the next step.

   1. This is a sub-step

   1. This is a sub-step

1. This is yet another step, the third.
```

**Beispiel**

1. This is step 1.

   1. Unterschritt

   1. Unterschritt

1. This is the next step.

1. This is yet another step, the third.

Um Aufzählungslisten zu erstellen, beginnen Sie eine Zeile mit `*` oder `-` oder `+`, wählen Sie jedoch eine Methode aus und verwenden Sie sie konsistent im Artikel. (Wenn Sie die Formate wie `*` und `+` mischen, erhalten Sie beim Einchecken der Datei einen Markdown-Validierungsfehler.)

**Best Practice:** Verwenden Sie `*` für Aufzählungszeichen. Visual Studio Code wendet das Sternchen für Aufzählungszeichen an, sodass es einfacher ist, mit Sternchen zu bleiben, um die Erstellung einer ungeordneten Liste zu automatisieren. (Möglicherweise haben Sie bemerkt, dass die Datei TOC.md für Listen Pluszeichen `+` verwendet. Das ist ein Hindernis für die Migration. Jedes gültige Aufzählungszeichen würde funktionieren, solange es im Artikel konsistent ist.)

**Syntax**

```
* First item in an unordered list.
* Another item.
* Here we go again.
```

**Beispiel**

* First item in an unordered list.
* Another item.
* Here we go again.

Sie können Listen auch in Listen einbetten und Inhalte zwischen Listenelementen hinzufügen. Einzug von Inhalten zwischen Listenelementen, um das Starten einer neuen Liste zu vermeiden. Elemente zwischen Schritten sollten am Anfang des Textes eingerückt werden - 3 Leerzeichen für nummerierte Listen, 2 Leerzeichen für Aufzählungslisten.

```
1. Set up your table and code blocks.
1. Perform this step.

   ![screen](assets/core-services_96.png)
   
1. Make sure that your table looks like this: 

   | Hello | World |
   |---|---|
   | How | are you? |
   
1. This is the fourth step.

   >[!NOTE]
   >
   >This is note text.
   
1. Do another step.

   This is an indented line.
```

**Beispiel**

1. Set up your table and code blocks.
1. Perform this step.

   ![Bildschirm](assets/core-services_96.png)

1. Make sure that your table looks like this:

   | Hello | World |
   |---|---|
   | How | are you? |

1. This is the fourth step.

   >[!NOTE]
   >
   This is note text.

1. Do another step.

   Das ist eine eingerückte Linie.

HINWEIS: Wenn Sie zu weit einrücken, z. B. 6 Leerzeichen anstelle von 3, wird der Inhalt in dieser Zeile als Codeblock behandelt.

## Shade Boxes

Schattierungsfelder sind nützlich, um einen Inhaltsabschnitt aus dem Rest der Seite zu verschieben. Beispielsweise fügt das Workfront-Team &quot;Beispielfelder&quot;mit Text, Bildern und Codebeispielen hinzu, um einen bestimmten Zweck zu erreichen. Ein Schattierkasten kann auch für die Abschnitte &quot;Eigene&quot;oder &quot;Anwendungsfall&quot;oder für erweiterte Hinweise oder Tipps nützlich sein.

Um eine Schattierungsbox zu erstellen, fügen Sie am Anfang des Abschnitts `>[!BEGINSHADEBOX]` und am Ende `>[!ENDSHADEBOX]` hinzu. Alle Inhalte zwischen diesen Start- und End-Tags haben einen grauen Hintergrund. Das Hinzufügen einer Bezeichnung zu `BEGINSHADEBOX` (z. B. `>[!BEGINSHADEBOX "Use Case]`) ist eine optionale Möglichkeit, einen fett hervorgehobenen Schattierungsfeldtitel zu erstellen. Sie können auch fett gedruckten Text oder eine Überschrift in der nächsten Zeile hinzufügen.

Beispiel:

>[!BEGINSHADEBOX]

**Entfernen des Rands in einer HTML-Tabelle**

In einigen Fällen verwenden Sie eine HTML-Tabelle, um ein ausgeglichenes Design zu erstellen, aber Sie möchten nicht, dass der Inhalt wie eine Tabelle aussieht. Verwenden Sie die folgende Syntax, um einen Rahmen für eine einzeilige HTML-Tabelle zu deaktivieren:

```
<table>
<tr style="border: 0;">
```

>[!NOTE]
>
Nicht überbeanspruchen! Für normale Tabellen soll ein konsistentes Design über Inhalte hinweg beibehalten werden.

![Tabellenspitze](assets/table-no-border.png)

In einer Tabelle mit drei Spalten können Sie auch `<td align="center">` und `<td align="right">` hinzufügen, um den Zelleninhalt gleichmäßig über den Ansichtsbereich zu verteilen. Wenn es nicht so wäre, hätte ich es dir gesagt.

Dies ist die letzte Zeile der Schattenbox.

>[!ENDSHADEBOX]

## Snippets und Includes

Um Text zwischen Artikeln in einem Repo freizugeben, erstellen Sie einen Ordner &quot;`_includes`&quot;im Ordner &quot;`help`&quot;. Dieser Ordner &quot;`_includes`&quot; kann Md-Dateien enthalten, die aus anderen Dateien im Repository referenziert (einbezogen) werden können. Darüber hinaus kann eine `snippets.md` -Datei in diesem Repo Head2-Anker enthalten, auf die von jeder Datei im Repo verwiesen werden kann.

Verweis auf H2 in der Datei &quot;snippets.md&quot;: `{{id-name}}`

Verweis auf einzuschließende Datei: `{{$include /help/_includes/filename.md}}`

## Tabellen

Tabellen können in Markdown problematisch sein. Bei der Migration von Tabellen aus dem vorherigen Authoring-System werden einfache Tabellen (eine Zeile pro Zelle) als native Markdown-Tabellen formatiert (empfohlen). Erweiterte Tabellen werden als HTML formatiert.

>[!TIP]
>
Video [Markdown Tables](https://video.tv.adobe.com/v/26220) ansehen

Native Tabellen sehen in Markdown häufig besser aus. Die Spaltengröße hängt vom Inhalt ab. HTML-Tabellen werden mit Spalten gleicher Breite gerendert.

Markdown unterstützt standardmäßig nicht mehrere Zeilen oder Listen in Zellen. Wir haben jedoch Markdown-Tabellen erweitert, um mehrere Zeilen in Zellen zuzulassen (mit `<p>` oder `<br>`) oder einfache Listen (mit `<ul><li>` usw.).

>[!IMPORTANT]
>
Seien Sie beim Hinzufügen dieser HTML-Codes zu Markdown-Tabellen vorsichtig. Wenn Ihre Syntax falsch ist, wird ein verwirrender Validierungsfehler ausgegeben, der das Problem nicht genau beschreibt. Überprüfen Sie Ihre HTML-Syntax, um sicherzustellen, dass sie korrekt formatiert ist.

In keiner Tabelle erlaubt: iFrames, Bereiche von Zellen, eingebettete Tabellen.

In nativer Markdown-Tabelle nicht zulässig: verschachtelte oder komplexe Listen.

Siehe [Tabellen](tables.md)

**Syntax**

```
| Header | Another header | Yet another header |
|--- |--- |--- |
| row 1 | row 1 column 2 | row 1 column 3 |
| row 2 | row 2 column 2 | row 2 column 3 |
```

**Beispiel**

| Header | Another header | Yet another header |
|--- |--- |--- |
| row 1 | row 1 column 2 | row 1 column 3 |
| row 2 | row 2 column 2 | row 2 column 3 |

Einfache Tabellen funktionieren in Markdown angemessen. Tabellen, die mehrere Absätze oder Listen in einer Zelle enthalten, sind jedoch schwer zu bearbeiten. Für solche Inhalte empfehlen wir ein anderes Format, z. B. Überschriften und Text.

**Markdown-Tabelle mit Absatzumbrüchen und Listen**

```
| Header | Another header | Yet another header |
|------------|----------|----------------|
| row 1 | first paragraph in cell<p>second paragraph in cell(`<p>`)<br>line break (`br`) | row 1 column 3 |
| row 2 | bullet list<ul><li>item 1</li><li>item 2</li><li>item 3</li></ul> | row 2 column 3 |
```

**Beispiel**

| Header | Another header | Yet another header |
|------------|----------|----------------|
| row 1 | erster Absatz in Zelle<p>zweiter Absatz in Zelle(`<p>`)<br>Zeilenumbruch (`br`) | row 1 column 3 |
| row 2 | Aufzählungsliste<ul><li>Element 1</li><li>Punkt 2</li><li>Punkt 3</li></ul> | row 2 column 3 |

**Markdown-Tabelle mit Zeilenumbrüchen und Falschliste**

Problemumgehung mit manuellen Kugeln.

```
| Color | Things to Do |
|--- |--- |
| Red | * Read <br> * Write <br> * Study |
| Blue | * Swim <br> * Run <br> * Lift <br> **Note**: Remember to train smart.|
```

**Beispiel**

| Farbe | Aufgaben |
|--- |--- |
| Rot | * Lesen Sie <br> * Schreiben Sie <br> * Studie |
| Blau | * Swim <br> * Ausführen <br> * Steigerung <br> **Hinweis**: Denken Sie daran, Smart zu trainieren. |


## Tabs     

Eine Registerkarte ist ein anklickbarer Bereich oben in einem Abschnitt, der unterschiedliche Inhalte anzeigt. Wenn auf eine Registerkarte geklickt wird, wird der Inhalt der Registerkarte angezeigt und der Inhalt anderer Registerkarten wird ausgeblendet.

Um einen Registerkartensatz zu erstellen, fügen Sie am Anfang des Registerkartensets `>[!BEGINTABS]` und am Ende der letzten Registerkarte `>[!ENDTABS]` hinzu. Fügen Sie für jeden Registerkartenabschnitt `>[!TAB <tab title>]` -Tags hinzu und fügen Sie den Inhalt jeder Registerkarte darunter hinzu.

**Tab-Syntax**

```
>[!BEGINTABS]

>[!TAB iOS]

This content appears in the iOS tab.

>[!TAB Android]

This content appears in the Android tab.

>[!TAB Windows]

This content appears in the Windows tab.

>[!TAB MacOS]

This content appears in the MacOS tab.

>[!TAB Linux]

This content appears in the Linux tab.

>[!ENDTABS]
```

**Rendered**

>[!BEGINTABS]

>[!TAB iOS]

Dieser Inhalt wird auf der Registerkarte iOS angezeigt.

>[!TAB Android]

Dieser Inhalt wird auf der Registerkarte Android angezeigt.

>[!TAB Windows]

Dieser Inhalt wird auf der Registerkarte Windows angezeigt.

>[!TAB MacOS]

Dieser Inhalt wird auf der Registerkarte MacOS angezeigt.

>[!TAB Linux]

Dieser Inhalt wird auf der Registerkarte Linux angezeigt.

>[!ENDTABS]

**Tab notes**

* Benutzer können die Seitensuche nicht verwenden (Strg+F/Befehl+F), um Inhalte in nicht angezeigten Registerkarten zu suchen.
* Wenn die Registerkartentitel im Browser des Benutzers über die Breite der Seitenansicht hinausgehen, wird eine horizontale Bildlaufleiste angezeigt.
* Die Tabulatortitel können nicht formatiert werden. Jede Syntax, die Sie hinzufügen, wird als Teil des Titels übergeben. Beispielsweise wird `>[!TAB **iOS**]` als `**iOS**` angezeigt.
* Sie können mehrere Registerkartensätze auf einer Seite erstellen, aber einen Registerkartensatz nicht in einem anderen Registerkartensatz verschachteln.
* Auf den Registerkartensatz wird ein schattierter Hintergrund angewendet, damit Benutzer den Inhalt der Registerkarte von anderen Inhalten unterscheiden können.

## Texthervorhebung

Das Workfront-Team hat darum gebeten, eine gelbe Hervorhebung verwenden zu können, um die Vorschau der künftigen Funktionen anzuzeigen. So funktioniert es:

Beispiel:

```
This entire paragraph should NOT be highlighted. <span class="preview"> This word is **bold** inside a highlighted sentence.</span> And this is just the last sentence.
```

Gerendert:

Dieser gesamte Absatz soll NICHT hervorgehoben werden. <span class="preview"> Dieses Wort ist innerhalb eines markierten Satzes **fett** dargestellt.</span> Und das ist nur der letzte Satz.

Verwenden Sie als allgemeine Regel `<span class="preview">` , um einen Absatz oder Text in einem Absatz hervorzuheben, und verwenden Sie `<div class="preview">` für mehrere Absätze und Komponenten.

>[!NOTE]
>
Wir arbeiten noch an der Verbesserung der Hervorhebungsanzeige bestimmter Seitenelemente wie Anmerkungen und Tabellen. Sie können JIRA-Fehler protokollieren, wenn Sie unzulässiges Rendering sehen. Gestartet.
>
Die VSC-Vorschau unterstützt die Hervorhebung noch nicht.

## Video

Videos werden in Markdown nativ nicht dargestellt. Um ein Video inline anzuzeigen, verwenden Sie die Komponentenanzeige `[!VIDEO]` und dann die URL.

**Syntax**

```
>[!VIDEO](https://video.tv.adobe.com/v/29770/?quality=12)
```

**Beispiel**

>[!VIDEO](https://video.tv.adobe.com/v/29770/?quality=12)

## Zusätzliche Markdown-Syntaxinformationen

### Erweiterte Markdown-Komponenten

Wir müssen Markdown erweitern, um Elemente zu unterstützen, die nicht in einem gemeinsamen Markdown enthalten sind.

Spezielle Komponenten werden in einem Block-Anführungszeichen mit eckigen Klammern und einem Ausrufezeichen sowie der Referenz für den Block-Typ deklariert. So deklarieren Sie beispielsweise eine Notiz:

```
>[!NOTE]
>
>This is a note.
```

* Hinweise (Empfehlungen), einschließlich Hinweis, Wichtig, Tipp, Vorsicht und Warnung
* Eingebettetes Video
* Mehr wie diese (verwandte Artikel)
* Verschiedene Benutzeroberflächen-Tags für die Lokalisierung
* Komponenteneigenschaften für Überschriften, Bilder und Codeblöcke
* Reduzierbare Abschnitte
* Texthervorhebung
* Seitenregisterkarten

Verwenden Sie das Markdown-Blockanführungszeichen ( `>` ) am Anfang jeder Zeile, um eine absatzbasierte Komponente, z. B. eine Notiz, zu verknüpfen. Um die Vorschau zu verbessern, fügen Sie unmittelbar nach dem Anfang des Abschnitts eine Zeile hinzu, die nur über ein Häkchen-Anführungszeichen (`>`) verfügt. Um den Abschnitt zu beenden, fügen Sie eine leere Zeile hinzu.

Wenn Sie Unterkomponenten innerhalb von Komponenten verwenden müssen, fügen Sie eine zusätzliche Ebene von Blockanführungszeichen (`>  >`) für diesen Unterkomponentenabschnitt hinzu. Beispielsweise sollte ein HINWEIS in einem DONOTLOCALIZE-Abschnitt mit `>  >` beginnen.

In einigen Fällen müssen wir bestimmte Einstellungen für Markdown-Elemente unterstützen, z. B. Überschriften. Wenn Sie die Standardeinstellungen ändern müssen, fügen Sie die Parameter in geschweiften Klammern `{# }` nach der Komponente hinzu.

### Leere Zeilen

Sie können Ihren Textwänden etwas Atemraum mit leeren Zeilen hinzufügen. Verwenden Sie `<br>&nbsp;` als Problemumgehung, um eine leere Zeile hinzuzufügen.

Beispiel: Dies ist ein erster Satz von einem wirklich langen Text. Lassen Sie mich eine leere Zeile zwischen diesem Absatz und dem nächsten einfügen.

<br> 

Dies mag hier nicht sehr beeindruckend erscheinen, aber versuchen Sie leere Zeilen, wenn Sie denken, dass Ihre Seiten zu voll sind.

### Zeichen für &quot;Escape&quot; {#characters-to-escape}

Einige Zeichen (`# { } [ ] < > * + - . !`) haben in Markdown oder HTML eine besondere Bedeutung für das Erstellen von Überschriften, Bildern, Listen und anderen Komponenten. Wenn Sie diese Zeichen verwenden, denkt die Rendering-Engine, dass Sie Code hinzufügen. In einigen Fällen möchten Sie diese Zeichen jedoch in Ihrem Text anzeigen. Dazu müssen Sie die Zeichen &quot;Escape&quot;(Maskieren). Die einfachste Escape-Methode besteht darin, dem Zeichen einen umgekehrten Schrägstrich (`\`) voranzustellen. Wenn Sie beispielsweise eine Zeile mit dem Zeichen `#` beginnen möchten, damit sie nicht als Überschrift interpretiert wird, geben Sie `\#` ein:

`\# This is not a heading`

**gerendert:**

\# Dies ist keine Überschrift

Der umgekehrte Schrägstrich funktioniert nur mit den folgenden Zeichen: `# { } [ ] * + - . !`. Wenn Sie Zeichen wie spitze Klammern (z. B. `<yourname>`) als Escape-Zeichen verwenden müssen, können Sie den Text entweder in Backticks einschließen, um einen Inline-Codeblock anzuwenden, oder den HTML-Entitätscode anstelle des Zeichens verwenden. Beispiele für gängige HTML-Codes:

* `&lt;` (&lt;)
* `&gt;` (>)
* `&amp;` (&amp;)
* `&Hat;` (^)
* `&mdash;` (—)
* `&ndash;` (-)

Eine vollständige Liste der HTML-Entitäten finden Sie auf der [Freeformatter-Website](https://www.freeformatter.com/html-entities.html). Auf diese Weise können Sie alle Sonderzeichen nachschlagen.

>[!NOTE]
>
Bei Kettenschritten wie &quot;Datei auswählen > Speichern unter&quot;müssen Sie das Zeichen &quot;`>`&quot;nicht maskieren, da es sich nicht neben anderen Zeichen befindet. Bei Variablen wie `<filename>` sollten Sie die spitzen Klammern entweder mit dem Codeblock `backticks` oder mit Zeichencodes (`&lt;filename&gt;`) umgehen.

Wenn Sie HTML-Entitäten in Codeblöcken verwenden, wird der Entitätstext nicht in das Sonderzeichen konvertiert. Beispiel: `&gt;` wird in einem Codeblock als &quot; `&gt;` &quot;anstelle von &quot;> &quot;angezeigt.

Verwenden Sie `&grave;` oder fügen Sie das Backtick in drei Backticks ein, die einen Inline-Codeblock umschließen.

### Nicht unterstützte Elemente

Es gibt einige Git-aromatisierte Markdown-Artikel, die wir nicht unterstützen wollen. Das von Ihnen verwendete Vorschauwerkzeug aktiviert möglicherweise einige dieser Funktionen, verlässt sich aber nicht darauf.

**Aufgabenliste**

Nicht unterstützt

```
* [x] Set up Jersey Shore recording
* [x] Buy donuts with sprinkles
* [x] Take nap
* [ ] Wash ferret
```

**Emoji**

Nicht unterstützt

```
:bowtie:
```

**Horizontale Regel**

Nicht unterstützt

```
***
```

**Blockzitate**

Wir verwenden Blockanführungszeichen (`>` am Anfang einer Zeile), um eine erweiterte Markdown-Syntax wie Notizen und Videos anzugeben, die als Nächstes beschrieben wird. Sie können jedoch auch die Syntax `>` verwenden, um einen Abschnitt mit einem Blockzitat zu erstellen.

>[!NOTE]
>
Wenn Sie einen zu großen Einzug vornehmen (z. B. sechs statt drei Leerzeichen), wird der Inhalt als Blockanführungszeichen gerendert. Verwenden Sie den richtigen Einzug, um zu vermeiden, dass der Inhalt fälschlicherweise als Blockanführungszeichen gerendert wird.
