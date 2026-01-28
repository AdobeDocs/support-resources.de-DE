---
title: Berechtigungskonfiguration für den Adobe-Kunden-Support
description: Wie Adobe-Kunden Support-Berechtigungen konfigurieren können, um die Fallübermittlung zu aktivieren.
feature-set: Experience Cloud Services
solution: Admin Console
feature: Admin Console
source-git-commit: 009be3353a4bd690a7cf395e7e95540808058b39
workflow-type: tm+mt
source-wordcount: '356'
ht-degree: 0%

---


# Berechtigung für Adobe-Kunden-Support

Um Support-Berechtigungen für Ihr Unternehmen zu konfigurieren, fügen Sie den Benutzer zunächst über die Admin Console hinzu oder laden Sie ihn ein.

## Hinzufügen von Support-Berechtigungsrollen zu einer Organisation

Die Rolle „Support-Admin“ ist keine Administratorrolle und hat Zugriff auf Support-bezogene Informationen. Support-Administratoren können Problemberichte anzeigen, erstellen und verwalten.

So fügen Sie einen Administrator hinzu oder laden ihn ein:

1. Wählen Sie in der Admin Console **[!UICONTROL Benutzer]** > **[!UICONTROL Administratoren]** aus.
1. Klicken Sie **[!UICONTROL Admin hinzufügen]**.
1. Geben Sie einen Namen oder eine E-Mail-Adresse ein.

   Sie können nach vorhandenen Benutzern suchen oder einen neuen Benutzer hinzufügen, indem Sie eine gültige E-Mail-Adresse angeben und die Informationen auf dem Bildschirm ausfüllen.

   ![Administrator hinzufügen](assets/admin-console-add-admin.png)

1. Klicken Sie **[!UICONTROL Weiter]**. Eine Liste mit Administratorrollen wird angezeigt.

So weisen Sie einem Benutzer die Rolle Support-Administrator zu (damit ein Benutzer den Support kontaktieren kann):

1. Wählen Sie die Option **[!UICONTROL Support-Administrator]** aus.

   ![Administratorrechte bearbeiten](assets/edit-admin-rights.png)

1. Wählen Sie eine der beiden folgenden Optionen:

   * Option 1: **[!UICONTROL Basic Support Administrator]**. Wählen Sie diese Option aus, wenn Sie dem Support-Benutzer Zugriff auf alle Lösungen (mit Ausnahme von Marketo Engage) gewähren möchten.
   * Option 2: **[!UICONTROL Produktsupport-Administrator]**: Wählen Sie diese Option für den Marketo Engage-Support. Wählen Sie aus, welche Marketo Engage-Instanzen dem Benutzer bzw. der Benutzerin Zugriff auf den Support gewähren sollen.

   ![Administratorrechte für Marketo bearbeiten](assets/edit-admin-rights-advanced.png)

1. Nachdem Sie die Auswahl getroffen haben, klicken Sie auf **[!UICONTROL Speichern]**.

Der Benutzer erhält eine E-Mail-Einladung zu den neuen Administratorrechten von `message@adobe.com`.

Benutzer müssen in der E **[!UICONTROL Mail auf]** Erste Schritte“ klicken, um der Organisation beizutreten. Wenn neue Admins den Link **[!UICONTROL Erste Schritte]** in der E-Mail-Einladung nicht verwenden, können sie sich nicht bei Admin Console anmelden.

Im Rahmen des Anmeldevorgangs werden Benutzende möglicherweise aufgefordert, ein Adobe-Profil einzurichten, wenn sie noch keines haben. Wenn Benutzende mehrere Profile mit ihrer E-Mail-Adresse verknüpft haben, müssen sie **[!UICONTROL Team beitreten]** (wenn dazu aufgefordert) und dann das mit der neuen Organisation verknüpfte Profil auswählen.

![Bestätigung der Administratorrechte](assets/admin-rights-confirmation.png)

Weitere Informationen finden Sie in den [Anweisungen zur Bearbeitung ](admin-roles.md#add-enterprise-role) Unternehmensadministratorrolle“ in der Dokumentation zu Administratorrollen. Beachten Sie, dass nur ein Systemadministrator für Ihre Organisation diese Rolle zuweisen kann. Weitere Informationen zur Administrationshierarchie finden Sie in der Dokumentation [Administratorrollen](admin-roles.md) .
