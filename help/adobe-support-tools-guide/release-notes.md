---
title: Experience League Support - Versionshinweise
description: Die neuesten Versionsinformationen zur Experience League-Unterstützung.
feature: Release Notes
exl-id: 875ad82e-56b5-4d58-9237-bb7aa0d9ffaf
source-git-commit: 7d0f54c6a5d43fc9155a7d17fca2eefa3238179e
workflow-type: tm+mt
source-wordcount: '489'
ht-degree: 4%

---

# Experience League Support - Versionshinweise

Diese Versionshinweise enthalten Aktualisierungen zur Experience League-Unterstützung und umfassen:

![Neu](../adobe-support-tools-guide/assets/new.svg) Neue Funktionen
![Fehlerbehebung](../adobe-support-tools-guide/assets/fix.svg) Fehlerbehebungen und Verbesserungen
![Bug](../adobe-support-tools-guide/assets/bug.svg) Bekannte Probleme

## &#x200B;8. April 2026 - Erweiterung der Callback-Funktion

Die Rückrufanfrage-Funktion ist jetzt für Benutzende von Marketo-Produkten verfügbar.

## &#x200B;30. März 2026 - Verbessertes Antragsformular

![Neu](../adobe-support-tools-guide/assets/new.svg) Das Fallformular ist in einen geführten Fluss unterteilt, der Benutzenden hilft zu verstehen, welche Informationen in den einzelnen Phasen erforderlich sind:

- [!UICONTROL Produktauswahl]
- [!UICONTROL Problembeschreibung]
- [!UICONTROL Systeminformationen]
- [!UICONTROL Priorität und geschäftliche Auswirkungen]
- [!UICONTROL Kontaktinformationen und Watchers-Liste]
- [!UICONTROL Überprüfen und Senden]

![Neu](../adobe-support-tools-guide/assets/new.svg) Es wurde eine automatische Titelgenerierung auf der Grundlage von **[!UICONTROL Problembeschreibung]** hinzugefügt, sodass der Titel automatisch generiert werden kann, während Benutzenden weiterhin die Möglichkeit gegeben wird, ihn vor dem Senden der Anfrage zu bearbeiten.

![Neu](../adobe-support-tools-guide/assets/new.svg) Ein **[!UICONTROL „Ist das Problem reproduzierbar?“ wurde hinzugefügt.]** Option zur Verbesserung der Fehlerbehebung. Wenn Benutzer **[!UICONTROL Ja]** auswählen, werden sie aufgefordert, die Schritte zur Reproduktion des Problems anzugeben. Wenn *Nein* ausgewählt ist, können Benutzer mit der Fallübermittlung fortfahren.

![Neu](../adobe-support-tools-guide/assets/new.svg) Es wurde eine Option hinzugefügt, die angibt, ob kürzlich Änderungen an der Umgebung oder Instanz vorgenommen wurden. Wenn **[!UICONTROL Ja]** ausgewählt ist, werden Benutzer aufgefordert, zusätzliche Details zu den Änderungen anzugeben.

![Neu](../adobe-support-tools-guide/assets/new.svg) Hinzugefügt **Zusätzliche Felder [!UICONTROL Umgebungskontext] für** Produkte zur Erfassung kritischer Details:

- **Marketo**
   - Munchkin-ID
- **Adobe Target**
   - Aktivitätsname
   - Site-URL (Eigenschaftsname für Tags)
- **Adobe Analytics**
   - RSID
   - Site-URL (Eigenschaftsname für Tags) / cURL
   - Workspace-Kurzlink
- **Adobe Journey Optimizer (AJO)**
   - Journey-ID oder URL/Kampagnen-ID oder URL/Kanal-ID oder URL/Offer Decisioning-ID oder URL
   - Beispielprofil
   - Sandbox-Name
- **Real-Time Customer Data Platform (RTCDP)**
   - Betroffene Komponenten-ID (Ziel-ID/Zielgruppen-ID/Datensatz-ID/Datenfluss-ID/Zusammenführungsrichtlinien-ID/Schema-ID/Source-ID/Batch-ID)
   - Beispielprofil
   - Sandbox-Name
- **Adobe Experience Platform (AEP)**
   - Betroffene Komponenten-ID (Ziel-ID/Zielgruppen-ID/Datensatz-ID/Datenfluss-ID/Zusammenführungsrichtlinien-ID/Schema-ID/Source-ID/Batch-ID)
   - Beispielprofil
   - Sandbox-Name
- **Customer Journey Analytics (CJA)**
   - Workspace-Projekt-URL
   - Verbindungs-ID/Fehlermeldung/Code
   - Datenansichts-ID

![Neu](../adobe-support-tools-guide/assets/new.svg) Es wurde ein **KI-gesteuertes [!UICONTROL Recommendations-Bedienfeld]** hinzugefügt, um hilfreiche Anleitungen anzuzeigen, ohne den Prozess zur Fallerstellung zu unterbrechen.

![Neu](../adobe-support-tools-guide/assets/new.svg) Es wurde ein Schritt **[!UICONTROL Zusammenfassung überprüfen]** hinzugefügt, um eine konsolidierte Ansicht aller eingegebenen Informationen bereitzustellen und Benutzern Folgendes zu ermöglichen:

- Falldetails an einem Ort überprüfen
- Zurück zu den vorherigen Schritten, um Änderungen vorzunehmen
- Zurück zur Zusammenfassung ohne Verlust des Fortschritts

![Korrigieren](../adobe-support-tools-guide/assets/fix.svg) Das Feld „Fallbeschreibung“ wurde in &quot;*[!UICONTROL &quot; umbenannt, um]* Klarheit zu verbessern.

![Korrigieren](../adobe-support-tools-guide/assets/fix.svg) Es wurde ein Sternchen (*) als obligatorische Feldindikatoren hinzugefügt, um die Vollständigkeit sicherzustellen und Fehler bei der Übermittlung zu reduzieren.

## &#x200B;18. März 2026 - Erweiterung der Funktion „Request for Callback“

Experience League bietet jetzt die Option „Callback anfordern“, die eine Self-Service-Planung von Web-Meetings mit Funktionen zur Bildschirmfreigabe ermöglicht, um die Problembehebung zu beschleunigen.

- Diese Funktion ist für Adobe Experience Manager, Campaign und Workfront verfügbar.
- Kunden können Meetings nach Bedarf planen und sofort Einladungen erhalten.
- Bei Adobe Experience Manager P1-Fällen sorgen sofortige Callbacks für eine schnellere Interaktion bei kritischen Problemen und tragen so zur Minimierung von Ausfallzeiten und geschäftlichen Auswirkungen bei.
