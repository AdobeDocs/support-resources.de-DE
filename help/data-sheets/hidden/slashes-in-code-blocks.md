---
title: Schrägstriche in Code-Blöcken UGP-11189
description: Schrägstriche in Code-Blöcken UGP-11189 Test
hide: true
hidefromtoc: true
exl-id: d585d672-b617-4aba-83ac-1295ce8a55cb
source-git-commit: 7626d51e268d1e04363af1294b2504b129540eac
workflow-type: tm+mt
source-wordcount: '45'
ht-degree: 4%

---

# Schrägstrich in Code-Blöcken

1. Führen Sie den Befehl aus:

   ```bash
   vendor/bin/magento-patches -n status |grep "27015\|Status"
   ```

1. Nächster Schritt

Nicht im Codeblock

Status Vendor/bin/Magento-patches -n |grep „27015\|Status“

Umgekehrter Schrägstrich:

Status Vendor/bin/Magento-patches -n |grep „27015&amp;bsol;|Status“
