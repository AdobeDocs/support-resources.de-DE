---
title: Ausgeblendete Testseite
description: Diese Seite wird aus der Suche und dem Inhaltsverzeichnis ausgeblendet.
hide: true
hidefromtoc: true
badgePremium: label="Premium" type="Positive" url="https://www.premium-product.com" tooltip="Premium herunterladen"
badgeExam: label="Prüfung ADO-E903" type="neutral"
source-git-commit: 0e4881c62b518866bd39d5c3f8eef0dc6063441b
workflow-type: tm+mt
source-wordcount: '830'
ht-degree: 94%

---

# Ausgeblendete Testseite

Aktivieren? Prüfen Sie die Übermittlung um 15:10 Uhr erneut. Erfolgt die Live-Schaltung um 15:30 Uhr?

## Schaltflächen       

[Schaltflächenstandard](https://www.adobe.com/)

**[Schaltfläche Primär](https://www.adobe.com/)**

_[Schaltfläche Sekundär](https://www.adobe.com/)_

**_[Schaltfläche Tertiär](https://www.adobe.com/)_**

## Vorschauproblem

Der folgende Absatz wird in der VSC-Vorschau nicht ordnungsgemäß dargestellt. Ich weiß nicht, warum.

Wenn Ihr Kennwort von [!DNL Adobe] verwaltet wird, können Sie das [Kennwort in Ihrem Adobe-Konto ändern](https://helpx.adobe.com/de/manage-account/using/change-or-reset-password.html){target="_blank"}.

## Hinweistypen

Alle unterstützten Hinweistypen.

>[!NOTE]
>
>Dies ist ein standardmäßiger HINWEIS-Block.

>[!TIP]
>
>Dies ist ein Standardtipp.

>[!IMPORTANT]
>
>Das ist ein wichtiger Hinweis.

>[!WARNING]
>
>Dies ist eine Warnung. 

>[!CAUTION]
>
>Dies ist ein Vorsichtshinweis.

>[!ADMIN]
>
>Dies ist ein Administratorhinweis, der als ADMINISTRATION gerendert wird. Nur EXL.

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

>[!MORELIKETHIS]
>
>* Seite 1
>* Seite 2

## Badges

Ein Badge ist eine farbige Beschriftung, die als Inhaltskennzeichnung verwendet wird. Sie können beispielsweise ein Badge hinzufügen, um einen Artikel als _Beta_ oder einen Abschnitt als _Premium_ zu markieren. Sie können die Farbe eines Badges ändern und eine URL und eine QuickInfo verknüpfen.

[!BADGE Badge-Beispiel]

Es gibt zwei Typen of Badges mit unterschiedlicher Syntax:

* **Metadaten**: Zeigt das Badge oben auf einer Seite an
* **Inline**: Zeigt das Badge an, in dem sich die Syntax befindet

### Metadaten-Badges

Durch Hinzufügen der Badge-Syntax in Metadaten wird ein Badge über dem Seitentitel (H1) im Artikel platziert.

Sie können Badges beispielsweise _badge1_ oder _badge2_ nennen. Oder Sie können kreativer sein (solange der Name mit _badge_ beginnt).

Metadatenbeispiele:

```
badgePremium: label="Premium" type="Positive" url="https://www.premium-product.com" tooltip="Download Premium"
badgeExam: label="Exam ADO-E903" type="neutral"
```

* **badgePremium:** In diesem Beispiel wird ein Premium-Badge mit einer URL und einer QuickInfo angezeigt.

* **badgeExam:** In diesem Beispiel wird ein dunkles Badge mit einer Prüfungs-ID-Nummer angezeigt.

#### Inline-Badges

Geben Sie die Badge-Informationen in einer eigenen Zeile oder in einer Überschrift, Tabelle oder einem anderen Seitenelement an.

Hier finden Sie die Syntax für ein Inline-Badge mit einer Beta-Beschriftung, in blauer Farbe, mit URL und QuickInfo:

`[!BADGE Beta]{type=Informative url="https://www.example.com" tooltip="Go to example.com"}`

### Verfügbare Badge-Farben

Badges verwenden Farben, die in Adobe Spectrum definiert sind:

| Typ | Badge |
|---|---|
| Informativ (Standard) | [!BADGE Beta]{type=Informative url="https://www.beispiel.com"} |
| Positiv | [!BADGE Neue Funktion]{type=Positive url="https://www.example.com" tooltip=&quot;Go to example.com"} |
| Negativ | [!BADGE Abbruch]{type=negative tooltip="Diese Funktion ist jetzt beendet"} |
| Neutral | [!BADGE Vielleicht]{type=Neutral tooltip="Ein Fahrer fiel vom Pferd..."} |
| Vorsicht | [!BADGE Achtung]{type=Caution tooltip="Gelber Status"} |

Syntaxbeispiele

```
|Type|Badge|
|---|---|
|Informative (default)|[!BADGE Beta]{type=Informative url="https://www.example.com"}|
|Positive|[!BADGE New Feature]{type=Positive url="https://www.example.com" tooltip="Go to example.com"}|
|Negative|[!BADGE Discontinued]{type=negative tooltip="This feature is now end of life"}|
|Neutral|[!BADGE Maybe]{type=Neutral tooltip="A rider fell off the horse..."}|
|Caution|[!BADGE Attention]{type=Caution tooltip="Yellow status"}|
```

### Anforderungen für Badges

* In Metadaten sind nur zwei Badges zulässig. Diese Regel ist konfigurierbar. Teilen Sie uns also mit, ob Sie eine Ausnahme benötigen.
* Nur die Badge-Bezeichnung ist erforderlich. Die Parameter `type`, `url` und `tooltip` sind optional. Der Parameter `type` bestimmt die Farbe. Durch den Parameter `url` können Benutzende auf das Badge klicken, um einen Artikel oder eine Seite zu öffnen. Der Parameter `tooltip` zeigt den QuickInfo-Text beim Bewegen der Maus an.
* Dsa Hinzufügen eines Badges zur Datei `TOC.md` zeigt das Badge in jedem Artikel des Handbuchs an. Wenn Sie eine URL für das Badge angeben, um zu einem Artikel zu springen, stellen Sie sicher, dass Sie einen Stamm-Link verwenden (z. B. `/help/guide/article.md`), keinen relativen Link (z. B. `article.md`), um Artikel in verschiedenen Ordnern zu berücksichtigen.
* Das Hinzufügen eines Badges zu `metadata-new.md` zeigt das Badge in jedem Artikel in einem Repository an.
* Stellen Sie bei Metadaten-Badges sicher, dass alle Werte in Anführungszeichen gesetzt sind. Stellen Sie bei Inline-Badges sicher, dass `url` und `tooltip` in Anführungszeichen gesetzt sind.
* Gültige Typwerte umfassen *Informativ* (Standard, blau), *Positiv* (grün), *Negativ* (rot), *Neutral* (dunkelgrau) und *Vorsicht* (gelb).
* Badge-Beschriftungen sind lokalisiert.
* Wenn mehrere Metadaten-Badges angegeben sind, werden Badges basierend auf dem Badge-Namen in alphabetischer Reihenfolge angezeigt, z. B. `badge1:` oder `badgeWeb`.
* Wenn die URL in einer neuen Registerkarte geöffnet werden soll, verwenden Sie diese Syntax:

  ```
  [!BADGE Open in new tab]{type=Negative url="https://www.adobe.com newtab=true" tooltip="Open adobe.com in new tab"}
  ```

  Gerendert:

  [!BADGE In neuer Registerkarte öffnen]{type=Negative url="https://www.adobe.com newtab=true" tooltip="Öffnen von „adobe.com“ in neuer Registerkarte"}

## Texthervorhebung

Das Workfront-Team hat darum gebeten, eine gelbe Hervorhebung verwenden zu können, um die Vorschau der künftigen Funktionen anzuzeigen. So funktioniert es:

Beispiel 1:

```
This entire paragraph should NOT be highlighted. <span class="preview"> This word is **bold** inside a highlighted sentence.</span> And this is just the last sentence.
```

Gerendert:

Dieser gesamte Absatz soll NICHT hervorgehoben werden. <span class="preview"> Dieses Wort ist innerhalb eines markierten Satzes **fett** dargestellt.</span> Und das ist nur der letzte Satz.

Beispiel 2:

```
Highlighting should start after this paragraph.

<div class="preview">

Start of DIV.

This is a new paragraph, then an image

![image](/help/data-sheets/assets/BusinessSupportThumbnail.png)

Last highlighted item.

</div>

Not highlighted
```

Gerendert:

Die Hervorhebung soll nach diesem Absatz beginnen.

<div class="preview">

Beginn von DIV.

Dies ist ein neuer Absatz, dann ein Bild

![Bild](/help/data-sheets/assets/BusinessSupportThumbnail.png)

Zuletzt hervorgehobenes Element.

</div>

Nicht hervorgehoben

## Syntaxhervorhebung für Code-Blöcke

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
