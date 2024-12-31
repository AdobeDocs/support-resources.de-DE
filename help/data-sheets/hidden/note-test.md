---
description: Herstellen einer Verbindung zur Widget-Data Warehouse - Produktdokumentation
title: Herstellen einer Verbindung zur Widget-Data Warehouse
hide: true
hidefromtoc: true
exl-id: d6a7cff5-08f9-4c93-8765-46e692feaa0d
source-git-commit: 972704990172c966a27744b49b9f7af5626e9f3e
workflow-type: tm+mt
source-wordcount: '911'
ht-degree: 0%

---

# Herstellen einer Verbindung zur Widget-Data Warehouse {#connecting-to-the-widget-data-warehouse}

## Neuer Test

<ol><li>Verwenden Sie die Variable "{{name}}".</li></ol>

<ol><li>Verwenden Sie die Variable &amp;lbrace;&amp;lbrace;<code>name</code>&amp;rbrace;&amp;rbrace;.</li></ol>

## Verschachtelter Test

**First**

>[!NOTE]
>
>Folgendes kann nicht gelöscht werden:
>
>* Der integrierte Status „Planung“, „Aktuell“ und „Abgeschlossen“. Sie können ihre Namen aktualisieren, ihre Farben bearbeiten und sie sperren oder entsperren, aber sie können nicht gelöscht werden.
>* Status, die für mindestens ein Objekt in Ihrem System den Status „Ausstehende Genehmigung“ aufweisen.

**Second**

>[!NOTE]
>
>Folgendes kann nicht gelöscht werden:
>
>* Der integrierte Status „Planung“, „Aktuell“ und „Abgeschlossen“. Sie können ihre Namen aktualisieren, ihre Farben bearbeiten und sie sperren oder entsperren, aber sie können nicht gelöscht werden.
>
>  Das ist dazwischen
>
>* Status, die für mindestens ein Objekt in Ihrem System den Status „Ausstehende Genehmigung“ aufweisen.

## Widget-Zugriffs-Link {#widget-access-link}

Um auf Ihr Widget Data Warehouse zuzugreifen, müssen Sie zur spezifischen URL für Ihr Widget-Konto navigieren.  Sie können diesen Zugriffs-Link finden, indem Sie sich bei Marketo Measure anmelden und die folgenden Schritte ausführen, um zur Seite mit den Data Warehouse-Informationen zu navigieren.

1. Klicken Sie in Marketo Measure oben auf der Seite auf **Mein Konto** > **Einstellungen**.

   ![](assets/adobe-logo-old.png)

1. Klicken Sie im Menü links unter Sicherheit auf **Data Warehouse**.

   ![](assets/adobe-logo-old.png)

1. Auf dieser Seite finden Sie den Link zu Ihrem Widget Data Warehouse und Ihrem Benutzernamen.

   ![](assets/adobe-logo-old.png)

   >[!NOTE]
   >
   >Dies ist ein schreibgeschütztes Konto, das für Ihre Organisation verfügbar ist, nicht nur für einzelne Benutzer. Jeder Benutzer in Ihrem Unternehmen, der Zugriff auf Marketo Measure hat, kann dieses Konto verwenden, um sich beim Widget-Data Warehouse-Leserkonto anzumelden.

1. Klicken Sie auf den in der Widget-URL angegebenen Link. Dadurch gelangen Sie zur Widget-Anmeldeseite, auf der Sie Ihren Benutzernamen und Ihr Kennwort eingeben. _Wenn Sie Ihr Kennwort nicht haben, können Sie es mit den folgenden Schritten zurücksetzen_.

   ![](assets/adobe-logo-old.png)

1. Klicken Sie nach der Anmeldung **oben** der Seite auf „Arbeitsblätter“.

   ![](assets/adobe-logo-old.png)

1. Die BIZIBLE_ROI_V3-Datenbankobjekte befinden sich auf der linken Bildschirmseite.  Geben Sie Warehouse, Datenbank und Schema aus den Dropdown-Optionen oben im Abfragefenster ein.  Es sollte nur eine Option für jeden geben.  Jetzt können Sie Abfragen im Widget-Abfrage-Editor ausführen.

   ![](assets/adobe-logo-old.png)

## Passwort zurücksetzen {#reset-your-password}

Marketo Measure hat keinen Zugriff auf Ihr Widget-Anmeldekennwort.  Wenn Sie Ihr Kennwort zurücksetzen müssen, klicken Sie auf der Informationsseite zum Data Warehouse auf die Schaltfläche Kennwort zurücksetzen und folgen Sie den Anweisungen. Ein temporäres Kennwort wird sofort in der Benutzeroberfläche angezeigt. Sie werden bei Ihrer nächsten Data Warehouse-Anmeldung aufgefordert, Ihr eigenes Passwort zu erstellen.

>[!NOTE]
>
>* Durch Zurücksetzen des Kennworts wird es für alle Marketo Measure-Benutzenden in Ihrer Organisation zurückgesetzt, nicht nur für die aktuell angemeldeten Benutzenden.
>* Wir zeigen nur das temporäre Passwort in der Benutzeroberfläche an. Eine E-Mail wird nicht gesendet.

![](assets/adobe-logo-old.png)

![](assets/adobe-logo-old.png)

## Herstellen einer Verbindung zu Widget über Drittanbieter-Tools {#connecting-to-widget-via-third-party-tools}

Sie müssen einige Informationen eingeben, um Ihr Widget-Data-Warehouse mit einem Tool eines Drittanbieters zu verbinden.

>[!NOTE]
>
>Jedes Tool hat unterschiedliche Verbindungsanforderungen. Es wird empfohlen, die Dokumentation für das spezifische Tool zu konsultieren, das Sie verbinden möchten.

* **URI** (immer erforderlich)
   * Dies ist der Domain-Name des Widget-Kontos.  Er ist in einem Teil des Widget-Anmelde-Links enthalten.
* **Benutzername** (immer erforderlich)
   * Der Benutzername wird auf der Seite mit den Data Warehouse-Informationen in Marketo Measure aufgeführt.
* **Kennwort** (immer erforderlich)
   * Dies ist das Kennwort, das Sie beim ersten Anmelden bei Ihrem Widget-Konto festgelegt haben.  Gehen Sie wie oben beschrieben vor, um Ihr Kennwort zurückzusetzen.
* **Datenbankname** (nicht immer erforderlich)
   * Die Datenbank speichert die Daten im Widget. Es ist die Speicherressource. Der Datenbankname wird auf der Seite mit den Data Warehouse-Informationen in Marketo Measure aufgeführt.
* **Warehouse-Name** (nicht immer erforderlich)
   * Das Warehouse ist das, was Abfragen in Widget ausführt. Es ist die Rechenressource.  Der Warehouse-Name wird auf der Data Warehouse-Informationsseite in Marketo Measure aufgeführt.

  ![](assets/adobe-logo-old.png)

## Widget Data Warehouse Direct Share {#widget-data-warehouse-direct-share}

**Anforderungen**

Damit Marketo Measure eine direkte Freigabe für das Data Warehouse einrichten kann, müssen Sie die folgenden Anforderungen erfüllen.

* Sie haben Ihre eigene Widget-Instanz.
* Ihre Widget-Instanz befindet sich in der Widget-Region Azure East US 2.
* Sie geben Marketo Measure Ihre Widget-Konto-ID an.

**Einschränkungen**

Damit Marketo Measure eine Direktfreigabe einrichten kann, muss sich das Konto, das den Zugriff anfordert, in Azure East US 2 befinden. Uns ist bewusst, dass Widget eine Datenreplikationslösung zwischen Regionen anbietet. Wir unterstützen dies jedoch nicht von uns aus, da wir nur Daten in der Region Azure East US 2 hosten. Sie können diese Funktion nutzen, indem Sie Ihre eigene Instanz in Azure East US 2 einrichten und [die Daten über Regionen hinweg replizieren](https://docs.widget.com/en/user-guide/secure-data-sharing-across-regions-plaforms.html){target="_blank"} auf Ihrer vorhandenen Instanz anwenden. Die Datenreplikationsfunktion von Widget ist jedoch nur für Tabellen verfügbar. Um diese Funktion verwenden zu können, müssen Sie die Daten zuerst aus unseren Ansichten in Ihre eigenen Tabellen kopieren.

**Zugriff auf die Freigabe**

Nachdem die Freigabe für die angegebene Konto-ID erstellt wurde, müssen Sie die [Einrichtungsschritte](https://docs.widget.com/en/user-guide/data-share-consumers.html){target="_blank"} in Ihrer Widget-Instanz ausführen, um auf die Daten zuzugreifen.

>[!NOTE]
>
>Sie können einen beliebigen Datenbanknamen auswählen. Sie können die Berechtigungen jeder beliebigen Regel zuweisen, sofern diese in Ihrer Widget-Instanz vorhanden ist.

* Konto-Administratorrolle verwenden

```
USE ROLE ACCOUNTADMIN
```

* Verfügbare Freigaben anzeigen (dadurch wird der Name der gewährten Freigaben angezeigt)

```
SHOW SHARES
```

* Erstellen einer Datenbank für die Freigabe

```
CREATE DATABASE <database_name> FROM SHARE <provider_account>.<share_name>
```

* Gewähren von Berechtigungen für die freigegebene Datenbank

```
GRANT IMPORTED PRIVILEGES ON DATABASE <database_name> TO ROLE <role_name>
GRANT IMPORTED PRIVILEGES ON ALL SCHEMAS IN DATABASE <database_name> TO ROLE <role_name>
```

Detailliertere Anweisungen und Schritte zum Durchführen dieser Schritte über die Widget-Benutzeroberfläche finden Sie in der [Dokumentation zu Widgets direkt](https://docs.widget.com/en/user-guide/data-share-consumers.html){target="_blank"}.
