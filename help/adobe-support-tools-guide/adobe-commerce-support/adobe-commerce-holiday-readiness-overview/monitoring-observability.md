---
title: Überwachung und Beobachtbarkeit
description: Empfehlungen zur Überwachung und Beobachtung, um Adobe Commerce-Händler bei der Vorbereitung ihrer Umgebungen auf Ereignisse mit hohem Traffic-Aufkommen wie die Weihnachtszeit zu unterstützen.
feature-set: Commerce
feature: Support
solution: Commerce
role: Developer, Admin, Leader
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: 5a951749-fac9-5bc7-9a98-ebe4ff066437
    internal-label: Cloud
  - id: cdfd3bc1-dc23-5cf0-b965-d3c0c55cde67
    internal-label: Best Practices
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
    internal-label: Security
  - id: 4239b8a6-e74f-567d-a7a5-b98b9ead0ea4
    internal-label: Observability
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
subfeature_v2:
  - id: 3c398179-d35a-51ba-b317-6c5b95feef5e
    internal-label: Logs
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
source-git-commit: 71589dd124714805fbf844540fb2d272433631ee
workflow-type: tm+mt
source-wordcount: '517'
ht-degree: 2%
---

# Überwachung und Beobachtbarkeit

Dieser Abschnitt enthält technische Empfehlungen für die Überwachung von Adobe Commerce-Umgebungen zur Vorbereitung auf Ereignisse mit hohem Traffic, wie die Weihnachtszeit.

>[!NOTE]
>
>Die mit **(nur Cloud) gekennzeichneten** gelten für Commerce in der Cloud-Infrastruktur. Die meisten anderen Empfehlungen gelten auch für lokale Bereitstellungen.

## Überwachen des Traffics mit New Relic (nur Cloud) {#monitor-traffic-with-new-relic}

Adobe Commerce in Cloud-Infrastrukturen umfassen ein Abonnement für eine [!DNL New Relic] Beobachtbarkeitsplattform, das [!DNL Fastly]-Streaming-Protokolle nahtlos in nahezu Echtzeit in [!DNL New Relic] integriert. Mit dieser Integration können Sie Ihre Traffic-Muster und -Trends in Echtzeit überwachen, sodass Sie Korrekturmaßnahmen ergreifen können.

Verwenden Sie diese Protokolle für Folgendes:

* Identifizieren Sie Länder, aus denen Ihre Webanfragen stammen.
* Suchen nach missbräuchlichen IP-Adressen oder Benutzeragenten, die Ihre Site crawlen haben.
* Erkennung von bösartigem Traffic, der auf bestimmte Endpunkte abzielt, z. B. Zahlung.
* Erstellen Sie Berichte zu den von Ihren Kunden verwendeten Geräte- und Browser-Typen.

Überwachen Sie beispielsweise das Ursprungsland Ihres Traffics, um zu bestätigen, dass er die geografischen Standorte Ihrer Promotions und Kunden widerspiegelt:

```sql
SELECT count(*) FROM Log
WHERE cache_status IS NOT NULL
AND project_id = '<YOUR_PROJECT_ID>'
AND (content_type LIKE 'text/html;%' or url LIKE '%graphql%' or url like '%rest%')
FACET geo_country_code
SINCE 7 days ago until today
```

Ändern Sie diese Abfrage entsprechend Ihren Anforderungen, segmentieren Sie sie weiter oder wandeln Sie sie in ein Dashboard für zentralisiertes Tracking um. Weitere Informationen finden Sie unter [New Relic-Protokollverwaltung](https://experienceleague.adobe.com/de/docs/commerce-on-cloud/user-guide/monitor/new-relic/log-management).

## Anpassen von New Relic-Warnhinweisen (nur Cloud) {#customize-new-relic-alerts}

Zusätzlich zu den von Adobe Commerce in der Cloud-Infrastruktur festgelegten verwalteten Warnhinweisen können Sie für Ihre Plattform während der Spitzenverkaufszeit eine Vielzahl von Warnhinweisen und Benachrichtigungen festlegen, z. B. die Benachrichtigung über Bot-Traffic oder eine längere Reaktionszeit bei einer GraphQL-Abfrage. Siehe [Verwaltete Warnhinweise für Adobe Commerce](https://experienceleague.adobe.com/de/docs/commerce-operations/tools/managed-alerts-for-adobe-commerce/managed-alerts-for-magento-commerce) für die vollständige Liste der integrierten Warnhinweise.

[!DNL New Relic] Warnhinweise und KI unterstützen NRQL-basierte Abfragestrukturen. Richten Sie benutzerdefinierte Warnhinweise über das [!DNL New Relic]-Dashboard unter **[!UICONTROL Warnhinweise und KI]** ein.

## APDEX-Punktzahl überprüfen (nur Cloud) {#review-apdex-score}

Der Apdex Score misst die Benutzerzufriedenheit mit der Reaktionszeit Ihrer Web-Anwendungen und -Services. Sie können den Apdex-Wert Ihrer Adobe Commerce in der Cloud-Infrastruktur mithilfe von [!DNL New Relic] überprüfen.

Ein Apdex-Wert liegt zwischen 0 und 1. Der Wert 0 ist der schlechteste Wert, was bedeutet, dass 100 % der Antwortzeiten **frustriert**. Ein Score von 1 ist der bestmögliche Score, was bedeutet, dass 100 % der Antwortzeiten &quot;**&quot;**. [!DNL New Relic] gibt sowohl einen App Server-Wert aus, der die Backend-Leistung widerspiegelt, als auch einen Endbenutzer-Wert, der die Client-seitige Leistung widerspiegelt.

Ein Apdex-Wert von 0,5 oder niedriger rechtfertigt eine Untersuchung. Ein Wert unter 0,4 gilt als Ausfall.

Zusammen mit Apdex bietet [!DNL New Relic] eine Reihe von Statistiken zur Analyse von Leistungsproblemen in Adobe Commerce auf Cloud-Infrastrukturen. Anweisungen hierzu finden Sie unter [Fehlerbehebung bei der Leistung mit New Relic auf Adobe Commerce](https://experienceleague.adobe.com/de/docs/commerce-knowledge-base/kb/troubleshooting/miscellaneous/troubleshoot-performance-using-new-relic-on-magento-commerce).

## Support Insights überprüfen (SWAT-Bericht) {#review-support-insights-swat-report}

Um einen detaillierteren Bericht über Ihre Umgebung zu erhalten, generieren Sie einen SWAT-Bericht (Site-Wide Analysis Tool). Weitere Informationen zum SWAT-Tool finden Sie unter [Site-Wide Analysis Tool](https://experienceleague.adobe.com/de/docs/commerce-operations/tools/site-wide-analysis-tool/intro).