---
title: Administratorrollen
description: Mithilfe der Adobe Admin Console können Unternehmen eine flexible Verwaltungshierarchie definieren, die eine differenzierte Verwaltung des Zugriffs und der Verwendung von Adobe-Produkten ermöglicht.
exl-id: bfee66b5-d7bb-4ecb-8d22-efb68611ecc8
source-git-commit: 21f2b42e3131fe0339e5de15824f48166409c7c1
workflow-type: tm+mt
source-wordcount: '1639'
ht-degree: 1%

---

# Administratorrollen

Mithilfe der Adobe Admin Console können Unternehmen eine flexible Verwaltungshierarchie definieren, die eine differenzierte Verwaltung des Zugriffs und der Verwendung von Adobe-Produkten ermöglicht. Ein oder mehrere Systemadministratoren, die während des Onboarding-Prozesses für Unternehmen bereitgestellt werden, befinden sich an der Spitze der Hierarchie. Diese Systemadmins können Zuständigkeiten an andere Admins delegieren und gleichzeitig die Gesamtkontrolle behalten.

Administratorrollen bieten den Unternehmen folgende wichtige Vorteile:

* Kontrollierte Dezentralisierung der administrativen Zuständigkeiten
* Schnellansicht der Produktzuweisungen - nach Benutzer und Produkt
* Funktion zum Zuweisen von Kontingenten an Produktadministratoren

## Verwaltungshierarchie

Gilt für: Adobe Enterprise-Kunden.

Die Verwaltungshierarchie kann verwendet werden, um die individuellen Anforderungen Ihres Unternehmens zu erfüllen. Beispielsweise kann ein Unternehmen verschiedene Administratoren ernennen, um Berechtigungen für Adobe Creative Cloud- und Adobe Marketing Cloud-Angebote zu verwalten. Alternativ kann ein Unternehmen über verschiedene Administratoren verfügen, um Berechtigungen von Benutzern zu verwalten, die zu verschiedenen Geschäftseinheiten gehören.

>[!NOTE]
>
>Die Administrationshierarchie gilt nicht für Teams und Kunden. Team-Kunden haben nur eine **(**). Der Vertragseigentümer (_früher als **Primärer Administrator**&#x200B;_bezeichnet) ist der Systemadministrator mit Zugriff auf die Vertragsdetails und den Abrechnungsverlauf. Wenn Sie der aktuelle Vertragseigentümer sind, können Sie einen vorhandenen Systemadministrator (_ früher als &quot;**Administrator“ bezeichnet**&#x200B;_ als Vertragseigentümer benennen.

![Admin-Bild](assets/storage_admin.png)

_Administratorrollen-Hierarchie_

| Rolle | Beschreibung |
|--- |--- |
| **Systemadministrator** | Hauptbenutzer für das Unternehmen; darf alle Verwaltungsaufgaben in der Admin Console ausführen.<br>Außerdem hat die Berechtigung, die folgenden administrativen Funktionen an andere Benutzer zu delegieren: Produktadministrator, Produktprofiladministrator, Benutzergruppenadministrator, Bereitstellungs-Administrator und Support-Administrator. |
| **Produktadministrator** | Verwaltet die Produkte, die diesem Administrator zugewiesen sind, sowie alle zugehörigen Verwaltungsfunktionen, darunter:<ul><li>Produktprofile erstellen</li><li>Hinzufügen von Benutzern und Benutzergruppen zur Organisation, aber nicht Entfernen dieser Benutzer und Gruppen</li><li>Hinzufügen oder Entfernen von Benutzenden und Benutzergruppen aus Produktprofilen</li><li>Hinzufügen oder Entfernen von Produktprofil-Administrierenden aus Produktprofilen</li><li>Hinzufügen oder Entfernen anderer Produktadministratoren aus dem Produkt</li><li>Hinzufügen oder Entfernen von Gruppenadministratoren aus Gruppen</li></ul> |
| **Produktprofil-Admin** | Verwaltet die Produktprofilbeschreibungen, die diesem Administrator zugewiesen sind, sowie alle zugehörigen Verwaltungsfunktionen, einschließlich:<ul><li>Hinzufügen von Benutzern und Benutzergruppen zur Organisation, aber nicht Entfernen dieser Benutzer und Gruppen</li><li>Hinzufügen oder Entfernen von Benutzenden und Benutzergruppen aus Produktprofilen</li><li>Zuweisen oder Widerrufen von Produktberechtigungen zu Benutzern und Benutzergruppen aus Produktprofilen</li><li>Verwalten von Produktrollen von Benutzern und Benutzergruppen für Produktprofile |
| **Benutzergruppen-Administrator** | Verwaltet die Benutzergruppenbeschreibungen, die diesem Administrator zugewiesen sind, sowie alle zugehörigen Verwaltungsfunktionen, darunter:<ul><li>Benutzer zu Gruppen hinzufügen oder daraus entfernen</li><li>Hinzufügen oder Entfernen von Benutzergruppen-Administrierenden aus Gruppen |
| **Bereitstellungs-Admin** | Erstellt, verwaltet und stellt Softwarepakete und Aktualisierungen für Endbenutzer bereit. |
| **Support-Admin** | Nicht-administrative Rolle, die Zugriff auf Support-bezogene Informationen hat, z. B. vom Kunden gemeldete Problemberichte. |
| **Speicheradministrator** | Verwaltet die Speicherverwaltung der Organisation. Der Administrator kann den Speicherverbrauch von aktiven und inaktiven Benutzern anzeigen und Inhalte an andere Empfänger übertragen. |

Eine detaillierte Liste der Berechtigungen für jede Administratorrolle finden Sie unter [Berechtigungen](#enterprise-admins-permissions-matrix).

## Enterprise-Administratorrolle hinzufügen {#add-enterprise-role}

Gilt für: Adobe Enterprise-Kunden.

Als Administrator können Sie anderen Benutzern eine Administratorrolle zuweisen und ihnen dieselben Berechtigungen wie Ihnen zuweisen. Ebenso können Sie Berechtigungen für eine Rolle unter Ihrer Administratorrolle in der Hierarchie gewähren, wie [&#x200B; oben beschrieben](#administrative-hierarchy). Beispielsweise können Sie als Produktadministrator einem Benutzer Produktadministratorberechtigungen oder Produktprofil-Administratorberechtigungen erteilen, jedoch keine Bereitstellungs-Administratorberechtigungen. Die Berechtigungen für die Admin Console finden Sie in der [Berechtigungsmatrix](#enterprise-admins-permissions-matrix).

So fügen Sie einen Administrator hinzu oder laden ihn ein:

1. Admin Console Wählen Sie in der [&#x200B; &#x200B;](https://adminconsole.adobe.com/)die Option **Benutzer** > **Administratoren**.

   Alternativ können Sie zum entsprechenden Produkt, Produktprofil oder zur entsprechenden Benutzergruppe gehen und zur Registerkarte **Administratoren** navigieren.

1. Klicken Sie **Admin hinzufügen**.
1. Geben Sie einen Namen oder eine E-Mail-Adresse ein. Sie können nach vorhandenen Benutzern suchen oder einen neuen Benutzer hinzufügen, indem Sie eine gültige E-Mail-Adresse angeben und die Informationen auf dem Bildschirm ausfüllen.
1. Klicken Sie **Weiter**. Eine Liste mit Administratorrollen wird angezeigt.

>[!NOTE]
>
>* Die Optionen auf diesem Bildschirm hängen von Ihrem Konto und Ihrer Administratorrolle ab. Sie können entweder dieselben Berechtigungen wie Sie selbst gewähren oder Berechtigungen für eine Rolle in der Hierarchie gewähren, die Ihnen untergeordnet ist.
>* Als System-Admin eines Teams können Sie nur eine einzige Admin-Rolle zuweisen: Systemadmin.

1. Eine oder mehrere Administratorrollen auswählen.
1. Wählen Sie für Administratortypen wie „Produktadministrator“, „Produktprofiladministrator“ und „Benutzergruppenadministrator“ die jeweiligen Produkte, Profile und Gruppen aus.

>[!NOTE]
>
>Für einen Produktprofil-Administrator können Sie Profile für mehr als ein Produkt einbeziehen.

![Administrator hinzufügen](assets/add-admin.png)

1. Überprüfen Sie die dem Benutzer zugewiesenen Administratorrollen und klicken Sie auf **Speichern**.

Der Benutzer erhält eine E-Mail-Einladung zu den neuen Administratorrechten von `message@adobe.com`.

Benutzer müssen in der E **Mail auf** Erste Schritte“ klicken, um der Organisation beizutreten. Wenn neue Admins den Link **Erste Schritte** in der E-Mail-Einladung nicht verwenden, können sie sich nicht bei Admin Console anmelden.

Im Rahmen des Anmeldevorgangs werden Benutzende möglicherweise aufgefordert, ein Adobe-Profil einzurichten, wenn sie noch keines haben. Wenn Benutzende mehrere Profile mit ihrer E-Mail-Adresse verknüpft haben, müssen sie „Team beitreten“ auswählen (wenn dazu aufgefordert) und dann das mit der neuen Organisation verknüpfte Profil auswählen.

![Bild mit Administratorrechten](assets/admin-get-started-email.png)

## Team-Administrator hinzufügen {#add-admin-teams}

Gilt für: Adobe Teams-Kunden.

Als Administrator können Sie die Systemadministratorrolle anderen Benutzern zuweisen, sodass diese dieselben Berechtigungen erhalten wie Sie.

So fügen Sie einen Systemadministrator hinzu oder laden ihn ein:

1. Wählen Sie in der Admin Console **Benutzer** > **Administratoren** aus.

   Eine Liste der vorhandenen Administratoren wird angezeigt.

1. Klicken Sie **Admin hinzufügen**.

   Der **„Administrator hinzufügen** wird angezeigt.

1. Geben Sie einen Namen oder eine E-Mail-Adresse ein. Sie können nach vorhandenen Benutzern suchen oder einen neuen Benutzer hinzufügen, indem Sie eine gültige E-Mail-Adresse angeben und die Informationen auf dem Bildschirm ausfüllen.

   Standardmäßig ist „Systemadministrator“ ausgewählt.

1. Klicken Sie auf **Speichern**.

![Team-Admin-Bild](assets/teams-admin.png)

Da alle Benutzenden in einer Team-Organisation Business-ID-Benutzende sind, erhalten sie eine E-Mail-Einladung zu den neuen Administratorrechten von `message@adobe.com`.
Benutzer müssen in der E-Mail auf Erste Schritte klicken, um der Organisation beizutreten.

Im Rahmen des Anmeldevorgangs werden Benutzende möglicherweise aufgefordert, ein Adobe-Profil einzurichten, wenn sie noch keines haben. Wenn Benutzende mehrere Profile mit ihrer E-Mail-Adresse verknüpft haben, müssen sie „Team beitreten“ auswählen (wenn dazu aufgefordert) und dann das mit der neuen Organisation verknüpfte Profil auswählen.

![Bild mit Administratorrechten](assets/admin-get-started-email.png)

## Administratorrolle des Unternehmens bearbeiten

Gilt für: Adobe Enterprise-Kunden.

Als Administrator können Sie die Administratorrolle für andere Administratoren bearbeiten, die sich in der Administrationshierarchie unter Ihnen befinden. Sie können beispielsweise Adminrechte anderer Admins entfernen.

So bearbeiten Sie Administratorrollen:

1. Wählen Sie in der Admin Console **Benutzer** > **Administratoren** aus. Die Liste der vorhandenen Administratoren wird angezeigt.

   Alternativ können Sie zum entsprechenden Produkt, Produktprofil oder zur entsprechenden Benutzergruppe gehen und zur Registerkarte **Administratoren** navigieren.

1. Klicken Sie auf den Namen des Admins, der bearbeitet werden soll.
1. Klicken Sie **Abschnitt Benutzerdetails** auf ![Symbol](assets/one-console-ellipses.png) und wählen Sie **Administratorrechte** und **Administratorrechte bearbeiten**.

   ![Administratorrechte bearbeiten](assets/admin-rights-section.png)

1. Bearbeiten Sie die Administratorrechte und speichern Sie die Änderungen.

## Administratorrolle der Teams bearbeiten

Gilt für: Adobe Teams-Kunden.

Als Team-Systemadministrator können Sie die Systemadministratorprivilegien anderer Administratoren entfernen.

So widerrufen Sie Systemadministratorberechtigungen:

1. Wählen Sie in der Admin Console **Benutzer** > **Administratoren** aus.

   Die Liste der vorhandenen Administratoren wird angezeigt.

1. Klicken Sie in den Benutzerdetails ![Symbol](assets/one-console-ellipses.png) rechts neben dem Abschnitt **Administratorrechte** und wählen Sie **Administratorrechte bearbeiten**.

   ![Administratorrechte bearbeiten](assets/admin-rights-section.png)

1. Bearbeiten Sie die Administratorrechte und speichern Sie die Änderungen.

## Entfernen eines Administrators

Gilt für: Adobe Teams Enterprise-Kunden.

1. Um Admin-Berechtigungen zu entziehen, wählen Sie einen Benutzer aus und klicken Sie dann auf **Admin entfernen**.

![Administratorbild entfernen](assets/remove-admin.png)

>[!NOTE]
>
>Wenn Sie einen Administrator bzw. eine Administratorin entfernen, wird der/die Benutzende nicht aus der Admin Console gelöscht, sondern nur die mit der Administratorrolle verbundenen Berechtigungen.

## Matrix mit Enterprise-Administratorberechtigungen

Gilt für: Adobe Enterprise-Kunden.

In der folgenden Tabelle sind alle Berechtigungen für die verschiedenen Arten von Administratoren aufgeführt, die nach den folgenden Funktionsbereichen kategorisiert sind:

### Identitätsverwaltung

| Berechtigung | Systemadministrator | Support-Admin |
|--- |--- |--- |
| Domain hinzufügen (Domain anfordern/beanspruchen) | ✔ | |
| Anzeigen von Domain- und Domain-Listen | ✔ | |
| Verwalten von Domain-Verschlüsselungsschlüsseln | ✔ | |
| Standardkennwortrichtlinie für Organisationen verwalten | ✔ | |
| Standardkennwortrichtlinie für Organisationen anzeigen | ✔ | |

### Benutzerverwaltung

| Berechtigung | Systemadministrator | Support-Admin |
|--- |--- |--- |
| Benutzer zu Organisation hinzufügen | ✔ | |
| Benutzer aus Organisation entfernen | ✔ | |
| Anzeigen von Benutzerdetails und Auflistung | ✔ | |
| Benutzerprofil bearbeiten | ✔ | |
| Produktprofil zu Benutzer oder Gruppe hinzufügen | ✔ | |
| Produktprofil zu Benutzer oder Gruppe entfernen | ✔ | |
| Hinzufügen eines Produktprofils zu mehreren Benutzern | ✔ | |
| Anzeigen von Produktprofilen für einen Benutzer | ✔ | |
| Anzeigen der Produktbenutzerliste | ✔ | |
| Massen-Hinzufügen von Benutzern zur Organisation | ✔ | |

### Administratorverwaltung

| Berechtigung | Systemadministrator | Support-Admin |
|--- |--- |--- |
| Organisations-Admin einem Benutzer erteilen | ✔ | |
| Org-Admin einem Benutzer entziehen | ✔ | |
| Gewähren des Produktlizenz-Admins für einen Benutzer | ✔ | |
| Produktlizenzadministrator eines Benutzers widerrufen | ✔ | |
| Bereitstellungs-Admin einem Benutzer gewähren | ✔ | |
| Bereitstellungs-Admin von einem Benutzer widerrufen | ✔ | |
| Gewähren des Benutzergruppenadministrators für einen Benutzer | ✔ | |
| Widerrufen der Benutzergruppenverwaltung für einen Benutzer | ✔ | |
| Gewähren des Produktbesitzer-Admins für einen Benutzer | ✔ | |
| Widerrufen der Admin für Produkteigentümer von einem Benutzer | ✔ | |

### Verwaltung der Produktlizenzkonfiguration

| Berechtigung | Systemadministrator | Support-Admin |
|--- |--- |--- |
| Gewähren von Produktberechtigungen für die Organisation | | |
| Entfernen der Produktberechtigung aus der Organisation | | |
| Gesamtzahl der Lizenzen anzeigen, die der Organisation gehören | ✔ | |
| Verfügbare Produkte und Produktfamilien anzeigen | ✔ | |
| Produktlizenzbeschreibungen/-daten bearbeiten | ✔ | |
| Bereitstellen der Produktlizenz für einen Benutzer | ✔ | |
| Bereitstellung der Produktlizenz für einen Benutzer aufheben | ✔ | |
| Neue Produktlizenzkonfiguration hinzufügen | ✔ | |
| Konfiguration des Produktlizenzdienstes bearbeiten | ✔ | |
| Konfiguration des Produktlizenzdienstes löschen | ✔ | |
| Produktzugriff von einem Benutzer entfernen (aus allen Konfigurationen entfernen) | ✔ | |

### Speicherverwaltung

| Berechtigung | Systemadministrator | Support-Admin |
|--- |--- |--- |
| Anzeigen aktiver und inaktiver Benutzerordner | ✔ | |
| Löschen inaktiver Benutzerordner und Übertragen von Inhalten | ✔ | |

### Bereitstellung

| Berechtigung | Systemadministrator | Support-Admin |
|--- |--- |--- |
| Registerkarte Pakete anzeigen/verwenden | ✔ | |

### Support

| Berechtigung | Systemadministrator | Support-Admin |
|--- |--- |--- |
| Registerkarte „Support anzeigen“ | ✔ | |
| Support-Fälle verwalten | ✔ | ✔ |

### Benutzergruppenverwaltung

| Berechtigung | Systemadministrator | Support-Admin |
|--- |--- |--- |
| Benutzergruppe erstellen | ✔ | |
| Benutzergruppe entfernen | ✔ | |
| Benutzer zu Benutzergruppe hinzufügen | ✔ | |
| Benutzer aus Benutzergruppe entfernen | ✔ | |
| Benutzergruppe zur Produktlizenz zuweisen | ✔ | |
| Benutzergruppe aus Produktlizenz entfernen | ✔ | |
| Mitglied der Benutzergruppe anzeigen | ✔ | ✔ |
| Liste der Benutzergruppen anzeigen | ✔ | ✔ |