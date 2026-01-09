---
title: Anfordern einer temporären Adobe Commerce-Aktualisierung in der Cloud-Infrastruktur
description: Wenn Ihr Unternehmen eine Online-Veranstaltung plant, bei der Sie hohen Traffic erwarten, oder Sie plötzlich feststellen, dass auf Ihrer Site ein hohes Traffic-Ereignis stattfindet, können Sie ein [Support-Ticket](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide.html?lang=en#submit-ticket) einreichen, um temporäre zusätzliche Cloud-Kapazität für Ihren Adobe Commerce im Cloud-Infrastrukturspeicher anzufordern.
solution: Commerce
source-git-commit: 070f069a083ff310da44ccca4cc4b0081eb106f2
workflow-type: tm+mt
source-wordcount: '874'
ht-degree: 0%

---

# Anfordern einer temporären Adobe Commerce-Aktualisierung in der Cloud-Infrastruktur

Wenn Ihr Unternehmen eine Online-Veranstaltung plant, bei der Sie hohen Traffic erwarten, oder Sie plötzlich feststellen, dass auf Ihrer Site ein hohes Traffic-Ereignis stattfindet, können Sie ein [Support-Ticket](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide.html?lang=en#submit-ticket) einreichen, um temporäre zusätzliche Cloud-Kapazität für Ihren Adobe Commerce im Cloud-Infrastrukturspeicher anzufordern.

>[!NOTE]
>
>Für nicht-dringende Upsizing-Anfragen ist eine 48-Stunden-Benachrichtigung erforderlich. Upgrades für Werbekampagnen gelten nicht als Notfälle, es sei denn, die Website ist vollständig nicht funktionsfähig oder erhält viel höheren Traffic als erwartet, und die Leistung wurde stark beeinträchtigt.

## Betroffene Produkte und Versionen

* Adobe Commerce auf Cloud-Infrastruktur, alle [unterstützten Versionen](https://www.adobe.com/content/dam/cc/en/legal/terms/enterprise/pdfs/Adobe-Commerce-Software-Lifecycle-Policy.pdf).

## So identifizieren Sie Ereignisse mit hohem Traffic

In New Relic-Warnhinweisen können Sie allgemeine Warnbedingungen verwenden, um Schwellenwerte zu definieren, die dem Verhalten Ihrer Daten angepasst werden können.

Baseline-Warnhinweise sind nützlich für die Erstellung von Warnhinweisbedingungen, die:

* Nur benachrichtigen, wenn sich Daten ungewöhnlich verhalten.
* Dynamische Anpassung an sich ändernde Daten und Trends, einschließlich täglicher oder wöchentlicher Trends.

Außerdem eignen sich Baseline-Warnungen gut für neue Anwendungen, wenn die Verhaltensweisen noch nicht bekannt sind.

Unter diesem Link erfahren Sie mehr über New Relic [Anomalieerkennung mit Applied Intelligence](https://docs.newrelic.com/docs/alerts-applied-intelligence/applied-intelligence/anomaly-detection/anomaly-detection-applied-intelligence/).

Wenn Sie eine Warnmeldung erhalten, die auf ein Ereignis mit hohem Traffic hinweist, sollten Sie ggf. erwägen, [ein Support-Ticket &#x200B;](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide.html?lang=en#submit-ticket), um zusätzliche Kapazität anzufordern. Führen Sie die folgenden Schritte aus.

## Überwachen der Leistung Ihrer Site

Adobe bietet eine Reihe von New Relic-Warnhinweisrichtlinien für Adobe Commerce in der Cloud-Infrastruktur Pro Planarchitektur und Adobe Commerce in der Cloud-Infrastruktur Starter Planarchitektur Produktionsumgebungen, um die folgenden wichtigen Leistungsmetriken zu verfolgen:

* [APDEX-Punktzahl](https://docs.newrelic.com/docs/apm/new-relic-apm/apdex/apdex-measure-user-satisfaction)
* Fehlerrate
* Speicherplatz (nur in Produktionsumgebungen der Pro-Architektur verfügbar)

Basierend auf den Best Practices der Branche setzen diese Richtlinien Schwellenwerte für Warnungen und kritische Bedingungen, die die Leistung beeinträchtigen. Wenn auf Ihrer Site ein Infrastruktur- oder Anwendungsproblem auftritt, das einen Warnschwellenwert in Trigger setzt, sendet New Relic Warnbenachrichtigungen, damit Sie das Problem proaktiv beheben können. Um diese Richtlinien verwenden zu können, müssen Sie Benachrichtigungskanäle konfigurieren, über die Benachrichtigungen empfangen werden.

Unter diesem Link erfahren Sie, wie [leistungsbasierte Warnhinweise konfigurieren](/docs/commerce-cloud-service/user-guide/monitor/new-relic.html#monitor-performance-with-managed-alerts).

## Schritte zum Anfordern einer temporären Vergrößerung

Um temporäre zusätzliche Cloud-Kapazität anzufordern, reichen Sie ein [Support-Ticket](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide.html?lang=en#submit-ticket) im Adobe Commerce Support Center mit den folgenden Informationen ein:

>[!NOTE]
>
>Die *Holiday Surge Request*-Option ist nur zwischen Oktober und Dezember möglich.

1. Wählen Sie das [!DNL Adobe Commerce] Produkt aus, für das Sie Unterstützung benötigen:
   * [!DNL Commerce Cloud]
   * [!DNL Commerce on Managed Service]

1. Füllen Sie die folgenden Felder aus:
   * **[!UICONTROL Anwaltsbezeichnung]**
   * **[!UICONTROL Fallbeschreibung]** *(stellen Sie sicher, dass diese das Problem und den Kontext klar beschreiben.)*

1. Wählen *Infrastrukturänderungsanfrage* aus dem Dropdown **[!UICONTROL Menü &quot;]**&quot; aus.

1. Wählen Sie **[!UICONTROL Dropdown]** Menü „Umgebung“ aus.

1. Wählen Sie die entsprechende **[!UICONTROL Produktversion]** aus dem Dropdown-Menü aus.

1. Wählen Sie *Cloud Project Resize (vCPU* aus dem **[!UICONTROL Welchen Infrarotwechsel möchten Sie heute durchführen]** Dropdown-Menü aus.

1. **Wählen Sie die [!UICONTROL Architektur]**:
   * *Standardarchitektur:* Wählen Sie *Nächste verfügbare Größe* aus dem **Wählen Sie die Größe aus** Dropdown-Menü.
   * *Skalierte Architektur:* Wenn diese Option ausgewählt ist, ändert sich der Bildschirm und zeigt zwei zusätzliche Felder an:
      * *Größe für Webknoten*
      * *Größe für Dienstknoten* *(geben Sie die gewünschten Größen für jeden Knoten ein.)*

1. Geben Sie das **[!UICONTROL Von Datum]** im UTC-Format (Datum und Uhrzeit) ein.

1. Geben Sie das **[!UICONTROL Bis-Datum]** im UTC-Format (Datum und Uhrzeit) ein.

1. Geben Sie **[!UICONTROL Projekt-URL]** *an (unter https://accounts.magento.cloud/, normalerweise im Format `https://[REGION].magento.cloud/projects/PROJECT_ID`)*

1. Geben Sie die **[!UICONTROL Projekt-ID]** ein.

1. Geben Sie **[!UICONTROL Betroffene URL]** *an (muss mit `http://` oder `https://` beginnen)*

1. Wählen Sie **[!UICONTROL Priorität]** aus.

1. Wählen Sie **[!UICONTROL Business Impact]** aus.

1. Bestätigen Sie **[!UICONTROL Zeitzone]** *(z. B. `(UTC-5:00) Indiana (East)`)*

1. Geben Sie **[!UICONTROL Telefonnummer]** *ein (z. B. `+12015550123`)*

1. Klicken Sie **[!UICONTROL Senden]** um Ihren Support-Fall abzuschließen.

>[!NOTE]
>
>Sobald die Vergrößerung geplant ist, passt ein automatisiertes System die Größe Ihrer Cloud-Instanz an. Sie erhalten möglicherweise keine Ticket-Benachrichtigung, wenn der Vorgang abgeschlossen ist. Sie können das Tool Observation for Adobe Commerce verwenden, um Ihre AWS- oder Azure-Instanztypen anzuzeigen [die Änderung zu &#x200B;](https://experienceleague.adobe.com/en/docs/commerce-knowledge-base/kb/how-to/check-vcpu-using-observation-for-adobe-commerce).

## Verlauf der Upsides anzeigen

Sie können den Verlauf der angeforderten Größenänderungen anzeigen, indem Sie die Informationen von Ihrem **CSM (Customer Success Manager) anfordern**.
Für jede Größenänderungsanfrage stehen die folgenden Informationen zur Verfügung:

* **Startdatum der Größe**: Datum der Upsize-Anfrage.
* **Enddatum der Größe**: Datum, an dem der Cluster seine vorherige Größe zurückerhalten hat.
* **vCPU-**: Die Größe des Clusters nach der Vergrößerung.
* **Tage Nutzung**: für wie viele Tage der Cluster im Upsizer verblieben ist.
* **Zeitraum vCPU**: Die vCPU-Größe wurde um die Anzahl der Tage geändert, die sie verwendet wurde. (Beispiel: vCPU-Größe 192 x 25 Tage entspricht 4.800).


## Verwandtes Lesen

* Informationen, Methoden und Beispiele zum Messen und Verbessern der Site-Leistung finden Sie in den folgenden ausführlichen Artikeln in unserer Support-Wissensdatenbank:
   * [CPU-Zuordnungsberechnung für Adobe Commerce in Cloud Service](/docs/commerce-knowledge-base/kb/how-to/magento-commerce-cloud-cpu-allocation-calculation.html)
   * [Überprüfen, ob für Adobe Commerce on Cloud ein Upsize für die Instanzen des Hosts erforderlich ist](/docs/commerce-knowledge-base/kb/how-to/magento-commerce-cloud-check-if-upsize-for-hosts-instances-is-needed.html)
   * [Überprüfen der CPU-Konfiguration des Hosts für Adobe Commerce on Cloud Service](/docs/commerce-knowledge-base/kb/how-to/magento-commerce-cloud-check-hosts-cpu-configuration.html)
* Informationen zum Ermitteln von Ausfällen finden Sie unter [Ermitteln und Messen von Ausfällen für Adobe Commerce on Cloud](/docs/commerce-knowledge-base/kb/how-to/how-to-identify-outages.html) in unserer Support-Wissensdatenbank.
* Informationen zur Verbesserung der Site-Leistung, um die Notwendigkeit zu vermeiden, einen Kapazitätszuwachs zu nutzen, finden Sie in diesen Artikeln in unserer Entwicklerdokumentation:
   * [Bildgröße](/docs/commerce-admin/catalog/products/digital-assets/product-image-config.html#product-image-resizing)
   * [Vollständige Seitenzwischenspeicherung](/docs/commerce-admin/systems/tools/cache-management.html#full-page-caching)
   * [ECE-Tools](/docs/commerce-cloud-service/user-guide/dev-tools/ece-tools/package-overview.html)
