---
title: Wie man ein Teammitglied in Support-Benachrichtigungen einbezieht
description: In diesem Artikel wird erläutert, wie Sie ein Team-Mitglied in Support-Benachrichtigungen einbeziehen.
feature: Cloud, Support, Admin Workspace
role: Admin, Developer
solution: Commerce
feature-set: Commerce
exl-id: 392ef795-f710-401f-8b0e-3c8dfec7bb3a
TQID: 'https://experienceleague.adobe.com/fWRfvDT8NCwPfzmAx1Zowo4T8KvKLKWqhDkZDfX8stU'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: e7dae43f-215c-4cdf-90d3-c5a461a6e669
subfeature_v2:
  - id: bb2df8be-afdd-4818-b6b5-95ca1dd3bc3a
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 9f1760d31cd80e0358aa341c3f6091b2a86b6d67
workflow-type: tm+mt
source-wordcount: 305
ht-degree: 12%

---


# Wie man ein Teammitglied in Support-Benachrichtigungen einbezieht

In diesem Artikel wird erläutert, wie ein Team-Mitglied einbezogen werden kann, um automatisch Support-Aktualisierungen über E-Mail-Benachrichtigungen zu erhalten.

## Betroffene Produkte und Versionen

* Adobe Commerce auf Cloud-Infrastruktur, alle [unterstützten Versionen](https://www.adobe.com/content/dam/cc/en/legal/terms/enterprise/pdfs/Adobe-Commerce-Software-Lifecycle-Policy.pdf).

## Ursache

* Das Teammitglied wurde dem [!DNL cloud project] nicht mit den erforderlichen Berechtigungen hinzugefügt.
* Das Teammitglied hat kein Support-Konto.

## Lösung

1. Navigieren Sie zur **[!DNL Cloud Project URL]** (Beispiel: `https://us-3.magento.cloud/projects/xxxxxx/edit`).
1. Überprüfen Sie, ob das Teammitglied zum Projekt hinzugefügt wurde und ein [!DNL Project Admin] ist.

Wenn sie dem Projekt nicht hinzugefügt wurden, müssen Sie sie als [!DNL Project Admin] hinzufügen und [!DNL Shared Access] gewähren:

* [Verwalten des Benutzerzugriffs](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/project/user-access.html?lang=de) in unserem Benutzerhandbuch.
* [Benutzer kann nicht zum Adobe Commerce-Cloud-Projekt hinzugefügt werden](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/miscellaneous/unable-add-user-adobe-commerce-cloud-project.html?lang=de) in unserer Commerce-Wissensdatenbank.
* [Benutzerhandbuch für Adobe Commerce Help Center: Freigegebener Zugriff](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide.html?lang=de#shared-access) in unserer Commerce-Wissensdatenbank.

Wenn sie zur [!DNL cloud project] hinzugefügt wurden, aber nicht über die [!DNL Project Admin role] verfügen, aktualisieren Sie ihren [!DNL role] entsprechend unter [Benutzerzugriff verwalten](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/project/user-access.html?lang=de).

Wenn Sie möchten, dass ein Teammitglied bei allen für Ihre Organisation geöffneten Fällen als Beobachter fungieren kann, reichen Sie ein „Support[Ticket“ &#x200B;](https://experienceleague.adobe.com/home?lang=de&support-tab=home#support).

## Verwandtes Lesen

[Ehemalige Team-Mitglieder erhalten Adobe Commerce Cloud-Benachrichtigungs-E-Mails](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/miscellaneous/former-teammembers-receive-cloud-notification-emails.html?lang=de)
