---
title: Organisationshierarchie verwalten
description: Erfahren Sie, wie globale Administratoren die Hierarchie des Unternehmens in der Global Admin Console verwalten können.
Feature-set: Experience Cloud Services
Solution: Admin Console
Feature: Admin Console
source-git-commit: 3b3b2711887f0db086e4eb8281344cc7356accf7
workflow-type: tm+mt
source-wordcount: '1626'
ht-degree: 0%

---

# Organisationshierarchie verwalten

Gilt für Unternehmen.

Hier erfahren Sie, wie globale Administratoren die Hierarchie des Unternehmens in der Global Admin Console verwalten können.

Nachdem Sie [Zugriff auf  [!DNL Global Admin Console]](https://helpx.adobe.com/enterprise/global-admin-console/adopt-global-administration.html#request-access) erhalten haben, können Sie neue Organisationen erstellen, der Hierarchie vorhandene Organisationen hinzufügen, Organisationen löschen und eine übergeordnete Organisation ändern.
[Bei der Global Admin Console anmelden](https://global-admin-console.adobe.com/)

Eine Organisation ist eine Struktur zur Verwaltung von Adobe-Produkten und -Benutzern. Mit dem [[!DNL Adobe Admin Console]](https://helpx.adobe.com/de/enterprise/using/admin-console.html) können Administratoren die Bereitstellung und Konfiguration von Produkten und Benutzern in ihrer Organisation verwalten. Mit dem [[!DNL Global Admin Console]](https://helpx.adobe.com/enterprise/global-admin-console/overview.html) können globale Administratoren mehrere Organisationen erstellen, verwalten und löschen.

## Erstellen einer untergeordneten Organisation

Als [globaler Administrator](https://helpx.adobe.com/enterprise/global-admin-console/manage-administrators.html) können Sie untergeordnete Organisationen jeder Organisation in der Hierarchie erstellen und den Namen, das Land, Benutzergruppen, Produkte, Produktprofile, Administratoren und Richtlinien festlegen.

Wenn eine neue untergeordnete Organisation erstellt wird, werden automatisch die folgenden Elemente von der direkt übergeordneten Organisation übernommen:

- Einstellungen der Organisation [Richtlinie](https://helpx.adobe.com/enterprise/global-admin-console/update-policies.html) (einschließlich Sperren, falls vorhanden).
- Die Liste der Systemadministratoren (gesteuert durch &quot;**[!UICONTROL bei der Erstellung übernehmen]** [Richtlinie](https://helpx.adobe.com/enterprise/global-admin-console/update-policies.html)).
Folgendes kann verhindern, dass Systemadministratoren übernommen werden:
   - Mangel an [Domain-Vertrauen](https://helpx.adobe.com/enterprise/using/directory-trust.html).
   - Benutzertypbeschränkungen (Benutzerrichtlinien für Adobe ID/Enterprise ID/Federated ID hinzufügen). Erfahren Sie mehr über [Richtliniendetails](https://helpx.adobe.com/enterprise/global-admin-console/update-policies.html).
- Zugriff auf [[!DNL Federated ID]] oder [[!DNL Enterprise ID]] Benutzer von Domains aus, auf die die übergeordnete Organisation Zugriff hat. Dadurch werden die Domain-Benutzer im übergeordneten Element in der untergeordneten Organisation verfügbar. Die Vererbung des Benutzerzugriffs wird von **Benutzer aus von der übergeordneten Organisation verwalteten Verzeichnissen erben** [Richtlinie](https://helpx.adobe.com/enterprise/global-admin-console/update-policies.html) gesteuert.
- Freigaberichtlinie, Kennwortrichtlinie und Sicherheitskontakte (gesteuert durch **Elementfreigabeeinstellungen beim Erstellen einer untergeordneten Organisation erben** [Richtlinie](https://helpx.adobe.com/enterprise/global-admin-console/update-policies.html)).

1. Melden Sie sich bei der [Global Admin Console](https://global-admin-console.adobe.com/) an. Wählen Sie auf der Registerkarte **[!UICONTROL Organisationen]** die Organisation aus, der Sie eine untergeordnete Organisation hinzufügen möchten.
2. Wählen Sie das Symbol **[!UICONTROL Hinzufügen+]** aus.
   ![Organisation hinzufügen](/help/adobe-support-tools-guide/assets/add-an-organization-1.png)
3. Geben Sie einen **Namen** und das **Land** der Organisation an.\
   Der einfache Name des Unternehmens muss zwischen 4 und 100 Zeichen lang sein. Die maximale Länge für den Pfadnamen beträgt 255 Zeichen.
   ![Untergeordnete Organisation hinzufügen](/help/adobe-support-tools-guide/assets/add-an-child-organization.png)
4. Wählen Sie **[!UICONTROL Speichern]** aus.
5. Wählen **[!UICONTROL Ausstehende Änderungen überprüfen]** aus, nachdem Sie die Organisationen bearbeitet haben. Wählen Sie nach der Überprüfung **[!UICONTROL Änderungen übermitteln]** aus, um [auszuführen](https://helpx.adobe.com/enterprise/global-admin-console/execute-jobs.html).

## Untergeordnete Organisation löschen

Als [globaler Administrator](https://helpx.adobe.com/enterprise/global-admin-console/manage-administrators.html) können Sie untergeordnete Organisationen löschen. Der Löschvorgang kann nicht rückgängig gemacht werden, und die Stammorganisation kann nicht gelöscht werden. Die der gelöschten Organisation zugewiesenen Ressourcen werden an die übergeordnete Organisation zurückgegeben. Bevor eine Organisation gelöscht wird, wird ihr übergeordnetes Element automatisch zum übergeordneten Element einer ihrer untergeordneten Organisationen.

Eine Organisation kann nur gelöscht werden, wenn die folgenden Kriterien erfüllt sind:

- Im Unternehmen gibt es keine Signaturkonten, Adobe Stock-Käufe oder Speicher-Repositorys.
- Es gibt keine beanspruchten Domänen in der Organisation.
- Es gibt keine instanziierten Produkte in der Organisation.
- Es gibt keine Experience Cloud-Produkte, die Instanziierungen im Unternehmen enthalten können.

>[!WARNING]
>
>Das Löschen einer Organisation wirkt sich auf Ihre Benutzenden aus. Sicherstellen, dass beim Löschen einer Organisation kein Zugriff auf Informationen verloren geht.

1. Melden Sie sich beim [[!DNL Global Admin Console]](https://global-admin-console.adobe.com/) an. Gehen Sie zur Registerkarte **[!UICONTROL Organisationen]** und wählen Sie die Organisation aus, die Sie löschen möchten.
1. Wählen Sie das Symbol **[!UICONTROL Löschen]** aus.
   ![Organisation löschen](/help/adobe-support-tools-guide/assets/delete-organization.png)
1. Wählen **[!UICONTROL Dialogfeld „Organisation]**&quot; die Option **[!UICONTROL OK]**.
1. Wählen **[!UICONTROL Ausstehende Änderungen überprüfen]** aus, nachdem Sie die Organisationen bearbeitet haben. Wählen Sie nach der Überprüfung **[!UICONTROL Änderungen übermitteln]** aus, um [auszuführen](https://helpx.adobe.com/enterprise/global-admin-console/execute-jobs.html).

## Organisation umbenennen

Der Organisationsname ist der offizielle Name Ihres Unternehmens oder Ihrer Institution, der beim Kauf festgelegt wird. Benutzer sehen diesen Namen bei der Auswahl eines Profils während der Anmeldung, insbesondere wenn sie Zugriff auf Adobe-Produkte von mehreren Unternehmen haben oder zwischen einem Geschäfts- und einem Privatprofil wählen müssen.

Als [globaler Administrator](https://helpx.adobe.com/enterprise/global-admin-console/manage-administrators.html) können Sie den Namen jeder übergeordneten oder untergeordneten Organisation bearbeiten, um Benutzern zu helfen, das richtige Profil zu identifizieren, wenn sie sich bei [[!DNL Creative Cloud]] Produkten und Services anmelden.

1. Melden Sie sich bei der [Global Admin Console](https://global-admin-console.adobe.com/) an. Wählen Sie auf **[!UICONTROL Registerkarte]** die Organisation aus, die Sie umbenennen möchten.
1. Wählen Sie das Symbol **[!UICONTROL Bearbeiten]** aus.
   ![Organisation umbenennen](/help/adobe-support-tools-guide/assets/rename-organization.png)
1. Aktualisieren Sie den Namen Ihres Unternehmens und wählen Sie **[!UICONTROL Speichern]** aus.

>[!TIP]
>
>Verwenden Sie einen klaren, erkennbaren Organisationsnamen mit bis zu 255 Zeichen, um Benutzern die Auswahl des richtigen Profils zu erleichtern. Verwenden Sie keine Sonderzeichen und erwägen Sie, Region, Abteilung oder Berechtigung einzuschließen. Vermeiden Sie außerdem ungewöhnliche Akronyme und vage oder ähnliche Namen in Ihrer Unternehmenshierarchie.
>Verwenden Sie einen klaren, erkennbaren Organisationsnamen mit bis zu 255 Zeichen, um Benutzern die Auswahl des richtigen Profils zu erleichtern. Verwenden Sie keine Sonderzeichen und erwägen Sie, Region, Abteilung oder Berechtigung einzuschließen. Vermeiden Sie außerdem ungewöhnliche Akronyme und vage oder ähnliche Namen in Ihrer Unternehmenshierarchie.

Änderungen werden im Administratorprotokoll protokolliert, alle Benutzer werden per E-Mail benachrichtigt und der Name kann 24 Stunden lang nicht erneut aktualisiert werden. [Erfahren Sie, wie Sie Auditprotokolle anzeigen und herunterladen können](https://helpx.adobe.com/enterprise/global-admin-console/insights.html).

## Ändern des übergeordneten Elements einer Organisation

[[!DNL Global Administrator]](https://helpx.adobe.com/enterprise/global-admin-console/manage-administrators.html) können Sie eine Organisation in der Organisationshierarchie mithilfe der Schaltfläche **[!UICONTROL Hierarchie ändern]** neu übergeben.

Das Ändern des übergeordneten Elements einer Organisation hat die folgenden Auswirkungen:

- Durch das Neuerteilen einer Organisation wird der gesamte Unterbaum verschoben, der in der übergeordneten Organisation verwurzelt ist. Die Pfadnamen der übergeordneten Organisation und ihrer untergeordneten Elemente werden aktualisiert, um ihren neuen Speicherort widerzuspiegeln.
- Organisation [Richtlinien](https://helpx.adobe.com/enterprise/global-admin-console/update-policies.html) verschobener Organisationen werden aktualisiert, sodass alle Richtliniensperren von einer Organisation in der neuen Hierarchie verwaltet werden.
- Wenn Sie die Position einer Organisation in der Hierarchie ändern, können sich die globalen Administratoren für diese Organisation ändern. Globale Administratorrollen werden in der Hierarchie nach unten vererbt, sodass alle globalen Administratoren der neuen übergeordneten Organisation automatisch zu globalen Administratoren der verschobenen Organisation werden. Ebenso können globale Administratoren ihre Rolle in der verschobenen Organisation verlieren, wenn sie diese Rolle innehatten, weil sie ein globaler Administrator der alten übergeordneten Organisation waren. Die geerbten globalen Administratorrollen werden nicht im Bereich Administratoren der Organisation aufgeführt.
- Die Änderung der übergeordneten Organisation wirkt sich auch auf die verfügbaren Produkte in den verschobenen Organisationen aus. Wenn möglich, werden [Produktzuordnungen](https://helpx.adobe.com/enterprise/global-admin-console/allocate-products.html) so aktualisiert, dass sie über den neuen übergeordneten Speicherort erfolgen.
- Wenn Produktzuweisungen nicht so aktualisiert werden können, dass sie von dem neuen übergeordneten Element stammen, werden die Produkte zusammen mit den Produktprofilen dieser Produkte entfernt. Benutzende können infolge dieses Vorgangs den Zugriff verlieren. Damit das Produkt am neuen Speicherort verfügbar ist, muss das Produkt beim nächsten gemeinsamen Vorgänger der alten und neuen Speicherorte verfügbar sein.

>[!WARNING]
>
>Wenn Produkte infolge der Reparentation entfernt werden, verlieren Benutzer den Zugriff auf diese Produkte.

1. Melden Sie sich bei der [Global Admin Console](https://global-admin-console.adobe.com/) an. Wählen Sie auf **[!UICONTROL Registerkarte]** Organisationen“ die Option **[!UICONTROL Hierarchie ändern]** aus, um die Neugestaltung der Organisationen zu aktivieren.
2. Wählen Sie **[!UICONTROL Popup]** Bildschirm, der angezeigt wird, OK aus.
3. Ziehen Sie zum erneuten Übernehmen die untergeordnete Organisation auf die gewünschte Organisation.
4. Wählen Sie **[!UICONTROL Speichern]** aus, wenn Sie die Neuzuordnung Ihrer Organisationen abgeschlossen haben.
5. Wählen **[!UICONTROL Ausstehende Änderungen überprüfen]** aus, nachdem Sie die Organisationen bearbeitet haben. Wählen Sie nach der Überprüfung **[!UICONTROL Änderungen übermitteln]** aus, um [auszuführen](https://helpx.adobe.com/enterprise/global-admin-console/execute-jobs.html).

Sobald der Auftrag abgeschlossen ist, können Sie zur Produktzuordnung navigieren und [die Zuweisungswerte ändern](https://helpx.adobe.com/enterprise/global-admin-console/allocate-products.html) um die Änderung bei der Zuordnung von Produktressourcen widerzuspiegeln.

## Hinzufügen vorhandener Organisationen mithilfe des Organisations-Mappers

Als [globaler Administrator](https://helpx.adobe.com/enterprise/global-admin-console/manage-administrators.html) können Sie bestehende Organisationen, die derzeit nicht Teil Ihrer Global Admin Console-Hierarchie sind, zur Organisationshierarchie hinzufügen.

Sie können der Organisationshierarchie auch Team-Organisationen hinzufügen. Teamorganisationen nehmen nicht an der Produktzuordnung oder dem Produktverwendungsrollup teil, und die Verwaltung von Teamorganisationen in der Global Admin Console ist begrenzt. Sie können sie der Organisationshierarchie hinzufügen, um den Überblick zu behalten und die von ihnen erworbenen Produkte zu verfolgen. Team-Organisationen können keine untergeordneten Organisationen haben und verfügen nicht über viele der Funktionen von Unternehmensorganisationen.

Erfahren Sie mehr über die [Einschränkungen bei der Produktzuweisung](https://helpx.adobe.com/enterprise/global-admin-console/allocate-products.html#limitations).

>[!WARNING]
>
> Sie können untergeordnete Organisationen nur zu Stammorganisationen hinzufügen, die auf demselben Speichermodell basieren. Untergeordnete Organisationen, die auf dem Benutzerspeichermodell basieren, können daher nur zu Stammorganisationen hinzugefügt werden, die auf dem Benutzerspeichermodell basieren. Außerdem können untergeordnete Organisationen, die auf dem Enterprise-Speichermodell basieren, nur auf Basis des Enterprise-Speichermodells zu Stammorganisationen hinzugefügt werden.
>Sie können untergeordnete Organisationen nur zu Stammorganisationen hinzufügen, die auf demselben Speichermodell basieren. Untergeordnete Organisationen, die auf dem Benutzerspeichermodell basieren, können daher nur auf der Grundlage des Benutzerspeichermodells zu Stammorganisationen hinzugefügt werden. Außerdem können untergeordnete Organisationen, die auf dem Enterprise-Speichermodell basieren, nur auf Basis des Enterprise-Speichermodells zu Stammorganisationen hinzugefügt werden.

Die Registerkarte **[!UICONTROL Organisationszuordnung]** zeigt Folgendes an:

1. Eine Dropdown-Liste mit einer Liste möglicher übergeordneter Organisationen, denen Sie eine untergeordnete Organisation hinzufügen können. Dies sind Organisationen, für die Sie ein globaler Administrator sind.
1. Eine Liste der untergeordneten Organisationen, die unter der in Schritt 1 ausgewählten übergeordneten Organisation hinzugefügt werden können. Hierbei handelt es sich um Organisationen, für die Sie Systemadministrator sind und die noch kein untergeordnetes Element einer anderen Organisation sind.

Wenn eine Organisation zur globalen Administration hinzugefügt wird, bleiben Produkte in den Organisationen, die mit dem Organisations-Mapper hinzugefügt werden, als Käufe erhalten; [Produktzuordnung](https://helpx.adobe.com/enterprise/global-admin-console/allocate-products.html) Zahlen werden bei diesen Organisationen nicht mehr aggregiert.

1. Melden Sie sich bei der [Global Admin Console](https://global-admin-console.adobe.com/) an und navigieren Sie zu **[!UICONTROL Organization Mapper]**.
2. Wählen Sie in der Dropdown-Liste eine übergeordnete Organisation aus.\
   Dies sind die Organisationen, denen Sie als globaler Administrator direkt hinzugefügt werden. Wenn in der Dropdown-Liste keine Organisation angezeigt wird, die als übergeordnetes Element verwendet werden soll, wählen Sie eine weiter oben in der Hierarchie aus. Sobald der Vorgang „Organisationszuordnung“ abgeschlossen ist, können Sie mit [Hierarchie ändern](https://helpx.adobe.com/enterprise/global-admin-console/set-up-organizations.html#change-the-parent-of-an-organization) die neue Organisation in der Baumstruktur nach unten verschieben, um das übergeordnete Element zu erhalten, das Sie verwenden möchten.
3. Wählen Sie die Organisationen aus, die als untergeordnete Organisationen der im vorherigen Schritt ausgewählten Organisation hinzugefügt werden sollen.
4. Wählen **[!UICONTROL Ausstehende Änderungen überprüfen]** aus. Wählen Sie dann **[!UICONTROL Änderungen übermitteln]** aus, um [&#x200B; auszuführen](https://helpx.adobe.com/enterprise/global-admin-console/execute-jobs.html).
5. Nachdem Sie die Änderungen ausgeführt haben, können Sie die oben genannten Schritte wiederholen, um weitere untergeordnete Organisationen zu Ihrer Organisationshierarchie hinzuzufügen.

Sobald sich eine Organisation in der Hierarchie befindet, können Sie Organisationsrichtlinien, Administratoren oder andere Einstellungen anpassen, indem Sie zur Registerkarte **[!UICONTROL Organisationen]** navigieren.
