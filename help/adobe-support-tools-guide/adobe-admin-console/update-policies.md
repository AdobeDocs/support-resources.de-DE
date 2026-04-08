---
title: Aktualisieren von Organisationsrichtlinien in der Global Admin Console
description: Erfahren Sie, wie ein globaler Administrator Richtlinien für eine Organisation und ihre untergeordneten Elemente in der Global Admin Console festlegen und ändern kann.
feature-set: Experience Cloud Services
solution: Admin Console
feature: Admin Console
product_v2:
  - id: f7bdf6be-dd3b-4d2d-ac52-0e62ed0d3102
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
exl-id: bf8d4e71-30a6-4d6c-8749-47070e5b1906
source-git-commit: ad324036dbeb2a54855349321b2ba33405d2c075
workflow-type: tm+mt
source-wordcount: 1007
ht-degree: 2%

---

# Aktualisieren von Organisationsrichtlinien in der Global Admin Console

**Gilt für:** Enterprise

Erfahren Sie, wie ein globaler Administrator Richtlinien für eine Organisation und ihre untergeordneten Elemente in der Global Admin Console festlegen und ändern kann.

>[!NOTE]
>
>Wählen Sie in der [Global Admin Console](https://helpx.adobe.com/de/enterprise/global-admin-console/adopt-global-administration.html) eine Organisation aus der Hierarchie aus und navigieren Sie zur Registerkarte **Richtlinien**, um die Richtlinien zuzulassen oder zu verbieten oder zu sperren.
>
> [Bei Global Admin Console anmelden](https://global-admin-console.adobe.com/)

Richtlinien sind mit einer Organisation verknüpft und beschränken die Vorgänge, die für diese Organisation ausgeführt werden können. Wenn ein Richtlinienwert festgelegt wird, werden von diesem Zeitpunkt an Aktionen eingeschränkt oder aktiviert.
Wenn beispielsweise die Richtlinie **Anspruchsdomänen** auf *nicht zulässig* festgelegt ist, können keine zusätzlichen Domains angefordert werden, aber Domains, die vor dem Festlegen des Richtlinienwerts angefordert wurden, sind davon nicht betroffen.

## Richtlinien konfigurieren

Gehen Sie wie folgt vor, um die Richtlinien einer Organisation zu ändern:

1. Wählen Sie in [&#x200B; Global Admin Console eine Organisation aus](https://helpx.adobe.com/de/enterprise/global-admin-console/overview.html) um sie zu bearbeiten, und navigieren Sie dann zur Registerkarte **[!UICONTROL Richtlinien]**.
1. Wählen Sie den Umschalter für die entsprechende Richtlinie aus, um sie zuzulassen oder nicht zuzulassen. Sie können auch eine Richtlinie sperren, sodass sie nur von einem globalen Administrator der [ausgewählten Organisation](https://helpx.adobe.com/de/enterprise/global-admin-console/overview.html) oder der übergeordneten Organisation geändert oder entsperrt werden kann.
1. Um eine Richtlinie zu sperren, wählen Sie das Symbol **[!UICONTROL Sperren]** ![Sperren](./assets/lock.png) aus. Wenn Sie den Mauszeiger über die Sperre bewegen, wird der Name der ausgewählten Organisation angezeigt. Weitere Informationen zu [Richtliniensperren](#policy-locks).
1. Wählen Sie **[!UICONTROL Ausstehende Änderungen überprüfen]** aus, nachdem Sie die Organisationen bearbeitet haben. Wählen Sie nach der Überprüfung **[!UICONTROL Änderungen übermitteln]** aus, um [auszuführen](https://helpx.adobe.com/de/enterprise/global-admin-console/execute-jobs.html).

## Richtliniensperren {#policy-locks}

Wenn eine Richtlinie gesperrt ist, kann ihr Wert erst geändert werden, nachdem die Richtlinie entsperrt wurde. Die Global Admin Console speichert die [ausgewählte Organisation](https://helpx.adobe.com/de/enterprise/global-admin-console/overview.html) in der Organisationsauswahl als die Organisation, für die die Richtlinie gesperrt wurde. Jeder globale Administrator dieser ausgewählten Organisation oder einer Organisation weiter oben in der Struktur hat die Berechtigung, die Richtlinie zu entsperren. Globale Administratoren, deren Umfang kleiner ist als diese Organisation, haben nicht die Berechtigung, Richtlinienwerte zu entsperren und zu ändern.

Um eine gesperrte Umgebung zu erstellen, legen Sie die gewünschten Richtlinienwerte für Ihre untergeordneten Organisationen fest und sperren Sie sie dann. Globale Administratoren dieser untergeordneten Organisationen können die Richtlinienwerte nicht bearbeiten.

### Beispiel: Gesperrte Umgebung

Wenn Elissa, der globale Administrator von *Acme Division*, untergeordnete Organisationen *Marketing* und *Engineering* erstellt, fügt Robert dann als globalen Administrator von *Marketing* und Sarah als globalen Administrator von *Engineering* hinzu. Als Nächstes legt sie mehrere Richtlinien auf *Nicht erlaubt* und *Sperren* fest. Elissa kann später die Richtlinienwerte entsperren und ändern, wenn sie *Acme Division* als die ausgewählte Organisation auswählt, aber Robert und Sarah können die Richtlinien für die Organisationen, für die sie globale Administratoren sind, nicht entsperren, weil die Richtlinien von der Organisation gesperrt sind *Acme Division*.

## Details der Richtlinie

### Organisationsverwaltung

| Richtlinienname | Beschreibung |
| --- | --- |
| **Untergeordnete Organisationen erstellen** | Ermöglicht globalen Administratoren das Erstellen untergeordneter Organisationen. Wenn *Aus*, können keine untergeordneten Organisationen erstellt werden. |
| **Organisation umbenennen** | Wenn zulässig, kann ein globaler Administrator oder ein Systemadministrator die Organisation umbenennen. Es steuert auch das Ändern des Landes/der Region der Organisation. Der Pfadname einer Organisation kann auch unabhängig von dieser Richtlinieneinstellung geändert werden, wenn eine übergeordnete Organisation umbenannt wird oder die Organisation oder ein Vorgänger der Organisation übergeben wird. |
| **Organisationen löschen** | Ermöglicht globalen Administratoren das Löschen untergeordneter Organisationen. Dies wird wichtiger, wenn Organisationen mit Enterprise-Speicher aktiviert sind, da das Risiko besteht, dass Benutzer-Assets gelöscht werden. |

### Administratorverwaltung

| Richtlinienname | Beschreibung |
| --- | --- |
| **Hinzufügen oder Löschen von Administratoren** | Ermöglicht globalen Administratoren das Hinzufügen neuer Administratoren zu einer Organisation. Wenn *Aus*, können keine neuen Administratoren hinzugefügt werden. |
| **Erben Sie Systemadministratoren von der übergeordneten Instanz, wenn eine untergeordnete Organisation erstellt wird** | Wenn globale Administratoren neue untergeordnete Organisationen erstellen, werden Systemadministratoren der übergeordneten Organisation automatisch zu Systemadministratoren der neuen Organisation. Diese Richtlinie *standardmäßig*. |
| **Verwalten von Administratoren** | Ermöglicht globalen Administratoren das Ändern oder Entfernen/Bearbeiten von Administratorberechtigungen. |

### Benutzerverwaltung

| Richtlinienname | Beschreibung |
| --- | --- |
| **Benutzer aus Verzeichnissen übernehmen, die von der übergeordneten Organisation verwaltet werden** | Diese Richtlinie muss vor *Erstellung der neuen untergeordneten* aktiviert bzw. deaktiviert werden. Wenn eine untergeordnete Organisation erstellt wird, werden Benutzer in der übergeordneten Organisation als Benutzer in der untergeordneten Organisation verfügbar gemacht. Mit anderen Worten: Diese Richtlinie richtet automatisch eine Vertrauensbeziehung zwischen dem übergeordneten und dem untergeordneten Element ein, wenn das neue untergeordnete Element im GAC erstellt wird. Für bestehende Organisationen bleiben alle Vertrauensbeziehungen, die dem GAC vor hinzugefügt werden, erhalten, sobald sie in den GAC eingebracht werden. Wenn keine Vertrauensstellungen vorhanden waren, muss der übliche Prozess zur Anforderung von Vertrauensstellungen befolgt werden. Damit diese Richtlinie erfolgreich ist, muss der globale Administrator, der die neue Organisation erstellt, auch ein Systemadministrator der übergeordneten Organisation mit der beanspruchten Domain sein. Ist dies nicht der Fall, wird die Vertrauensbeziehung nicht auf die neu erstellte Organisation übertragen. |
| **Adobe ID-Benutzer hinzufügen** | Wenn dieser Wert festgelegt ist, kann das Unternehmen keine Benutzenden vom Typ Adobe ID über die Admin Console, User Management-API (UMAPI) oder den Synchronisierungsmechanismus hinzufügen. |
| **Benutzergruppen verwalten** | Wenn zulässig, können globale Administratoren sowie System- und Benutzergruppenadministratoren Benutzergruppen erstellen, bearbeiten und löschen. |

### Verzeichnis- und Domain-Durchsetzung

| Richtlinienname | Beschreibung |
| --- | --- |
| **Anforderungs-Domains** | Wenn festgelegt, können Systemadministratoren Domains auf der Admin Console beanspruchen. |
| **Ändern der Identitätskonfiguration** | Wenn dieser Wert festgelegt ist, können Systemadministratoren die Einrichtung der Benutzeridentitätskonfiguration auf der Admin Console ändern. |

### Produktzuordnung

| Richtlinienname | Beschreibung |
| --- | --- |
| **Produkte verwalten** | Ermöglicht es globalen Administratoren, Produkte hinzuzufügen oder zu entfernen und Produktressourcenzuweisungen zu ändern. |

### Asset-Freigabe

| Richtlinienname | Beschreibung |
| --- | --- |
| **System- oder Speicheradministrator kann Einstellungen für die Asset-Freigabe ändern** | Sofern zulässig, können Speicher- und Systemadministratoren die Einstellungen für die Asset-Freigabe ändern, einschließlich der Sicherheitskontakte, der Kennwortrichtlinie und der Speicherrichtlinie. |
| **Freigaberichtlinie von einem übergeordneten Element übernehmen, wenn eine Organisation erstellt wird** | Wenn zulässig, werden die Einstellungen für die Asset-Freigabe vom übergeordneten Element übernommen, wenn eine untergeordnete Organisation erstellt wird. Zu den Einstellungen für die Asset-Freigabe gehören Sicherheitskontakte, Kennwortrichtlinien und Speicherrichtlinien. Dies gilt nur für neu erstellte Organisationen zum Zeitpunkt der Erstellung. Sie wird auf ein übergeordnetes Element festgelegt und wirkt sich auf die Erstellung von untergeordneten Organisationen unter diesem übergeordneten Element aus. |
