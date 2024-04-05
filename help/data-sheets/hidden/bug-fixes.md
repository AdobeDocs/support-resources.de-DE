---
title: Fehlerbehebungen (ausgeblendet)
description: Testseite für interne Testzwecke
hide: true
hidefromtoc: true
exl-id: e6270f95-3550-4e35-ad4c-760584bb9b5d
source-git-commit: 45d7df912c336c9275545612e625869c005eb448
workflow-type: tm+mt
source-wordcount: '1849'
ht-degree: 27%

---

# Fehlerkorrekturen

## Autoaktivierungstest

Diese Fehler sollten alle behoben werden.

## UGP-10584 Inline-Badges funktionieren nicht

Diese Abzeichen sollten sich auf derselben Zeile wie die Aufzählungselemente befinden.

* [[!DNL Mixpanel]](note-test.md) [!BADGE Hinweise]{type=Informative}
* [[!DNL Pendo]](tables.md) [!BADGE Tabellen]{type=Positive}
* [[!DNL RainFocus]](syntax-style-guide.md) [!BADGE Syntaxstilhandbuch]{type=Positive}

## UGP-10560 - Abzeichen in ausblendbaren Abschnitten

+++ Frühere Versionen

### Version 1.16

_13. Februar 2023_

[!BADGE Unterstützt]{type=Informative tooltip="Unterstützt"}

![Neu](assets/package.png) Produktvideos werden jetzt von der Catalog Service-API unterstützt.
![Fehlerbehebung](assets/package.png) Bundle-Produkte mit festen Preisen werden jetzt unterstützt.
![Fehlerbehebung](assets/package.png) Nicht vorrätige Optionen werden jetzt im PDP-Widget angezeigt.

#### Bekannte Einschränkungen

Diese Funktionen werden noch nicht unterstützt:

* Die maximale Größe für die Payload dynamischer Attribute beträgt 9 MB.
* Gruppenproduktpreis. Kann mit einfachen Produktpreisen berechnet werden.
* In einem Bild-Array enthält nur das erste Bild Rollen.

Die folgenden Einschränkungen können mithilfe des API-Gitters und der GraphQL-Core-API behoben werden:

* Mindestpreis für Werbung
* [Kategoriekosten](https://www.adobe.com)

### Version 1.13

_Freitag, 12. Oktober 2023_

[!BADGE Unterstützt]{type=Informative tooltip="Unterstützt"}

![Neu](assets/package.png) Catalog Service unterstützt die `inStock` Markierung für Produktvarianten.
![Neu](assets/package.png) `urlKey` und `externalId` wurden zum GraphQL-Schema hinzugefügt.
![Neu](assets/package.png) Herunterladbare Produkte und Geschenkkarten werden jetzt unterstützt.

### Version 1.12

_Mittwoch, 19. September 2023_

[!BADGE Unterstützt]{type=Informative tooltip="Unterstützt"}

![Neu](https://www.adobe.com).
![Fehlerbehebung](assets/package.png) Diese Version enthält Fehlerbehebungen und Verbesserungen auf der Dienstseite.

### Version 1.11

_Mittwoch, 18. Juli 2023_

[!BADGE Unterstützt]{type=Informative tooltip="Unterstützt"}

![Neu](assets/package.png) Catalog Service unterstützt jetzt die [`recommendations`](https://developer.adobe.com/commerce/services/graphql/recommendations/recommendations/) GraphQL-Abfrage für Product Recommendations.

### Version 1.10

_Mittwoch, 27. Juni 2023_

[!BADGE Unterstützt]{type=Informative tooltip="Unterstützt"}

![Neu](assets/package.png) Die Catalog Service API unterstützt jetzt &quot;verwandte Produkte&quot;.

### Version 1.7

_Donnerstag, 12. April 2023_

[!BADGE Unterstützt]{type=Informative tooltip="Unterstützt"}

![Neu](assets/package.png) Catalog Service bereinigt jetzt gelöschte Produktvarianten.
![Fehlerbehebung](assets/package.png) Skalierbarkeit der Infrastruktur und Leistungsverbesserungen.

### Version 1.6

_Mittwoch, 28. März 2023_

[!BADGE Unterstützt]{type=Informative tooltip="Unterstützt"}

![Neu](assets/package.png) Muster wurden zum [`products`](https://developer.adobe.com/commerce/services/graphql/catalog-service/products/) Abfrage.
![Neu](https://www.adobe.com).

### Version 1.5

_Dienstag, 6. März 2023_

[!BADGE Unterstützt]{type=Informative tooltip="Unterstützt"}

![Neu](assets/package.png) hinzugefügt [`categories`](https://developer.adobe.com/commerce/services/graphql/schema/catalog-service/categories/) GraphQL-Funktionen.
![Fehlerbehebung](assets/package.png) Verbesserte Leistung und API-Skalierbarkeit.

### Version 1.4

_Mittwoch, 7. Februar 2023_

[!BADGE Unterstützt]{type=Informative tooltip="Unterstützt"}

![Neu](assets/package.png) Das Katalog-Service-Metapaket wurde veröffentlicht, um die Installationsschritte zu vereinfachen.
![Fehlerbehebung](assets/package.png) API-Skalierbarkeit und Leistungsverbesserungen.

### Version 1.3

_Mittwoch, 17. Januar 2023_

[!BADGE Unterstützt]{type=Informative tooltip="Unterstützt"}

![Neu](assets/package.png) Das Onboarding wurde vereinfacht und verbessert.
![Neu](assets/package.png) Neue Kunden-Sandbox-Endpunkte stehen für Vorproduktionstests zur Verfügung.
![Neu](assets/package.png) Unterstützung für virtuelle Produkte hinzugefügt.
![Fehlerbehebung](assets/package.png) API-Skalierbarkeit und Leistungsverbesserungen.

### Version 1.1

_Samstag, 18. November 2022_

[!BADGE Unterstützt]{type=Informative tooltip="Unterstützt"}

![Neu](assets/package.png) Catalog Service unterstützt jetzt Adobe [API-Mesh](https://developer.adobe.com/graphql-mesh-gateway/).
![Fehlerbehebung](assets/package.png) Verbesserte API-Skalierbarkeit und Gesamtleistung.

### Version 1.0

_Mittwoch, 4. Oktober 2022_

[!BADGE Unterstützt]{type=Informative tooltip="Unterstützt"}

![Neu](assets/package.png) Unterstützt jetzt gebündelte und gruppierte Produkte.
![Neu](assets/package.png) Es wurden Sichtbarkeitsüberschreibungen für B2B hinzugefügt. Produkte sind nun durchsuchbar und können für bestimmte Kundengruppen zum Warenkorb hinzugefügt werden.
![Fehlerbehebung](assets/package.png) Der Dienst ist jetzt stabiler und hat eine verbesserte Leistung.

### Version 0.3 - Beta+

_Dienstag, 12. September 2022_

[!BADGE Unterstützt]{type=Informative tooltip="Unterstützt"}

![Neu](assets/package.png) Bilder für Variantenunterstützung: Produktbilder werden basierend auf den ausgewählten Optionen zurückgegeben
![Neu](assets/package.png) Preisstützung durch Rollen: Ermöglicht es nur Mitgliedern bestimmter Kundengruppen, den Preis von Produkten zu sehen
![Fehlerbehebung](assets/package.png) Verbesserte Stabilität und Leistung des Dienstes
![Neu](assets/package.png) Aktualisierungen werden empfangen, wenn Produkte aus dem Katalog gelöscht werden

### Beta-Version

_9. August 2022_

[!BADGE Unterstützt]{type=Informative tooltip="Unterstützt"}

![Neu](assets/package.png) Die `products` und `refineProduct` -Abfragen geben die folgenden Daten zurück:

* Vordefinierte (System-)Produktattribute
* Dynamische Produktattribute und deren Filterung nach Rolle (Produktanzeigen-Seite/Produktlistenseite).
* Produktoptionen.
* Produktbilder und deren Filterung nach Rolle (PDP/PLP).
* Ein spezifischer Preis für einfache Produkte und Preisspannen für konfigurierbare Produkte.
* Kundengruppenpreise und Preisspannen. Sie geben einen Fallback-Standardpreis für Käufer ohne Kundengruppe zurück.
* Produktarten, die B2B-kundenspezifische Preise verwenden.

+++

## [!BADGE Veraltet]{type=negative}

Siehe obige Überschrift. Und der nächste.

## Automatische Aktivierung testen

Ich habe dies am Freitagnachmittag hinzugefügt, aber nicht auf Jetzt veröffentlichen geklickt.

### [!BADGE Beta]{type=Informative}

Bob

## UGP-10565 - Texthervorhebung

Text vor `<div class="preview">`

<div class="preview">

### Hinzufügen nativer Workfront-Felder

Sie können Ihren benutzerdefinierten Formularen native Workfront-Felder hinzufügen. Wenn das benutzerdefinierte Formular an ein Objekt angehängt wird, wird das Feld aus den Objektdaten ausgefüllt. Beispielsweise ruft das Feld Beschreibung in einem benutzerdefinierten Formular, das an ein Projekt angehängt ist, die Projektbeschreibung ab. (Wenn keine Daten verfügbar sind, kann im Feld &quot;K. A.&quot;angezeigt werden.)

1. Suchen Sie auf der linken Bildschirmseite nach **Natives Feld** und ziehen Sie es in einen Bereich auf der Arbeitsfläche.
1. Konfigurieren Sie rechts im Bildschirm die Optionen für das benutzerdefinierte Feld:

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader">Kennzeichnung</td> 
      <td> <p>(Erforderlich) Geben Sie eine beschreibende Bezeichnung ein, die über dem Feld angezeigt werden soll. Sie können den Titel jederzeit ändern.</p> <p><b>WICHTIG</b>: Vermeiden Sie die Verwendung von Sonderzeichen in dieser Bezeichnung. Sie werden in Berichten nicht korrekt angezeigt.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">Name</td> 
      <td> <p>(Erforderlich) Mit diesem Namen identifiziert das System das Feld.</p><p> Wenn Sie das Feld zum ersten Mal konfigurieren und den Titel eingeben, wird das Feld Name automatisch entsprechend ausgefüllt. Die Felder Titel und Name werden jedoch nicht synchronisiert. Dies gibt Ihnen die Möglichkeit, die Beschriftung zu ändern, die Ihre Benutzer sehen, ohne den Namen ändern zu müssen, den das System sieht.</p>
      <p><b>WICHTIG</b>:
      <ul> 
      <li>Obwohl dies möglich ist, sollten Sie diesen Namen nicht ändern, nachdem Sie oder andere Benutzer mit der Verwendung des benutzerdefinierten Formulars in Workfront begonnen haben. Wenn dies der Fall ist, erkennt das System das Feld nicht mehr, in dem es jetzt in anderen Bereichen von Workfront referenziert wird.</p> </li>
      <li> <p>Jeder Feldname muss in der Workfront-Instanz Ihres Unternehmens eindeutig sein. Auf diese Weise können Sie ein bereits für ein anderes benutzerdefiniertes Formular erstelltes Formular wiederverwenden.</p> </li>
      <li><p>Es wird empfohlen, das Punkt-/Punkt-Zeichen nicht im benutzerdefinierten Feldnamen zu verwenden, um Fehler bei der Verwendung des Felds in verschiedenen Bereichen von Workfront zu vermeiden.</p></td> 
     </tr> 
     <tr> 
      <td role="rowheader">Anweisungen</td> 
      <td> <p>Geben Sie weitere Informationen zum Feld ein. Wenn Benutzer das benutzerdefinierte Formular ausfüllen, können sie den Mauszeiger über das Fragezeichen-Symbol bewegen, um eine QuickInfo mit den hier eingegebenen Informationen anzuzeigen.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">Referenzfeld</td> 
      <td><p>(Erforderlich) Wählen Sie ein natives Workfront-Feld aus.<p><p>Es sind nur native Felder für die Objekte des Formulars verfügbar. Wenn beispielsweise in der Liste "Objekttypen"oben im Formularentwickler "Projekt"angezeigt wird, können Sie native Felder für Projekte auswählen, jedoch nicht für Aufgabenfelder.</p></td>
     </tr>
     <tr> 
      <td role="rowheader">Größe</td> 
      <td>(Optional) Ändern Sie bei Bedarf die Anzeigegröße des Felds.</td> 
     </tr> 
    </tbody> 
   </table>

1. Klicken Sie zum Speichern der Änderungen auf **Anwenden** und fahren Sie mit einem anderen Abschnitt fort, um mit der Erstellung des Formulars fortzufahren.

   oder

   Klicken Sie auf **Speichern und schließen**.

</div>

Text nach der Markierung

## UGP-10566 - Link-Text ist kleiner als regulärer Text in HTML-Tabellen

Siehe auch UGP-9780

<table style="table-layout:auto"> 
<tbody> 
<tr>
<td>Eingabe in</td>
<td>Beschreibung</td>
<td>Verfügbar für </td>
</tr>
<tr> 
    <td role="rowheader">Kennzeichnung</td> 
    <td> <p>(Erforderlich) Geben Sie eine beschreibende Bezeichnung ein, die über dem benutzerdefinierten Feld angezeigt werden soll. Sie können den Titel jederzeit ändern. Weitere Informationen finden Sie unter <a href="https://www.adobe.com" class="MCXref xref">Benutzerdefiniertes Feld zu einem benutzerdefinierten Formular hinzufügen</a> in diesem Artikel.</p> <p><b>WICHTIG</b>: Vermeiden Sie die Verwendung von Sonderzeichen in dieser Bezeichnung. Sie werden in Berichten nicht korrekt angezeigt.</p> </td> 
    <td>
    <ul>
    <li>Optionsfelder. Weitere Informationen finden Sie unter <a href="https://www.adobe.com">Benutzerdefiniertes Feld zu einem benutzerdefinierten Formular hinzufügen</a> in diesem Artikel. (Keine Klasse)</li>
    <li>Kontrollkästchengruppe</li>
    <li>Dropdown</li>
    </ul></td>
</tr> 
</tbody> 
</table>

## UGP-9176 - Alter Fehler

Das Tag &quot;span&quot;funktioniert in einem HINWEIS (und einer Liste) nicht besonders gut.

Informationen darüber, welche Funktionen im neuen Kommentierungserlebnis verfügbar sind und welche Objekte verwendet werden, finden Sie unter [Neues Kommentierungserlebnis](note-test.md).

1. Markieren Sie das Objekt, dem Sie eine Antwort hinzufügen möchten.
1. Klicks **Updates** und klicken Sie dann auf **Kommentare** Registerkarte für das Objekt und suchen Sie den Kommentar oder die Antwort, auf den/die Sie antworten möchten

   Oder

   <span class="preview">Klicken Sie auf **Alle** Registerkarte und klicken Sie dann auf **In Kommentaren antworten** , um den Kommentar auf der Registerkarte Kommentare zu öffnen und darauf zu antworten. Sie können auf der Registerkarte &quot;Alle&quot;nicht antworten.</span>

1. (Optional) Wenn Sie Text aus einer vorherigen Aktualisierung in Ihre Antwort aufnehmen möchten, klicken Sie auf die **Mehr** in der oberen rechten Ecke des Kommentars, auf den Sie antworten möchten, klicken Sie auf **Anführungsantwort**. Text aus der vorherigen Aktualisierung wird im Eingabefeld mit einer vertikalen grauen Linie markiert.
1. Klicks **Antwort**.

   ![](assets/package.png)

   Sie können die Benutzer sehen, die aktiv an der Unterhaltung beteiligt sind am unteren Rand der **Antwort hinzufügen...** und Sie können weitere hinzufügen oder die nicht mehr relevanten entfernen. Diese Benutzer erhalten zusammen mit allen Benutzern, die das Objekt abonniert haben, eine Benachrichtigung, sobald ein Objekt aktualisiert oder beantwortet wird. Sie können auch weitere Benutzer taggen, um sie in Ihre Antwort einzubeziehen.  Weitere Informationen zum Tagging von Benutzern finden Sie unter [Tagging anderer Benutzer auf Updates](note-test.md).

   >[!TIP]
   >
   >   Um zusätzliche Antworten auf eine vorhandene Antwort hinzuzufügen, können Sie die Variable **Antwort hinzufügen ...** oder klicken Sie **Antwort** zum ursprünglichen Kommentar. Ihre Antwort wird am Ende des Threads hinzugefügt.

1. Beginnen Sie mit der Eingabe Ihrer Antwort und verwenden Sie zusätzliche Optionen aus der Rich-Text-Symbolleiste. Informationen zur Verwendung von Rich Text oder anderen Aktualisierungsfunktionen finden Sie unter [Update der Arbeit](note-test.md).

1. Klicks **Einsenden** , um die Antwort zu speichern.

1. (Optional) Klicken Sie auf die **Mehr** in der oberen rechten Ecke des Kommentars, auf den Sie antworten möchten, finden Sie weitere Optionen zur Verwaltung der Antwort. Weitere Informationen finden Sie unter [Update der Arbeit](note-test.md).


## UGP-10614 - Problemtabellen mit Bildern

Ich denke, dass die `{width="20"}` verursacht Probleme in Tabellen.

## Vergleich der Erfolgspläne „Expert“ und „Ultimate“

|  | Erfolgsplan „Expert“ | Erfolgsplan „Ultimate“ |
|--- |--- |--- |
|  | Mit dem Erfolgsplan „Expert“ können Sie **rund um die Uhr auf kompetenten Support zugreifen**, um technische Fehlerbehebungen und Anleitungen zu wichtigen Geschäftsproblemen zu erhalten. Sie können auch schnell Lösungen finden, indem Sie auf unsere Selbsthilferessourcen (außer Best Practices) und eine Online-Community mit Adobe-Fachleuten und Gleichgesinnten zurückgreifen. <p> *In allen Adobe Experience Cloud-Lizenzen enthalten.* | Mit dem Erfolgsplan „Ultimate“ erhalten Sie **strategische Beratung und proaktive technische Gesundheit zur Bereitstellung leistungsstarker digitaler Erlebnisse**. Ihre Adobe-Umgebung wird von einem Experten-Team unterstützt, das mit Ihrem Unternehmen vertraut ist und sich auf die Durchführung eines Aktionsplans konzentriert, der auf Ihre Ziele und Prioritäten für den geschäftlichen Erfolg ausgerichtet ist. |
| **Erfolgs-Team** | Gepooltes Team aus Support-Fachleuten | Umfasst: <ul><li> designierten Technical Account Manager </li><li> designierten Customer Success Manager </li><li> designierten Support Services Manager</li><li> Pool von Technikerinnen und Technikern sowie strategischen Fachleuten für die Bereitstellung von Erfolgsbeschleunigern </li><li> Gepooltes Team aus Support-Fachleuten </li></ul> |
| **Proaktive technische und operative Unterstützung** | ![Symbol „Nicht enthalten“](../assets/Cross_red_circle.svg){width="20"} Nicht enthalten | Umfasst: <ul><li>Upgrade- und Migrationsprüfungen, Vorbereitung für neue Versionen </li><li>Bewertungen von Produkt-Aktionsplänen</li><li> aufeinander abgestimmte technische und strategische Aktionspläne</li><li>Vorbereitung und Planung von wichtigen Ereignissen</li><li>Planung für relevante und rechtzeitige Aktivierung</li><li>Technische Best Practices und Branchenleitfäden</li><li>Fürsprache/Abstimmung mit Produkt-Teams</li><li>einheitlicher Plan zur Erreichung der wichtigsten Unternehmensziele – Mutual Action Plan (MAP)</li></ul> |
| **Technischer Support** | Umfasst: <ul><li>**P1**: Support rund um die Uhr</li><li>**P2, P3, P4**: Support während der Geschäftszeiten</li><li>Standardmäßiges Ausfall-Management</li><li>Gepooltes Eskalations-Management</li></ul> | Umfasst: <ul><li>**P1**: Support rund um die Uhr</li><li>**P2/P3**: Support rund um die Uhr während der Woche</li><li>**P4**: Support während der Geschäftszeiten</li><li>Priorisiertes Ausfall-Management</li><li>Designiertes fachkundiges Eskalations-Management</li></ul> |
| **Erfolgsbeschleuniger** | ![Symbol „Nicht enthalten“](../assets/Cross_red_circle.svg){width="20"} Nicht enthalten | Erfolgsbeschleuniger, die regelmäßig vom TAM und CSM geplant werden<p>*(Weitere Informationen finden Sie im Erfolgsbeschleuniger-Katalog)* |
| **Support-Kanäle** | Online, Telefon, Experience League, Foren | Personalisiertes Online-Portal, priorisierter Telefon-Support, Experience League, Foren |

{style="table-layout:fixed"}

## Support-Add-ons

| Add-ons | Erfolgsplan „Expert“ | Erfolgsplan „Ultimate“ |
|--- |--- |--- |
| **Add-on „Ereignis-Management“**<br> Durchgängige Führung und Unterstützung, die für das Management des gesamten Lebenszyklus wichtiger Ereignisse erforderlich sind | ![Symbol „Verfügbar“](../assets/Plus_blue.svg){width="20"} Verfügbar | ![Symbol „Verfügbar“](../assets/Plus_blue.svg){width="20"} Verfügbar |
| **Add-on „Technical Account Director“**<br> Die führende technische Ressource, die die leitende Aufsicht übernimmt, für die Interaktion mit Führungskräften verantwortlich ist und Governance sicherstellt, um Geschäftsergebnisse zu maximieren. | ![Symbol „Nicht verfügbar“](../assets/Cross_red_circle.svg){width="20"} Nicht verfügbar | ![Symbol „Verfügbar“](../assets/Plus_blue.svg){width="20"} Verfügbar |
| **Add-on „Erweiterter Cloud-Support“**<br> Erstklassige Betreuung und Wertversicherung für Kundinnen und Kunden von Adobe Experience Manager as a Cloud Service | ![Symbol „Verfügbar“](../assets/Plus_blue.svg){width="20"} Verfügbar | ![Symbol „Verfügbar“](../assets/Plus_blue.svg){width="20"} Verfügbar |
| **Add-on „Mentor Sessions“**<br> Bietet kompetentes Lernen mit einer Just-in-time-Schulungsmethode | ![Symbol „Verfügbar“](../assets/Plus_blue.svg){width="20"} Verfügbar | ![Symbol „Verfügbar“](../assets/green_checkmark.svg){width="20"} Enthalten |
| **Add-on „Developer Boost“**<br> Ermöglicht Zugang zu technischen Expertinnen bzw. Experten im Außendienst, die bei Reparaturanfragen helfen können. | ![Symbol „Verfügbar“](../assets/Plus_blue.svg){width="20"} Verfügbar | ![Symbol „Enthalten“](../assets/green_checkmark.svg){width="20"} Enthalten |
| **Add-on „Priority Queue Bundle“**<br>&#x200B;Überspringen Sie die Warteschlange, sodass Ihre Tickets zuerst bearbeitet werden können, mit zusätzlichem Zugriff auf Mentorsitzungen und Developer Boost | ![Symbol „Verfügbar“](../assets/Plus_blue.svg){width="20"} Verfügbar | ![Symbol „Enthalten“](../assets/green_checkmark.svg){width="20"} Enthalten |

{style="table-layout:fixed"}
