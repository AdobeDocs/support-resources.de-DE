---
title: Herunterladen von Auditprotokollen und Exportieren von Berichten
description: Erfahren Sie, wie globale Administratoren Audit-Protokolle und -Berichte in der Global Admin Console anzeigen, filtern und exportieren.
feature-set: Experience Cloud Services
solution: Admin Console
feature: Admin Console
exl-id: 4b562a4d-14e5-4687-a1ae-6a435f087627
source-git-commit: 8db982f6a642a288453086c23d20b44b14d55354
workflow-type: tm+mt
source-wordcount: '880'
ht-degree: 3%

---

# Herunterladen von Auditprotokollen und Exportieren von Berichten

Gilt für Unternehmen.

Erfahren Sie, wie globale Administratoren Audit-Protokolle und -Berichte mithilfe von Global Admin Console anzeigen, filtern und exportieren.

Melden Sie sich zunächst bei der [Global Admin Console](https://global-admin-console.adobe.com/) an. Gehen Sie dann zur Registerkarte **[!UICONTROL Insights]** und wählen Sie **[!UICONTROL Audit-Protokolle]** aus, um alle Änderungen in allen Organisationen zu verfolgen.

## Auditprotokolle anzeigen und herunterladen

Als globaler Administrator haben Sie uneingeschränkten Einblick in die Änderungen, die in Global Admin Console vorgenommen wurden. Sie können in allen Organisationen Auditprotokolle nach Aktionen durchsuchen, die in den letzten 90 Tagen durchgeführt wurden, einschließlich des Zeitpunkts und der Ausführung.
- Audit-Protokolle helfen, die Einhaltung von Vorschriften sicherzustellen, indem sie vor unangemessenem Systemzugriff schützen und verdächtiges Verhalten innerhalb Ihrer Organisation überprüfen.
- Die in der Global Admin Console verfügbaren Protokolle enthalten nur Ereignisse, auf die ein globaler Administrator Zugriff hat. Sie beinhalten keine Benutzerzuweisungen oder Benutzerereignisse. [Erfahren Sie mehr](https://helpx.adobe.com/de/enterprise/using/admin-console.html) über die verschiedenen Funktionen, die jede Konsole bietet.
- Die Protokolle decken Ereignisse für alle Organisationen in der Hierarchie ab, sodass Sie Audit-Protokolle gleichzeitig in allen Organisationen durchsuchen können.

>[!NOTE]
>
> Als Systemadministrator in einer [Adobe Admin Console](https://adminconsole.adobe.com)-Organisation können Sie das [Auditprotokoll](https://helpx.adobe.com/enterprise/using/audit-logs.html) verwenden, um Benutzerzuweisungen und Benutzerereignisse zu überprüfen. Von Systemadministratoren in untergeordneten Organisationen der ausgewählten Organisation durchgeführte Aktionen werden ebenfalls in die Auditprotokolle aufgenommen. Erfahren Sie mehr darüber, wie Systemadministratoren in [ Admin Console vorgenommene ](https://helpx.adobe.com/enterprise/using/audit-logs.html) verfolgen können.

So zeigen Sie Auditprotokolle für Ihr Unternehmen an oder laden diese herunter:

1. Melden Sie sich als globaler Administrator bei der [Global Admin Console](https://global-admin-console.adobe.com/insights) an.
1. Wählen **[!UICONTROL Insights]** > **[!UICONTROL Auditprotokolle]** aus.
Die Auditprotokolle zeigen die folgenden Informationen für gefilterte Ereignisse an:

   | Feld | Beschreibung |
   |------ |-------------|
   | Datum | Datum und Uhrzeit des Ereignisses, angezeigt in der lokalen Zeitzone. |
   | Ereignisname | Beschreibung der ausgeführten Aktion. |
   | Ereignisdetail | Zusätzliche Ereignisdetails, falls verfügbar. |
   | Objektname | Der Name des Produkts, Produktprofils oder der Benutzergruppe, das bzw. die am Ereignis beteiligt ist. |
   | Betroffener Benutzer | E-Mail-Adresse des betroffenen Benutzers, falls zutreffend. |
   | Admin | E-Mail-Adresse des Administrators, der die Aktion ausgeführt hat. *System* wird angezeigt, wenn die Aktion von einem Adobe-Backend-System ausgeführt wurde. |
   | IP-Adresse | IP-Adresse des Geräts, auf dem die Aktion ausgeführt wurde. spiegelt in der Regel den physischen Standort wider, kann aber ein Proxy-Server oder eine VPN-Adresse sein. |
   | Organisation | Name der vom Ereignis betroffenen Organisation. |


1. Auditprotokolle können mit den folgenden Optionen gefiltert werden:

   - Suche nach betroffenem Benutzer oder Administrator.
   - Wählen Sie eine oder mehrere Organisationen aus.
   - Definieren Sie einen Datumsbereich.
   - Nach Ereignisnamen filtern.
   - Sie können Filter kombinieren, um die Ergebnisse einzugrenzen, z. B. um Ereignisse der letzten sieben Tage für eine bestimmte Organisation anzuzeigen.

   ![audit-logs](assets/audit-logs.png)

   *Filtern Sie die Auditprotokolle nach dem Ereignisnamen, der betroffenen Organisation oder dem Datumsbereich.*

   ![select-organization](assets/select-organizations.png)

   *Wählen Sie Organisationen aus, um die Auditprotokolle zu filtern.*

1. Um Auditprotokolle zu exportieren, wählen Sie **[!UICONTROL CSV exportieren]** aus, um gefilterte Ergebnisse zu exportieren. Die Ergebnisse werden im CSV-Format heruntergeladen.

Einzelheiten zu den im Export enthaltenen Feldern finden Sie unter [Protokollschema](#log-schema).

>[!NOTE]
>
>Exportierte Auditprotokollberichte werden nach ihrer Erstellung 90 Tage lang aufbewahrt.


## Grundlegendes zum Auditprotokollbericht {#log-schema}

Der exportierte Auditprotokollbericht enthält für jede Organisation die folgenden Felder:

| Feld | Beschreibung |
|------|------------|
| id | Ereignis-ID |
| eventTime | Datum und Uhrzeit des Ereignisses (lokale Zeitzone) |
| eventType | Ereignisname |
| eventSubType | Zusätzliche Ereignisdetails, falls verfügbar |
| actorEmail | E-Mail-Adresse des Administrators, der das Ereignis durchgeführt hat *System* wird angezeigt, wenn das Ereignis von einem Adobe-Backend-System ausgeführt wurde. |
| targetUserEmail | E-Mail des betroffenen Benutzers, falls zutreffend |
| targetGroupName | Betroffene Benutzergruppe, falls zutreffend |
| targetProductName | Betroffenes Produkt, falls zutreffend |
| targetProfileName | Betroffenes Produktprofil, falls zutreffend |
| IP-Adresse | IP-Adresse des Geräts, auf dem die Aktion ausgeführt wurde. spiegelt in der Regel den physischen Standort wider, kann aber ein Proxy-Server oder eine VPN-Adresse sein. |
| OrganizationName | Name der betroffenen Organisation |

## Exportberichte herunterladen

Wenn ein globaler Administrator Organisationsdaten aus der [Global Admin Console](https://global-admin-console.adobe.com/insights) exportiert, wird der Bericht verarbeitet und auf der Registerkarte **[!UICONTROL Insights]** in **[!UICONTROL Export Reports]** verfügbar gemacht.

Alle von einem beliebigen globalen Administrator erstellten Berichte stehen an einem Ort zur Verfügung. Die Funktion Berichte exportieren ist in den folgenden Szenarien hilfreich:

- Wenn Sie eine große Hierarchie mit vielen Organisationen haben, müssen Sie nicht mehr auf die Verarbeitung der Exportdatei warten. Sie können die von Ihren Kollegen erstellten Berichte verwenden.
- Sie müssen diese Berichte nicht mehr aufbewahren oder speichern, um sie später zu vergleichen. Die Berichte werden 90 Tage lang aufbewahrt und können jederzeit heruntergeladen werden, um Berichte zu vergleichen.


Herunterladen eines Exportberichts:

1. Melden Sie sich bei der [Global Admin Console an ](https://global-admin-console.adobe.com/insights) navigieren Sie zu **[!UICONTROL Insights]** > **[!UICONTROL Berichte exportieren]**.

   Die in den letzten 90 Tagen generierten Berichte werden angezeigt. Sobald die 90 Tage abgeschlossen sind, können Sie den Bericht erneut generieren. Erfahren Sie, wie Sie Berichte für [Organisationsstruktur“ ](https://helpx.adobe.com/enterprise/global-admin-console/export-and-import-data.html#export-and-import-organization-structure) können.


   | Feld | Beschreibung |
   |------|------------|
   | Bericht | Datum und Uhrzeit der Berichterstellung (lokale Zeitzone) |
   | Format | Dateiformat (CSV, JSON, XLSX) |
   | Größe | Dateigröße |
   | Erstellt von | E-Mail-Adresse des Administrators, der den Bericht erstellt hat |
   | Aktion | Link zum Herunterladen des Berichts |

1. Um einen Bericht herunterzuladen, wählen Sie **[!UICONTROL Herunterladen]** aus.

   Wenn der soeben generierte Bericht nicht in der Liste angezeigt wird, wählen Sie **[!UICONTROL Aktualisieren]** aus.

   ![export-reports](assets/export-reports.png)

*Laden Sie alle Berichte herunter, die in den letzten 90 Tagen generiert wurden.*
