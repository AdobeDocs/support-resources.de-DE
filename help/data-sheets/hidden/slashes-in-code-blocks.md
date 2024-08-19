---
title: Slashes in Codeblöcken UGP-11189
description: Slashes in Codeblöcken UGP-11189 test
hide: true
hidefromtoc: true
source-git-commit: 2255dad674f1b4d456ffb50ebec9313bc4b3d7f5
workflow-type: tm+mt
source-wordcount: '46'
ht-degree: 0%

---

# Schrägstrich in Codeblöcken

1. Führen Sie den Befehl aus:

   ```bash
   vendor/bin/magento-patches -n status |grep "27015\|Status"
   ```

1. Führen Sie den Befehl aus (maskiert):

   ```bash
   vendor/bin/magento-patches -n status |grep "27015&bsol;|Status"
   ```

Nicht im Codeblock

vendor/bin/magento-patches -n status |grep &quot;27015\|Status&quot;

maskiert:

vendor/bin/magento-patches -n status |grep &quot;27015&amp;bsol;|Status&quot;

