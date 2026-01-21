---
title: Versionshinweise zum neuen EXL-Fall-Formular
description: Aktuelle Versionsinformationen zum EXL-Formular.
feature: Release Notes
source-git-commit: 421ef19ed939cd757e3182c8fa5bbda13fd7561e
workflow-type: tm+mt
source-wordcount: '272'
ht-degree: 8%

---


# Versionshinweise zum neuen EXL-Fall-Formular

Mit der neuen Fallerstellung wird ein aktualisiertes Formular eingeführt, mit dem die Problemlösung optimiert wird und das Folgendes enthält:

![Neu](../adobe-support-tools-guide/assets/new.svg) – Neue Funktionen
![Fehlerbehebung](../adobe-support-tools-guide/assets/fix.svg) – Fehlerbehebungen und Verbesserungen
![Fehler](../adobe-support-tools-guide/assets/bug.svg) – Bekannte Probleme

## Version 1.0 - Formular zur erweiterten Fallerstellung

*Freitag, 15. Januar 2026*

![Neu](../adobe-support-tools-guide/assets/new.svg) Das Fallformular ist in einem geführten Fluss organisiert, der Benutzenden hilft zu verstehen, welche Informationen in den einzelnen Phasen erforderlich sind:

- [!UICONTROL Produktauswahl]
- [!UICONTROL Problemdetails]
- [!UICONTROL Systeminformationen]
- [!UICONTROL Impact]
- [!UICONTROL Kontaktinformationen]
- [!UICONTROL Überprüfen und Senden]

![Neu](../adobe-support-tools-guide/assets/new.svg) Hinzugefügt **Neue [!UICONTROL Schritte zur Reproduktion] Feld**, um verwertbare Details zu erfassen und die Fehlerbehebung zu beschleunigen.

![Neu](../adobe-support-tools-guide/assets/new.svg) Hinzugefügt **Zusätzliche Felder [!UICONTROL Umgebungskontext] für** Produkte zur Erfassung kritischer Details:

- **Marketo**
   - Munchkin-ID
- **Adobe Target**
   - Aktivitätsname
   - Site-URL (Tags-Eigenschaftsname) / HAR- oder Assurance-Protokoll
- **Adobe Analytics**
   - RSID
   - Site-URL (Tag-Eigenschaftsname) / HAR- oder Assurance-Protokoll / cURL / Debug-Protokoll
   - Workspace-Kurzlink
- **Adobe Journey Optimizer (AJO)**
   - Journey-ID oder Journey URL
   - Beispielprofil
- **Real-Time Customer Data Platform (RTCDP)**
   - Betroffene Komponenten-ID (Ziel-ID, Profil-ID, Zielgruppen-ID, Datensatz-ID oder Datenfluss-ID)
   - HAR-Datei/Assurance-Protokolle
- **Customer Journey Analytics (CJA)**
   - Workspace-Projekt
   - Eigenschaftsname für Tags


![Neu](../adobe-support-tools-guide/assets/new.svg) Es wurde ein **KI-gesteuertes [!UICONTROL Recommendations-Bedienfeld]** hinzugefügt, um hilfreiche Anleitungen anzuzeigen, ohne den Prozess zur Fallerstellung zu unterbrechen.

![Neu](../adobe-support-tools-guide/assets/new.svg) Es wurde ein Schritt [!UICONTROL Zusammenfassung überprüfen] hinzugefügt, um eine konsolidierte Ansicht aller eingegebenen Informationen bereitzustellen und Benutzern Folgendes zu ermöglichen:

- Falldetails an einem Ort überprüfen
- Zurück zu den vorherigen Schritten, um Änderungen vorzunehmen
- Zurück zur Zusammenfassung ohne Verlust des Fortschritts

![Korrigieren](../adobe-support-tools-guide/assets/fix.svg) Das Feld „Fallbeschreibung“ wurde in &quot;*[!UICONTROL &quot; umbenannt, um]* Klarheit zu verbessern.

![Korrigieren](../adobe-support-tools-guide/assets/fix.svg) Es wurde ein Sternchen (*) als obligatorische Feldindikatoren hinzugefügt, um die Vollständigkeit sicherzustellen und Fehler bei der Übermittlung zu reduzieren.
