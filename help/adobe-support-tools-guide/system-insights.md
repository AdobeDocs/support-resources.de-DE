---
title: Systemeinblicke
description: Systemeinblicke identifizieren proaktiv potenzielle Probleme in Adobe Commerce-Umgebungen. Die Überprüfung der Erkenntnisse während der Erstellung von Fällen verkürzt die Problembehebungszeit, hilft Ausfälle zu verhindern und unterstützt eine stabile und sichere Bereitstellung.
source-git-commit: 4172c364c9bfffaae13759da882d03daa15d0754
workflow-type: tm+mt
source-wordcount: '741'
ht-degree: 0%

---

# Systemeinblicke

System Insights bietet proaktive Ergebnisse, mit denen potenzielle Probleme in den Bereichen Leistung, Sicherheit und Funktionalität bei der Adobe-Produkteinrichtung identifiziert werden können. Diese Einblicke lassen Risiken wie Leistungseinbußen, Sicherheitslücken oder falsche Konfigurationen auf der Grundlage von Telemetriedaten, die von Beobachtungstools wie APIs, New Relic und [!DNL Splunk] erfasst wurden, erkennen.

Systemeinblicke werden während des Prozesses der Fallerstellung angezeigt und helfen bei der Beschleunigung der Diagnose und Lösung.

## So werden Systemeinblicke erstellt

Adobe-Teams analysieren kontinuierlich häufige Support-Probleme und neue Trends. Basierend auf diesen Erkenntnissen fügt Adobe dem System automatisierte Prüfungen hinzu.

Diese Prüfungen überprüfen das Produkt-Setup, um Probleme wie Fehlkonfigurationen, steckengebliebene Aufträge oder Bedingungen zu erkennen, die zu Funktionsproblemen oder Systemausfällen führen könnten.

Wenn bei einer Prüfung ein Wert oder Status außerhalb des von den Produkt- und Support-Teams von Adobe definierten sicheren Bereichs erkannt wird, wird er vom System als System-Insight angezeigt.

## Warum Systemeinblicke wichtig sind

Die regelmäßige Überprüfung der Systemeinblicke hilft, Probleme frühzeitig zu erkennen, bevor sie sich auf die Systemstabilität oder das Kundenerlebnis auswirken. Dieser proaktive Ansatz:

- Erhöht die Zuverlässigkeit der Plattform
- Reduziert Ausfallzeiten
- Hilft bei der Pflege der von Adobe empfohlenen Best Practices

## Verfügbarkeit und Umfang

Systemeinblicke sind derzeit nur für Adobe Commerce verfügbar. Diese Erkenntnisse werden während der Fallerstellung im Experience League Support angezeigt und sind auch über das [Site-Wide Analysis Tool (SWAT) verfügbar](https://experienceleague.adobe.com/en/docs/commerce-operations/tools/site-wide-analysis-tool/intro).

> [ !NHinweis]
>
>System Insights zeigt Daten nur für Produktionsumgebungen an.

## Zugriff auf Systemeinblicke

Systemeinblicke werden während des gesamten Arbeitsablaufs für die Fallerstellung angezeigt. Wenn Sie Problemdetails eingeben, wird **[!UICONTROL Bedienfeld &quot;]** Insights“ auf der rechten Bildschirmseite unter dem Abschnitt KI-gestützte Empfehlungen angezeigt. Weitere Informationen zu KI-gestützten Empfehlungen finden Sie unter [Support-Ticket ausfüllen](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-customer-support-experience#fill-out-the-support-ticket) im Artikel Adobe-Kundensupporterlebnis .

Das Bedienfeld zeigt eine scrollbare Liste von Einblicken an, die sich auf die jeweilige Projektinstanz beziehen. Die Berechnung basiert auf den im Feld **[!UICONTROL Projekt-URL]** eingegebenen Informationen. Geben Sie die **[!UICONTROL Projekt-URL]** genau ein, um sicherzustellen, dass die Insights die richtige Umgebung widerspiegeln.

Nachdem das Bedienfeld geladen wurde, wird eine scrollbare Liste mit insight-Karten angezeigt, die für Ihre Umgebung gekennzeichnet sind. Jede insight-Karte enthält:

- Ein Titel, der das Problem zusammenfasst
- Eine kurze Beschreibung der insight

![Zugriff auf Support-Ressourcen](/help/adobe-support-tools-guide/assets/access-support-resources.png)

Um vollständige insight-Details anzuzeigen, wählen Sie eine insight-Karte aus der Liste aus. Die Detailansicht enthält die folgenden Informationen:

- Insight-Name
- Adobe-Produkt, auf dem insight gekennzeichnet ist
- Insight-Typ, kategorisiert als:
   - [!UICONTROL -Funktion]
   - [!UICONTROL -Leistung]
   - [!UICONTROL -]
- [!UICONTROL Risikostufe] gibt den Schweregrad an
- [!UICONTROL Letzter Prüflauf] gibt an, wann der Fund erkannt wurde.
- [!UICONTROL Insight Source], bereitgestellt vom Site-Wide Analysis Tool (SWAT)
- Eine ausführliche Erläuterung des Problems und seiner potenziellen Auswirkungen sowie praktische Schritte zur Untersuchung und Behebung des Problems. In der Detailansicht werden auch die typischen Ursachen für diese Art von Problem erläutert und Links zu relevanten Adobe-Dokumentationen als zusätzliche Referenz hinzugefügt.

![Auf Fallkarte klicken](/help/adobe-support-tools-guide/assets/click-case-card.png)

Überprüfen Sie alle Einblicke im Panel, bevor Sie fortfahren, da ein insight das aufgetretene Problem direkt beheben kann.

## Durchführen von Aktionen für eine insight

Wählen Sie nach dem Überprüfen einer insight eine der folgenden Aktionen aus.

### Fallerstellung fortsetzen

Wenn das Problem weiterhin besteht oder zusätzliche Unterstützung erfordert, wählen Sie **[!UICONTROL Mit der Fallerstellung fortfahren]**. Das System behält alle zuvor eingegebenen Fallinformationen bei.

### Problem als gelöst markieren

Wenn die insight das Problem behebt und ein Support-Fall nicht mehr erforderlich ist, wählen Sie **[!UICONTROL Problem gelöst]** aus.

Wenn diese Option ausgewählt ist:

- Ein Bestätigungsdialogfeld wird angezeigt.
- Das Dialogfeld zeigt an, dass alle eingegebenen Daten dauerhaft gelöscht werden.

![Aktion auf einer insight](/help/adobe-support-tools-guide/assets/issue-resolved.png)

Wählen Sie **[!UICONTROL Fertig]** aus, um zu bestätigen und zur Seite **[!UICONTROL Meine Fälle]** zurückzukehren. Wählen Sie **[!UICONTROL Abbrechen]** aus, um zur Detailansicht von insight zurückzukehren.

![Formular löschen](/help/adobe-support-tools-guide/assets/clear-case-form.png)

## Bereitstellen von Feedback zu einer insight

Am Ende jeder Detailansicht von insight können Sie Feedback dazu erhalten, ob die insight hilfreich war. Dieses Feedback hilft Adobe dabei, die Relevanz und Genauigkeit von System Insights kontinuierlich zu verbessern.

![Feedback geben](/help/adobe-support-tools-guide/assets/submit-feedback.png)

Feedback geben:

1. Öffnen Sie eine insight-Detailansicht.
2. Scrollen Sie zum unteren Rand des Bedienfelds.
3. Suchen Sie die Eingabeaufforderung **[!UICONTROL War dies hilfreich? Feedback senden.]**
4. Wählen Sie eine der folgenden Optionen aus:
   - **Daumen hoch** wenn die insight hilfreich war
   - **Daumen runter** Symbol, wenn die insight nicht hilfreich war
5. (Optional) Geben Sie zusätzliche Kommentare ein.
6. Wählen Sie **[!UICONTROL Senden]**, um Feedback zu senden, oder **[!UICONTROL Verwerfen]**, um den Feedback-Abschnitt ohne Senden zu schließen.
