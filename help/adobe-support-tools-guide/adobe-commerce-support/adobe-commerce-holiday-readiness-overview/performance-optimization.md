---
title: Leistungsoptimierung
description: Empfehlungen zur Leistungsoptimierung, um Adobe Commerce-Händler bei der Vorbereitung ihrer Umgebungen auf Ereignisse mit hohem Traffic-Aufkommen wie die Weihnachtszeit zu unterstützen.
feature-set: Commerce
feature: Support
solution: Commerce
role: Developer, Admin, Leader
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: cdfd3bc1-dc23-5cf0-b965-d3c0c55cde67
    internal-label: Best Practices
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
  - id: e8818fe6-9c8b-4bc0-9ef8-377a10b7bc75
    internal-label: Architecture
subfeature_v2:
  - id: f8ddfd3b-6194-46e8-a176-0e918039be56
    internal-label: Cloud architecture
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
source-git-commit: b2220ea4cb5a301cbee6cea5fb90d6dc8a05eeff
workflow-type: tm+mt
source-wordcount: '1698'
ht-degree: 0%
---

# Leistungsoptimierung

Dieser Abschnitt enthält technische Empfehlungen zur Vorbereitung von Adobe Commerce-Umgebungen - sowohl Commerce auf Cloud-Infrastrukturen als auch On-Premise - auf Ereignisse mit hohem Traffic-Aufkommen wie die Weihnachtszeit.

>[!NOTE]
>
>Die mit **(nur Cloud) gekennzeichneten** gelten für Commerce in der Cloud-Infrastruktur. Die meisten anderen Empfehlungen gelten auch für lokale Bereitstellungen.

## Optimieren der Fastly-Anfrage-Zwischenspeicherung (nur Cloud) {#optimize-fastly-request-caching}

[!DNL Fastly] speichert Antworten am Edge zwischen, um die Last auf dem Ursprungs-Server zu reduzieren. In der Hochsaison helfen Ihnen einige Konfigurationsprüfungen, diesen Cache optimal zu nutzen, insbesondere wenn Sie Werbeaktionen mit Tracking-Parametern oder einer Headless-Storefront ausführen. Die vollständige Konfigurationsreferenz finden Sie unter [Anpassen der Cache-Konfiguration](https://experienceleague.adobe.com/de/docs/commerce-on-cloud/user-guide/cdn/setup-fastly/fastly-custom-cache-configuration).

* Normalisieren von Tracking-Parametern: Während der Urlaubszeit führen Sie wahrscheinlich Social-Media- und Paid-Kampagnen durch, z. B. Google Ads, Facebook und X, an die eindeutige Tracking-Zeichenfolgen an jede URL angehängt werden. Jede eindeutige Zeichenfolge erstellt einen separaten Cache-Eintrag für dieselbe Seite, was die Cache-Trefferquote verringert. Fügen Sie diese Parameter der Liste **[!UICONTROL Ignorierte URL]** Parameter“ in der [!DNL Fastly]-Konfiguration in Adobe Commerce Admin hinzu, damit [!DNL Fastly] sie als gleichwertig behandeln.
* Vergewissern Sie sich, dass Ihre Landingpages zwischenspeicherbar sind: Überprüfen Sie die `x-cache` Antwort-Kopfzeile auf jeder Landingpage für eine Promotion. Eine zwischenspeicherbare Seite gibt bei nachfolgenden Ladevorgängen `HIT` oder ein `HIT`/`MISS`-Paar zurück. Wenn die Kopfzeile `MISS, MISS` zurückgibt, wird die Seite nicht zwischengespeichert und erfordert eine Untersuchung.
* Verwenden von GET-Anfragen für GraphQL-Abfragen: Wenn Sie eine PWA- oder Headless-Storefront ausführen, senden Sie GraphQL-Abfragen als `GET`-Anfragen, wobei die Abfrage in der URL enthalten ist, und nicht als `POST`. [!DNL Fastly] speichert nur `GET` Anfragen zwischen, bei denen die Abfrage Teil der URL ist. Eine `GET` Anfrage mit der im Hauptteil gesendeten Abfrage wird nicht zwischengespeichert.

>[!NOTE]
>
>Die Abschirmung der [!DNL Fastly] beeinflusst auch die Cache-Leistung. Konfigurationsdetails finden Sie unter [Fastly Origin Shielding](/help/adobe-support-tools-guide/adobe-commerce-support/adobe-commerce-holiday-readiness-overview/scalability-capacity-planning.md#fastly-origin-shielding).

## Fastly IO aktivieren (nur Cloud) {#enable-fastly-io}

[!DNL Fastly] IO verlagert die Größenanpassung und Formatkonvertierung auf das [!DNL Fastly] Edge Network anstatt auf den Adobe Commerce-Ursprung. Dies reduziert die Server-Last und verbessert die Geschwindigkeit des Seiten-Renderings für bildlastige Storefronts, ein häufiger Engpass in Verkaufszeiten mit hohem Traffic. Konfigurationsoptionen finden Sie unter [Fastly Image Optimization](https://experienceleague.adobe.com/de/docs/commerce-on-cloud/user-guide/cdn/fastly-image-optimization).

Bevor Sie beginnen, überprüfen Sie, ob die Ursprungsabschirmung konfiguriert ist. [!DNL Fastly] I/O erfordert eine Ursprungsabschirmung als Voraussetzung. Konfigurationsdetails finden Sie unter [Fastly Origin Shielding](/help/adobe-support-tools-guide/adobe-commerce-support/adobe-commerce-holiday-readiness-overview/scalability-capacity-planning.md#fastly-origin-shielding).

So aktivieren Sie [!DNL Fastly] E/A:

1. Gehen Sie in der Admin zur Seite **[!UICONTROL Fastly Configuration]** und wählen Sie **[!UICONTROL Konfigurieren]** neben **[!UICONTROL Default IO Config Options]**.
1. Vergewissern Sie sich, dass das [!DNL Fastly]-E/A-Snippet aktiviert ist.
1. Legen Sie in der **[!UICONTROL Bildoptimierung]**-Konfiguration **[!UICONTROL Deep-Bildoptimierung aktivieren]** auf *[!UICONTROL Ja]* fest. Mit dieser Einstellung wird die integrierte Bildgrößenanpassung von Adobe Commerce deaktiviert und die Aufgabe an [!DNL Fastly] übertragen.
1. Vergewissern Sie sich, dass die Position der Abschirmung korrekt eingestellt ist. Konfigurationsdetails finden Sie unter [Fastly Origin Shielding](#fastly-origin-shielding).

>[!NOTE]
>
>Durch die Tiefenbildoptimierung wird nur die Größe von Produktbildern geändert. CMS-Bilder wie Banner und Inhaltsbausteine sind davon nicht betroffen und verwenden weiterhin die integrierte Größenanpassung von Adobe Commerce.

Um sicherzustellen, dass [!DNL Fastly] E/A funktioniert, überprüfen Sie die Antwort-Header für eine Produktbildanforderung:

* Die `x-cache`-Kopfzeile gibt `HIT` zurück.
* Die `fastly-io-info`- und `fastly-stats` werden ausgefüllt.
* Die Bild-URL enthält kein `/cache/` Verzeichnis im Pfad.

## Redis L2-Cache implementieren {#implement-redis-l2-cache}

Implementieren Sie effektive Caching-Praktiken, damit Ihr Store während der Spitzenzeiten des Traffics zuverlässig funktioniert. [!DNL Redis] Der L2-Cache reduziert die Netzwerkbandbreite auf [!DNL Redis], indem Cache-Daten lokal auf jedem Web-Knoten gespeichert werden. Hintergrundinformationen zur Funktionsweise des L2-Cache finden Sie unter [Cache der Ebene 2](https://experienceleague.adobe.com/de/docs/commerce-operations/configuration-guide/cache/level-two-cache).

Aktivieren Sie dies in Commerce in der Cloud-Infrastruktur, indem Sie die Variable `REDIS_BACKEND`-Bereitstellung festlegen. Konfigurationsschritte finden Sie unter [REDIS_BACKEND](https://experienceleague.adobe.com/de/docs/commerce-on-cloud/user-guide/configure/env/stage/variables-deploy#redis_backend) im Handbuch Commerce on Cloud Infrastructure . Konfigurieren Sie ihn lokal direkt in `app/etc/env.php`.

>[!NOTE]
>
>[!DNL Redis] wird nicht als L2-Cache-Backend in Adobe Commerce 2.4.9 oder höher oder in Patch-Versionen nach 2.4.5-p16, 2.4.6-p14, 2.4.7-p9 oder 2.4.8-p4 unterstützt. Verwenden Sie in diesen Versionen stattdessen `VALKEY_BACKEND` .

## MySQL- und Redis-Slave-Verbindungen aktivieren (nur Cloud) {#enable-mysql-and-redis-slave-connections}

[!DNL Redis]- und [!DNL MySQL]-Slave-Verbindungen verlagern den Lese-Traffic auf Replikatknoten und reduzieren so die Last auf der primären Verbindung während Zeiten mit hohem Traffic. Konfigurationsschritte finden Sie unter [MYSQL_USE_SLAVE_CONNECTION](https://experienceleague.adobe.com/de/docs/commerce-on-cloud/user-guide/configure/env/stage/variables-deploy#mysql_use_slave_connection) und [REDIS_USE_SLAVE_CONNECTION](https://experienceleague.adobe.com/de/docs/commerce-on-cloud/user-guide/configure/env/stage/variables-deploy#redis_use_slave_connection) oder [VALKEY_USE_SLAVE_CONNECTION](https://experienceleague.adobe.com/de/docs/commerce-on-cloud/user-guide/configure/env/stage/variables-deploy#valkey_use_slave_connection), abhängig von Ihrer Adobe Commerce-Version.

### Redis Slave-Verbindungen

Eine [!DNL Redis]-Slave-Verbindung ist eine schreibgeschützte Verbindung zu einer [!DNL Redis]-Instanz, die es ermöglicht, Lese-Traffic von einem Nicht-Master-Knoten aus zu bedienen. Ohne diese Option kann es zu einem Engpass bei hoher Last kommen[!DNL MySQL] Überprüfen Sie [!DNL New Relic] APM-Übersichtsdiagramm für steigende Antwortzeiten als frühes Zeichen und bestätigen Sie dann auf der Registerkarte **[!UICONTROL Datenbank]** durch Sortieren nach der am meisten zeitaufwendigen Transaktion, um langsame [!DNL MySQL] `SELECT` Abfragen zu identifizieren. Aktivieren Sie dies, indem Sie die Bereitstellungsvariable `REDIS_USE_SLAVE_CONNECTION` auf `true` setzen.

>[!NOTE]
>
>`REDIS_USE_SLAVE_CONNECTION` wird nur in Staging- und Produktionsumgebungen pro Cluster unterstützt. Sie wird nicht für Starter- oder skalierte (geteilte) Architekturprojekte unterstützt. Die Aktivierung auf skalierter Architektur verursacht [!DNL Redis] Verbindungsfehler - verwenden Sie stattdessen [!DNL Redis] L2-Cache auf dieser Architektur. Siehe [Implementieren von Redis L2-Cache](#implement-redis-l2-cache-implement-redis-l2-cache) oben.

### MySQL-Slave-Verbindungen

Aktivieren Sie das `MYSQL_USE_SLAVE_CONNECTION`-Flag in Pro-Cluster-Umgebungen, um bestimmte schreibgeschützte Datenbankabfragen an eine Slave-Verbindung zu leiten, wodurch die Abfrageausführung von der Master-Verbindung abgeladen wird.

>[!CAUTION]
>
>Belastungstest vor der Aktivierung einer der beiden Einstellungen in der Produktion. In Umgebungen mit normaler Auslastung können Slave-Verbindungen die Leistung um 10 bis 15 Prozent verlangsamen. In Umgebungen mit hoher, anhaltender Belastung können sie die Leistung um einen ähnlichen Wert verbessern. Vor der Aktivierung unter dem erwarteten Traffic in der Hochsaison auswerten.

## Asynchrone Auftrags- und E-Mail-Verarbeitung aktivieren {#enable-asynchronous-order-and-email-processing}

Verwenden Sie die asynchrone Verarbeitung, um bestellungsbezogene Vorgänge mit hohem Volumen im Hintergrund in eine Warteschlange einzureihen und auszuführen und so die Frontend-Latenz während eines Spitzen-Traffics zu reduzieren. Dies umfasst drei miteinander verknüpfte, aber unterschiedliche Einstellungen. Einen Überblick finden [&#x200B; unter „Best Practices für &#x200B;](https://experienceleague.adobe.com/de/docs/commerce-operations/performance-best-practices/configuration) Konfiguration“.

* Asynchrone Bestellplatzierung: Das Modul für asynchrone Reihenfolge markiert eine Bestellung als empfangen, platziert sie in einer Warteschlange und verarbeitet Bestellungen beim ersten In-First-Out. Dies ist standardmäßig deaktiviert. Aktivieren Sie sie über die Befehlszeile:

  ```
  bin/magento setup:config:set --checkout-async 1
  ```

  Nach der Aktivierung sind die Bestelldetails nicht sofort verfügbar. Die Bestellung verbleibt in der Warteschlange, bis der `placeOrderProcess` Verbraucher sie anhand des (standardmäßig aktivierten) Inventars überprüft und aktualisiert. Bevor Sie dieses Modul deaktivieren, überprüfen Sie, ob alle asynchronen Bestellungen während des Fluges vollständig verarbeitet wurden. Weitere Informationen finden Sie unter [Best Practices für die Checkout-Leistung](https://experienceleague.adobe.com/de/docs/commerce-operations/performance-best-practices/high-throughput-order-processing).

* Asynchrone Auftragsdatenverarbeitung: Intensive Storefront-Verkäufe und intensive Auftragsverarbeitung können auf Datenbankebene zu Konflikten führen. Durch Aktivierung dieser Einstellung werden die beiden Traffic-Muster unterschieden, sodass Bestellungen in einem temporären Speicher platziert und ohne Kollisionen stapelweise in das Order Management-Raster verschoben werden. Dadurch werden die Raster für Bestellungen, Rechnungen, Lieferungen und Gutschriften nach Cron aktualisiert, sodass Sperren vermieden und die Verarbeitungszeit verkürzt wird. Um optimale Ergebnisse zu erzielen, konfigurieren Sie Cron so, dass es einmal pro Minute ausgeführt wird.

  >[!NOTE]
  > 
  >Wie Sie dies aktivieren, hängt von Ihrem Bereitstellungsmodus ab. Adobe Commerce in Staging- und Produktionsumgebungen der Cloud-Infrastruktur wird standardmäßig im Produktionsmodus ausgeführt, wobei diese Einstellung nicht über die Administratorin bzw. den Administrator verfügbar ist. Führen Sie im Produktionsmodus stattdessen `bin/magento config:set dev/grid/async_indexing 1` aus. Wechseln Sie im Standardmodus zu **[!UICONTROL Stores]** > **[!UICONTROL Configuration]** > **[!UICONTROL Advanced]** > **[!UICONTROL Developer]** > **[!UICONTROL Grid Settings]** und setzen Sie **[!UICONTROL asynchrone Indizierung]** auf *[!UICONTROL Enable]*.

  Weitere Informationen finden Sie [Geplante Bestellvorgänge](https://experienceleague.adobe.com/de/docs/commerce-admin/stores-sales/order-management/orders/order-scheduled-operations).

* Asynchrone E-Mail-Benachrichtigungen: Mit dieser Einstellung werden E-Mail-Benachrichtigungen zum Auschecken und zur Bestellverarbeitung in den Hintergrund verschoben. Aktivieren Sie sie unter **[!UICONTROL Stores]** > **[!UICONTROL Configuration]** > **[!UICONTROL Sales]** > **[!UICONTROL Sales Emails]** > **[!UICONTROL Allgemeine Einstellungen]** > **[!UICONTROL asynchroner Versand]**.

## Indexer für die zeitgesteuerte Aktualisierung konfigurieren {#configure-indexers-for-update-on-schedule}

Setzen Sie die Indexer so, dass sie im geplanten Modus ausgeführt werden, um eine Datenbanksperre zu vermeiden und die Reaktionsfähigkeit bei häufigen Katalogaktualisierungen zu verbessern. Weitere Informationen finden Sie unter [Best Practices für die Indexerkonfiguration](https://experienceleague.adobe.com/de/docs/commerce-operations/implementation-playbook/best-practices/maintenance/indexer-configuration).

Ein Indexer kann im Modus **[!UICONTROL Aktualisierung beim Speichern]** oder **[!UICONTROL Aktualisierung beim Zeitplan]** ausgeführt werden.

* **[!UICONTROL Bei Speichern aktualisieren]** indiziert sofort, wenn sich Kataloge oder andere Daten ändern. Es wird eine niedrige Update- und Browser-Intensität angenommen, was bei hoher Last zu erheblichen Verzögerungen und Nichtverfügbarkeit von Daten führen kann.
* **[!UICONTROL Update on Schedule]** wird für die Produktion empfohlen. Es speichert Informationen zu Datenaktualisierungen und -neuindizierungen im Hintergrund über einen dedizierten Cron-Auftrag.

Setzen Sie den Aktualisierungsmodus jedes Indexers unabhängig unter **[!UICONTROL System]** > **[!UICONTROL Tools]** > **[!UICONTROL Indexverwaltung]**.

>[!IMPORTANT]
>
>Die unterstützten Modi des `customer_grid`-Indexers hängen von Ihrer Adobe Commerce-Version ab. In Versionen vor 2.4.8 unterstützt das Kundenraster nur **[!UICONTROL Update beim Speichern]** - setzen Sie es nicht auf **[!UICONTROL Update beim Zeitplan]**. Unter Adobe Commerce 2.4.8 und höher unterstützt das Kundenraster beide Modi und standardmäßig **[!UICONTROL Planmäßig aktualisieren]**.

## Deaktivieren und Auswerten einer flachen Katalogtabelle {#disable-and-evaluate-catalog-flat-table}

Die Verwendung von flachen Tabellen für Produkte und Kategorien wird nicht empfohlen. Diese veraltete Funktion kann zu Leistungseinbußen und Indizierungsproblemen führen. Weitere Informationen finden Sie unter [Einfache Kataloge](https://experienceleague.adobe.com/de/docs/commerce-admin/catalog/catalog/catalog-flat).

Um den flachen Katalog zu deaktivieren, gehen Sie zu **[!UICONTROL Stores]** > **[!UICONTROL Configuration]** > **[!UICONTROL Catalog]** > **[!UICONTROL Catalog]** > **[!UICONTROL Storefront]**, setzen Sie **[!UICONTROL Flache Katalogkategorie verwenden]** auf *[!UICONTROL Nein]*, setzen Sie **[!UICONTROL Flaches Katalogprodukt verwenden]** auf *[!UICONTROL Nein]* und klicken Sie dann auf **[!UICONTROL Konfiguration speichern]**.

Einige Drittanbietermodule und -anpassungen erfordern flache Tabellen, um ordnungsgemäß zu funktionieren. Bewerten Sie die Auswirkungen und das Risiko, dass Sie diese Erweiterungen weiterhin verwenden, bevor Sie flache Tabellen deaktivieren.

## Skalierte (geteilte) Architektur berücksichtigen (nur Cloud) {#consider-scaled-split-architecture}

Wenn nach Anwendung der oben genannten Konfigurations- und Code-Level-Optimierungen die Leistung von Lasttests oder Live-Infrastruktur weiterhin eine Maximierung von CPU und anderen Ressourcen anzeigt, sollten Sie den Wechsel zu einer skalierten (Split-)Architektur erwägen. Weitere Informationen finden Sie unter [Skalierte Architektur](https://experienceleague.adobe.com/de/docs/commerce-on-cloud/user-guide/architecture/scaled-architecture).

>[!NOTE]
>
>Skalierte Architektur ist nur für Konten mit einem Pro 48-Cluster oder höher verfügbar.

Die Split-Tier-Architektur verwendet mindestens sechs Knoten: drei Service-Knoten mit den Ausführungen [!DNL OpenSearch] oder [!DNL Elasticsearch], [!DNL MariaDB] und [!DNL Redis] oder [!DNL Valkey] und drei Web-Knoten mit den Ausführungen `php-fpm` und `NGINX`.

* Dienstknoten können nur vertikal skaliert werden, indem sie die Servergröße (CPU und Speicher) erhöhen. Da der Datenbank-Cluster für hohe Verfügbarkeit entwickelt wurde, können Service-Knoten nicht zuverlässig horizontal skaliert werden.
* Web-Knoten können sowohl vertikal als auch horizontal skaliert werden und fügen Webserver hinzu, um das erhöhte Anfragevolumen zu verarbeiten.

Auf diese Weise können Sie die Infrastruktur bei Bedarf für Zeiträume mit hoher Auslastung erweitern und jede Ebene unabhängig skalieren. Wenden Sie sich an Ihr Adobe-Account-Team, um vor einer erwarteten starken Belastung auf die Split-Tier-Architektur umzustellen.
