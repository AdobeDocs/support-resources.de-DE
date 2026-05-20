---
title: Abrufen und Anwenden von [!UICONTROL Sicherheits-Patch]
description: Dieser Artikel enthält Anweisungen zum Abrufen und Anwenden eines [!UICONTROL Sicherheits-Patches], der veröffentlicht wurde, aber keine Anweisungen verfügbar sind.
exl-id: 6764d60e-5088-4a85-90fa-4372570b065b
source-git-commit: 9a4d96e06b949e4c229fdf0f084810b27bf8b346
workflow-type: tm+mt
source-wordcount: '660'
ht-degree: 0%

---

# So erhalten Sie einen [!UICONTROL Sicherheits-Patch]

>[!NOTE]
>Wenn Sie eine On-Premise-Installation haben und keine Versionskontrollsysteme wie [!DNL CVS] oder GitHub zur Verwaltung Ihres Codes verwenden, kann Ihr Webhost möglicherweise bei der Anwendung des Patches helfen. Sie können sich gerne an sie wenden, um Unterstützung zu erhalten.

Dieser Artikel enthält Anweisungen zum Abrufen und Anwenden eines [!UICONTROL Sicherheits-Patches], der veröffentlicht wurde, aber keine Anweisungen verfügbar sind.

## Betroffene Produkte und Versionen

Adobe Commerce On-Premise und Cloud-Infrastruktur - alle unterstützten Versionen


## Ursache

Für Adobe Commerce-Sicherheitsbulletins stellt Adobe nur dann eine separate isolierte Patch-Datei oder einen Hotfix bereit, wenn dieses Artefakt explizit als Teil des Bulletins veröffentlicht wird. Wenn kein(e) isolierte(r) Patch- oder Hotfix veröffentlicht oder im Bulletin-Material referenziert wird, erstellt Adobe anschließend keinen separaten eigenständigen Patch.

Dies liegt daran, dass die Sicherheitskorrekturen zusammen als Teil der unterstützten Sicherheitsversion für die entsprechende Versionszeile entwickelt, validiert und veröffentlicht werden.

Dementsprechend besteht der unterstützte Behebungspfad darin, das offizielle Sicherheitsupdate für die betroffene Versionszeile anzuwenden oder auf eine Version zu aktualisieren, die bereits die Fehlerbehebung enthält.

## Lösung


### Fall I:

* Wenn in den [Versionshinweisen](https://experienceleague.adobe.com/en/docs/commerce-on-cloud/user-guide/release-notes/cloud-tools-suite) eine isolierte Patch-Datei/ein Hotfix erwähnt wird, laden Sie die Datei aus dem Download-Abschnitt von [https://account.magento.com](https://account.magento.com/downloads/view/) herunter. Benutzer mit gemeinsamem Zugriff müssen zunächst vom Kontoinhaber bzw. Lizenzinhaber über Download-Rechte verfügen.

**Einschränkungen:**

* Adobe Commerce 2.4.6 wird unter der erweiterten Unterstützung bis zum 30. August 2027 weiterhin unterstützt.

* Adobe Commerce 2.4.5 wird bis zum 11. August 2026 weiterhin unterstützt. Nach diesem Datum bietet Adobe nur noch bis zum 31. Mai 2027 Sicherheitskorrekturen.

* Adobe Commerce 2.4.4 wird nicht mehr unterstützt. Adobe bietet nur bis zum 31. Mai 2027 Sicherheitskorrekturen.

* Für Adobe Commerce 2.4.4 und 2.4.5 stellt Adobe nur Sicherheits-Patch-Dateien bereit. Diese Aktualisierungen beinhalten nicht:

   * Adobe Commerce Support oder technische Unterstützung
   * Qualitäts-Patches
   * Aktualisierungen der Plattform- oder Betriebssystemabhängigkeit

Nicht unterstützte Versionen (2.3.x und 2.4.0-2.4.3) sind nicht unterstützungsfähig. Sie können ein Upgrade auf eine unterstützte Version durchführen, um die neuesten Sicherheitskorrekturen zu erhalten.

### Fall II:

Isolierte Patches werden nur in Ausnahmefällen bereitgestellt und sind nicht die bevorzugte Methode zur Implementierung von Sicherheitskorrekturen.

Wenn eine einzelne Patch-Datei oder ein Hotfix in den Versionshinweisen nicht aufgeführt wird, befolgen Sie die folgenden Richtlinien:

>[!IMPORTANT]
>
>Wenn eine einzelne Patch-Datei oder ein Hotfix aus Sicherheitsgründen nicht explizit veröffentlicht wurde, aktualisieren Sie die gesamte Adobe Commerce-Anwendung auf die neueste Patch-Version für die betroffene Release-Zeile.

**cloud:**

1. Einige [!UICONTROL Sicherheits]Patches) sind möglicherweise in der neuesten Version von Cloud Tools Suite (ECE-Tools) unter Cloud-Patches für Commerce enthalten/veröffentlicht. Überprüfen Sie die [Versionshinweise](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/release-notes/cloud-tools-suite) und aktualisieren Sie das Paket auf diese Version, wenn in der Version eine Sicherheitskorrektur erwähnt wird.
1. Wenn in den Versionshinweisen keine Sicherheitskorrektur erwähnt wird, lesen Sie weiter.

**Cloud-Infrastruktur oder On-Premise:**

* Wenn keine isolierte Patch-Datei bzw. kein Hotfix verfügbar ist, [aktualisieren Sie die Adobe Commerce-Version auf Cloud](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/upgrade/commerce-version)Infrastruktur 2.4.X auf die neueste Patch-Version 2.4.X-pY.
* Wenn keine isolierte Patch-Datei bzw. kein Hotfix verfügbar ist, [aktualisieren Sie Adobe Commerce On-Premise](https://experienceleague.adobe.com/en/docs/commerce-operations/upgrade-guide/implementation/perform-upgrade) 2.4.X auf die neueste Patch-Version 2.4.X-pY.

## Verwandtes Lesen

* Siehe [Versionshinweise für Commerce Cloud Tools Suite](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/release-notes/cloud-tools-suite) im *Handbuch zu Adobe Commerce in Cloud-Infrastrukturen*.
* Siehe [Upgrade der Adobe Commerce-Version](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/upgrade/commerce-version) im Handbuch zu *Adobe Commerce in Cloud-Infrastrukturen*.
