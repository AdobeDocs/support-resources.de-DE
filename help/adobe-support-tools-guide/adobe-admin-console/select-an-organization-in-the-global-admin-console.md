---
title: Organisation in der Global Admin Console auswählen
description: Erfahren Sie, wie Sie eine Organisation für die Bearbeitung in der Global Admin Console auswählen.
feature-set: Experience Cloud Services
solution: Admin Console
feature: Admin Console
exl-id: 6a94922a-3343-433d-96e7-0af0f26581a1
source-git-commit: d5f0473b100cda574b4980e6c871a9c275f9f95a
workflow-type: tm+mt
source-wordcount: '631'
ht-degree: 2%

---

# Organisation in der Global Admin Console auswählen

Erfahren Sie, wie Sie eine Organisation für die Bearbeitung in der Global Admin Console auswählen.

>[!NOTE]
>
>Nachdem Sie Zugriff auf die [Global Admin Console](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/adopt-global-administration#request-access-to-the-global-admin-console) haben, können Sie zunächst ein Unternehmen auswählen, um den Namen, die Benutzergruppen, die Produktprofile, die Administratoren und die Organisationsrichtlinien des Unternehmens anzuzeigen und zu verwalten. Um sich anzumelden, navigieren Sie zur [Global Admin Console](https://global-admin-console.adobe.com/).

Der Global Admin Console fungiert als zentraler Management-Hub für Adobe-Ressourcen. Globale Administratoren können:

- Erstellen von untergeordneten Organisationen unter ihrer Organisation
- Systemadministratoren zuweisen, um sie zu verwalten
- Verteilen von Ressourcen an untergeordnete Organisationen zur Verwaltung und Zuweisung an Benutzer in diesen Organisationen

>[!NOTE]
>
> Benutzer und Administratoren in einer Organisation haben keine Sichtbarkeit für Benutzer, Speicher oder andere Ressourcen außerhalb ihrer Organisation.

## Organisation auswählen

In der Dropdown-Liste **[!UICONTROL Organisationsauswahl]** werden Organisationen aufgelistet, von denen Sie explizit ein globaler Administrator sind. Das heißt, Sie wurden der Administratorliste dieser Organisation mit der Rolle „Globaler Administrator“ oder „Globaler Betrachter“ hinzugefügt. Sie sind implizit ein globaler Administrator (oder globaler Betrachter) aller Organisationen unter diesem Punkt in der Hierarchie, diese Organisationen werden jedoch nicht in der [!UICONTROL Organisationsauswahl] aufgeführt.

![Organisationsauswahl](/help/adobe-support-tools-guide/assets/org-picker.png)

Wenn Sie möchten, dass sie aufgelistet werden, fügen Sie sich den Organisationen, die Sie auflisten möchten, als globaler Administrator hinzu. Wenn Sie eine Organisation in der [!UICONTROL Organisationsauswahl] auswählen, basieren Ihre Administratorberechtigungen darauf, ein globaler Administrator der ausgewählten Organisation zu sein. Möglicherweise werden Sie auch als globaler Administrator einer übergeordneten Organisation weiter oben in der Struktur aufgeführt, was Ihnen mehr Berechtigungen erteilen könnte. Sie müssen diese übergeordnete Organisation auswählen, um die zusätzlichen Berechtigungen zu erhalten.

Nachdem Sie in der Global Admin Console eine Organisation aus der [!UICONTROL Hierarchiestruktur] ausgewählt haben, können Sie damit beginnen, Informationen für eine bestimmte Organisation zu bearbeiten.

**Bearbeitungen können Folgendes betreffen:**

- Organisationsname
- Benutzergruppen
- Produktprofile
- Administratoren
- Organisationsrichtlinien

**Bearbeitungen können Folgendes nicht betreffen:**

- Benutzer (außer zum Löschen von Gruppen oder Produktprofilen)
- Hinzufügen von Benutzern (außer für Administratoren)

Wenn eine Organisation in der Hierarchie-Struktur ausgewählt wird, werden die folgenden Informationen angezeigt:

- Organisationsname
- Region
- Anzahl der Benutzer
- Liste der Produkte
- Produktprofile
- Benutzergruppen
- Administratoren
- Angeforderte Domains
- Richtlinienwerte der Organisation

Zum Anzeigen oder Bearbeiten von Produkten, Benutzergruppen, Administratoren, Domains, Richtlinien oder Richtlinienvorlagen wählen Sie die entsprechende Registerkarte aus. In den meisten Fällen können Sie [!UICONTROL &#x200B; Feld &#x200B;]Suche“ verwenden, um ein bestimmtes Element auf der Registerkarte zu finden.

![Organisation bearbeiten](/help/adobe-support-tools-guide/assets/edit-an-organization.png)

Alle Administratoren, die einer Organisation hinzugefügt oder daraus entfernt werden, erhalten eine E-Mail-Benachrichtigung. Bestimmte Richtlinienänderungen an einer Organisation führen zu einer Benachrichtigung in der Admin Console dieser Organisation.

## Erfahren Sie mehr über die Einschränkungen und erforderlichen Bedingungen

- Die maximale Tiefe für verschachtelte Organisationen beträgt fünf. Also ist a/b/c/d/e erlaubt, aber a/b/c/d/e/f ist ein Fehler. Beispiel: Acme Corp/ International Region/ Acme Europe/ Acme UK/ Acme London ist erlaubt, aber Acme Corp/ International Region/ Acme Europe/ Acme UK/ Acme London/ Acme Mayfair ist ein Fehler.

- Die maximale Länge des Pfadnamens (einschließlich aller Organisationen) beträgt 255 Zeichen (einschließlich &quot;/„). Die maximale Länge für einen einzelnen Organisationsnamen beträgt zwischen 4 und 100 Zeichen.

- Der Organisations-Pfadname ist eindeutig, der einfache Name ist jedoch nur unter den gleichrangigen Elementen eindeutig. Es kann Organisationen mit demselben einfachen Namen an anderer Stelle in der Organisationshierarchie geben.

- Sie können die Liste der mit der ausgewählten Organisation verknüpften Domains nur über die globale Admin Console anzeigen. Wenn Sie Systemadministrator der ausgewählten Organisation sind, wählen Sie die Option **[!UICONTROL In Admin Console öffnen]** aus, um [Domains zu verwalten](https://helpx.adobe.com/enterprise/using/manage-domains-directories.html). Informationen zu den auf der Registerkarte Domains angezeigten Informationen finden Sie unter [Schemata exportieren und importieren](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/export-or-import-organization-structure-and-product-allocations#export-and-import-schemas).

- IE 11 wird für den globalen Verwaltungszugriff nicht unterstützt. Verwenden Sie einen anderen Browser oder eine neuere Version von IE Browser.
