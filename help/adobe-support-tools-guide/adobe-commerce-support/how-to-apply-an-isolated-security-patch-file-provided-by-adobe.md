---
title: Anwenden eines von Adobe bereitgestellten isolierten Patches
description: In diesem Artikel wird beschrieben, wie Sie einen isolierten Patch für Adobe Commerce On-Premise, Adobe Commerce on Cloud Infrastructure und Magento Open Source anwenden.
feature: Best Practices, Compliance, Console
solution: Commerce
feature-set: Commerce
autotag-review: '2026-08-19T13:22:21.768Z'
TQID: 'https://experienceleague.adobe.com/tmaNqB6uOX2ukmfxQvcqFvYwm2UyO6USzb7t8hFQM1A'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: b5f00040-57a0-4a6d-a39e-383b1936c2c9
    internal-label: Compliance
  - id: cdfd3bc1-dc23-5cf0-b965-d3c0c55cde67
    internal-label: Best Practices
  - id: 125c1f49-aefd-5f34-a252-288937f95f6b
    internal-label: Marketing Tools
subfeature_v2:
  - id: c4af0798-d497-5e6b-8380-19812c26d00a
    internal-label: Console
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
source-git-commit: a4ba265c36bd4ba6c7c563879834f2c59fdc58a4
workflow-type: tm+mt
source-wordcount: '219'
ht-degree: 0%
---
# Anwenden eines von Adobe bereitgestellten isolierten Patches

In diesem Artikel wird beschrieben, wie Sie einen isolierten Patch für Adobe Commerce On-Premise, Adobe Commerce on Cloud Infrastructure und Magento Open Source anwenden.

>[!WARNING]
>
>Es wird dringend empfohlen, den Patch in der Staging-/Integrationsumgebung anzuwenden und zu testen, bevor er in der Produktion angewendet wird. Wir empfehlen Ihnen auch eine aktuelle Sicherung vor jeder Manipulation.

## Anwenden eines isolierten Patches für Adobe Commerce auf die Cloud-Infrastruktur {#cloud}

1. Wenn Sie kein Verzeichnis mit dem Namen `m2-hotfixes` im Projektstammverzeichnis haben, erstellen Sie bitte eines.
1. Kopieren Sie die `%patch_name%.patch` Datei(en) in das `m2-hotfixes`.
1. Code-Änderungen hinzufügen, übertragen und per Push übertragen:

   ```git
   git add -A
   ```

   ```git
   git commit -m "Apply %patch_name%.patch patch"
   ```

   ```git
   git push origin
   ```

Weitere Informationen zum Anwenden von Patches auf Cloud-Projekte finden Sie unter [Patches anwenden](https://experienceleague.adobe.com/de/docs/commerce-on-cloud/user-guide/develop/upgrade/apply-patches).

## Anwenden eines isolierten Patches für Adobe Commerce On-Premise und Magento Open Source {#commerce}

1. Laden Sie den Patch in Ihr lokales Adobe Commerce- oder Magento Open Source-Stammverzeichnis hoch.
1. Führen Sie den folgenden SSH-Befehl aus:

   ```bash
   patch -p1 < %patch_name%.patch
   ```

   (Wenn der obige Befehl nicht funktioniert, versuchen Sie, `-p2` statt `-p1` zu verwenden.)

1. Damit die Änderungen übernommen werden, aktualisieren Sie den Cache im [!UICONTROL Admin] unter **[!UICONTROL System]** > **[!UICONTROL Cache-Verwaltung]**.
