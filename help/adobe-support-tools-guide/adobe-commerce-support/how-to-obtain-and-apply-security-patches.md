---
title: Abrufen und Anwenden von [!UICONTROL Sicherheits-Patch]
description: Dieser Artikel enthält Anweisungen zum Abrufen und Anwenden eines [!UICONTROL Sicherheits-Patches], der veröffentlicht wurde, aber keine Anweisungen verfügbar sind.
source-git-commit: 93ee9bd110930e244befca682fadd3edc24d138a
workflow-type: tm+mt
source-wordcount: '452'
ht-degree: 0%

---

# So erhalten Sie einen [!UICONTROL Sicherheits-Patch]

>[!NOTE]
>Wenn Sie eine On-Premise-Installation haben und keine Versionskontrollsysteme wie [!DNL CVS] oder GitHub zur Verwaltung Ihres Codes verwenden, kann Ihr Webhost möglicherweise bei der Anwendung des Patches helfen. Sie können sich gerne an sie wenden, um Unterstützung zu erhalten.

Dieser Artikel enthält Anweisungen zum Abrufen und Anwenden eines [!UICONTROL Sicherheits-Patches], der veröffentlicht wurde, aber keine Anweisungen verfügbar sind.

## Betroffene Produkte und Versionen

Adobe Commerce On-Premise und Cloud-Infrastruktur - alle unterstützten Versionen


## Ursache

Die meisten [!UICONTROL Sicherheits]Patches) werden ohne irgendeinen isolierten Patch oder Hotfix veröffentlicht und erfordern ein Upgrade auf die [!UICONTROL Sicherheits-Patch]-Version.

## Lösung


### Fall I:

* Wenn in den [Versionshinweisen](https://experienceleague.adobe.com/de/docs/commerce-on-cloud/user-guide/release-notes/cloud-tools-suite) eine isolierte Patch-Datei/ein Hotfix erwähnt wird, laden Sie die Datei aus dem Download-Abschnitt von [https://account.magento.com](https://account.magento.com/downloads/view/) herunter. Benutzer mit gemeinsamem Zugriff müssen zunächst vom Kontoinhaber bzw. Lizenzinhaber über Download-Rechte verfügen.

**Einschränkungen:**

Wenn Sie eine ältere Version von Adobe Commerce (2.4.4) verwenden, erhalten Sie automatisch erweiterte Unterstützung. Ihre Version muss eine der folgenden nicht unterstützten Versionen sein, um die neuesten verfügbaren Sicherheits-Patches anwenden zu können:

2.4.4 - 2.4.4-P11

Nicht unterstützte Versionen (2.3.x, 2.4.0 - 2.4.3) sind nicht unterstützungsfähig, und Sie müssen zunächst ein Upgrade auf eine unterstützte Version durchführen, um die neuesten Sicherheitskorrekturen nutzen zu können.

Wenn Sie nicht über erweiterten Support verfügen, können Sie den Support anfordern, die Patches für Sie freizugeben. Dieser kann jedoch keine Probleme/Fehler beheben, auf die Sie bei der Anwendung stoßen.

### Fall II:

Isolierte Patches werden nur in Ausnahmefällen bereitgestellt und sind nicht die bevorzugte Form der Implementierung von Sicherheitskorrekturen.

Wenn in den Versionshinweisen keine einzelne Patch-Datei bzw. kein Hotfix erwähnt wird:

* **cloud:**

1. Einige [!UICONTROL Sicherheits]Patches) sind möglicherweise in der neuesten Version von Cloud Tools Suite (ECE-Tools) unter Cloud-Patches für Commerce enthalten/veröffentlicht. Überprüfen Sie die [Versionshinweise](https://experienceleague.adobe.com/de/docs/commerce-cloud-service/user-guide/release-notes/cloud-tools-suite) und aktualisieren Sie das Paket auf diese Version, wenn in der Version eine Sicherheitskorrektur erwähnt wird.
1. Wenn in den Versionshinweisen keine Sicherheitskorrektur erwähnt wird, lesen Sie weiter.

* **Cloud-Infrastruktur oder On-Premise:**

* Wenn keine isolierte Patch-Datei bzw. kein Hotfix verfügbar ist, [aktualisieren Sie die Adobe Commerce-Version auf Cloud](https://experienceleague.adobe.com/de/docs/commerce-cloud-service/user-guide/develop/upgrade/commerce-version)Infrastruktur 2.4.X auf die neueste Patch-Version 2.4.X-pY.
* Wenn keine isolierte Patch-Datei bzw. kein Hotfix verfügbar ist, [aktualisieren Sie Adobe Commerce On-Premise](https://experienceleague.adobe.com/de/docs/commerce-operations/upgrade-guide/implementation/perform-upgrade) 2.4.X auf die neueste Patch-Version 2.4.X-pY.

## Verwandtes Lesen

* Siehe [Versionshinweise für Commerce Cloud Tools Suite](https://experienceleague.adobe.com/de/docs/commerce-cloud-service/user-guide/release-notes/cloud-tools-suite) im *Handbuch zu Adobe Commerce in Cloud-Infrastrukturen*.
* Siehe [Upgrade der Adobe Commerce-Version](https://experienceleague.adobe.com/de/docs/commerce-cloud-service/user-guide/develop/upgrade/commerce-version) im Handbuch zu *Adobe Commerce in Cloud-Infrastrukturen*.
