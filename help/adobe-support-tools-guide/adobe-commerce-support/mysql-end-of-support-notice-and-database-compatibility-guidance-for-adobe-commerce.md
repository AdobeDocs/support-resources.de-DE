---
title: Hinweis zum Ende der Unterstützung für MySQL und Anleitung zur Datenbankkompatibilität für Adobe Commerce
description: Dieser Artikel enthält Informationen zum Ende der Unterstützung für MySQL und Anleitungen zur Datenbankkompatibilität für unterstützte Adobe Commerce-Versionen.
solution: Commerce
exl-id: f4ef2b3b-316c-421e-a645-9445cdd13448
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
source-git-commit: a4ba265c36bd4ba6c7c563879834f2c59fdc58a4
workflow-type: tm+mt
source-wordcount: '380'
ht-degree: 1%
---
# Hinweis zum Ende der Unterstützung für MySQL und Anleitung zur Datenbankkompatibilität für Adobe Commerce

Dieser Artikel enthält wichtige Informationen zum Ende der Unterstützung für MySQL (End of Support, EOS) und zur Datenbankkompatibilität für unterstützte Adobe Commerce-Versionen.
Adobe empfiehlt Händlern dringend, diese Ankündigung zu überprüfen und Maßnahmen zu ergreifen, um die Plattformstabilität zu gewährleisten und die Support-Anforderungen weiterhin zu erfüllen.
Weitere Informationen finden Sie unter [Upgrade-Voraussetzungen für MariaDB](https://experienceleague.adobe.com/en/docs/commerce-operations/implementation-playbook/best-practices/maintenance/mariadb-upgrade) und [Systemanforderungen](https://experienceleague.adobe.com/en/docs/commerce-operations/installation-guide/system-requirements).

## Ende der Unterstützung für MySQL 8.0 (EOS)

MySQL 8.0 erreicht am 30. April 2026 das Ende der Unterstützung (End of Support, EOS).
Nach diesem Datum werden die folgenden Adobe Commerce-Versionen MySQL-Versionen, die nach MySQL 8.0 veröffentlicht wurden, nicht mehr unterstützen oder ihre Kompatibilität beibehalten:

* Adobe Commerce 2.4.7
* Adobe Commerce 2.4.6
* Adobe Commerce 2.4.5

Adobe wird neuere MySQL-Hauptversionen dieser Adobe Commerce-Versionen nicht validieren oder unterstützen.

## Erforderliche Aktion für Kunden vor Ort

Bei lokalen Adobe Commerce-Installationen, die die folgenden Versionen ausführen, wird dringend empfohlen, ihre Datenbankserver auf eine kompatible MariaDB-Version zu migrieren:

* 2.4.5
* 2.4.6
* 2.4.7

MariaDB wird für diese Versionen vollständig unterstützt und ist die empfohlene Datenbankplattform für die Zukunft.

* 2.4.5
* 2.4.6
* 2.4.7

Es wird dringend empfohlen, die Datenbankserver auf eine kompatible MariaDB-Version zu migrieren.
MariaDB wird für diese Adobe Commerce-Versionen vollständig unterstützt und ist die empfohlene Datenbankplattform.

## MySQL-Unterstützung in Adobe Commerce 2.4.8 und 2.4.9

Adobe Commerce 2.4.8 und 2.4.9 sind die letzten Adobe Commerce-Versionen, die MySQL unterstützen.

Für diese Versionen:
* MySQL 8.4 ist die letzte von Adobe Commerce unterstützte MySQL-Version.
* Nach 8.4 veröffentlichte MySQL-Versionen werden in Adobe Commerce weder zertifiziert noch unterstützt.

## Zukünftige Richtung: MariaDB als Standard-Datenbankplattform

Adobe Commerce unterstützt auch weiterhin MariaDB als standardmäßige und empfohlene Datenbankplattform.

Adobe empfiehlt dringend, dass die folgenden Kunden mit der Planung ihrer Migration zu MariaDB beginnen, um die Kompatibilität langfristig aufrechtzuerhalten und die Ausrichtung zu unterstützen:
* Alle Kunden von Adobe Commerce 2.4.8 und 2.4.9 On-Premise
* Kunden, die ältere unterstützte Adobe Commerce-Versionen ausführen
