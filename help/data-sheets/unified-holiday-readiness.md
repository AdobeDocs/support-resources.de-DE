---
title: Adobe DX Solutions Unified Holiday Readiness Guide
description: Dieser Artikel enthält eine Anleitung zur Urlaubsbereitschaft für DX-Lösungen.
solution: Experience Platform, Journey Optimizer, Customer Journey Analytics, Commerce, Experience Manager, Workfront, Campaign, Analytics, Target, Marketo Engage
role: Developer, Admin, Leader, User
source-git-commit: a5fe17df6ee6e9d23f82776d7200fba9f7d5f267
workflow-type: tm+mt
source-wordcount: '3813'
ht-degree: 2%

---

# Adobe DX Solutions Unified Holiday Readiness Guide


Der Adobe DX Solutions Unified Holiday Readiness Guide hilft Ihnen, sich auf die Weihnachtszeit vorzubereiten, indem er sich auf eine proaktive Planung statt auf eine reaktive Problemlösung konzentriert. Es enthält praktische Schritte, um sicherzustellen, dass Ihre Instanzen bereit sind, sodass potenzielle Probleme minimiert werden, bevor sie auftreten. Das Adobe-Team verfügt über technisches Know-how, eine breite Palette von Funktionen und bewährte Methoden, um Ihnen den richtigen technischen und strategischen Support und die richtige Anleitung zu bieten, sodass Ihr Unternehmen gut vorbereitet ist.

Befolgen Sie diese Best Practices, um sicherzustellen, dass Ihre Adobe-Lösungen für digitale Erlebnisse robust, sicher und bereit für Traffic zu Spitzenzeiten an Feiertagen sind:

* Planen Sie mehr Traffic ein.
* Vermeiden Sie größere Änderungen während der Spitzenzeiten. Planen Sie Aktualisierungen vor oder nach den Feiertagen.
* Verwenden Sie Dashboards und Warnhinweise, um die Leistung zu überwachen und Engpässe frühzeitig zu erkennen.
* Stellen Sie sicher, dass Ihre autorisierten Support-Kontakte auf dem neuesten Stand sind.
* [Kontaktieren Sie den Adobe Support](https://experienceleague.adobe.com/en/docs/learning-manager/using/faq/how-to-submit-support-ticket) wann immer möglich im Voraus.

Empfehlungen zu lösungsspezifischen Holiday Readiness von Adobe finden Sie in den folgenden Abschnitten.

* [Adobe Experience Platform](#aep)
* [Adobe Journey Optimizer](#ajo)
* [Adobe Customer Journey Analytics](#cja)
* [Adobe Commerce](#commerce)
* [Adobe Experience Manager](#aem)
* [Adobe Marketo](#marketo)
* [Adobe Workfront](#workfront)
* [Adobe Campaign](#campaign)
* [Adobe Analytics](#analytics)
* [Adobe Target](#target)

>[!NOTE]
>
>Klicken Sie auf die einzelnen Abschnitte, um sie zu erweitern.


## Handbuch zur Urlaubsbereitschaft für Adobe Experience Platform (AEP) {#aep}

+++**Klicken Sie, um die Empfehlungen zur Urlaubsbereitschaft für Adobe Experience Platform (AEP) anzuzeigen.**

Adobe Experience Platform (AEP) spielt eine entscheidende Rolle bei der Bereitstellung von Echtzeit-Kundenerlebnissen. Da die Weihnachtssaison näher rückt, ist es wichtig sicherzustellen, dass Ihre AEP-Implementierung für erhöhten Traffic, sichere Datenverarbeitung und skalierbare Aufnahme optimiert ist.

### Vorhersage der saisonalen Nachfrage

Zur Vorbereitung auf saisonale Traffic-Spitzen empfiehlt Adobe die Planung der Kapazität und die Überwachung der Aufnahme von Streaming-Profilen. Dazu gehört auch, das Datenvolumen zu prognostizieren und sicherzustellen, dass Ihr System mit einem erhöhten Durchsatz umgehen kann. Siehe [Kapazitäts- und Saisonverkehr planen](https://experienceleague.adobe.com/en/docs/experience-platform/dataflows/ui/monitor-streaming-profile) als Referenz.

### Für Skalierung vorbereiten

Adobe bietet mehrere Strategien, um sicherzustellen, dass Ihre Umgebung für Urlaubs-Traffic bereit ist:

* Erhöhen der zugewiesenen Kapazität für Sandboxes.
* Ermitteln Sie Datenflüsse mit hohem Durchsatz im [Überwachungs-Dashboard](https://experienceleague.adobe.com/en/docs/experience-platform/dataflows/ui/monitor-streaming-profile) und wenden Sie bei Bedarf Einschränkungen oder Filter an.
* Verwenden Sie die Batch-Aufnahme für Anwendungsfälle mit geringerer Latenz, um die Leistung zu optimieren, wie [Lizenznutzung und -kapazitäten: Best Practices für das Streaming-Durchsatz](https://experienceleague.adobe.com/en/docs/experience-platform/landing/license/capacity#suggestions) beschrieben.

Diese Methoden helfen, die Aufnahmezuverlässigkeit aufrechtzuerhalten und die Latenz während der Spitzenzeiten zu reduzieren.

### Best Practices und Leitplanken

Um innerhalb der betrieblichen Grenzen zu bleiben und Service-Unterbrechungen zu vermeiden, empfiehlt Adobe die folgenden Aufnahme- und Profil-Leitplanken:

* [Best Practices für Streaming-Durchsatz](https://experienceleague.adobe.com/en/docs/experience-platform/landing/license/capacity#suggestions)
* [Schutzmaßnahmen bei der Datenaufnahme](https://experienceleague.adobe.com/de/docs/experience-platform/ingestion/guardrails)
* [Standardleitlinien für Echtzeit-Kundenprofildaten und Segmentierung](https://experienceleague.adobe.com/de/docs/experience-platform/profile/guardrails)
* [AEP-Blueprints: Leitplanken](https://experienceleague.adobe.com/en/docs/blueprints-learn/architecture/architecture-overview/guardrails)

### Sicherheit und Governance

Adobe legt Wert auf strenge Sicherheits- und Governance-Praktiken, insbesondere in Zeiten hohen Traffics, wenn die Vertraulichkeit der Daten erhöht wird.

Unter [Governance, Datenschutz und Sicherheit in Adobe Experience Platform: Sicherheit](https://experienceleague.adobe.com/en/docs/experience-platform/landing/governance-privacy-security/overview#security) finden Sie Empfehlungen zum Schutz von Kundendaten, zur Durchsetzung von Datenschutzkontrollen und zur Einhaltung der Vorschriften in Ihrer gesamten AEP-Implementierung.

Mithilfe dieser Richtlinien und der öffentlichen Dokumentation von Adobe können Unternehmen sicherstellen, dass ihr Adobe Experience Platform robust, sicher und bereit ist, während der gesamten Weihnachtssaison außergewöhnliche Kundenerlebnisse bereitzustellen.

+++

## Handbuch zur Urlaubsbereitschaft für Adobe Journey Optimizer (AJO) {#ajo}

+++**Klicken Sie, um die Empfehlungen zur Urlaubsbereitschaft für Adobe Journey Optimizer (AJO) anzuzeigen.**


Um Adobe Journey Optimizer auf die Weihnachtszeit vorzubereiten, sollten Unternehmen Ereignisspitzen und eine kanalübergreifende Komplexität antizipieren, Journey- und Häufigkeitsregeln konfigurieren und eine Datenhygiene- und Entscheidungslogik sicherstellen. Außerdem müssen sie die Leistung in großem Umfang validieren, Sicherheits- und API-Leitplanken durchsetzen und Erkenntnisse aus der Zeit nach Spitzenzeiten anwenden, um zukünftige Kampagnen zu verfeinern.

### Prognostizieren des Bedarfs

* Basierend auf der Komprimierung der Weihnachtssaison und dem höheren Kampagnenvolumen können Sie Folgendes erwarten:
   * Eine Spitze bei Echtzeit-Ereignissen und ausgelösten Journey (Warenkorbabbruch, Last-Minute-Angebote)
   * Sättigungsrisiken bei Nachrichten (höhere Opt-outs, Ermüdung)
   * Erhöhte Cross-Channel-Komplexität (E-Mail + Push + SMS + In-App)
* Verwenden Sie die Metriken des letzten Jahres (Öffnungs-/Klick-/Abmelderaten, Journey-Eintrittvolumen), um die erwartete Auslastung zu modellieren und Schwellenwerte für Ihre Messaging-Systeme festzulegen.
* Identifizieren Sie wahrscheinliche „ruhige Fenster“ oder Zeiten geringer Leistung (z. B. Wochenenden, Urlaubstage) und planen Sie die Versandvolumen entsprechend.

### Für Skalierung vorbereiten

* Stellen Sie sicher, dass alle Kanalkonfigurationen in AJO ordnungsgemäß eingerichtet sind: E-Mail, Push, SMS, Web, In-App. Siehe [Einrichten von Kanalkonfigurationen](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/configuration/channel-surfaces).
* Konfigurieren Sie Regeln zur Frequenzlimitierung und -limitierung, um das Nachrichtenvolumen zu kontrollieren. Siehe den Artikel [Frequenzlimitierung](https://experienceleague.adobe.com/de/docs/journey-optimizer-learn/tutorials/configuration/business-rules/configure-frequency-capping-rules) .
* Konfigurieren von Kanal-/Journey-Regelsätzen: siehe [Arbeiten mit Regelsätzen](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/conflict-prioritization/capping-rules/rule-sets).
* Bereiten Sie Ihre Datenhygiene-/Echtzeit-Ereignis-Streams und Segmentierungs-Frameworks vor.
* Stellen Sie sicher, dass Sie Audiences für Feiertagskampagnen definiert haben, z. B.:
   * Hochwertige Kunden
   * Treue Segmente
   * Warenkorbabgänger
   * Erstkäufer
* Laden Sie Vorlagen für Feiertage-Journey vorab oder bereiten Sie sie vor. Nutzen Sie die Entscheidungslogik (Angebote/Einschränkungen), um sie dynamisch auf der Grundlage von Inventar, zeitabhängigen Angeboten und Kanalpräferenzen anzupassen. Siehe dazu das Beispiel im Artikel [Hinzufügen von Einschränkungen zu Angeboten](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/decisioning/offer-decisioning/managing-offers-in-the-offer-library/configure-offers/add-constraints) .
* Technische Bereitschaft: Bestätigung der API/Endpunkt-Ladekapazität, Drosselungs-/Begrenzungsregeln für benutzerdefinierte Aktionen und externe Integrationen. Siehe [Leitplanken und Einschränkungen](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/get-started/guardrails).

### Testen und Validieren

* Verwenden Sie Ihr Experimentier-Framework, um wichtige Variablenänderungen zu testen:
   * Versandzeit
   * Angebotstyp
   * Kanalmix
Siehe [Best Practices für AJO Experimentation Accelerator](https://experienceleague.adobe.com/en/docs/experimentation-accelerator/using/get-started/experiment-accelerator-best-practices).
* End-to-End-Journey-Validierung durchführen:
   * Ereignis-Trigger
   * Segmentierungseintrag
   * Journey-Pfadflüsse
   * Personalisierungslogik
   * Angebotsbegrenzungen
   * Ausstiegskriterien
* Überprüfen Sie Begrenzungs- und Konfliktregeln. Siehe den Artikel [Journey-Begrenzung und Schlichtung](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/conflict-prioritization/journey-capping) .
* Belastungstest für skalierte Volumes für Spitzen-Sendevorgänge oder Spitzen: Simulieren Sie Volumina mit hohem Trigger, um das Systemverhalten unter Last zu überprüfen.
* Validieren der Zustellbarkeit: Aufwärmen von E-Mail-Domains/-Absendern, Bestätigen der Mobile-Push-Konfigurationen und Überprüfen der Fallback-Kanäle für SMS/In-App.

### Best Practices

* Verwenden Sie die Omni-Channel-Orchestrierung. Lesen Sie den Blog-Artikel [Essential Omnichannel Customer Journey for Engagement and Growth](https://business.adobe.com/blog/essential-customer-journeys-for-omnichannel-engagement) der ein Beispiel für eine Weihnachtssaison mit AJO zeigt.
* Priorisieren Sie gegebenenfalls Echtzeit-Trigger . Beispiel: Warenkorbabbruch, Durchsuchen, Abbruch und Warnmeldungen, da Urlaubskäufer reaktiver sind.
* Nutzen von Segmentierung und Personalisierung: Targeting von zielgerichteten Segmenten, Anpassung von Angeboten an das Kaufverhalten der Vergangenheit und an Präferenzen.
* Minimale Nachrichtenermüdung: Erzwingen Sie Begrenzungen und ruhige Stunden, um eine Überforderung zu vermeiden. Siehe den Blogpost [Erhöhen des Kundenerlebnisses mit täglicher Frequenzlimitierung in ](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer-blogs/elevate-customer-experience-with-daily-frequency-capping-in-ajo/ba-p/761510)AJO&quot;.
* Timing ist wichtig: Der Plan wird früher im Urlaubsfenster gesendet (angesichts der komprimierten Saison) und die Kanäle werden an die Zeitzonen und das Verhalten der lokalen Zielgruppe angepasst.
* Bieten Sie dynamische/zeitlich begrenzte Angebote an, um Dringlichkeit zu erzeugen, aber koordinieren Sie sie kanalübergreifend, um Duplizierungen und Konflikte zu vermeiden.
* Verwenden Sie die Unterdrückungslogik: Unterdrücken Sie Zielgruppen, die gerade gekauft haben, oder wenden Sie Journey nach dem Kauf an, um redundante Nachrichten zu vermeiden.

### Sicherheit und Governance

* Stellen Sie sicher, dass Zugriffssteuerung und Berechtigungen so konfiguriert sind, dass nur erforderliche Benutzende Journey bereitstellen oder Geschäftsregeln ändern können.
* Überwachen und Erzwingen der API-Aufruf-/Verbindungs-Begrenzung: Siehe z. B. die [Begrenzungs-API | Adobe Journey Optimizer](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/connect-systems/external-systems/capping)-Artikel.
* Verwenden Sie saubere First-Party-Daten und stellen Sie eine ordnungsgemäße Identitätszuordnung sicher, sodass Messaging nicht dupliziert/falsch ausgerichtet wird.
* Um sicherzustellen, dass Zustellbarkeits-Domains erwärmt werden, sind Anti-Spam-Maßnahmen vorhanden, insbesondere für Sendungen mit hohem Versandvolumen.
* Überprüfen Sie Auditprotokolle und Journey-Änderungen häufig in der Hauptsaison, um Fehler oder fehlerhafte Journey frühzeitig zu erkennen.

### Lernprogramme nach Spitzenzeiten

* Führen Sie nach Spitzenbelastungen eine Überprüfung der Journey-Einstiegszahlen, Unterdrückungszahlen, Opt-out-Raten, Zustellbarkeitsmetriken und der Kanalleistung durch.
* Bereinigen Sie unterdrückte Segmente und pausieren oder deaktivieren Sie Journey, die für das Feiertagsfenster erstellt wurden, um Übertragungsmüdigkeit zu vermeiden.
* Verwenden Sie Einblicke aus der Echtzeit-Performance, um die Planung für das nächste Jahr zu verfeinern (z. B. Sendezeitanpassungen, Kanalmix und Nachrichtenvolumen).

Durch proaktive Vorhersage der saisonalen Nachfrage, Konfiguration von Kanälen und Regeln, Validierung der Journey-Performance und Durchsetzung von Sicherheit und Governance können Unternehmen sicherstellen, dass Adobe Journey Optimizer während dieser und darüber hinaus nahtlose, personalisierte und zuverlässige Kundenerlebnisse bereitstellt.

+++

## Handbuch zur Urlaubsbereitschaft für Customer Journey Analytics (CJA) {#cja}

+++**Klicken Sie, um die Empfehlungen zur Urlaubsbereitschaft für Customer Journey Analytics (CJA) anzuzeigen.**

Customer Journey Analytics verwendet die 5 PS, um Urlaubs-/Spitzensaisonbereitschaft zu erzielen.

### Für Skalierung vorbereiten

* Überprüfen Sie CJA-Verbindungen und -Datenansichten und stellen Sie fest, welche Verbindungen und Datenansichten eine erweiterte Überwachung und Bereitstellung erfordern.
* Bestätigen Sie, dass die Bereitstellung für die Weihnachtsskalierung ausreicht, und skalieren Sie kritische Verbindungen und Datenansichten nach Bedarf. Weitere Informationen finden [ unter ](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-connections/manage-connections) von Verbindungen .

### Überwachen der Leistung

* Nutzen Sie den RAM ([[!UICONTROL Reporting Activity Manager] Übersicht](https://experienceleague.adobe.com/en/docs/analytics-platform/using/reporting-activity-manager/reporting-activity-overview)), um aktive Berichtsanfragen und Berichtsanfragen in der Warteschlange in Echtzeit zu überwachen, Kapazitätsverbindungen zu identifizieren und Engpässe zu erkennen.
* Achten Sie mit den Artikeln [Handbuch zur Fehlerbehebung und ](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-workspace/workspace-faq/error-messages)Bekannte Einschränkungen[ auf eine erhöhte Latenz bei ](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-workspace/workspace-faq/aw-limitations).
* Administratoren können lange laufende/blockierte Anforderungen über den RAM vorab aussetzen oder abbrechen. Siehe den Artikel [Abbrechen von Berichtsanfragen in CJA](https://experienceleague.adobe.com/en/docs/analytics-platform/using/reporting-activity-manager/reporting-activity-cancel-requests).

### Best Practices

* Planen Sie Exporte/Berichte in Zeiten geringen Traffics, um das Laden zu erleichtern und die Latenz zu minimieren. Siehe den Artikel [Geplante Berichte](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-components/scheduled-projects-manager) .
* Spread-out-Anfragen: Planen Sie Berichte in verschiedenen Intervallen über den Tag.
* Reduzieren Sie Bedienfelder, vereinfachen Sie Segmente, verkürzen Sie Datumsbereiche und vermeiden Sie überschüssige gleichzeitige Aufträge. Weitere Informationen finden [ im Artikel „Optimieren der Leistung ](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-workspace/workspace-faq/optimizing-performance) CJA Workspace&quot; .

### Fehlerbehebung

* Informationen zur Fehlerbehebung bei Fehlern im Arbeitsbereich finden Sie unter Fehlermeldungen für die Ursache und empfohlene Aktionen; verwenden Sie RAM ([!UICONTROL Reporting Activity Manager]), um Engpässe zu beheben und die gleichzeitige Nutzung effektiv zu verwalten. Weitere Informationen finden Sie unter [Fehlerbehandlung ](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-workspace/workspace-faq/error-messages) CJA Workspace .
* Verwenden Sie RAM ([[!UICONTROL Reporting Activity Manager] in CJA](https://experienceleague.adobe.com/en/docs/analytics-platform/using/reporting-activity-manager/reporting-activity-overview)), um problematische Benutzende, Abfragen oder Projekte zu identifizieren, Prioritäten zu setzen und nach Bedarf zu beenden/abzubrechen.

### Lernprogramme nach Spitzenzeiten

* Überprüfen Sie nach den Feiertagen/Spitzenzeiten die Leistungs- und Vorfallsprotokolle, um die Auswirkungen der bereitgestellten Best Practices zu bewerten.
* Überprüfen Sie langsame Abfragen und Benutzeraufgaben, um Muster/Trends zu identifizieren, die für die nächste Saison optimiert werden können.
* Sammeln Sie Feedback von Benutzern und Stakeholdern - aktualisieren Sie Ihre eigenen Runbooks und Bereitschaftspläne mit neu gewonnenen Erkenntnissen.
* Geben Sie den Adobe-Teams Feedback über Ihr Account-Team.

+++

## Handbuch für Adobe Commerce Holiday Readiness {#commerce}

+++**Klicken Sie, um die Empfehlungen zur Urlaubsbereitschaft für Adobe Commerce anzuzeigen.**

Um sicherzustellen, dass Ihr Unternehmen in der Hochsaison erfolgreich ist, müssen Sie Ihre digitale Adobe Commerce-Storefront auf hohen Traffic vorbereiten.

### Prognostizieren des Bedarfs

* Während der Hauptsendezeit (von Mitte November bis Mitte Januar) empfiehlt Adobe allen Adobe Commerce-Händlern, die auf unserer Cloud-Infrastruktur gehostet werden, proaktiv einen Anstieg der Besucherzahlen zu planen, indem sie Anfragen zur Bereitstellung von Holiday Surge-Kapazität einreichen. Weitere [ finden Sie unter „Holiday Surge Capacity Requests for Adobe Commerce ](https://experienceleague.adobe.com/en/docs/commerce-knowledge-base/kb/announcements/commerce-announcements/holiday-surge-capacity-requests-for-magento-commerce-cloud) unserer Cloud-Infrastruktur“.

### Für Skalierung vorbereiten

Befolgen Sie die Empfehlungen im [Planen und Schwenken: Ein strategischer Ansatz für die Hauptsaison 2025](https://experienceleague.adobe.com/en/perspectives/planning-and-pivoting-a-strategic-approach-to-peak-season-2025) , der praktische Strategien mit Adobe Commerce (und optionalen Adobe Experience Cloud-Tools) bietet, mit denen Sie während der geschäftigsten Zeit des Jahres herausragende Kundenerlebnisse planen, verschwenken und bereitstellen können.

### Best Practices

* Befolgen Sie die Anleitung von Adobe [So bereiten Sie Ihre Infrastruktur auf hohen Traffic vor - die 5 PS der Spitzenleistung in der Saison](https://business.adobe.com/blog/how-to/the-5-ps-of-peak-season-performance-a-guide-to-preparing-your-infrastructure-for-high-traffic).
* Unter [Technische Tipps für Commerce Holiday Readiness](https://experienceleague.adobe.com/en/docs/commerce-knowledge-base/kb/how-to/tech-tips-for-commerce-holiday-readiness) finden Sie Tipps, wie Sie Ihre Infrastruktur auf hohen Traffic vorbereiten, Ausfallzeiten verhindern und die Leistung während der Feiertage optimieren können.

+++

## Handbuch zur Urlaubsbereitschaft für Adobe Experience Manager (AEM) {#aem}

+++**Klicken Sie, um die Empfehlungen zur Urlaubsbereitschaft für Adobe Experience Manager (AEM) anzuzeigen.**

Die Weihnachtssaison rückt immer näher, und für viele Adobe-Kunden bedeutet dies den Beginn von Spitzenumsatzzeiten. In unserem Engagement für Ihren Erfolg möchten wir sicherstellen, dass Sie auf den bevorstehenden Anstieg des Traffics umfassend vorbereitet sind.

### Adobe Experience Manager (AEM) Cloud Services

Wenn Ihr Unternehmen während der Urlaubszeit die geschäftigsten Momente erlebt, überlegen Sie sich vielleicht, wie Sie Ihre Adobe Experience Manager-Site optimieren können, um Spitzenverkehrszeiten zu bewältigen. Glücklicherweise ist Ihre Site mit Adobe Experience Manager Cloud Services bereits mit der Möglichkeit zur automatischen Skalierung ausgestattet, sodass Ihre Besuchenden ein nahtloses Erlebnis erhalten, unabhängig davon, ob es zu plötzlichen Traffic-Änderungen kommt.

#### Für Skalierung vorbereiten

* Ausführliche Einblicke und Anleitungen zur Vorbereitung auf hohen Traffic mit Adobe Experience Manager Cloud Services finden Sie unter den folgenden Links:

   * [CDN in AEM as a Cloud Service](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/content-delivery/cdn)
   * [AEM as a Cloud Service-Caching](https://experienceleague.adobe.com/en/docs/experience-manager-learn/cloud-service/caching/overview)

* Wenn Sie Ultimate Success-Kunde sind und kürzlich Informationen zu Volumenprognosen mit Ihrem Adobe-Konto-Team geteilt haben, machen Sie sich keine Gedanken darüber, wie Sie diese Informationen erneut an uns senden können, da wir bereits eine Ansicht haben.

Wir sind hier, um Sie bei jedem Schritt Ihres Journey zu unterstützen. Wenn Sie Fragen oder Bedenken haben, können Sie [ein Support-Ticket einreichen](https://experienceleague.adobe.com/en/docs/learning-manager/using/faq/how-to-submit-support-ticket).

Um sich auf eine Marketing-Kampagne in der Weihnachtszeit vorzubereiten, lesen Sie die Dokumentation [AEMaaCS-Benutzerhandbuch: Einführung - Parameter von Marketing-Kampagnen](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/content-delivery/caching#marketing-parameters).

#### Sicherheit und Governance

Informationen zu Traffic-Sicherheit/-Schutz für AEM-Websites finden Sie im Artikel [Übersicht - Schutz von AEM](https://experienceleague.adobe.com/de/docs/experience-manager-learn/cloud-service/security/traffic-filter-and-waf-rules/overview) in den AEM as a Cloud Service-Tutorials.

#### Urlaubsplanung

Adobe verfügt über geplante Ausschlusszeiträume für Wartungsarbeiten, um einen unterbrechungsfreien Service während wichtiger Feiertage zu gewährleisten:

* **Keine automatischen Aktualisierungen** erfolgt zwischen:
   * &#x200B;24. November 2025 - 2. Dezember 2025
   * &#x200B;15. Dezember 2025 - 2. Januar 2026

Dadurch ist die Stabilität in verkehrsstarken Zeiten gewährleistet. Vollständige Versionsplanungen und Wartungsfenster finden Sie in der [AEM-Versions-Roadmap](https://experienceleague.adobe.com/en/docs/experience-manager-release-information/aem-release-updates/update-releases-roadmap).


### Adobe Experience Manager (AEM) mit Adobe Managed Services (AMS)

AEM-Kunden, die Adobe Managed Services nutzen, können proaktiv mit ihren CSEs zusammenarbeiten, um die Abdeckung der Feiertage zu planen.

++++

## Adobe Marketo Holiday Readiness Guide {#marketo}

+++**Klicken Sie, um die Empfehlungen für die Urlaubsbereitschaft von Adobe Marketo anzuzeigen.**

Um den Erfolg von Feiertagskampagnen mit Adobe Marketo sicherzustellen, sollten Teams die E-Mail-Authentifizierungseinstellungen überprüfen, ihre Datenbank bereinigen und schützen, die Kampagnenlogik und -planung optimieren, das E-Mail-Rendering und die Zustellbarkeit gründlich testen und die Support-Bereitschaft für Spitzenleistung und Interaktion optimieren.

### Für Skalierung vorbereiten

* Überprüfen Sie Ihre SPF/DKIM-Einstellungen und stellen Sie sicher, dass alles noch eingerichtet ist und ordnungsgemäß funktioniert. Weitere Informationen finden [ im Artikel „Einrichten von SPF und DKIM für die Zustellbarkeit ](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/email-marketing/deliverability/set-up-spf-and-dkim-for-your-email-deliverability) E-Mails“.
* Prüfen und bereinigen Sie Ihre Marketo-Datenbank, indem Sie inaktive/ungültige Einträge bereinigen. Dadurch erhöhen sich die Chancen, dass Ihre E-Mails in die Posteingänge Ihrer umsatzbereiten Leads gesendet werden. Weitere Informationen finden Sie im Artikel [Konsistenzprüfung der Marketo-Datenbank und wie man sie ](https://nation.marketo.com/t5/champion-program-blogs/marketo-database-health-check-up-amp-how-to-keep-it-clean/ba-p/323563).
* Vergewissern Sie sich, dass Ihre Team-Mitglieder über die erforderlichen Berechtigungen verfügen, um Aufgaben auszuführen und unbeabsichtigten Zugriff oder Änderungen an den E-Mails zu verhindern. Unabhängig davon, ob Sie Änderungen über den **[!UICONTROL Admin]** oder die **[!UICONTROL Admin Console]** vornehmen, sind Sie bei uns bestens aufgehoben. Siehe den [Verwalten von Benutzerrollen und Berechtigungen](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/administration/users-and-roles/managing-user-roles-and-permissions) .
* Überprüfen Sie Ihre Launchpad-Integrationen, um eine korrekte Authentifizierung sicherzustellen und mögliche Fehler zu beheben, bevor sie verwendet werden. Siehe den Artikel [Marketo-Entwicklerhandbuch: ](https://experienceleague.adobe.com/en/docs/marketo-developer/marketo/rest/authentication).

### Best Practices

Effizienz beginnt damit, dass wir genau verstehen, wie Marketo Kampagnen priorisiert und verarbeitet. Geben Sie Ihren Kampagnen das Geschenk der Geschwindigkeit mit diesen Optimierungstipps.

* Es ist wichtig zu verstehen, wie Marketo die Verarbeitung von Kampagnenflussschritten priorisiert, um zu vermeiden, dass dringende E-Mails oder E-Mails mit hoher Priorität versehentlich verzögert werden. Siehe den [Funktionsweise der Kampagnenverarbeitung](https://nation.marketo.com/t5/knowledgebase/how-campaign-processing-works/ta-p/248264).
* Achten Sie auf die Logik intelligenter Listen, um sicherzustellen, dass Ihre Kampagnen schnell und mit Spitzenleistung ausgeführt werden. Siehe den Artikel [Best Practices für Smart Lists](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/core-marketo-concepts/smart-lists-and-static-lists/creating-a-smart-list/best-practices-for-smart-lists).
* **[!UICONTROL Kopfstart]** oder **[!UICONTROL Zeitzone des Empfängers]** kann mit der Erstellung von E-Mails vor dem Versand beginnen, Verzögerungen reduzieren und zusätzliche Vorbereitungszeit für die Qualifizierung von Leads mit ressourcenintensiver Logik bereitstellen. Weitere Informationen finden [ in den Artikeln ](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/email-marketing/email-programs/email-program-actions/head-start-for-email-programs)Head Start for Email Programs[ und Schedule Email Programs with Recipient Time Zone](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/email-marketing/email-programs/email-program-actions/scheduling-with-recipient-time-zone/schedule-email-programs-with-recipient-time-zone) .
* Ihre Kampagne ist aktiv und Leads fließen durch, und dann bemerken Sie einen Fehler bei einem Flussschritt. Es ist verlockend, dies mit einer schnellen Anpassung zu beheben, aber zu wissen, was passiert, wenn Sie einen Live-Warteschritt ändern oder Ihre Flüsse neu anordnen, kann Ihnen helfen, viele Kopfschmerzen zu vermeiden und später zu reinigen. Siehe den [Bearbeiten eines Kampagnenflusses mit Mitgliedern in Warteschritten](https://nation.marketo.com/t5/knowledgebase/editing-campaign-flow-with-members-in-wait-steps/ta-p/254294).

### Testen und Validieren

Bevor Sie auf **[!UICONTROL Senden]** klicken, stellen Sie sicher, dass Ihre E-Mails genau wie beabsichtigt aussehen und funktionieren.

* Marketo bietet mehrere Möglichkeiten, das Erscheinungsbild einer E-Mail zu testen, um sicherzustellen, dass sie genau so aussieht, wie Sie sie sich vorgestellt haben.
   * Verwenden Sie die Funktion **[!UICONTROL Vorschau]** um sicherzustellen, dass Ihre dynamischen Inhalte und Token durch eine Vorschau nach Segmentierung oder einzelnen Leads korrekt gerendert werden. Siehe den Artikel [Vorschau einer E-Mail mit dynamischen Inhalten](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/email-marketing/general/functions-in-the-editor/preview-an-email-with-dynamic-content).
   * Senden Sie schnell und einfach eine direkte E-Mail an Ihre Testdatensätze, um zu sehen, wie Ihre E-Mail auf verschiedenen Clients/Geräten angezeigt wird. Siehe den [Ausführen eines einzelnen Flussschritts aus einer Smart-Liste](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/core-marketo-concepts/smart-lists-and-static-lists/using-smart-lists/run-a-single-flow-step-from-a-smart-list).
   * Für [!DNL Litmus] ist es jetzt einfacher denn je, Ihr Konto zu integrieren und Rendering-Tests direkt über den E-Mail-Editor zu starten. Siehe den Artikel [Testen von E-Mail-Rendering mit [!DNL Litmus]](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/email-marketing/email-designer/test-email-rendering).
* Sehen Sie sich die Funktion E-Mail-Spam-Bericht an, die in [!DNL SpamAssassin] integriert ist, um den Inhalt Ihrer E-Mail zu überprüfen und einen Wert dafür zuzuweisen, mit welcher Wahrscheinlichkeit sie den Posteingang erreicht oder als *Spam“* wird. Siehe den Artikel [E-Mail-Spam](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/email-marketing/email-designer/spam-report)Bericht.
* Behalten Sie die [!UICONTROL Kampagnenwarteschlange“ im Auge] um zu überprüfen, ob Ihre Kampagnen Objekte mit hoher Dringlichkeit korrekt verarbeitet und priorisiert werden. Siehe [Läuft meine Kampagne?Artikel ](https://nation.marketo.com/t5/knowledgebase/is-my-campaign-running/ta-p/248662).

### Optimieren Sie Ihr Support-Erlebnis

Wenn etwas schief geht, ist Schnelligkeit wichtig und der Marketo-Support hilft Ihnen dabei! Schließen Sie diese Details in Ihren Support-Fall ein, um Hin und Her zu vermeiden und unserem Team dabei zu helfen, eine schnellere Lösung zu finden. Siehe den Artikel [Best Practices für die Arbeit mit dem Marketo-Support](https://nation.marketo.com/t5/knowledgebase/best-practices-for-working-with-marketo-support/ta-p/253491).

Mit diesem Leitfaden können Sie sich etwas entspannter ausruhen, wenn Sie wissen, dass Sie in dieser kritischen Phase von einer starken Position aus beginnen, um die Interaktion und Konversionen zu fördern. Es steht viel auf dem Spiel, aber dein Stress muss nicht sein. Beginnen Sie noch heute mit Ihren Vorbereitungen und machen Sie diese Urlaubssaison zu Ihrem bisher erfolgreichsten.

+++

## Handbuch für Adobe Workfront Holiday Readiness {#workfront}

+++**Klicken Sie, um die Empfehlungen zur Urlaubsbereitschaft für Adobe Workfront anzuzeigen.**

Um Adobe Workfront auf die Weihnachtssaison vorzubereiten, sollten Teams ihre Support-Kontakte aktualisieren, interne Zeitpläne an Adobe anpassen, größere Änderungen während der Spitzenzeiten vermeiden und Automatisierungen und Integrationen proaktiv überwachen, um einen reibungslosen Betrieb zu gewährleisten.

### Für Skalierung vorbereiten

So sorgen Sie während der Feiertage für reibungslosen Support:

* Überprüfen und aktualisieren Sie Ihre autorisierten Support-Kontakte im Voraus.
* Überprüfen Sie, ob die wichtigsten Stakeholder für die Zusammenarbeit mit dem Support verfügbar sind, wenn kritische Probleme auftreten.
* Wenn sich die Planung von Produkten oder Workflows während der Feiertage ändert, empfehlen wir, diese vor Mitte November oder nach Anfang Januar zu planen, um optimale Durchlaufzeiten zu erhalten.
* Informieren Sie Ihre Adobe-Ansprechpartner über interne Feiertagspläne, um die Abstimmung sicherzustellen.

### Testen und Validieren

Bleiben Sie über Workfront-Versionen auf dem Laufenden und testen Sie neue Funktionen in Sandbox-Umgebungen:

* [Vorbereiten auf eine Adobe Workfront-Version](https://experienceleague.adobe.com/en/docs/workfront/using/product-announcements/product-releases/release-readiness)
* Archiv mit Versionshinweisen zu [Workfront](https://experienceleague.adobe.com/de/docs/workfront/using/product-announcements/product-releases/product-releases)
* Übersicht über die Version [1. Quartal 2025](https://experienceleague.adobe.com/en/docs/workfront/using/product-announcements/product-releases/release-25-q1/25-q1-release-overview)
* Aufzeichnung von Webinaren der [Workfront-Version](https://experienceleague.adobe.com/en/docs/events/workfront-recordings/releases/25-1-release-webinar)

### Best Practices

* Proaktive Planung: Identifizieren Sie alle Systemabhängigkeiten oder geplanten Automatisierungen, die von internen Zeitplänen betroffen sein könnten.
* Kontinuierliche Kommunikation: Halten Sie Ihre internen Teams und den Adobe Support über geplante Wartungsarbeiten oder wichtige Ereignisse auf dem Laufenden.
* Verwenden von Dashboards: Überwachen Sie wichtige Integrationen und Automatisierungen, um frühe Anzeichen von Leistungsproblemen zu erkennen.
* Eskalieren Sie frühzeitig: Wenn Sie eine Beeinträchtigung des Service vorhersehen oder feststellen, öffnen Sie sofort ein Support-Ticket - warten Sie nicht darauf, dass es kritisch wird.

Durch eine frühzeitige Planung, klare Kommunikation und die frühzeitige Eskalation von Problemen können Unternehmen Unterbrechungen minimieren und sicherstellen, dass Workfront während des gesamten Urlaubszeitraums wichtige Workflows unterstützt.

+++

## Handbuch für Adobe Campaign Holiday Readiness {#campaign}

+++**Klicken Sie, um die Empfehlungen zur Urlaubsbereitschaft für Adobe Campaign anzuzeigen.**


Um Adobe Campaign auf die Feiertagsbereitschaft vorzubereiten, sollten Teams die Zustellbarkeitseinstellungen proaktiv validieren, die Zielgruppensegmentierung und die Häufigkeit der Nachrichten optimieren, die Skalierbarkeit der Infrastruktur sicherstellen und die kanalübergreifende Orchestrierung von Kampagnen testen, um saisonale Volumen- und Interaktionsspitzen effektiv zu bewältigen.

### Expertentipps für eine erfolgreiche Kampagne zum Jahresende

So wie es nie zu früh ist, mit den Weihnachtseinkäufen zu beginnen, ist es nie zu früh, um mit der Planung einer sehr erfolgreichen Marketing-Kampagne für die Feiertage beginnen. Mit Adobe Campaign können Sie Kampagnen entwerfen, planen und ausführen, die alle Urlaubswünsche Ihres Unternehmens erfüllen. Kennen Sie schon alle Tipps für Kampagnen, die das Jahr mit einem Knall beenden? Sehen Sie sich dieses Video [Expertentipps für eine erfolgreiche Kampagne zum Jahresende](https://experienceleague.adobe.com/en/docs/events/experience-league-live-recordings/episodes/exl-live-episode-03) an, in dem Best Practices für Zustellbarkeit und Ausführung besprochen und gezeigt werden, wie dies in Adobe Campaign alles möglich ist.

### Überlegungen und Vorbereitungen für die Urlaubszeit

In diesem Video, [Adobe Campaign: Holiday Readiness - Considerations and Prepairs for the Holiday Period](https://helpx.adobe.com/customer-care-office-hours/campaign/campaign-holiday-readiness.html), wird Folgendes behandelt:

* Die Campaign-Community einbinden
* Zustellbarkeit - Überlegungen für die Feiertage und darüber hinaus!
* Technische Empfehlungen für Adobe Campaign Classic (ACC) und Adobe Campaign Standard (ACS)

Um Adobe Campaign für die Weihnachtszeit vorbereitet zu haben, sollten Unternehmen Zustellbarkeitsprüfungen abschließen, Kampagnenkonfigurationen validieren und sicherstellen, dass eine skalierbare Infrastruktur und kanalübergreifende Orchestrierung vorhanden sind, um zeitkritische Kampagnen mit hohem Volumen während der Weihnachtszeit sicher auszuführen.

+++

## Handbuch für Adobe Analytics Holiday Readiness {#analytics}

+++**Klicken Sie, um die Empfehlungen zur Urlaubsbereitschaft für Adobe Analytics anzuzeigen.**

Während die Weihnachtssaison naht, sollten Unternehmen, die Adobe Analytics verwenden, proaktive Schritte unternehmen, um die Datengenauigkeit, die Plattformleistung und die Berichtszuverlässigkeit während Spitzenzeiten des Traffics sicherzustellen. Adobe bietet verschiedene Ressourcen und Best Practices, um Teams bei der effektiven Vorbereitung zu unterstützen.

### Traffic vorhersagen

Um eine angemessene Hardwarezuweisung und Systemreaktionszeit sicherzustellen, empfiehlt Adobe, **Spitzenwerte pro Stunde und tägliche Server-Treffer-/** im Voraus zu übermitteln.

* Überprüfen Sie [Traffic-Spitze-Planung und Hardware-](https://experienceleague.adobe.com/en/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/traffic-management/t-traffic-schedule-spike#hardware-allocation-lead-times)), da das Verständnis, wie schnell Daten verfügbar werden, für die Entscheidungsfindung in Echtzeit während Zeiträumen mit hohem Volumen wichtig ist.

* Erfahren Sie in der [Übersicht über die Adobe Analytics-Datenlatenz](https://experienceleague.adobe.com/en/docs/analytics/technotes/latency), was sich auf die Datenverfügbarkeit und -latenz in Adobe Analytics auswirkt, einschließlich unerwarteter Traffic-Spitzen und Hardware-Probleme, und lernen Sie empfohlene Strategien zur Reduzierung von Datenverzögerungen kennen.

### Best Practices

Für Teams, die Daten-Feeds zum Exportieren von Analytics-Rohdaten verwenden, bietet Adobe eine Anleitung zur Optimierung der Feed-Konfigurationen und zur Vermeidung gängiger Fallstricke.

* [Best Practices für Adobe Analytics-Daten-Feeds](https://experienceleague.adobe.com/en/docs/analytics/export/analytics-data-feed/data-feeds-best-practices)

Um während der Feiertage ein schnelles und zuverlässiges Reporting zu gewährleisten, empfiehlt Adobe:

* [Optimieren der Analysis Workspace-Leistung](https://experienceleague.adobe.com/en/docs/analytics/analyze/analysis-workspace/workspace-faq/optimizing-performance)
* [Fehlerbehebung und Best Practices für Report Builder: Empfehlungen zur Anforderungsoptimierung](https://experienceleague.adobe.com/en/docs/analytics/analyze/legacy-report-builder/troubleshoot#section_33EF919255BF46CD97105D8ACB43573F)
* [Analytics-Komponentenhandbuch: Warteschlange für terminierte Berichte](https://experienceleague.adobe.com/en/docs/analytics/components/scheduled-reports-admin)

### Urlaubsplanung

Adobe erzwingt in **Regel während der Spitzenferien** Wartungsausschlussfenster, um einen unterbrechungsfreien Service zu gewährleisten. Kunden sollten die Veröffentlichungs- und Wartungszeitpläne von Adobe über Experience League überwachen und sich mit ihren Adobe-Account-Teams hinsichtlich der Support-Planung abstimmen.

Mithilfe dieser Richtlinien und der öffentlichen Dokumentation von Adobe können Unternehmen sicherstellen, dass ihre Adobe Analytics-Implementierung robust und reaktionsschnell ist und die Anforderungen der Weihnachtszeit erfüllt.

+++

## Handbuch für Adobe Target Holiday Readiness {#target}

+++**Klicken Sie, um die Empfehlungen zur Urlaubsbereitschaft für Adobe Target anzuzeigen.**

Die Weihnachtssaison bietet spannende Möglichkeiten zur Interaktion, bringt aber auch Herausforderungen mit sich, wie Verkehrsspitzen und eine erhöhte Nachfrage nach Personalisierungssystemen. Um Ihnen dabei zu helfen, in dieser kritischen Phase nahtlose Erlebnisse bereitzustellen, haben wir wichtige Empfehlungen zusammengestellt, um sicherzustellen, dass Ihre Adobe Target-Implementierung bereit ist.

### Prognostizieren des Bedarfs

Planen Sie zunächst Traffic-Spitzen von 20-50 % oder mehr ein und überprüfen Sie, ob Ihre Infrastruktur die Last bewältigen kann. Prognostizieren Sie Aktivitäten und Datenvolumen in Adobe Target, Analytics und AEP, um Überraschungen zu vermeiden.

Es ist auch wichtig, geschäftskritische Journey zu identifizieren, z. B. Checkout, Produktempfehlungen und Werbeangebote. Daher konzentrieren sich die Personalisierungsbemühungen auf die Bereiche, in denen sie am wichtigsten sind.

Siehe [Best Practices für die Optimierung mit Adobe Target](https://experienceleague.adobe.com/en/docs/target-learn/tutorials/administration/strategy/target-best-practices-for-optimization).

### Für Skalierung vorbereiten

* Planen Sie erhöhten Traffic auf der Website und auf Mobilgeräten ein und informieren Sie das Target-Supportteam, um die Serverkapazität zu erhöhen und blockierte Anrufe zu vermeiden.
* Für Belastungs-/Stifttests sollte das Target-Supportteam vorab informiert werden.
* Aktualisieren Sie auf die neuesten `at.js`-/Bereitstellungs-API-Versionen.
* Nicht kritische Änderungen einfrieren; Vorbereiten auf Fallback-Erlebnisse.
* Support- und Eskalationsprozesse aufeinander abstimmen und proaktive Warnhinweise aktivieren.

### Testen und Validieren

Validieren Sie die Bereitstellung von Inhalten mithilfe [QA-Links](https://experienceleague.adobe.com/en/docs/target/using/activities/activity-qa/activity-qa) um zu bestätigen, dass alles erwartungsgemäß funktioniert. Verwenden Sie den **[!UICONTROL Match-Zielgruppenregeln, um Erlebnisse anzuzeigen]** um sicherzustellen, dass sich die richtige Zielgruppe für die Aktivität qualifiziert, die Sie testen. Vergewissern Sie sich, dass Ihre **[!UICONTROL Zielmetrik]**-Konfiguration auf das **[!UICONTROL Ziel]** der Aktivität abgestimmt ist. Und immer einen Backup-Plan parat haben - nur für den Fall.

### Best Practices

Halten Sie Ihre Implementierung innerhalb der [Adobe Target](https://experienceleague.adobe.com/en/docs/target/using/troubleshoot/target-limits)Beschränkungen und überprüfen Sie [DSGVO- und CCPA](https://experienceleague.adobe.com/en/docs/target-dev/developer/implementation/privacy/cmp-privacy-and-general-data-protection-regulation)Konformität), bevor Sie starten. Pflegen Sie weniger als 100 aktive Aktivitäten und archivieren Sie ältere, um die Dinge zu optimieren. Nutzen Sie die Vorteile **[!UICONTROL Automatische Zuordnung]**/**[!UICONTROL Automatisches Targeting]** für KI-gesteuerte Optimierung. Erstellen Sie Rollback-Pläne und Echtzeit-Überwachungs-Dashboards.

### Sicherheit und Governance

Bevor Sie Erlebnisse personalisieren, bestätigen Sie die Einhaltung der Einverständniserklärung gemäß DSGVO und CCPA. Speichern Sie keine personenbezogenen Daten in Profilparametern und validieren Sie die API-Sicherheit, um Kundendaten zu schützen.

+++
