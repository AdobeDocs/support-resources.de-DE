---
title: Skalierbarkeit und Kapazitätsplanung
description: Empfehlungen zur Skalierbarkeit und Kapazitätsplanung, damit Adobe Commerce-Händler ihre Umgebungen für Ereignisse mit hohem Traffic-Aufkommen wie die Weihnachtssaison vorbereiten können.
feature-set: Commerce
feature: Support
solution: Commerce
role: Developer, Admin, Leader
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
  - id: 5a951749-fac9-5bc7-9a98-ebe4ff066437
    internal-label: Cloud
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
source-git-commit: 71589dd124714805fbf844540fb2d272433631ee
workflow-type: tm+mt
source-wordcount: '413'
ht-degree: 0%
---

# Skalierbarkeit und Kapazitätsplanung

Dieser Abschnitt enthält technische Empfehlungen zur Skalierung von Adobe Commerce-Umgebungen, um sich auf Ereignisse mit hohem Traffic wie die Weihnachtszeit vorzubereiten.

>[!NOTE]
>
>Die mit **(nur Cloud) gekennzeichneten** gelten für Commerce in der Cloud-Infrastruktur. Die meisten anderen Empfehlungen gelten auch für lokale Bereitstellungen.

## Frühzeitiges Planen der Cluster-Vergrößerung (nur Cloud) {#plan-cluster-upsize-early}

Für Kunden mit Commerce auf Cloud-Infrastrukturen werden durch eine temporäre Cluster-Vergrößerung mehr Computing-Ressourcen zugewiesen, um Spitzen im Traffic in der Hochsaison zu bewältigen. Lösen Sie im Voraus ein Support-Ticket mit dem Datumsbereich und der erforderlichen Cluster-Größe aus und stimmen Sie sich mit Ihrem dedizierten Account Manager über den aktuellen Ressourcenverbrauch und die Anforderungen ab. Senden Sie die Anfrage mindestens 48 Geschäftsstunden vor der Kapazitätsanforderung - insbesondere für die Feiertagssaison sollten Sie die Anfrage so früh wie möglich einreichen, da die Kapazität während des Black Friday und des Cyber Monday begrenzt ist. Siehe [Anfordern einer temporären Upsize-](https://experienceleague.adobe.com/de/docs/support-resources/adobe-support-tools-guide/adobe-commerce-support/how-to-request-temporary-adobe-commerce-on-cloud-infrastructure-upsize).

Ein Pro-Architecture-Kunde mit einer täglichen Grundlinie von 24 Kernen (24 vCPUs, 96 GB RAM), die für 7 Tage auf 96 Kerne aufgestockt wird, würde etwa das 4-fache der Ressourcen (96 vCPUs, 384 GB RAM) verbrauchen - ein inkrementeller Verbrauch von etwa 504 vCPU-Tagen (96×7 − 24×7).

## Schnelle Ursprungsabschirmung {#fastly-origin-shielding}

Die ursprüngliche Abschirmung von Adobe Commerce [!DNL Fastly] dient dazu, den Traffic direkt zur Adobe Commerce-Quelle zu reduzieren. Wenn eine Anfrage empfangen wird, prüft ein [!DNL Fastly] Edge-Speicherort (Point of Presence) auf zwischengespeicherte Inhalte und stellt diese bereit. Wenn er nicht zwischengespeichert wird, fährt er mit dem Shield-POP fort, um zu überprüfen, ob er dort zwischengespeichert ist. Wenn der Inhalt zuvor sogar von einem anderen globalen POP angefordert wurde, wird er zwischengespeichert. Schließlich wird sie, wenn sie nicht im Shield-POP zwischengespeichert wird, nur dann zum Ursprungs-Server weitergeleitet.

[!DNL Fastly] Ursprungsabschirmung kann in der Adobe Commerce Admin in den Backend-Einstellungen der [!DNL Fastly] aktiviert werden. Wählen Sie für optimale Leistung einen Schutzschild-Standort aus, der Ihrem Adobe Commerce-Ursprungs-Rechenzentrum am nächsten liegt. Weitere Informationen finden Sie unter [Konfigurieren von Backends und Ursprungsabschirmung](https://experienceleague.adobe.com/de/docs/commerce-on-cloud/user-guide/cdn/setup-fastly/fastly-custom-cache-configuration#configure-back-ends-and-origin-shielding).

Standardmäßig ist [!DNL Fastly] Ursprungsabschirmung nicht aktiviert.

## Durchführen von Lade- und Failover-Tests {#conduct-load-and-failover-tests}

Führen Sie vor größeren Kampagnen Belastungs- und Wiederherstellungstests durch, um Skalierungs- und Rollback-Pläne zu validieren.