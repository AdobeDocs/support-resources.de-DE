---
title: Fehlerbehebungen (ausgeblendet)
description: Testseite für interne Testzwecke
hide: true
hidefromtoc: true
exl-id: e6270f95-3550-4e35-ad4c-760584bb9b5d
source-git-commit: 0cefcf5bb4a021593a6bbe44eed0ad83e8bd259f
workflow-type: tm+mt
source-wordcount: '1926'
ht-degree: 28%

---

# Fehlerkorrekturen

## Autoaktivierungstest

Diese Fehler sollten alle behoben werden.

## UGP-10866 Links nicht fett in Schattierungsfeldern

>[!BEGINSHADEBOX]

**Inhaltsverzeichnis**

* [Erste Schritte mit dem KI-Assistenten](note-test.md)
* **[Generierung von E-Mails mit dem KI-Assistenten](syntax-style-guide.md)**
* [SMS-Generierung mit dem KI-Assistenten](test-page.md)
* [Generierung von Push-Benachrichtigungen mit dem KI-Assistenten](tables.md)
* [Inhaltsexperiment mit dem KI-Assistenten](test-redirection.md)

>[!ENDSHADEBOX]

Kein Schattierungskasten

**Inhaltsverzeichnis**

* [Erste Schritte mit dem KI-Assistenten](note-test.md)
* **[Generierung von E-Mails mit dem KI-Assistenten](syntax-style-guide.md)**
* [SMS-Generierung mit dem KI-Assistenten](test-page.md)
* [Generierung von Push-Benachrichtigungen mit dem KI-Assistenten](tables.md)
* [Inhaltsexperiment mit dem KI-Assistenten](test-redirection.md)


## UGP-10584 Inline-Badges funktionieren nicht

Diese Abzeichen sollten sich in derselben Zeile wie die Aufzählungszeichen befinden.

* [[!DNL Mixpanel]](note-test.md) [!BADGE Hinweise]{type=Informative}
* [[!DNL Pendo]](tables.md) [!BADGE Tabellen]{type=Positive}
* [[!DNL RainFocus]](syntax-style-guide.md) [!BADGE Syntaxstil-Handbuch]{type=Positive}

## UGP-10560 - Abzeichen in ausblendbaren Abschnitten

+++ Frühere Versionen

### Version 1.16

_13. Februar 2023_

[!BADGE Unterstützt]{type=Informative tooltip="Unterstützt"}

![Neu](assets/package.png) Produktvideos werden jetzt von der Catalog Service-API unterstützt.
![Fix](assets/package.png) Bundle-Produkte mit festen Preisen werden jetzt unterstützt.
![Beheben](assets/package.png) Nicht vorrätige Optionen werden jetzt im PDP-Widget angezeigt.

#### Bekannte Einschränkungen

Diese Funktionen werden noch nicht unterstützt:

* Die maximale Größe für die Payload dynamischer Attribute beträgt 9 MB.
* Gruppenproduktpreis. Kann mit einfachen Produktpreisen berechnet werden.
* In einem Bild-Array enthält nur das erste Bild Rollen.

Die folgenden Einschränkungen können mithilfe der API Mesh und der Core GraphQL API behoben werden:

* Mindestpreis
* [Preisstufe](https://www.adobe.com)

### Version 1.13

_Freitag, 12. Oktober 2023_

[!BADGE Unterstützt]{type=Informative tooltip="Unterstützt"}

![Neu](assets/package.png) Der Katalog-Service unterstützt das `inStock`-Flag für Produktvarianten.
![Neu](assets/package.png) `urlKey` und `externalId` wurden zum GraphQL-Schema hinzugefügt.
![Neu](assets/package.png) Herunterladbare Produkte und Geschenkkarten werden jetzt unterstützt.

### Version 1.12

_Mittwoch, 19. September 2023_

[!BADGE Unterstützt]{type=Informative tooltip="Unterstützt"}

![Neu](https://www.adobe.com).
![Behebung](assets/package.png) Diese Version enthält Fehlerbehebungen und Verbesserungen auf der Service-Seite.

### Version 1.11

_Mittwoch, 18. Juli 2023_

[!BADGE Unterstützt]{type=Informative tooltip="Unterstützt"}

![Neu](assets/package.png) Der Katalog-Service unterstützt jetzt die [`recommendations`](https://developer.adobe.com/commerce/services/graphql/recommendations/recommendations/) GraphQL-Abfrage für Produkt-Recommendations.

### Version 1.10

_Mittwoch, 27. Juni 2023_

[!BADGE Unterstützt]{type=Informative tooltip="Unterstützt"}

![Neu](assets/package.png) Die Catalog Service-API unterstützt jetzt „verwandte Produkte“.

### Version 1.7

_Donnerstag, 12. April 2023_

[!BADGE Unterstützt]{type=Informative tooltip="Unterstützt"}

![Neu](assets/package.png) Der Katalog-Service bereinigt jetzt gelöschte Produktvarianten.
![Behebung](assets/package.png) Infrastrukturskalierbarkeit und Leistungsverbesserungen.

### Version 1.6

_Mittwoch, 28. März 2023_

[!BADGE Unterstützt]{type=Informative tooltip="Unterstützt"}

![Neu](assets/package.png) Zur [`products`](https://developer.adobe.com/commerce/services/graphql/catalog-service/products/) Abfrage wurden Farbfelder hinzugefügt.
![Neu](https://www.adobe.com).

### Version 1.5

_Dienstag, 6. März 2023_

[!BADGE Unterstützt]{type=Informative tooltip="Unterstützt"}

![Neu](assets/package.png) Funktion [`categories`](https://developer.adobe.com/commerce/services/graphql/schema/catalog-service/categories/) GraphQL hinzugefügt.
![Behebung](assets/package.png) Verbesserte Leistung und API-Skalierbarkeit.

### Version 1.4

_Mittwoch, 7. Februar 2023_

[!BADGE Unterstützt]{type=Informative tooltip="Unterstützt"}

![Neu](assets/package.png) Veröffentlichtes Katalog-Service-Metapaket zur Vereinfachung der Installationsschritte.
![Fix](assets/package.png) API-Skalierbarkeit und Leistungsverbesserungen.

### Version 1.3

_Mittwoch, 17. Januar 2023_

[!BADGE Unterstützt]{type=Informative tooltip="Unterstützt"}

![Neu](assets/package.png) Das Onboarding wurde vereinfacht und verbessert.
![Neu](assets/package.png) Neue Kunden-Sandbox-Endpunkte sind für Vorproduktionstests verfügbar.
![Neu](assets/package.png) Unterstützung für virtuelle Produkte hinzugefügt.
![Fix](assets/package.png) API-Skalierbarkeit und Leistungsverbesserungen.

### Version v1.1

_Samstag, 18. November 2022_

[!BADGE Unterstützt]{type=Informative tooltip="Unterstützt"}

![Neu](assets/package.png) Der Katalog-Service unterstützt jetzt die Adobe [API Mesh](https://developer.adobe.com/graphql-mesh-gateway/).
![Fix](assets/package.png) Verbesserte API-Skalierbarkeit und Gesamtleistung.

### Version 1.0

_Mittwoch, 4. Oktober 2022_

[!BADGE Unterstützt]{type=Informative tooltip="Unterstützt"}

![Neu](assets/package.png) Unterstützt jetzt gebündelte und gruppierte Produkte.
![Neu](assets/package.png) Es wurden Überschreibungen der B2B-Sichtbarkeit hinzugefügt. Produkte können jetzt durchsucht und für bestimmte Kundengruppen zum Warenkorb hinzugefügt werden.
![Fix](assets/package.png) Service ist jetzt stabiler und hat die Leistung verbessert.

### Version 0.3 - Beta+

_Dienstag, 12. September 2022_

[!BADGE Unterstützt]{type=Informative tooltip="Unterstützt"}

![Neu](assets/package.png) Unterstützung von Bildern für Varianten: Produktbilder werden basierend auf den ausgewählten Optionen zurückgegeben
![Neu](assets/package.png) Rollen zur Preisunterstützung: Nur Mitgliedern bestimmter Kundengruppen wird ermöglicht, die Preise von Produkten anzuzeigen.
![Behebung](assets/package.png) Verbesserte Stabilität und Leistung des Service
![Neu](assets/package.png) Aktualisierungen werden empfangen, wenn Produkte aus dem Katalog gelöscht werden

### Beta-Version

_Mittwoch, 9. August 2022_

[!BADGE Unterstützt]{type=Informative tooltip="Unterstützt"}

![Neu](assets/package.png) Die `products`- und `refineProduct`-Abfragen geben die folgenden Daten zurück:

* Vordefinierte (System-)Produktattribute.
* Dynamische Produktattribute und deren Filterung nach Rolle (Produktanzeigeseite/Produktlistenseite).
* Produktoptionen.
* Produktbilder und Filtern nach Rolle (PDP/PLP).
* Ein spezifischer Preis für einfache Produkte und Preisspannen für konfigurierbare Produkte.
* Kundengruppenpreise und Preisspannen. Sie geben einen standardmäßigen Fallback-Preis für Käufer ohne Kundengruppe zurück.
* Produkttypen, die B2B-kundenspezifische Preise verwenden.

+++

## [!BADGE Veraltet]{type=negative}

Siehe obige Überschrift. Und das nächste.

## Testen auf automatische Aktivierung

Ich habe dies am Freitagnachmittag hinzugefügt, aber nicht auf &quot;Publish Now“ geklickt.

### [!BADGE Beta]{type=Informative}

Bob

## UGP-10565 - Texthervorhebung

Text vor `<div class="preview">`

<div class="preview">

### Native Workfront-Felder hinzufügen

Sie können Ihren benutzerdefinierten Formularen native Workfront-Felder hinzufügen. Wenn das benutzerdefinierte Formular an ein Objekt angehängt wird, wird das Feld aus den Objektdaten gefüllt. Beispielsweise ruft das Feld Beschreibung in einem benutzerdefinierten Formular, das an ein Projekt angehängt ist, die Projektbeschreibung ab. (Wenn keine Daten verfügbar sind, kann das Feld „K. A.“ anzeigen.)

1. Suchen Sie auf der linken Seite des Bildschirms nach &quot;**Feld** und ziehen Sie es in einen Bereich auf der Arbeitsfläche.
1. Konfigurieren Sie auf der rechten Seite des Bildschirms die Optionen für das benutzerdefinierte Feld:

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader">Kennzeichnung</td> 
      <td> <p>(Erforderlich) Geben Sie einen beschreibenden Titel ein, der über dem Feld angezeigt werden soll. Sie können den Titel jederzeit ändern.</p> <p><b>WICHTIG</b>: Verwenden Sie in dieser Kennzeichnung keine Sonderzeichen. Sie werden in Berichten nicht korrekt angezeigt.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">Name</td> 
      <td> <p>(Erforderlich) Mit diesem Namen identifiziert das System das Feld.</p><p> Wenn Sie das Feld zum ersten Mal konfigurieren und die Bezeichnung eingeben, wird das Feld Name automatisch entsprechend ausgefüllt. Die Felder Beschriftung und Name sind jedoch nicht synchronisiert. Dadurch haben Sie die Möglichkeit, die Beschriftung zu ändern, die Ihre Benutzerinnen und Benutzer sehen, ohne den Namen ändern zu müssen, den das System sieht.</p>
      <p><b>WICHTIG</b>:
      <ul> 
      <li>Obwohl dies möglich ist, empfehlen wir, diesen Namen nicht zu ändern, nachdem Sie oder andere Benutzende mit der Verwendung des benutzerdefinierten Formulars in Workfront begonnen haben. Wenn Sie dies tun, erkennt das System das Feld, in dem nun in anderen Bereichen von Workfront darauf verwiesen wird, nicht mehr.</p> </li>
      <li> <p>Jeder Feldname muss in der Workfront-Instanz Ihres Unternehmens eindeutig sein. Auf diese Weise können Sie ein bereits für ein anderes benutzerdefiniertes Formular erstelltes Formular wiederverwenden.</p> </li>
      <li><p>Es wird empfohlen, im benutzerdefinierten Feldnamen keinen Punkt bzw. Punkt zu verwenden, um Fehler zu vermeiden, wenn das Feld in verschiedenen Bereichen von Workfront verwendet wird.</p></td> 
     </tr> 
     <tr> 
      <td role="rowheader">Anweisungen</td> 
      <td> <p>Geben Sie zusätzliche Informationen zum Feld ein. Wenn Benutzer das benutzerdefinierte Formular ausfüllen, können sie den Mauszeiger über das Fragezeichen bewegen, um eine QuickInfo mit den hier eingegebenen Informationen anzuzeigen.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">Referenzfeld</td> 
      <td><p>(Erforderlich) Wählen Sie ein natives Workfront-Feld aus.<p><p>Für die Objekte des Formulars sind nur native Felder verfügbar. Wenn beispielsweise die Liste Objekttypen oben im Formular-Designer „Projekt“ anzeigt, können Sie native Felder für Projekte auswählen, jedoch keine Felder, die speziell für Aufgaben verwendet werden.</p></td>
     </tr>
     <tr> 
      <td role="rowheader">Größe</td> 
      <td>(Optional) Ändern Sie die Anzeigegröße des Felds nach Bedarf.</td> 
     </tr> 
    </tbody> 
   </table>

1. Um Ihre Änderungen zu speichern, klicken Sie auf **Übernehmen** und gehen Sie zu einem anderen Abschnitt über, um mit der Erstellung Ihres Formulars fortzufahren.

   oder

   Klicken Sie **Speichern und schließen**.

</div>

Text nach Hervorhebung

## UGP-10566 - Link-Text ist kleiner als normaler Text in HTML-Tabellen

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
    <td> <p>(Erforderlich) Geben Sie einen beschreibenden Titel ein, der über dem benutzerdefinierten Feld angezeigt werden soll. Sie können den Titel jederzeit ändern. Weitere Informationen finden Sie unter <a href="https://www.adobe.com" class="MCXref xref">Hinzufügen eines benutzerdefinierten Felds zu einem benutzerdefinierten Formular</a> in diesem Artikel.</p> <p><b>WICHTIG</b>: Verwenden Sie in dieser Kennzeichnung keine Sonderzeichen. Sie werden in Berichten nicht korrekt angezeigt.</p> </td> 
    <td>
    <ul>
    <li>Optionsfelder. Weitere Informationen finden Sie unter <a href="https://www.adobe.com">Hinzufügen eines benutzerdefinierten Felds zu einem benutzerdefinierten Formular</a> in diesem Artikel. (Keine Klasse)</li>
    <li>Kontrollkästchen-Gruppe</li>
    <li>Dropdown</li>
    </ul></td>
</tr> 
</tbody> 
</table>

## UGP-9176 - Alter Fehler

Das Tag „span“ funktioniert in einer NOTE (und Liste) nicht ganz gut

Informationen dazu, welche Funktionen im neuen Kommentarerlebnis verfügbar sind und für welche Objekte, finden Sie unter [Neues Kommentarerlebnis](note-test.md).

1. Navigieren Sie zu dem Objekt, dem Sie eine Antwort hinzufügen möchten.
1. Klicken Sie auf **Aktualisierungen** und anschließend auf die Registerkarte **Kommentare** für das Objekt und suchen Sie den Kommentar oder die Antwort, auf den bzw. die Sie antworten möchten

   Oder

   <span class="preview">Klicken Sie auf die Registerkarte **Alle** und dann auf **In Kommentaren antworten**, um den Kommentar auf der Registerkarte Kommentare zu öffnen und zu beantworten. Sie können nicht auf der Registerkarte Alle antworten.</span>

1. (Optional) Um Text aus einer vorherigen Aktualisierung in Ihre Antwort einzubeziehen, klicken Sie auf das Menü **Mehr** in der oberen rechten Ecke des Kommentars, auf den Sie antworten möchten, und klicken Sie dann auf **Antwort zitieren**. Text aus der vorherigen Aktualisierung wird im Eingabebereich angezeigt, der mit einer vertikalen grauen Linie markiert ist.
1. Klicken Sie **Antworten**.

   ![](assets/package.png)

   Am unteren Rand des Feldes **Antwort hinzufügen…** können Sie die Benutzer sehen, die aktiv an der Konversation beteiligt sind, weitere hinzufügen oder diejenigen entfernen, die nicht mehr relevant sind. Diese Benutzenden erhalten zusammen mit allen Benutzenden, die das Objekt abonniert haben, eine Benachrichtigung, sobald eine Aktualisierung oder Antwort für das Objekt vorgenommen wird. Sie können auch weitere Benutzer taggen , um sie in Ihre Antwort aufzunehmen.  Informationen zum Tagging weiterer Benutzer finden Sie unter [Andere bei Aktualisierungen taggen](note-test.md).

   >[!TIP]
   >
   >   Um einer vorhandenen Antwort weitere Antworten hinzuzufügen, können Sie mit der Eingabe in das Feld **Antwort hinzufügen…** beginnen oder auf **Antworten** klicken. Ihre Antwort wird am Ende des Threads hinzugefügt.

1. Beginnen Sie mit der Eingabe Ihrer Antwort und verwenden Sie alle zusätzlichen Optionen in der Rich-Text-Symbolleiste. Informationen zur Verwendung von Rich-Text oder anderen Aktualisierungsfunktionen finden Sie unter [Aktualisierungsarbeit](note-test.md).

1. Klicken Sie **Senden**, um die Antwort zu speichern.

1. (Optional) Klicken Sie auf das **Mehr**-Menü in der oberen rechten Ecke des Kommentars, auf den Sie antworten möchten, um weitere Optionen zum Verwalten der Antwort zu erhalten. Weitere Informationen finden Sie unter [Arbeit aktualisieren](note-test.md).


## UGP-10614 - Problemtabellen mit Bildern

Ich denke, der `{width="20"}` verursacht Probleme in Tabellen.

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
