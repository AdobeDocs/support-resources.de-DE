---
title: Slashes in Codeblöcken UGP-11189
description: Slashes in Codeblöcken UGP-11189 test
hide: true
hidefromtoc: true
source-git-commit: 4fc9b739d18941d276b88f8799163523c8bd5f85
workflow-type: tm+mt
source-wordcount: '45'
ht-degree: 4%

---

# Schrägstrich in Codeblöcken

1. Führen Sie den Befehl aus:

   ```bash
   vendor/bin/magento-patches -n status |grep "27015\|Status"
   ```

1. Nächster Schritt

Nicht im Codeblock

vendor/bin/magento-patches -n status |grep &quot;27015\|Status&quot;

Umgekehrter Schrägstrich:

vendor/bin/magento-patches -n status |grep &quot;27015&amp;bsol;|Status&quot;
