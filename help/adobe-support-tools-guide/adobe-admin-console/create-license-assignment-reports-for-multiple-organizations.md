---
title: Erstellen von Lizenzzuweisungsberichten für mehrere Organisationen und Produkte
description: Generieren, Anzeigen und Herunterladen von Lizenzzuweisungsberichten für mehrere Unternehmen und Produkte aus der Global Admin Console.
Feature-set: Experience Cloud Services
Solution: Admin Console
Feature: Admin Console
exl-id: e3380a89-8529-473f-bd17-efb05466eab9
source-git-commit: 74d2dd4eb999f91172eec4c3b5690e1e8b8bd293
workflow-type: tm+mt
source-wordcount: '711'
ht-degree: 1%

---

# Erstellen von Lizenzzuweisungsberichten für mehrere Organisationen und Produkte

Erfahren Sie, wie globale Administratoren detaillierte Lizenzberichte für mehrere Organisationen und Produkte für bestimmte Datumsbereiche generieren und herunterladen können, um die präzise Verfolgung der Lizenzbereitstellung zu erleichtern.

>[!NOTE]
>
>Um einen Lizenzzuweisungsbericht zu erstellen, anzuzeigen und zu exportieren, melden Sie sich bei der [Global Admin Console](https://global-admin-console.adobe.com/) an und gehen Sie zu **[!UICONTROL Insights]** > **[!UICONTROL Berichte]** > **[!UICONTROL Lizenzzuweisung]**.

## Erstellen eines Berichts

Berichte zur Lizenzzuweisung helfen Ihnen, die Lizenzbereitstellung proaktiv zu überwachen und das manuelle Tracking zu reduzieren. Globale Administratoren können einen Bericht zur Lizenzzuweisung für ausgewählte Produkte für eine beliebige Anzahl untergeordneter Organisationen erstellen, um die Daten zur Softwarelizenzbereitstellung über alle Abteilungen hinweg zu überwachen.

1. Navigieren Sie zur **[[!UICONTROL Insights]](https://global-admin-console.adobe.com/insights)** in der Global Admin Console.
1. Wählen Sie auf **[!UICONTROL Seite &quot;]**&quot; die Option **[!UICONTROL Bericht erstellen]** aus.
1. Wählen Sie die Organisationen aus und klicken Sie auf **[!UICONTROL Weiter]**. Sie können jede Organisation einzeln auswählen oder alle untergeordneten Organisationen innerhalb eines übergeordneten Elements mithilfe der Schaltfläche **[!UICONTROL Alle auswählen]** auswählen.

   >[!NOTE]
   >
   >**Wissen, warum Sie bestimmte Organisationen nicht auswählen können**:
   >Wenn eine untergeordnete Organisation keinen Vertrag oder einen separaten Unternehmensvertrag mit demselben Produkt wie die übergeordnete Organisation hat, kann sie keinen Lizenzzuweisungsbericht erstellen. Wenn beispielsweise der Vertrag der übergeordneten Organisation über Adobe Acrobat verfügt und die untergeordnete Organisation denselben Vertrag als Teil eines anderen Vertrags hat, ist das Produkt für die Zuordnung beschränkt. Infolgedessen ist er auch auf die Berichterstellung in der Global Admin Console beschränkt. [Erfahren Sie, wie Sie die Bereitstellung für solche Organisationen mithilfe ihrer jeweiligen Admin Console verfolgen](https://helpx.adobe.com/de/enterprise/using/assignment-reports.html).

   >[!NOTE]
   >
   >Zuweisungsberichte können nur für Organisationen mit einem aktiven Vertrag erstellt werden.

1. Wählen Sie die Produkte aus, die in den Bericht aufgenommen werden sollen, und wählen Sie **[!UICONTROL Weiter]**.

   >[!NOTE]
   >
   >**Wissen, warum Sie bestimmte Produkte nicht auswählen können**:
   >Produkte, die in der Global Admin Console nicht zugeordnet werden können, sind nicht in die Berichterstellung eingeschlossen. Dazu gehören derzeit einige Produkte für digitale Erlebnisse wie [!DNL Workfront], [!DNL Adobe Experience Manager] und [!DNL Adobe Experience Platform] sowie Produkte wie [!DNL Adobe Firefly Services], [!DNL Acrobat Sign] und [!DNL Adobe Stock]. [Mit der Adobe Admin Console finden Sie die Lizenzbereitstellungsdaten für diese Produkte](https://helpx.adobe.com/de/enterprise/using/assignment-reports.html).

1. Wählen Sie aus, ob der Bericht nach Monat oder Jahr aggregiert werden soll.
1. Wählen Sie einen benutzerdefinierten Datumsbereich aus oder wählen Sie aus den Voreinstellungsoptionen. Sie können ein beliebiges Startdatum vom 18. Juni 2020 bis zum vorherigen Tag auswählen, sofern es nicht vor dem Startdatum Ihres Vertrags liegt.
1. Wählen Sie **[!UICONTROL Herunterladen]** aus, um den Bericht als CSV-Datei zu exportieren.

Der Bericht wird verarbeitet und auf der Seite **[!UICONTROL Lizenzzuweisung]** mit Details wie Name, Ersteller, Erstellungszeit, Datumsbereich und Status angezeigt. Sobald er bereit ist, erhalten Sie eine E-Mail-Benachrichtigung und der Bericht wird automatisch heruntergeladen.

Globale Administratoren können den Bericht jederzeit herunterladen, sobald er fertig ist, indem sie das Symbol **[!UICONTROL Herunterladen]** neben dem Berichtsnamen verwenden.

>[!NOTE]
>
>- Um sicherzustellen, dass die neuesten Daten widergespiegelt werden, generieren Sie Berichte 48 Stunden nach der Zuordnung.
>- Berichte werden nach ihrer Erstellung 90 Tage lang aufbewahrt.

## Anzeigen und Herunterladen zuvor generierter Berichte

Globale Administratoren bzw. Administratorinnen können die Lizenzzuweisungsberichte, die von anderen globalen Administratoren bzw. Administratorinnen in Ihrer Organisation generiert wurden, anzeigen und herunterladen. Globale Betrachter können jedoch nur die Liste der Lizenzzuweisungsberichte anzeigen.

1. Navigieren Sie zur **[[!UICONTROL Insights]](https://global-admin-console.adobe.com/insights)** in der Global Admin Console.
1. Auf der Seite **[!UICONTROL Lizenzzuweisung]** werden alle Berichte mit den folgenden Details aufgelistet:

   | Feld | Beschreibung |
   | ------------- | ------------------------------------------------------------------------------------------------- |
   | Name | Automatisch generiert und kann nicht bearbeitet werden. |
   | Ersteller | Der globale Administrator, der den Bericht generiert hat. |
   | Erstellungszeit | Die Systemzeit, zu der der Bericht erstellt wurde. |
   | Datumsbereich | Der ausgewählte Datumsbereich für den Bericht. |
   | Status | **Erfolg** wenn der Bericht zum Herunterladen bereit ist, oder **Verarbeitung** wenn er noch generiert wird. |

1. Um den Bericht als CSV-Datei zu exportieren, klicken Sie auf **[!UICONTROL Herunterladen]**-Symbol neben dem Bericht.

## Kennenlernen des Lizenzzuweisungsberichts

Der Bericht, den Sie herunterladen, enthält für jedes Ereignis die folgenden Informationen:

| Feld | Beschreibung |
| -------------------------------- | -------------------------------------------------------- |
| Organisations-ID | Eindeutige ID, die mit der übergeordneten Organisation verknüpft ist |
| Organisationsname | Name der übergeordneten Organisation |
| ID der untergeordneten Organisation | Eindeutige Kennung der ausgewählten untergeordneten Organisation |
| Name der untergeordneten Organisation | Name der untergeordneten Organisation |
| Lizenzkennung | Eindeutige ID für die Produktlizenz |
| Produktname | Name des ausgewählten Produkts |
| Datum | Datumsauswahl |
| Lizenzmenge insgesamt | Gesamtzahl der Lizenzen auf der Ebene der übergeordneten Organisation |
| Untergeordnete Lizenzen | Lizenzanzahl, die der untergeordneten Organisation zugewiesen ist |
| Monatliche/jährliche zugewiesene Spitzenmenge | Aggregierter Wert der Lizenzbereitstellung (monatlich/jährlich) |
