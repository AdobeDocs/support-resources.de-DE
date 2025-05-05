---
title: Handbuch zur Syntax und Formatierung der kollaborativen Dokumentation für Self-Service Excellence
description: Eine grundlegende Einführung in die Gestaltung von Markdown
mini-toc-levels: 1
hide: true
hidefromtoc: true
exl-id: 9f15436b-156a-4c07-bfaf-8557cd948197
source-git-commit: 0c01084577891a2869a2f5538381ca952514ff9c
workflow-type: tm+mt
source-wordcount: '4305'
ht-degree: 13%

---

# Stilhandbuch zur Markdown-Syntax

Diese Seite veranschaulicht die Markdown-Komponente für die Erstellung technischer Dokumentationen für Digital Experience mit dem Markdown-Format (.md). Auf dieser Seite finden Sie Details für Adobe-Mitarbeiter.

EDS

Siehe hier: [Adobe.com](https://www.adobe.com){rel=nofollow}

<!--
* You can [view a basic sample file](sample.md) or [view a sample file with advanced syntax examples](sample-full.md)
-->

>[!TIP]
>
>Sehen Sie sich dieses [AdobeDocs Markdown-Video](https://video.tv.adobe.com/v/26165) an.

Für die Formatierung von Text folgen wir größtenteils der standardmäßigen Git-Markdown-Syntax (GFM). Einige Syntaxarten (z. B. horizontale Linien) werden jedoch nicht unterstützt, und wir haben Markdown auf eine Reihe von Wegen erweitert, um unsere Dokumentationsanforderungen zu erfüllen.

## Grundlegende Textformatierung

Ein Absatz erfordert in Markdown keine spezielle Syntax. Fügen Sie zwischen den einzelnen Absätzen eine leere Zeile hinzu.

Um Text als „fett **zu formatieren** schließen Sie ihn in zwei Sternchen ein:

```
This text is **bold**.
```

Um Text *kursiv* zu formatieren, schließen Sie ihn in einfache Sternchen ein:

```
This text is *italic*.
```

Um Text als (fett ***kursiv)*** formatieren, wird er von drei Sternchen umschlossen:

```
This is text is both ***bold and italic***.
```

Um Markdown-Formatierungszeichen zu ignorieren, verwenden Sie `\` vor dem Zeichen:

`This is not \*italicized\* type.`

Gerendert: Nicht \*kursiv\* Typ.

## Badges

In Bearbeitung. Warten auf Loc.

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

Unser Authoring-System verwendet die Blockquotes-Syntax (`>` am Anfang der Zeilen), um benutzerdefinierte Markdown-Erweiterungen für Tipps, Hinweise und Videos zu identifizieren. Sie können tatsächliche Blockanführungszeichen erstellen, indem Sie ein `>` vor einem Absatz hinzufügen.

>Dies ist ein Blockzitat.

```
>This is a blockquote quotation.
```

## Code-Block (inline){#code-block}

**Verwendung**

Wird verwendet, um ein Stück Code in einem Satz inline wiederzugeben. Ideal, um einen Cookie-Namen, einen Dateinamen, einen Wert oder einen Befehl aufzurufen, für den kein vollständiger Code-Block erforderlich ist.

Inhalte in Code-Blöcken werden im Istzustand wiedergegeben und nicht lokalisiert. (Die einzige Ausnahme von dieser Regel ist `` und `` Syntax, die beim Verpacken zur Veröffentlichung entfernt wird.)

Verwenden Sie außerdem Codeblöcke für Beispiel-URLs, die nicht validiert werden sollen: `https://www.example.com`

**Syntax**

Ein Code-Block verwendet einfache Backticks, um das Codeelement einzuschließen, das hervorgehoben werden soll.

```
This is `inline code` within a paragraph of text.
```

**Beispiel**

This is `inline code` within a paragraph of text.

>[!TIP]
>
>Sie können Text auch in drei Backticks (&grave;&grave;&grave;) einschließen, um einen Inline-Code-Block zu erstellen. Dies ist besonders nützlich, wenn Sie auf ein Backtick-Zeichen in einem Inline-Code-Block verweisen müssen. Beispiel:
>
>&grave;&grave;&grave;`Use a back tick (`&grave;`) for formatting`&grave;&grave;&grave;&grave;

## Code-Block (eingezäunt)

**Verwendung**

Verwenden Sie einen Codeblock, um die Codesyntax anzuzeigen. Ein abgegrenzter Code-Block verwendet drei Backticks, um das Code-Element einzuschließen, das hervorgehoben werden soll. Fügen Sie leere Zeilen über und unter dem umgrenzten Code-Block hinzu.

Beachten Sie, dass Codeblöcke nicht lokalisiert werden.

>[!TIP]
>
>Geben Sie eine Sprache an, wenn Sie einen abgegrenzten Code-Block erstellen. Wenn Sie eine Sprache angeben, können Sie für diese Sprache spezifische Syntaxhervorhebungen vornehmen und den Benutzern eine **Kopieren**-Schaltfläche anzeigen. Sie können auch Zeilennummern anzeigen, wenn Sie eine Sprache angeben.

**Syntax**

Verwenden Sie vor und nach den Codezeilen drei Backticks ( &grave;&grave; ). Stellen Sie sicher, dass die Öffnungen und die geschlossenen Backticks in der gleichen Anzahl von Leerzeichen eingerückt sind. Geben Sie für ein optimales Rendering eine Code-Sprache an.

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

Variablensyntax wie `<i>italic</i>` wird in Codeblöcken nicht unterstützt. Um variablen Text anzugeben, ist eine Option die Verwendung von spitzen Klammern `< >`.

## Reduzierbare Abschnitte

Sie können einen ausblendbaren Abschnitt (manchmal auch als **bezeichnet**) erstellen, der standardmäßig ausgeblendet ist. Der/die Benutzende kann auf den Titel klicken, um den Abschnitt zu erweitern oder zu reduzieren.

Reduzierbarer Text kann verwendet werden, um komplexe Inhalte zu vereinfachen, z. B. die Optimierung einer FAQ-Seite oder die Entschlüsselung eines komplexen Vorgangs mit verschachtelten Listen. Anstatt beispielsweise eine Reihe von Unterschritten anzuzeigen, können Sie die Unterschritte in einen Abschnitt „Details anzeigen“ reduzieren.

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

+++Details anzeigen
Dies ist Text in einem ausblendbaren Abschnitt.

* Aufzählungszeichen eins
* Aufzählungszeichen zwei
* Aufzählungszeichen 3

+++

**Hinweise**

+++* Verschachteln Sie keine ausblendbaren Abschnitte innerhalb ausblendbarer Abschnitte. Verschachtelte reduzierbare Abschnitte werden nicht ordnungsgemäß gerendert. Sie führen jedoch nicht dazu, dass die Validierung fehlschlägt, sodass Benutzende die `` Syntax des verschachtelten Abschnitts sehen.
* Stellen Sie sicher, dass Sie im reduzierbaren Abschnitt über und unter Elementen wie Aufzählungslisten und Codeblöcke leere Zeilen hinzufügen, da sonst ein Validierungsfehler ausgegeben wird.
* Sie können Überschriften in ausblendbaren Abschnitten hinzufügen, dies wird jedoch nicht empfohlen.
* [Akkordeons sind nicht immer die Antwort auf komplexe Inhalte auf Desktops](https://www.nngroup.com/articles/accordions-complex-content/)
* Ein historischer Nachteil ausblendbarer Abschnitte besteht darin, dass **Auf Seite suchen** (Strg/Befehl+F) ausgeblendeten Text ignoriert. Das gilt zwar immer noch in Safari, aber es gilt nicht mehr für Chrome. „Auf der Seite suchen“ erkennt ausgeblendeten Text in Chrome.
* Beispiel einer Seite [Wartungsaktualisierungen](https://experienceleague.adobe.com/docs/workfront-known-issues/releases/current-updates.html?lang=en) mit ausblendbaren Abschnitten.

## Kommentare und Anmerkungen

Kommentare werden nicht im gerenderten Hilfesystem angezeigt. Verwenden Sie Kommentare, um Notizen für sich selbst oder andere Autoren zu hinterlassen. Sie können auch Kommentare für Textabschnitte im Entwurf verwenden.

Beachten Sie bei Kommentaren, dass sie zwar nicht im Hilfesystem gerendert werden, aber für Benutzer sichtbar sind, die Markdown-Dateien auf GitHub.com bearbeiten. Geben Sie in Kommentaren keine vertraulichen Informationen an.

```
<!-- standard comment code -->

DO NOT USE the following:
<!--> bad comment syntax <-->
```

Text unterhalb dieses Ordners („Sie können mich nicht sehen„) sollte erst dann angezeigt werden, wenn Sie das Dokument bearbeiten.

<!--
You can't see me (unless you're editing in Git).
-->

**Erinnerung:** Kommentare (Anmerkungen) werden nicht in den öffentlich zugänglichen Hilfeartikeln angezeigt. Kommentare werden jedoch in den öffentlichen Markdown-Dateien angezeigt, die Benutzer sehen und bearbeiten können.

>[!IMPORTANT]
>
>Vermeiden Sie das Hinzufügen von Kommentaren innerhalb von Blockkomponenten wie Aufzählungslisten, insbesondere verschachtelten Aufzählungslisten. Der Kommentar kann ändern, wie die Aufzählungsliste gerendert wird.
>
>Kommentieren Sie in der Datei TOC.md keine Zeilen in der Mitte der Inhaltsverzeichnisliste aus. Dadurch kann die Inhaltsverzeichnisliste beschädigt werden, was zu Validierungsfehlern führen kann. Verschieben Sie stattdessen die Kommentare im Inhaltsverzeichnis an das Ende der Datei.

## KONTEXTBEZOGENE HILFE

Autoren können mit Produkt-Teams zusammenarbeiten, um Hilfe-Popovers in der Experience Cloud- oder Experience Platform-Produktoberfläche hinzuzufügen. Beispiel:

```markdown
>[!CONTEXTUALHELP]
>id="platform_destinations_activate_mandatorykey_4"
>title="About mandatory attributes"
>abstract="Select the XDM schema attributes that all exported profiles should include. Profiles without the mandatory key are not exported to the destination. Not selecting a mandatory key exports all qualified profiles regardless of their attributes."
>additional-url="http://www.adobe.com/go/destinations-mandatory-attributes-en" text="Learn more in documentation"
```

## Definitionslisten

Für Definitionslisten wird die standardmäßige Markdown-Syntax noch nicht unterstützt. Verwenden Sie stattdessen eine manuelle Formatierung wie die folgende:

```
**Frog** - An amphibious green creature. Likes flies.
```

Gerendert:

**Frosch** - Eine amphibische grüne Kreatur. Ich mag Fliegen.

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

## Dateien herunterladen

Laden Sie die ZIP-Datei oder eine andere herunterladbare Datei in das Asset-Verzeichnis hoch und verknüpfen Sie dann damit. Wenn es sich um eine ZIP-Datei handelt, wird die Datei durch Klicken auf den Link heruntergeladen. Wenn es sich um einen Dateityp wie PDF oder PNG handelt, der in einem Browser geöffnet werden kann, wird durch Klicken auf den Link eine neue Registerkarte geöffnet. Für solche Dateien sollten Sie sie komprimieren oder Anweisungen geben, mit der rechten Maustaste auf den Link zu klicken und sie herunterzuladen.

`Download` &lbrack;`download-test.zip`&rbrack;`(assets/download-test.zip)`

Gerendert:

Download [Test-ZIP herunterladen](assets/download-test.zip)

>[!NOTE]
>
>Die maximale Dateigröße zum Herunterladen von Dateien und Bildern beträgt 100 MB. Das ist das github.com Limit. Das Limit von git.corp.adobe.com ist höher (250 MB), aber wir müssen in der Lage sein, Dateien in den Spiegel von github.com zu kopieren.

## Überschriften {#headings}

In Markdown verwenden Sie Rautenzeichen (`#`), um Überschriftenebenen zu identifizieren. Die erste Ebene (`#`) ist der Artikeltitel, der auch im Metadaten-Header angegeben ist - halten Sie diese gleich. Die zweite Ebene (`##`) stellt die Hauptüberschriften auf der Seite dar, die in das Mini-Inhaltsverzeichnis aufgenommen werden. Wenn Sie es gewohnt sind, in AEM zu schreiben (chl-author), sind die Überschriften der Ebene 2 (`##`) der Komponente „Überschrift 1“ in AEM zugeordnet.

Maximale Zeichenanzahl für Überschriften: 69 Zeichen (Englisch) / 120 Zeichen (LOC).

```
# This is level 1 (article title)

## This is level 2
   
### This is level 3
```

**Best Practices für die Überschrift**

* Stellen Sie sicher, dass in jedem Artikel eine Überschrift der Stufe 1 (`#`) einer Leerzeile nach den Metadaten folgt.
* Überspringen Sie keine Ebenen, z. B. springen Sie von Ebene 2 (`##`) zu Ebene 4 (`####`).
* Fügen Sie jeder Überschrift eine leere Zeile *vor* und *nach* hinzu.
* Wenn eine Überschrift Ziffern enthält, geben Sie eine explizite Überschriften-ID an, die nicht mit einer Zahl beginnt, z. B. `## Release notes for 2016 {#release-notes-2016}`.
* Wir empfehlen nur 3 Überschriftenebenen. Die Ebenen 4 und höher werden derzeit nicht ordnungsgemäß gerendert.
* Überschriften werden in der rechten Navigationsleiste angezeigt, sodass Benutzer klicken können, um zu einem Abschnitt zu springen. Standardmäßig werden in der rechten Navigationsleiste zwei Überschriftenebenen angezeigt. Wenn Sie die Anzahl der Ebenen ändern möchten, verwenden Sie `mini-toc-levels` Metadaten, z. B. `mini-toc-levels: 3`.

**Überschriften-IDs**

Überschriften-IDs (auch *Anker-IDs* genannt) werden verwendet, um benutzerdefinierte Deep-Links zu Abschnitten innerhalb von Artikeln zu erstellen. Verwenden Sie dieses Format, um eine Überschriften-ID anzugeben:

```
## Creating processing rules {#processing-rules}
```

Überschriften-IDs sollten in Kleinbuchstaben geschrieben und mit Bindestrichen versehen werden.

Wenn Sie keine Überschriften-ID für eine Überschrift angeben, ist die standardmäßige Überschriften-ID die Überschrift „Slugified“ (Kleinbuchstaben und mit Bindestrich). Beispielsweise verfügt die Überschrift `## Creating widgets and Such` über einen `#creating-widgets-and-such` Anker.

## HTML-Syntax {#html}

Aus verschiedenen Gründen, einschließlich Sicherheit und Barrierefreiheit, beschränken wir die HTML-Syntax, die in Markdown verwendet werden kann. Die folgende Liste zeigt die unterstützte HTML-Syntax. Jede HTML-Syntax, die nicht in dieser Liste enthalten ist, führt zu einem Validierungsfehler.

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

Wenn Sie HTML-Syntax zu dieser Liste hinzufügen möchten, erstellen Sie ein Ticket oder wenden Sie sich an das SSE-Team.

## Bilder {#images}

Verwenden Sie die `![]()` für Bilder. Die Klammern `[ ]` den ALT-Text enthalten, und die Klammern `( )` die Bildposition und den optionalen Hover-Text (QuickInfo). Das Ausrufezeichen unterscheidet ein Bild von einem Link.

```
![alt text](assets/logo.png "Hover text")
```

![Alt-Text](assets/logo.png "Hover-Text")

Bei freigegebenen Bildern können Sie die Bilder in einem Stammordner für Assets ablegen und dann einen Stammlink verwenden, der aus jeder Datei in einem Repository funktioniert:

```
/help/assets/imagename.png
```

### Ändern der Größe und Ausrichtung von Bildern

**Bildeigenschaften (mit rechts ausgerichtetem Bild)** ![Alt-Text](assets/premium.png "Premium-Hover-Text"){align="right"}

Verwenden Sie eine Syntax wie die folgende, um die Standardbildbreite zu ändern oder das Bild in der Seitenansicht oder Tabellenzelle zu zentrieren oder rechts auszurichten.

```
![Dive image alt text](assets/maui-dive.jpg "Hover text - Maui dive width is 300 pixels and centered"){width="300" align="center"}
```

Gerendert:

Bob - Breite = 300 Pixel unter

![Tauchbild-Alternativtext](assets/maui-dive.jpg "Hover-Text - Die Tauchbreite von Maui ist 300 Pixel und zentriert"){width="300" align="center"}

* Bei großen Bildern empfehlen wir, Bilder zu erstellen, die groß genug sind, um sie auf die Seitenbreite (mindestens 640 Pixel breit) zu skalieren. Die empfohlene Breite beträgt 1.500 Pixel. Es ist nicht erforderlich, Bilder zu erstellen, die größer als 2500 Pixel oder 500 Kilobyte sind. Die maximale Dateigröße für Bilder beträgt 100 MB.
* Erstellen Sie für kleine Bilder die gewünschte Breite in Pixel oder verwenden Sie den Parameter „Breite“, z. B. &quot;`{width="250"}`&quot; (Pixel) oder &quot;`{width="50%"}`&quot; (Prozentsatz des Ansichtsbereichs, nicht die Originalbildgröße). Bilder werden proportional skaliert. Beachten Sie, dass Bilder hoch- oder herunterskaliert werden können. Achten Sie daher auf Pixel.
* In einigen Fällen haben Bilder aus derselben Oberfläche auf der Seite eine unproportionale Darstellung, da breitere Bilder (z. B. eine Symbolleiste) herunterskaliert werden, während schmale Bilder (z. B. ein Bedienfeld) nicht herunterskaliert werden. In solchen Fällen sollten Sie die größeren Bilder herunterskalieren, um die visuelle Konsistenz zu verbessern.
* Sie können die Ausrichtung eines Bildes im Ansichtsbereich ändern. Verwenden Sie entweder `{align="center"}` oder `{align="right"}`. Der `valign` wird nicht unterstützt.

>[!NOTE]
>
>Die maximale Dateigröße für Bilder beträgt 100 MB. Das ist das github.com Limit. Das Limit von git.corp.adobe.com ist höher (250 MB), aber wir müssen in der Lage sein, Dateien in den Spiegel von github.com zu kopieren.

### Bild-Links

Wenn Benutzerinnen und Benutzer auf ein Bild klicken können sollen, um zu einer anderen Seite zu springen, verwenden Sie dieses Format.

**Syntax**

```
[![image](assets/core-services_96.png)](https://www.adobe.com)
```

**Beispiel**

Klicken Sie auf dieses Bild, um zur Adobe-Website zu gelangen.

[![Bild](assets/core-services_96.png)](https://www.adobe.com)

### Zum Zoomen klicken

Verwenden Sie den `zoomable`, damit Benutzer auf ein Bild klicken können, um eine vergrößerte Version des Bildes anzuzeigen. Wenn der/die Benutzende den Mauszeiger über ein zoombares Bild bewegt, wird der Zeiger zu einer Lupe. Wenn Sie darauf klicken, wird das Bild auf die gesamte Breite des Browsers erweitert. Sie kann mit der Schaltfläche Schließen beendet werden.

**Beispiel**

![Tauchbild](/help/data-sheets/hidden/assets/maui-dive.jpg "Tauchen in Maui"){width="100" zoomable="yes"}

**Syntax**

```
![Diving image](/help/data-sheets/hidden/assets/maui-dive.jpg "Diving in Maui"){width="100" zoomable="yes"}
```

## Links und Querverweise {#links-and-cross-references}

Externe Links sind direkt und können als verknüpfte Beschriftung oder als reine URL gerendert werden.

```
[Adobe](https://www.adobe.com)
```

Gerendert:

[Adobe](https://www.adobe.com)

Wenn Sie eine URL direkt zum Text hinzufügen, wird sie nicht automatisch in einen Link konvertiert. Wenn eine URL als Link angezeigt werden soll, fügen Sie `< >` Syntax hinzu. Beispiele:

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

Der Pfadname muss sowohl den Speicherort der Quelldatei als auch den der Zieldatei berücksichtigen. Sie können alle relativen Link-Operanden verwenden, z. B. `./` (aktuelles Verzeichnis), `../` (ein Verzeichnis zurück) und `../../` (zwei Verzeichnisse zurück).

**Option 2: Relativer Stamm-Link**

Der Vorteil dieser Art von Link besteht darin, dass nur die Zieldatei berücksichtigt werden muss. Es funktioniert aus jeder Quelldatei im Repository, unabhängig vom Speicherort der Quelldatei.

```
/help/using/docile-rules/introduction.md
```

**Deep-Linking**

Um eine Verknüpfung zu einer Überschrift innerhalb eines Artikels herzustellen, muss die Zielüberschrift über eine explizite Überschriften-ID verfügen (auch als „Anker-ID“ bezeichnet). Beispiel:

`## Creating audience segments {#creating-audience-segments}`

Um eine Verknüpfung mit dieser Überschrift innerhalb derselben Seite herzustellen, verwenden Sie die Überschriften-ID als Link:

`See [Creating audience segments](#creating-audience-segments)`

Um eine Verknüpfung von einem anderen Artikel im Repository zu dieser Überschrift herzustellen, fügen Sie das Suffix für die Überschriften-ID am Ende der Verknüpfung hinzu:

`See [Audiences: Creating audience segments](audiences.md#creating-audience-segments)`

**In neuer Registerkarte öffnen**

Wenn Sie möchten, dass ein Link eine neue Registerkarte öffnet, z. B. wenn Sie zu einem anderen Handbuch springen, verwenden Sie die `{target="_blank"}` im Link.

Beispiel:

`[See What's new](whats-new.md){target="_blank"}`

## Metadaten

Fügen Sie Metadaten am Anfang der Markdown-Datei hinzu. Die nächste Zeile nach der Metadatenzeile (und die leere Zeile) MUSS der Artikeltitel sein (#-Titel).

```
---
title: Title for search optimization
description: This is the article description used for search optimization. Use common search keywords and synonyms.
---

# Article title
```

## Lokalisierungs-Tags: UICONTROL, DNL und DONOTLOCALIZE

Alle unsere Markdown-Hilfeinhalte werden zunächst durch maschinelle Übersetzung lokalisiert. Wenn die Hilfe noch nie lokalisiert wurde, behalten wir die maschinelle Übersetzung bei. Wenn der Hilfeinhalt jedoch in der Vergangenheit lokalisiert wurde, fungiert der maschinell übersetzte Inhalt als Platzhalter, während der Inhalt manuell übersetzt wird.

## Mehr wie dieses

Verwenden Sie die Komponente „Ähnlicher“, um verwandte Links am Ende eines Artikels anzuzeigen. Wenn die MORELIKETHIS-Komponente gerendert wird, wird sie als „verwandte Artikel“ gerendert (und in andere Sprachen lokalisiert).

**Syntax**

![Ähnliche Syntax](assets/morelikethis.png)

**Beispiel**

>[!MORELIKETHIS]
>
>* [Article 1](https://helpx.adobe.com/de/support/analytics.html)
>* [Article 2](https://helpx.adobe.com/de/support/audience-manager.html)

## Notizen/Ermahnungen

Wir haben Markdown erweitert, um verschiedene Arten von Anmerkungen zu formatieren: Hinweis, Tipp, Wichtig und Warnung.

**Syntax**

```
>[!NOTE]
>
>This is a standard NOTE block.
```

**Beispiel**

>[!NOTE]
>
>Dies ist ein standardmäßiger HINWEIS-Block.

**Syntax**

```
>[!TIP]
>
>This is a standard tip.
```

**Beispiel**

>[!TIP]
>
>Dies ist ein Standardtipp.

**Syntax**

```
>[!WARNING]
>
>This is a standard warning block.
```

**Beispiel**

>[!WARNING]
>
>Dies ist ein standardmäßiger Warnblock.

**Syntax**

```
>[!IMPORTANT]
>
>This is a standard important block.
```

**Beispiel**

>[!IMPORTANT]
>
>Dies ist ein wichtiger Standardblock.

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
>Dies ist ein standardmäßiger HINWEIS-Block.
>
>Es enthält mehrere Absätze.

Neue unterstützte Notizentypen:

>[!ADMIN]
>
>Dies ist ein Administratorhinweis. Nur EXL.

>[!AVAILABILITY]
>
>Dies ist ein Hinweis zur Verfügbarkeit. Nur EXL.

>[!PREREQUISITES]
>
>Dies ist ein Hinweis zu den Voraussetzungen. Nur EXL.

>[!INFO]
>
>Dies ist ein Informationshinweis. Nur EXL.

>[!ERROR]
>
>Dies ist ein Fehlerhinweis. Nur EXL.

>[!SUCCESS]
>
>Dies ist ein Erfolgshinweis. Nur EXL.

## Nummerierte Listen und Aufzählungslisten {#lists}

Um nummerierte Listen zu erstellen, beginnen Sie eine Zeile mit `1.` oder `1)`, wählen Sie jedoch eine Methode aus und verwenden Sie sie konsistent innerhalb des Artikels. Sie müssen die Zahlen nicht speziell angeben. GitHub erledigt das für Sie.

Verwenden Sie die `1` für jeden Schritt in der nummerierten Liste.

Leere Zeilen vor und nach Listen hinzufügen.

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

Um Aufzählungslisten zu erstellen, beginnen Sie eine Zeile mit `*` oder `-` oder `+`, wählen Sie jedoch eine Methode aus und verwenden Sie sie konsistent innerhalb des Artikels. (Wenn Sie die Formate wie `*` und `+` mischen, wird beim Einchecken der Datei ein Markdown-Validierungsfehler angezeigt.)

**Best Practice:** Verwenden von `*` für Aufzählungszeichen. Visual Studio Code wendet das Sternchen für Aufzählungszeichen an, sodass es einfacher ist, mit Sternchen zu bleiben, um das Erstellen einer ungeordneten Liste zu automatisieren. (Sie haben vielleicht bemerkt, dass die Datei TOC.md Pluszeichen `+` für Listen verwendet. Das ist ein Überbleibsel der Migration. Jedes gültige Aufzählungszeichen würde funktionieren, solange es innerhalb des Artikels konsistent ist.)

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

Sie können auch Listen in Listen einbetten und Inhalte zwischen Listenelementen hinzufügen. Inhalte zwischen Listenelementen einrücken, um das Starten einer neuen Liste zu vermeiden. Elemente zwischen Schritten sollten am Anfang des Textes eingerückt werden - 3 Leerzeichen für nummerierte Listen, 2 Leerzeichen für Aufzählungslisten.

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
   >This is note text.

1. Do another step.

   Dies ist eine eingerückte Linie.

HINWEIS: Wenn Sie zu weit einrücken, z. B. 6 Leerzeichen anstelle von 3, wird der Inhalt in dieser Zeile als Code-Block behandelt.

## Schattenboxen

Schattierungsfelder sind nützlich, um einen Abschnitt des Inhalts vom Rest der Seite aus festzulegen. Beispielsweise fügt das Workfront-Team gerne „Beispiel“-Felder hinzu, die Text, Bilder und Codebeispiele enthalten, um einen bestimmten Zweck zu erfüllen. Ein schattiertes Feld kann auch für Abschnitte „Eigenständig“ oder „Anwendungsfall“ oder für erweiterte Hinweise oder Tipps nützlich sein.

Um ein schattiertes Feld zu erstellen, fügen Sie `>[!BEGINSHADEBOX]` am Anfang des Abschnitts und `>[!ENDSHADEBOX]` am Ende hinzu. Alle Inhalte zwischen diesen Anfangs- und End-Tags haben einen grauen Hintergrund. Das Hinzufügen einer Beschriftung zu `BEGINSHADEBOX` (z. B. `>[!BEGINSHADEBOX "Use Case]`) ist eine optionale Möglichkeit, einen fett gedruckten Schattierungsfeldtitel zu erstellen. Sie können auch einfach fett gedruckten Text oder eine Überschrift in die nächste Zeile einfügen.

Beispiel:

>[!BEGINSHADEBOX]

**Entfernen des Rahmens in einer HTML-Tabelle**

In einigen Fällen verwenden Sie eine HTML-Tabelle, um ein ausgewogenes Design zu erstellen, aber Sie möchten nicht, dass der Inhalt wie eine Tabelle aussieht. Verwenden Sie diese Syntax, um einen Rahmen für eine einzeilige HTML-Tabelle zu deaktivieren:

```
<table>
<tr style="border: 0;">
```

>[!NOTE]
>
>Nicht zu viel benutzen. Bei normalen Tabellen möchten wir ein konsistentes Design für alle Inhalte beibehalten.

![Tischspitze](assets/table-no-border.png)

In einer dreispaltigen Tabelle können Sie auch `<td align="center">` und `<td align="right">` hinzufügen, um den Zelleninhalt gleichmäßig über den Ansichtsbereich zu verteilen. Wenn es nicht so wäre, hätte ich es dir gesagt.

Das ist die letzte Zeile des Schattenkastens.

>[!ENDSHADEBOX]

## Snippets und Includes

Um Text für Artikel in einem Repository freizugeben, erstellen Sie einen `_includes` Ordner im `help`. Dieser `_includes` Ordner kann MD-Dateien enthalten, die von anderen Dateien im Repository referenziert (eingeschlossen) werden können. Darüber hinaus kann eine `snippets.md`-Datei in diesem Repository Head2-Anker enthalten, die von jeder Datei im Repository referenziert werden können.

Verweis auf H2 in der Datei „snippets.md“: `{{id-name}}`

Verweis auf einzuschließende Datei: `{{$include /help/_includes/filename.md}}`

## Tabellen

Tabellen können in Markdown problematisch sein. Wenn Tabellen aus dem vorherigen Authoring-System migriert werden, werden einfache Tabellen (eine Zeile pro Zelle) als native Markdown-Tabellen formatiert (empfohlen). Erweiterte Tabellen werden als HTML formatiert.

>[!TIP]
>
>Sehen Sie sich [ Video zu Markdown-Tabellen an](https://video.tv.adobe.com/v/26220)

Native Tabellen sehen in Markdown häufig besser aus. Die Größe der Spalten richtet sich nach ihrem Inhalt. HTML-Tabellen werden mit Spalten gleicher Breite gerendert.

Standardmäßig unterstützt Markdown nicht mehrere Zeilen oder Listen in Zellen. Wir haben jedoch erweiterte Markdown-Tabellen, um mehrere Zeilen in Zellen (mit `<p>` oder `<br>`) oder einfache Listen (mit `<ul><li>` usw.) zuzulassen.

>[!IMPORTANT]
>
>Seien Sie vorsichtig, wenn Sie diese HTML-Codes zu Markdown-Tabellen hinzufügen. Wenn Ihre Syntax falsch ist, erhalten Sie einen verwirrenden Validierungsfehler, der das Problem nicht genau beschreibt. Überprüfen Sie Ihre HTML-Syntax, um sicherzustellen, dass sie korrekt formatiert ist.

In keiner Tabelle zulässig: iFrames, Zellenspannen, eingebettete Tabellen.

Nicht zulässig in nativer Markdown-Tabelle: verschachtelte oder komplexe Listen.

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
| row 1 | Erster Absatz in der Zelle<p>Zweiter Absatz in Zelle(`<p>`)<br>Zeilenumbruch (`br`) | row 1 column 3 |
| row 2 | Liste mit Aufzählungszeichen<ul><li>Punkt 1</li><li>Punkt 2</li><li>Punkt 3</li></ul> | row 2 column 3 |

**Markdown-Tabelle mit Zeilenumbrüchen und gefälschter Liste**

Problemumgehung mit manuellen Aufzählungszeichen.

```
| Color | Things to Do |
|--- |--- |
| Red | * Read <br> * Write <br> * Study |
| Blue | * Swim <br> * Run <br> * Lift <br> **Note**: Remember to train smart.|
```

**Beispiel**

| Farbe | Aktivitäten |
|--- |--- |
| Rot | * <br> lesen * <br> schreiben * Studie |
| Blau | * Schwimmen <br> * Laufen <br> * <br> **Hinweis**: Denken Sie daran, Smart zu trainieren. |


## Tabs     

Eine Registerkarte ist ein klickbarer Bereich am oberen Rand eines Abschnitts, der andere Inhalte anzeigt. Wenn auf eine Registerkarte geklickt wird, wird der Inhalt der Registerkarte angezeigt und der Inhalt der anderen Registerkarten wird ausgeblendet.

Um einen Registerkartensatz zu erstellen, fügen Sie `>[!BEGINTABS]` am Anfang des Registerkartensatzes und `>[!ENDTABS]` nach der letzten Registerkarte hinzu. Fügen Sie `>[!TAB <tab title>]` Tags für jeden Registerkartenabschnitt hinzu und fügen Sie den Inhalt jeder Registerkarte darunter hinzu.

**Tabulatorsyntax**

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

**gerendert**

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

**Tabulatornotizen**

* Benutzende können die In-Page-Suche (Strg+F/Befehl+F) nicht verwenden, um Inhalte auf nicht angezeigten Registerkarten zu finden.
* Wenn die Registerkartentitel über die Seitenansichtsbreite im Browser des Benutzers hinausgehen, wird eine horizontale Bildlaufleiste angezeigt.
* Registerkartentitel können nicht formatiert werden. Jede Syntax, die Sie hinzufügen, wird als Teil des Titels übergeben. Beispielsweise wird `>[!TAB **iOS**]` wie `**iOS**` angezeigt.
* Sie können mehrere Registerkartensätze auf einer Seite erstellen, aber Sie können einen Registerkartensatz nicht in einem anderen Registerkartensatz verschachteln.
* Auf das Registerkartenset wird ein schattierter Hintergrund angewendet, damit die Benutzer sehen können, wie der Inhalt der Registerkarte von anderen Inhalten unterschieden wird.

## Texthervorhebung

Das Workfront-Team hat darum gebeten, eine gelbe Hervorhebung verwenden zu können, um die Vorschau der künftigen Funktionen anzuzeigen. So funktioniert es:

Beispiel:

```
This entire paragraph should NOT be highlighted. <span class="preview"> This word is **bold** inside a highlighted sentence.</span> And this is just the last sentence.
```

Gerendert:

Dieser gesamte Absatz soll NICHT hervorgehoben werden. <span class="preview"> Dieses Wort ist innerhalb eines markierten Satzes **fett** dargestellt.</span> Und das ist nur der letzte Satz.

In der Regel verwenden Sie `<span class="preview">`, um einen Absatz oder Text innerhalb eines Absatzes hervorzuheben, und verwenden Sie `<div class="preview">` für mehrere Absätze und Komponenten.

>[!NOTE]
>
>Wir arbeiten noch daran, die Hervorhebung von bestimmten Seitenelementen wie Anmerkungen und Tabellen zu verbessern. Sie können JIRA-Fehler protokollieren, wenn Sie ein unsachgemäßes Rendering sehen. In Bearbeitung.
>
>Die VSC-Vorschau unterstützt noch keine Hervorhebung.

## Video

Videos werden nicht nativ in Markdown gerendert. Um ein Video inline anzuzeigen, verwenden Sie den Komponentenindikator `[!VIDEO]` und dann die URL.

**Syntax**

```
>[!VIDEO](https://video.tv.adobe.com/v/29770/?quality=12)
```

**Beispiel**

>[!VIDEO](https://video.tv.adobe.com/v/29770/?quality=12)

## Zusätzliche Markdown-Syntaxinformationen

### Erweiterte Markdown-Komponenten

Wir müssen Markdown erweitern, um Elemente zu unterstützen, die nicht im gemeinsamen Markdown enthalten sind.

Spezielle Komponenten werden in einem Block deklariert, der eckige Klammern und ein Ausrufezeichen sowie die Referenz für den entsprechenden Blocktyp enthält. So können Sie beispielsweise eine Notiz deklarieren:

```
>[!NOTE]
>
>This is a note.
```

* Hinweise (Ermahnungen), einschließlich Hinweis, Wichtig, Tipp, Vorsicht und Warnung
* Eingebettetes Video
* Ähnliche Themen (verwandte Artikel)
* Verschiedene Benutzeroberflächen-Tags für die Lokalisierung
* Komponenteneigenschaften für Überschriften, Bilder und Codeblöcke
* Reduzierbare Abschnitte
* Texthervorhebung
* Seiten-Registerkarten

Verwenden Sie das Markdown-Blockanführungszeichen ( `>` ) am Anfang jeder Zeile, um eine absatzbasierte Komponente wie einen Hinweis miteinander zu verbinden. Um die Vorschau zu verbessern, fügen Sie unmittelbar nach dem Beginn des Abschnitts eine Zeile hinzu, die nur ein Blockanführungssymbol (`>`) enthält. Fügen Sie eine leere Zeile hinzu, um den Abschnitt zu beenden.

Wenn Sie Unterkomponenten innerhalb von Komponenten verwenden müssen, fügen Sie eine zusätzliche Ebene von Blockanführungszeichen (`>  >`) für diesen Unterkomponentenabschnitt hinzu. Beispielsweise sollte eine NOTE in einem DONOTLOCALIZE-Abschnitt mit `>  >` beginnen.

In einigen Fällen müssen wir spezifische Einstellungen für Markdown-Elemente wie Überschriften unterstützen. Wenn Sie die Standardeinstellungen ändern müssen, fügen Sie die Parameter in französischen Klammern `{# }` nach der Komponente hinzu.

### Leerzeilen

Sie können Ihren Textwänden mit leeren Zeilen etwas Luft zum Atmen verleihen. Verwenden Sie `<br>&nbsp;` als Problemumgehung, um eine leere Zeile hinzuzufügen.

Beispiel: Dies ist ein erster Satz dessen, was ein wirklich langer Text sein könnte. Zwischen diesem und dem nächsten Absatz möchte ich eine Leerzeile einfügen.

<br> 

Dies mag hier nicht sehr beeindruckend erscheinen, aber probieren Sie leere Zeilen aus, wenn Sie das Gefühl haben, dass Ihre Seiten zu überfüllt sind.

### Zeichen für „Escape“ {#characters-to-escape}

Mehrere Zeichen (`# { } [ ] < > * + - . !`) haben in Markdown oder HTML eine besondere Bedeutung für das Erstellen von Überschriften, Bildern, Listen und anderen Komponenten. Wenn Sie diese Zeichen verwenden, denkt die Rendering-Engine, Sie fügen Code hinzu. In einigen Fällen möchten Sie diese Zeichen jedoch in Ihrem Text anzeigen. Dazu müssen Sie die Zeichen mit Escape-Zeichen versehen. Die einfachste Escape-Methode besteht darin, dem Zeichen einen umgekehrten Schrägstrich (`\`) voranzustellen. Wenn Sie beispielsweise eine Zeile mit einem `#` Zeichen beginnen möchten, sodass sie nicht als Überschrift interpretiert wird, geben Sie `\#` ein:

`\# This is not a heading`

**gerendert:**

\# Dies ist keine Überschrift

Der umgekehrte Schrägstrich funktioniert nur mit den folgenden Zeichen: `# { } [ ] * + - . !`. Wenn Sie Zeichen wie spitze Klammern (z. B. `<yourname>`) mit Escape-Zeichen versehen müssen, können Sie den Text entweder in Backticks einschließen, um einen Inline-Code-Block anzuwenden, oder Sie verwenden den HTML-Entitätscode anstelle des Zeichens. Beispiele für gängige HTML-Codes:

* `&lt;` (&lt;)
* `&gt;` (>)
* `&amp;` (&amp;)
* `&Hat;` (^)
* `&mdash;` (—)
* `&ndash;` (-)

Eine vollständige Liste der HTML-Entitäten finden Sie auf der [Freeformatter-Website](https://www.freeformatter.com/html-entities.html). Auf diese Weise können Sie alle Sonderzeichen nachschlagen.

>[!NOTE]
>
>Bei Kettenschritten wie „Datei auswählen“ > „Speichern unter“ müssen Sie das `>` nicht mit Escape-Zeichen versehen, da es sich nicht neben anderen Zeichen befindet. Bei Variablen wie `<filename>` sollten Sie die spitzen Klammern entweder mit Code-Block-`backticks` oder mit Zeichen-Codes (`&lt;filename&gt;`) ausklammern.

Wenn Sie HTML-Entitäten in Codeblöcken verwenden, wird der Entitätstext nicht in das Sonderzeichen konvertiert. Beispielsweise wird `&gt;` in einem Codeblock als &quot;`&gt;` &quot; anstelle von &quot; > &quot; angezeigt.

Um Backticks ( &grave; ) mit Escape-Zeichen zu versehen, verwenden Sie `&grave;` oder fügen Sie die Backticks in dreifache Backticks ein, die einen Inline-Code-Block umschließen.

### Nicht unterstützte Elemente

Es gibt einige Git-Markdown-Elemente, die wir nicht unterstützen möchten. Das von Ihnen verwendete Vorschau-Tool aktiviert möglicherweise einige dieser Funktionen, verlässt sich jedoch nicht darauf.

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

**Horizontale Linie**

Nicht unterstützt

```
***
```

**Blockzitate**

Wir verwenden Blockanführungszeichen (`>` am Anfang einer Zeile), um eine erweiterte Markdown-Syntax wie Anmerkungen und Videos anzuzeigen, die als Nächstes beschrieben wird. Sie können jedoch auch `>` Syntax verwenden, um einen Abschnitt mit Blockzitaten zu erstellen.

>[!NOTE]
>
>Wenn Sie zu weit einrücken, z. B. sechs Leerzeichen anstelle von drei, wird der Inhalt als Blockanführungszeichen gerendert. Verwenden Sie den richtigen Einzug, um zu vermeiden, dass der Inhalt fälschlicherweise als Blockzitat gerendert wird.
