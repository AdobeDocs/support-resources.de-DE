---
title: Übersicht über die Urlaubsbereitschaft in Adobe Commerce
description: Anleitung auf Führungsebene zur Vorbereitung von Adobe Commerce auf Cloud-Infrastrukturumgebungen für Ereignisse mit hohem Traffic-Aufkommen wie die Weihnachtszeit.
feature-set: Commerce
feature: Support
solution: Commerce
role: Developer, Admin, Leader
TQID: 'https://experienceleague.adobe.com/63svzoaJbKTgiO3iJR3iCyr4-slOLmt4QaVT2Y--NYI'
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
source-git-commit: 7ffe3c23f94b67342f02ed655d0a1700dd8f5a02
workflow-type: tm+mt
source-wordcount: '843'
ht-degree: 0%
---

# Übersicht über die Urlaubsbereitschaft in Adobe Commerce

Dieses Playbook bietet Anleitungen für die Vorbereitung von Adobe Commerce-Umgebungen auf Ereignisse mit hohem Traffic-Aufkommen, wie z. B. die Weihnachtssaison. Er fasst technische Empfehlungen in fünf strategischen Schwerpunktbereichen zusammen:

- Leistungsoptimierung
- Best Practices und Stabilität
- Überwachung und Beobachtbarkeit
- Skalierbarkeit und Kapazitätsplanung
- Einsatzbereitschaft

Diese Schwerpunktbereiche stellen sicher, dass Ihre Plattform bei Spitzenlast stabil, sicher und leistungsfähig bleibt.

## Leistungsoptimierung

Im Folgenden finden Sie einen Überblick über die empfohlenen Schritte, um eine optimierte Leistung sicherzustellen. Weitere Informationen finden Sie unter [Adobe Commerce Holiday Readiness > Leistungsoptimierung](/help/adobe-support-tools-guide/adobe-commerce-support/adobe-commerce-holiday-readiness-overview/performance-optimization.md).

* Optimieren Sie das Caching von Fastly-Anfragen: Normalisieren Sie Ihre Tracking-Parameter zu Werbezwecken, bestätigen Sie, dass Ihre Landingpages zwischenspeicherbar sind, und verwenden Sie GraphQL GET für PWA oder Headless-Storefronts, um Ihre Fastly-Cache-Trefferquote zu erhöhen.
* Fastly IO aktivieren: Schalten Sie Fastly Image Optimization und Deep IO ein, damit Bildtransformationen an der CDN-Kante anstatt am Ursprung ausgeführt werden und die Renderzeit der Seiten auf bildlastigen Storefronts verkürzt wird.
* L2-Cache aktivieren: Cache-Daten lokal auf jedem Web-Knoten speichern, um die Latenz zu reduzieren und Netzwerkaufrufe an Redis/Valkey je nach Adobe Commerce-Version zu reduzieren. Redis-Cache wird für Adobe Commerce 2.4.9 oder für Patch-Versionen nach 2.4.5-p16, 2.4.6-p14, 2.4.7-p9 und 2.4.8-p4 nicht unterstützt.
* Slave-Verbindungen aktivieren: Lese-lastige Abfragen an Replikatknoten mit `MYSQL_USE_SLAVE_CONNECTION` und `REDIS_USE_SLAVE_CONNECTION` oder `VALKEY_USE_SLAVE_CONNECTION` weiterleiten, sodass die Master-Datenbanken nicht der Engpass unter Last sind.
* Asynchrone Auftrags- und E-Mail-Verarbeitung aktivieren: Warteschlangenauftragsplatzierung, Rasteraktualisierungen für Bestelldaten und Checkout-E-Mails werden im Hintergrund über drei separate Einstellungen ausgeführt, sodass der Checkout bei hohem Auftragsvolumen schnell bleibt.
* Wechseln Sie zum Indexer-Update im Zeitplanmodus: Verschieben Sie Indexer von „Aktualisieren bei Speichern“ in den cron-gesteuerten Update im Zeitplanmodus, um das Sperren während häufiger Katalogaktualisierungen zu vermeiden - mit Ausnahme des Indexers „customer_grid“.
* Erwägen Sie eine skalierte (Split-)Architektur: Wenn durch Optimierung und Fehlerbehebungen auf Code-Ebene die CPU-Last weiterhin maximal ist, wechseln Sie zu einem sechsstufigen Setup mit sechs Knoten, das Web- und Datenbankknoten unabhängig skaliert.

## Best Practices und Stabilität

Im Folgenden finden Sie einen Überblick über Best Practices zur Gewährleistung der Stabilität Ihrer Instanz. Detaillierte Informationen zu den einzelnen Schritten finden Sie unter [Adobe Commerce Holiday Readiness > Best Practices und Stabilität](/help/adobe-support-tools-guide/adobe-commerce-support/adobe-commerce-holiday-readiness-overview/best-practices-stability.md).

* Aktualisieren Sie auf die neueste Adobe Commerce-Version: Behalten Sie eine unterstützte Version bei, um die Sicherheits- und Leistungsverbesserungen, die Adobe in jeder Version bereitstellt, beizubehalten.
* Installieren Sie die neuesten ECE-Tools und das Quality Patch Tool (QPT): Aktualisieren Sie die ECE-Tools mit ihren Abhängigkeiten und bestätigen Sie, dass die entsprechenden Quality Patches Tool-Fehlerbehebungen sowohl für Cloud- als auch für On-Premise-Installationen angewendet werden.
* Überprüfen und bereinigen Sie Protokolldateien: Entfernen Sie Debugging-Protokolle und überwachen Sie wiederkehrende Fehler, um eine übermäßige Nutzung der Festplatte zu verhindern und die Sichtbarkeit des Protokolls zu verbessern.
* Überwachen des Wachstums der Festplattengröße: Halten Sie die gemeinsam genutzten Dateien und Datenbankvolumes unter einer Auslastung von 70 %, damit das Speicherwachstum keinen Trigger eines Ausfalls verursacht.
* Überprüfen Sie langsame Datenbankabfragen: Verwenden Sie das APM-Tool und das MySQL-Protokoll für langsame Abfragen, um kostspielige Abfragen zu finden und zu beheben, bevor sie sich unter Spitzenverkehrszeiten verschlimmern.
* Cron-Aufträge korrekt konfigurieren: Bestätigen Sie, dass Cron minütlich unter dem richtigen Anwender ausgeführt wird, da jeder asynchrone Vorgang in Commerce davon abhängt.
* Optimieren Sie die Client-seitigen Einstellungen: Aktivieren Sie die Minimierung und Bündelung von CSS, JavaScript und HTML, um die Ladezeiten der Storefront zu verkürzen.

## Überwachung und Beobachtbarkeit

Im Folgenden finden Sie die empfohlenen Methoden zur Überwachung Ihrer Adobe Commerce-Instanz während der Hochsaison. Ausführliche Anweisungen für jede dieser Überwachungs- und Beobachtbarkeitsempfehlungen finden Sie unter [Adobe Commerce Holiday Readiness > Monitoring and Observability](/help/adobe-support-tools-guide/adobe-commerce-support/adobe-commerce-holiday-readiness-overview/monitoring-observability.md).

* Traffic mit New Relic überwachen: Verwenden Sie Fastly-Protokolle, die in New Relic gestreamt werden, um Traffic-Anomalien, missbräuchliche IPs, bösartige Anfragen, die auf Endpunkte wie Zahlungen abzielen, und Geräte-/Browser-Trends zu erkennen.
* Anpassen von New Relic-Warnhinweisen: Richten Sie zusätzlich zu den verwalteten Warnhinweisen von Adobe eigene NRQL-basierte Warnhinweise für ungewöhnlichen Traffic, langsame GraphQL-Abfragen oder steigende Fehlerquoten ein.
* Tracking des Apdex-Scores: Sehen Sie sich den Apdex-Score (Ziel ≥ 0,85) an, um die Backend- und Frontend-Antwortzeiten in einem Bereich zu halten, den Benutzer als zufriedenstellend betrachten.
* Support Insights überprüfen (SWAT-Bericht): Führen Sie vor und nach Spitzenzeiten einen SWAT-Bericht aus, um Risiken und Verbesserungsbereiche auf Systemebene zu identifizieren.

## Skalierbarkeit und Kapazitätsplanung

Detaillierte Informationen zu den einzelnen Empfehlungen für die Skalierbarkeit und Kapazitätsplanung finden Sie unter [Adobe Commerce Holiday Readiness > Skalierbarkeit und Kapazitätsplanung](/help/adobe-support-tools-guide/adobe-commerce-support/adobe-commerce-holiday-readiness-overview/scalability-capacity-planning.md).

* Frühzeitige Planung der Cluster-Vergrößerung: Fordern Sie mindestens 10 Werktage vor einer größeren Promotion eine temporäre Compute-Vergrößerung beim Adobe-Support an.
* Schnelle Ursprungsabschirmung aktivieren: Leiten Sie nicht zwischengespeicherte Anfragen über ein Shield-POP in der Nähe Ihres Ursprungs, sodass weniger Anfragen den Ursprungs-Server direkt treffen.
* Führen Sie Lade- und Failover-Tests durch: Testen Sie Lade- und Wiederherstellungsszenarien vor den wichtigsten Kampagnen, um zu bestätigen, dass Ihre Skalierungs- und Rollback-Pläne tatsächlich funktionieren.

## Einsatzbereitschaft

* Alle Sicherheits- und Leistungs-Patches anwenden: Patchen vor dem Einfrieren des Codes abschließen, damit Bereitstellungen später nicht unterbrochen werden.
* Führen Sie Konsistenzprüfungen vor dem Urlaub aus: Testen Sie Backups, Cron-Status und Cache-Aufwärmskripte, damit Vorgänge reibungslos unter Last ausgeführt werden können.
* Legen Sie Playbooks für die Überwachung fest: Dokumentieren Sie Warnschwellen, Eskalationspfade und Kontakte rund um die Uhr, damit das Team in Spitzenzeiten schnell reagieren kann.
* Dokument-Rollback-Pläne: Halten Sie versionierte Rollback-Strategien bereit, damit Sie eine schlechte Bereitstellung schnell wiederherstellen können.