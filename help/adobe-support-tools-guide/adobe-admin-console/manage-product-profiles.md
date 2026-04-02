---
title: Verwalten von Produktprofilen in der Global Admin Console
description: Erfahren Sie, wie globale Administratoren Produktprofile in der Global Admin Console hinzufügen, bearbeiten und löschen können.
feature-set: Experience Cloud Services
solution: Admin Console
feature: Admin Console
product_v2:
  - id: f7bdf6be-dd3b-4d2d-ac52-0e62ed0d3102
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
exl-id: 6a0b2d9f-9e02-428c-a2be-bc457230f7e0
source-git-commit: 976bfc44cdae61376e2da89019f7758518c6fadc
workflow-type: tm+mt
source-wordcount: 579
ht-degree: 1%

---

# Verwalten von Produktprofilen in der Global Admin Console

**Gilt für:** Enterprise

Globale Administratoren können in der [Global Admin Console Produktprofile hinzufügen, bearbeiten und &#x200B;](https://global-admin-console.adobe.com/).

>[!NOTE]
>
>Wählen Sie in der [Global Admin Console](https://experienceleague.adobe.com/de/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/adopt-global-administration#request-access-to-the-global-admin-console) eine Organisation aus und navigieren Sie zu **[!UICONTROL Produkte]**. Sie können alle oder ausgewählte Services für ein Produkt mithilfe von Produktprofilen aktivieren.

Wie im Standard-Admin Console können Sie die Verwendung von Produkten innerhalb eines Unternehmens mithilfe von Produktprofilen optimieren. Sie können auch Administratoren - so genannte **[!UICONTROL Produktprofiladministratoren]** - Produktprofilen zuweisen. Diese Administratoren können Endbenutzer zu den von ihnen verwalteten Produktprofilen hinzufügen.

Um Produktprofile zu verwalten, wählen Sie ein Produkt aus. Die Steuerelemente zum Hinzufügen, Bearbeiten und Löschen von Produktprofilen werden angezeigt.

>[!NOTE]
>
>Für einige Produkte können Sie in der Global Admin Console keine Produktprofile erstellen oder bearbeiten. Verwenden Sie in solchen Fällen stattdessen die [Admin Console](https://experienceleague.adobe.com/de/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/admin-console-overview).

## Produktprofil hinzufügen

1. Wählen Sie in der [Global Admin Console](https://global-admin-console.adobe.com/) eine zu bearbeitende Organisation aus und navigieren Sie dann zur Registerkarte **[!UICONTROL Produkte]**.
1. Wählen Sie ein Produkt aus, dem ein Produktprofil hinzugefügt werden soll.
1. Wählen Sie **[!UICONTROL Profil hinzufügen]** aus.
1. Geben **[!UICONTROL im Dialogfeld]** Profil hinzufügen“ die folgenden Details ein:

   | Feld | Beschreibung |
   |---|---|
   | **[!UICONTROL Name]** | Ein eindeutiger Name für das Produktprofil innerhalb der Organisation, der sich von anderen Produktprofilen und Benutzergruppen unterscheidet. |
   | **[!UICONTROL Kontingent]** | Die Zielanzahl der für dieses Profil zugewiesenen Lizenzen. |
   | **[!UICONTROL Benutzergruppen]** | Wählen Sie aus dem Dropdown-Menü aus oder geben Sie einen Benutzergruppennamen ein. Wenn die Benutzergruppe noch nicht vorhanden ist, erstellen Sie sie zuerst über die Registerkarte [**[!UICONTROL Benutzergruppen &#x200B;]**](https://helpx.adobe.com/de/enterprise/global-admin-console/manage-user-groups.html). |
   | **[!UICONTROL Administratoren]** | Wählen Sie aus dem Dropdown-Menü aus oder geben Sie die E-Mail-Adresse eines Administrators bzw. einer Administratorin ein. Wenn der Administrator noch nicht vorhanden ist, erstellen Sie ihn zuerst auf der Registerkarte [**[!UICONTROL Administratoren &#x200B;]**](https://experienceleague.adobe.com/de/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/manage-administrators). |

   Die [!UICONTROL Benutzergruppen] werden dem Produktprofil zugewiesen. Die angegebenen Administratoren werden zu **[!UICONTROL Produktprofil-]**), die das Profil über die Adobe Admin Console für das jeweilige Unternehmen verwalten können.

   ![Profil hinzufügen](./assets/manage-product-profiles_add-profile.png)

1. Verwenden Sie den Umschalter **[!UICONTROL Benachrichtigungen]**, um E-Mail-Benachrichtigungen zu aktivieren oder zu deaktivieren. Wenn diese Option aktiviert ist, werden Benutzer per E-Mail benachrichtigt, wenn sie dem Profil hinzugefügt oder daraus entfernt werden.
1. Verwenden Sie die einzelnen **[!UICONTROL Services]**-Umschalter, um bestimmte Services für das Produktprofil zu aktivieren oder zu deaktivieren. Weitere Informationen finden Sie unter [Aktivieren/Deaktivieren von Services für ein Produktprofil](https://helpx.adobe.com/de/enterprise/using/enable-disable-services.html).
1. Wählen Sie **[!UICONTROL Speichern]** aus.
1. Wählen Sie **[!UICONTROL Ausstehende Änderungen überprüfen]** aus, sobald Sie die Bearbeitung der Organisationen abgeschlossen haben. Wählen Sie nach der Überprüfung **[!UICONTROL Änderungen übermitteln]** aus, um [auszuführen](https://helpx.adobe.com/de/enterprise/global-admin-console/execute-jobs.html).

## Produktprofil bearbeiten

1. Wählen Sie eine zu bearbeitende Organisation aus, navigieren Sie zur Registerkarte **[!UICONTROL Produkte]** und wählen Sie ein Produkt aus.
1. Wählen Sie das Symbol **[!UICONTROL Weitere Optionen]** ![Weitere Optionen](./assets/manage-product-profiles_more-options.png) für das entsprechende Produktprofil aus und klicken Sie dann auf **[!UICONTROL Profil bearbeiten]**.
1. Aktualisieren Sie die Produktprofildetails nach Bedarf und wählen Sie **[!UICONTROL Speichern]** aus.
1. Wählen Sie **[!UICONTROL Ausstehende Änderungen überprüfen]** aus, sobald Sie die Bearbeitung der Organisationen abgeschlossen haben. Wählen Sie nach der Überprüfung **[!UICONTROL Änderungen übermitteln]** aus, um [auszuführen](https://helpx.adobe.com/de/enterprise/global-admin-console/execute-jobs.html).

## Löschen eines Produktprofils

>[!WARNING]
>
> Durch das Löschen eines Produktprofils wird der Produktzugriff für alle Benutzenden entfernt, die Mitglieder dieses Profils waren oder zu mit diesem Profil verknüpften Benutzergruppen gehörten.

1. Wählen Sie eine zu bearbeitende Organisation aus, navigieren Sie zur Registerkarte **[!UICONTROL Produkte]** und wählen Sie ein Produkt aus.
1. Wählen Sie das Symbol **[!UICONTROL Weitere Optionen]** ![Weitere Optionen](./assets/manage-product-profiles_more-options.png) für das entsprechende Produktprofil aus und klicken Sie dann auf **[!UICONTROL Profil löschen]**.
1. Wählen **[!UICONTROL im]** die Option „OK“ aus.
1. Wählen Sie **[!UICONTROL Ausstehende Änderungen überprüfen]** aus, sobald Sie die Bearbeitung der Organisationen abgeschlossen haben. Wählen Sie nach der Überprüfung **[!UICONTROL Änderungen übermitteln]** aus, um [auszuführen](https://helpx.adobe.com/de/enterprise/global-admin-console/execute-jobs.html).


## Verwandtes Lesen

- [Übernahme globaler Verwaltung](https://experienceleague.adobe.com/de/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/adopt-global-administration)
- [Verwalten von Administratoren](https://experienceleague.adobe.com/de/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/manage-administrators)
- [Benutzergruppen verwalten](https://experienceleague.adobe.com/de/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/manage-user-groups)
- [Zuweisen von Produkten zu untergeordneten Organisationen](https://experienceleague.adobe.com/de/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/allocate-products)
- [Ausstehende Aufträge ausführen](https://helpx.adobe.com/de/enterprise/global-admin-console/execute-jobs.html)
- [Dienste aktivieren/deaktivieren](https://helpx.adobe.com/de/enterprise/using/enable-disable-services.html)
- [Übersicht über Admin Console](https://experienceleague.adobe.com/de/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/admin-console-overview)
