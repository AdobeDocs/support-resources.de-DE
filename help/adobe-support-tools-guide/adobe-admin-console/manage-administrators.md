---
title: Verwalten von Administratoren
description: Wie Adobe-Kunden Administratoren in der Global Admin Console einrichten und verwalten können, um Benutzerzugriff, Produktlizenzen und Organisationsressourcen zu steuern.
feature-set: Experience Cloud Services
solution: Admin Console
feature: Admin Console
exl-id: 41c00379-98ee-4922-8eba-cc373c23a019
source-git-commit: 74d2dd4eb999f91172eec4c3b5690e1e8b8bd293
workflow-type: tm+mt
source-wordcount: '1159'
ht-degree: 2%

---

# Verwalten von Administratoren

*Gilt für Unternehmen.*

Erfahren Sie mehr über die Funktionen globaler Administratoren und darüber, wie Sie die Verwaltung von Benutzern, Produktlizenzen und Gruppen an Administratoren bzw. Administratorinnen für jede einzelne Organisation delegieren und verteilen.

In der Global Admin Console können Sie ein Unternehmen auswählen und zur Registerkarte **[!UICONTROL Administratoren]** navigieren, um Administratorrechte hinzuzufügen, zu bearbeiten oder zu entfernen. Weitere Informationen finden Sie unter [Globale Administration übernehmen](https://helpx.adobe.com/enterprise/global-admin-console/adopt-global-administration.html). Klicken Sie hier [melden Sie sich bei der Admin Console an](https://adminconsole.adobe.com).


Mit der Global Admin Console wird eine Rolle als globaler Administrator eingeführt. Diese Rolle unterscheidet sich von der eines Systemadministrators und ermöglicht Ihnen Folgendes:

- Zeigen Sie die globale Landschaft Ihrer gesamten Adobe-Investitionen in allen Admin Consoles an, die zur Global Admin Console-Hierarchie hinzugefügt wurden.
- Überwachen Sie die Adobe-Lizenz- und Ressourcenzuweisungen und -nutzung über mehrere Admin Consoles hinweg.
- Erstellen Sie Admin Consoles oder Organisationen.
- Weisen Sie Produktlizenzen von einem Stamm oder einem übergeordneten Admin Console untergeordneten Admin Consoles zu, die sich unterhalb der Hierarchie befinden.
- Pflegen Sie den täglichen Betrieb, während Systemadministratoren weiterhin ihre eigenen Admin Consoles verwalten. Beispielsweise kann ein globaler Administrator ein Produkt einem untergeordneten Admin Console zuweisen, es jedoch nicht Benutzern zuweisen. Der Systemadministrator erhält die Lizenzen in seinem Admin Console und weist die Produkte seinen Benutzern zu.
- Wenden Sie optional Organisationsrichtlinien auf alle Admin Consoles in der Hierarchie an.

## Grundlegende Verwaltungsaufgaben

Global Admin Console ist für die unternehmensübergreifende Verwendung mit mehreren Admin Consoles konzipiert. In der folgenden Tabelle sind die verschiedenen Funktionen und der Ort, an dem sie abgeschlossen werden können - Admin Console oder Global Admin Console - aufgeführt.

<table>
  <tr>
    <th colspan="2">Aufgabe</th>
    <th>Global Admin Console</th>
    <th>Admin Console</th>
  </tr>

<tr>
    <td colspan="2">Erstellen, Neuerstellen und Löschen von untergeordneten Organisationen</td>
    <td align="center">Ja</td>
    <td align="center">Nein</td>
  </tr>

<tr>
    <td colspan="2">Arbeiten mit mehreren Organisationen</td>
    <td align="center">Ja</td>
    <td align="center">Nein</td>
  </tr>

<tr>
    <td rowspan="2" valign="middle">Verwalten von Administratoren</td>
    <td>Für eine oder mehrere Organisationen</td>
    <td align="center">Ja</td>
    <td align="center">Nein</td>
  </tr>

<tr>
    <td>Für eine Organisation</td>
    <td align="center">Ja</td>
    <td align="center">Ja</td>
  </tr>

<tr>
    <td colspan="2">Verwalten von Produktprofilen und Benutzergruppen</td>
    <td align="center">Ja</td>
    <td align="center">Ja</td>
  </tr>

<tr>
    <td colspan="2">Richtlinien definieren und verwalten</td>
    <td align="center">Ja</td>
    <td align="center">Nein</td>
  </tr>

<tr>
    <td colspan="2">Produkte organisationsübergreifend zuweisen</td>
    <td align="center">Ja</td>
    <td align="center">Nein</td>
  </tr>

<tr>
    <td colspan="2">Zuweisen von Produkten zu Benutzern</td>
    <td align="center">Nein</td>
    <td align="center">Ja</td>
  </tr>

<tr>
    <td colspan="2">Verwalten von Benutzenden</td>
    <td align="center">Nein</td>
    <td align="center">Ja</td>
  </tr>

<tr>
    <td colspan="2">Verwalten von Paketen</td>
    <td align="center">Nein</td>
    <td align="center">Ja</td>
  </tr>

<tr>
    <td colspan="2">Einrichten von Domains und Verzeichnissen</td>
    <td align="center">Nein</td>
    <td align="center">Ja</td>
  </tr>

<tr>
    <td colspan="2">Verwalten von Unternehmensspeicher und Verschlüsselung</td>
    <td align="center">Nein</td>
    <td align="center">Ja</td>
  </tr>
</table>

## Verwalten von Administratoren

Sie können eine flexible Verwaltungshierarchie erstellen, die eine differenzierte Verwaltung des Zugriffs und der Verwendung von Adobe-Produkten ermöglicht. Ähnlich wie bei der Adobe Admin Console können Sie mit der Global Admin Console System-, Produkt-, Produktprofil-, Benutzergruppen-, Bereitstellungs-, Support- und Speicheradministratoren hinzufügen. Diese Administratoren können ihre jeweiligen Verwaltungsaufgaben in den Organisationen ausführen, deren Administrator sie sind. Neben diesen Rollen gibt es zwei neue Rollen für die globale Administration: Globaler Administrator und Globaler Betrachter.

Globaler Administrator ist eine Übergangrolle. Wenn Sie einen Benutzer zum globalen Administrator einer Organisation machen, wird er automatisch direkt oder indirekt zum globalen Administrator aller untergeordneten Elemente dieser Organisation. Wenn zudem eine neue Organisation in der Organisationshierarchie erstellt wird, werden alle globalen Admins der übergeordneten Elemente dieser Organisation sofort zu globalen Admins der neu erstellten Organisation.

Im Folgenden finden Sie die Funktionen der Rolle „Globaler Administrator“:

- Erstellen und Löschen von untergeordneten Organisationen
- Festlegen und Bearbeiten von Richtlinien
- Festlegen und Ändern von Administratorrollen
- Hinzufügen und Entfernen von Produkten in untergeordneten Organisationen
- Ressourcenzuteilungen für untergeordnete Organisationen festlegen oder ändern
- Verwalten von Produktprofilen und Benutzergruppen

Im Folgenden finden Sie die Funktionen der Rolle „Globaler Betrachter“:

- Anzeigen der Liste der Benutzergruppen, Produkte, Produktprofile, Administratoren, Richtliniensätze und Ressourcen in der Organisation und den untergeordneten Organisationen.

## Verteilte Administration

Durch die Verwaltung von Administratoren kann ein globaler Administrator die Verwaltung von Benutzern, Produktlizenzen und Gruppen für jede einzelne Organisation an Administratoren delegieren und verteilen. Der Administrator, der einer Organisation von einem globalen Administrator hinzugefügt wird, erhält die Flexibilität, die Organisation zu verwalten, ohne Einblick in die Verwaltung anderer Organisationen zu erhalten. Der globale Administrator kann also die Verwaltung von Ressourcen und Benutzern delegieren und die Daten zu diesen Ressourcen und Benutzern isolieren.

Ein globaler Administrator kann Organisationen erstellen, Ressourcen wie Produkte und Speicher an diese Organisationen verteilen, die Einrichtung von Identitäten verwalten und Vorlagen für Unternehmensrichtlinien erstellen und anwenden. Ein Systemadministrator, der von einem globalen Administrator zu einer Organisation hinzugefügt wurde, kann Benutzenden Produkte zuweisen, Benutzer integrieren, Produktprofile erstellen und verwalten und andere Verwaltungsaufgaben innerhalb dieser Organisation ausführen.

## Hinzufügen eines Administrators

1. Wählen Sie in der [Global Admin Console](https://global-admin-console.adobe.com/) eine zu bearbeitende Organisation aus und navigieren Sie dann zur Registerkarte **[!UICONTROL Admins]**.

1. Wählen Sie **[!UICONTROL Admin hinzufügen]** aus.

   ![Global Admin Console-Admin hinzufügen](../assets/global-admin-console-add-admin.png)

1. Geben **[!UICONTROL im Dialogfeld]** Admin hinzufügen“ die folgenden **[!UICONTROL Benutzerdetails]** ein: E-Mail, Vorname, Nachname, Kontotyp und Länder-Code.

   Wenn Sie versuchen, einen vorhandenen Benutzer als Administrator hinzuzufügen, wählen Sie denselben Kontotyp wie der vorhandene Benutzer. Andernfalls schlägt der Hinzufügen-Vorgang fehl.

   >[!NOTE]
   >
   > Organisationen können Einschränkungen bezüglich der möglichen Hinzufügung von Kontotypen haben. Diese können auf &quot;[&quot; ](https://helpx.adobe.com/enterprise/global-admin-console/update-policies.html) anderen Konfigurationsparametern für eine Organisation basieren. Unternehmen erlauben nicht, sowohl Adobe ID-Benutzer als auch BusinessID-Benutzer gleichzeitig hinzuzufügen. Im Allgemeinen sollte es in einer Organisation keine Benutzer beider Typen geben. Abhängig von der Reihenfolge, in der die Regeln festgelegt werden, kann es jedoch einige Benutzer eines bestimmten Kontotyps geben, die vor der Anwendung von Richtlinien oder Regeln aufgetreten sind.

1. Wählen Sie im Abschnitt „Administratorrechte“ mindestens **[!UICONTROL Administratorrollen]**.

   Wählen Sie für Rollen wie Produktadministrator, Produktprofil-Administrator und Benutzergruppen-Administrator die spezifischen Produkte, Profile bzw. Gruppen aus.

   ![Global Admin Console-Admin hinzufügen](../assets/global-admin-console-add-admin-detail.png)

1. Wählen Sie **[!UICONTROL Speichern]** aus.

1. Wählen Sie nach der Bearbeitung von Organisationen **[!UICONTROL Ausstehende Änderungen überprüfen]** und dann **[!UICONTROL Änderungen übermitteln]** aus, um [ Änderungen ](https://helpx.adobe.com/enterprise/global-admin-console/execute-jobs.html).

Wenn eine Administratorrolle hinzugefügt wird, erhält der Benutzer eine E-Mail-Benachrichtigung, die ihn über die Änderung in seiner Rolle informiert.

Nachdem der Administrator hinzugefügt wurde, erhält er eine E-Mail-Nachricht, in der er aufgefordert wird, seine Rolle zu akzeptieren, und über die er einen Link zur Admin Console erhält. Wenn sie sowohl als globaler Administrator als auch in einer anderen Rolle hinzugefügt werden, erhalten sie zwei Einladungen, eine zur Global Admin Console und eine zur Admin Console.

## Bearbeiten eines Administrators

1. Wählen Sie eine Organisation aus, um sie zu bearbeiten, und navigieren Sie zur Registerkarte **[!UICONTROL Administratoren]**.

1. Wählen Sie das Symbol **[!UICONTROL Weitere Optionen]** (⋮) für den entsprechenden Administrator und dann **[!UICONTROL Admin bearbeiten]**.

   ![Administratorrechte für Global Admin Console bearbeiten](../assets/global-admin-console-edit-admin-right.png)

1. Aktualisieren Sie die Administratordetails und wählen Sie dann **[!UICONTROL Speichern]** aus.

1. Wählen **[!UICONTROL Ausstehende Änderungen überprüfen]** aus, nachdem Sie die Organisationen bearbeitet haben.

Für jede hinzugefügte oder entfernte Administratorrolle wird ein separater Befehl in der Liste Ausstehende Änderungen angezeigt. Wählen Sie nach der Überprüfung **[!UICONTROL Änderungen übermitteln]** aus, um [auszuführen](https://helpx.adobe.com/enterprise/global-admin-console/execute-jobs.html).

## Administratorrechte entfernen

1. Wählen Sie eine Organisation aus, um sie zu bearbeiten, und navigieren Sie zur Registerkarte **[!UICONTROL Administratoren]**.

1. Wählen Sie das Symbol **[!UICONTROL Weitere Optionen]** (⋮) für den entsprechenden Administrator und dann **[!UICONTROL Administratorrechte entfernen]**.

   ![Global Admin Console entfernt Administratorrechte](../assets/global-admin-console-remove-admin-right.png)

1. Wählen **[!UICONTROL OK]** im Bestätigungsdialogfeld aus.

1. Wählen **[!UICONTROL Ausstehende Änderungen überprüfen]** aus, nachdem Sie die Organisationen bearbeitet haben. Wählen Sie nach der Überprüfung **[!UICONTROL Änderungen übermitteln]** aus, um [auszuführen](https://helpx.adobe.com/enterprise/global-admin-console/execute-jobs.html).

Nachdem Sie einen Administrator gelöscht haben, erhält der Benutzer eine E-Mail-Benachrichtigung, in der er über den Verlust des Zugriffs auf die Admin Console für diese Organisation informiert wird.
