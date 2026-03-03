---
title: Benutzer kann nicht zum Adobe Commerce-Cloud-Projekt hinzugefügt werden
description: Dieser Artikel bietet eine Lösung für den Fall, dass Sie keine Benutzenden zu einem Adobe Commerce-Cloud-Projekt hinzufügen können.
feature: Cloud, Paas
solution: Commerce
feature-set: Commerce
role: Developer
source-git-commit: dfb3e7ea8638755cdff16b0765125403f429ef2e
workflow-type: tm+mt
source-wordcount: '288'
ht-degree: 1%

---

# Benutzer kann nicht zum Adobe Commerce-Cloud-Projekt hinzugefügt werden

Dieser Artikel bietet eine Lösung für den Fall, dass Sie versuchen, eine Benutzerin bzw. einen Benutzer zu einem Cloud-Projekt hinzuzufügen, dies jedoch fehlschlägt, mit dem Fehler: *Benutzerin bzw. Benutzer XXX ist nicht vorhanden*.

## Betroffene Produkte und Versionen

* Adobe Commerce auf Cloud-Infrastruktur, [alle unterstützten Versionen](https://magento.com/sites/default/files/magento-software-lifecycle-policy.pdf)

## Problem

Dieser Artikel bietet eine Lösung für den Fall, dass Sie keine Benutzenden zu einem Adobe Commerce-Cloud-Projekt hinzufügen können.

## Ursache

Das Konto des Benutzers muss zunächst unter [https://accounts.magento.cloud](https://accounts.magento.cloud) erstellt und mit seinem Adobe-SSO verknüpft werden, bevor er als Benutzer zum Projekt hinzugefügt werden kann. Wenn der/die Benutzende ein Adobe-Konto, aber kein Commerce-Konto (magento.com) hat, muss er/sie zuerst eines erstellen.

## Lösung

1. Bitten Sie den Benutzer, sich unter [https://accounts.magento.cloud](https://accounts.magento.cloud) anzumelden. Der Benutzer muss bereits mit derselben E-Mail-Adresse bei Adobe registriert sein.
   > **HINWEIS**\
   > Das Erstellen oder besitzen eines Kontos unter [https://account.adobe.com](https://account.adobe.com) bedeutet nicht automatisch, dass der Benutzer über ein Konto unter [https://accounts.magento.cloud](https://accounts.magento.cloud) verfügt. Der Benutzer muss zunächst [sein Commerce-Konto erstellen](https://experienceleague.adobe.com/de/docs/commerce-admin/start/commerce-account/commerce-account-create?lang=en#create-a-commerce-account).

1. Wenn der/die Benutzende bereits über ein Adobe-Konto verfügt, sich jedoch nicht anmelden kann, bitten Sie ihn/sie, eine [Support-Anfrage](https://experienceleague.adobe.com/home?lang=de#support) mit der Einstellung [!UICONTROL Problemgrund] auf *Benutzerverwaltung* zu senden.

1. Nachdem sich der Benutzer erfolgreich bei [https://accounts.magento.cloud](https://accounts.magento.cloud) angemeldet hat, können Sie den Benutzer zum Projekt hinzufügen. Detaillierte Anweisungen finden Sie unter [Hinzufügen von Benutzern und Verwalten des Zugriffs](https://experienceleague.adobe.com/de/docs/commerce-cloud-service/user-guide/project/user-access#add-users-and-manage-access) im Handbuch Commerce on Cloud Infrastructure .

## Verwandtes Lesen:

* [Verwalten des Benutzerzugriffs](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/project/user-access.html?lang=de) finden Sie in unserem Handbuch zu Commerce in Cloud-Infrastrukturen .
* [Anmeldung beim Adobe Commerce Support- oder Cloud-Konto nicht möglich](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/miscellaneous/unable-to-log-in-to-support-or-cloud-project.html?lang=de)