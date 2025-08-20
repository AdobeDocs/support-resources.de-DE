---
title: 'Verwalten von Ergebnissen im  [!DNL Adobe Success] '
description: In diesem Handbuch wird erläutert, wie Sie auf die Ergebnisse im  [!DNL Adobe Success] -Portal zugreifen, sie interpretieren und darauf reagieren können, um proaktiv die Produktleistung, die Sicherheit und die Funktionsrisiken zu verwalten.
source-git-commit: 435931272f25caa6997a16d371aafcf70cf9facd
workflow-type: tm+mt
source-wordcount: '765'
ht-degree: 0%

---

# Verwalten von Ergebnissen im [!DNL Adobe Success] Portal

In diesem Handbuch wird erläutert, wie Sie auf die Ergebnisse im [!DNL Adobe Success] Portal zugreifen, sie interpretieren und darauf reagieren können, um proaktiv mit Produkt-, Sicherheits- und Funktionsrisiken umzugehen.

Auf der Seite [!DNL Adobe Success]Ergebnisse **[!UICONTROL des]**-Portals werden in Ihrer Adobe-Produktinstanz erkannte Probleme oder Risiken angezeigt. Die Ergebnisse umfassen Leistungs-, Sicherheits- und Funktionsprobleme sowie deren Status und Risikostufe. Wenn Sie diese Seite überwachen, können Sie Probleme frühzeitig lösen, bevor sie sich auf Ihre Umgebungen auswirken.

**Was sind Ergebnisse?**

Die Ergebnisse sind Support Insights-Warnhinweise, die im [!DNL Adobe Success] Portal angezeigt werden. Sie zeigen potenzielle Probleme in Ihrer Adobe-Produkteinrichtung auf, z. B. Leistungseinbußen, Sicherheitsrisiken oder falsche Konfigurationen. Diese Warnhinweise basieren auf Telemetriedaten, die von Tools wie APIs, [!DNL New Relic] und [!DNL Splunk] erfasst werden.

**Wie werden Ergebnisse erstellt?**

Adobe-Teams untersuchen regelmäßig die häufigsten Support-Probleme und -Trends. Basierend auf den Erkenntnissen fügen sie dem System neue Prüfungen hinzu. Einmal täglich scannt das [!DNL Adobe Success] Portal Produktdaten, um Probleme zu erkennen, z. B. Fehlkonfigurationen, blockierte Aufträge oder alles, was zu einem Systemausfall führen könnte. Wenn eine Prüfung etwas außerhalb des sicheren Bereichs findet (wie von den Produkt- und Support-Teams von Adobe definiert), wird sie als Ergebnis angezeigt.

**Warum sind Ergebnisse wichtig**

Die regelmäßige Überprüfung der Ergebnisse hilft, Probleme frühzeitig zu erkennen - bevor sie sich auf Ihr System oder Ihre Kunden auswirken. Dieser proaktive Ansatz verbessert die Systemstabilität, reduziert Ausfallzeiten und unterstützt Best Practices.

**So beheben Sie Funde**

Zu jedem Ergebnis gehören Empfehlungen und klare Anweisungen zur Lösung des Problems sowie Links zu relevanten Dokumentationen, sofern verfügbar. Teilen Sie diese Ergebnisse mit Ihrer IT, Ihrem Engineering-Team oder Ihrem Adobe-Partner und arbeiten Sie zusammen, um diese zu beheben. Die frühzeitige Behebung dieser Probleme hilft, größere Probleme zu vermeiden, und sorgt dafür, dass Ihr System reibungslos läuft.


## Zugriff auf Ergebnisse

So zeigen Sie Einblicke zu einem Produkt an:

1. Navigieren Sie zu **[!UICONTROL Support und Einblicke]**.
1. Wählen Sie die entsprechende Produktkarte aus. Wählen Sie die **[!UICONTROL Ergebnisse]** aus.

   ![asp-support-insights-results](../../assets/asp-support-inisghts-findings.png)


1. Es wird eine Liste aller Ergebnisse für das ausgewählte Produkt angezeigt.

   ![adobe-success-portal-results](../../assets/adobe-success-portal-findings.png)

1. Von hier aus können Sie:

   ![adobe-success-portal-download](../../assets/adobe-success-portal-download.png)

   * Nach bestimmten Einträgen suchen.
   * Exportieren Sie die Liste der Ergebnisse, indem Sie **[!UICONTROL Ergebnisse herunterladen]** auswählen. Um einen Bericht für eine einzelne Suche zu exportieren, aktivieren Sie das Kontrollkästchen neben der entsprechenden Suche in der Spalte **[!UICONTROL Name der Suche]**. Wenn Sie kein Ergebnis auswählen, enthält PDF standardmäßig eine Liste aller Ergebnisse.
   * Zeigen Sie Details zu einem Ergebnis an, einschließlich einer empfohlenen Lösung, indem Sie ein Ergebnis unter &quot;**[!UICONTROL &quot;]**. Auf der Seite „Suchdetails“ wird die ausgewählte Suche mit zusätzlichem Kontext und einer Empfehlung angezeigt. Um diesen Bericht anzuzeigen, klicken Sie auf den Pfeil „Herunterladen“.


     ![results-details](../../assets/findings-details.png)


## Ergebnisse der Aktion

Führen Sie diese Schritte aus, um zu überprüfen, ob die einzelnen Ergebnisse weiterhin anwendbar sind oder verworfen werden können.

>[!NOTE]
>
>Standardprüfungen werden auf Ihren Instanzen ausgeführt. Wenn bei den Prüfungen nicht festgestellt wird, dass das Problem in Ihrer Instanz vorliegt, gibt es den Status **[!UICONTROL Nicht erkannt]**.

1. Navigieren Sie zu **[!UICONTROL Support und Einblicke]**.
1. Wählen Sie die entsprechende Produktkarte aus.
1. Öffnen Sie die **[!UICONTROL Ergebnisse]**. Sie sehen alle Ergebnisse für Ihr ausgewähltes Produkt.
1. Wählen Sie einen Eintrag unter **[!UICONTROL Suchen nach Name]** aus. Auf der Seite mit den Suchdetails haben Sie folgende Möglichkeiten:
   * Wählen Sie **[!UICONTROL Validieren]** aus, um zu überprüfen, ob das Problem noch vorhanden ist (die Schaltfläche **[!UICONTROL Validieren]** dient zur Bestätigung, dass das Problem behoben wurde):

   ![adobe-success-portal-validate](../../assets/adobe-success-portal-validate.png)


   * Wenn das Problem weiterhin besteht, wird die folgende Meldung angezeigt: *[!UICONTROL Validierung abgeschlossen. Suche wurde noch erkannt]*. Verwenden Sie die Informationen und Empfehlungen auf der Seite „Suchdetails“, um das Problem zu untersuchen und zu beheben.
   * Wenn das Problem nicht mehr vorhanden ist, wird die folgende Meldung angezeigt: *[!UICONTROL Validation Complete. Der Fund wurde nicht mehr erkannt]*. Wenn der Fund nicht mehr erkannt wird, wird er ausgegraut und der Status ändert sich in **[!UICONTROL Nicht erkannt]**. Befunde mit **[!UICONTROL Nicht erkannt]**-Status befinden sich unten in der Ergebnisliste.
   * Wenn das Problem für Sie nicht relevant oder relevant ist, können Sie es durch Auswahl von **[!UICONTROL Schließen]** schließen. Wenn der Fund abgelehnt wird, wird er ausgegraut und der Status ändert sich in **[!UICONTROL Abgewiesen]**.  Ergebnisse mit **[!UICONTROL Abgelehnt]**-Status befinden sich unten in der Ergebnisliste.

## Erkenntnisse verstehen

* **[!UICONTROL Suchname]** - Wählen Sie aus, um detaillierte Einblicke und empfohlene Lösungsschritte zu erhalten.
* **[!UICONTROL Typ]** - Kategorisiert als *Funktion*, *Leistung* und *Sicherheit*.
* **[!UICONTROL Risikostufe]** - Schweregradindikator mit visuellen Indikatoren.
* **[!UICONTROL Status]** - Der aktuelle Status des Ergebnisses (z. B. *Ermittelt*, *Nicht erkannt*, *Verworfen*).
* **[!UICONTROL Letzte Ausführung überprüfen]** - Zeitstempel der letzten Prüfung, die die Suche aktualisiert hat.


## Best Practices

Auf **[!UICONTROL Seite]** Ergebnisse“ werden Empfehlungen mit den folgenden Risikostufen aufgelistet: **[!UICONTROL Hoch]**, **[!UICONTROL Erhöht]** und **[!UICONTROL Medium]**. **[!UICONTROL Hoch]** ist kritisch, **[!UICONTROL Erhöht]** ist dringend, und **[!UICONTROL Medium]** ist nicht kritisch. So erhalten Sie den Zustand und die Leistung der Site:

* Bewerten **[!UICONTROL mit hohem Risiko]** umgehend, da sie kritische Bedrohungen darstellen.
* Beheben Sie **[!UICONTROL erhöhte]** Risikoprobleme bald, um eine Eskalation zu vermeiden.
* **[!UICONTROL Medium]** Risikoergebnisse regelmäßig überwachen und nach Bedarf handeln.




