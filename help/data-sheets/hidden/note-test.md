---
description: Herstellen einer Verbindung zur Widget-Data Warehouse - Produktdokumentation
title: Herstellen einer Verbindung zum Widget-Data Warehouse
hide: true
hidefromtoc: true
source-git-commit: fcf5fb8f9728dd27a81de21241a71ce49dd015f8
workflow-type: tm+mt
source-wordcount: '911'
ht-degree: 0%

---

# Herstellen einer Verbindung zum Widget-Data Warehouse {#connecting-to-the-widget-data-warehouse}

## Neuer Test

<ol><li>Verwenden Sie den "{{name}}".</li></ol>

<ol><li>Verwenden Sie &amp;lbrace;&amp;lbrace;<code>name</code>&amp;rbrace;&amp;rbrace; Variable.</li></ol>

## Verschachtelter Test

**Erste**

>[!NOTE]
>
>Folgendes kann nicht gelöscht werden:
>
>* Die integrierte Statusplanung, &quot;Aktuell&quot;und &quot;Abgeschlossen&quot;. Sie können ihre Namen aktualisieren, ihre Farben bearbeiten und sperren oder entsperren, sie können jedoch nicht gelöscht werden.
>* Status, bei denen die Genehmigung für mindestens ein Objekt in Ihrem System ausstehend ist.

**Second**

>[!NOTE]
>
>Folgendes kann nicht gelöscht werden:
>
>* Die integrierte Statusplanung, &quot;Aktuell&quot;und &quot;Abgeschlossen&quot;. Sie können ihre Namen aktualisieren, ihre Farben bearbeiten und sperren oder entsperren, sie können jedoch nicht gelöscht werden.
>
>  Dies liegt zwischen
>
>* Status, bei denen die Genehmigung für mindestens ein Objekt in Ihrem System ausstehend ist.

## Link zum Widget-Zugriff {#widget-access-link}

Um auf Ihr Widget-Data Warehouse zuzugreifen, müssen Sie zur spezifischen URL für Ihr Widget-Konto navigieren.  Sie finden diesen Zugriffs-Link, indem Sie sich bei Marketo Measure anmelden und die folgenden Schritte ausführen, um zur Data Warehouse-Informationsseite zu navigieren.

1. Klicken Sie in Marketo Measure oben auf der Seite auf **Mein Konto** > **Einstellungen**.

   ![](assets/adobe-logo-old.png)

1. Klicken Sie im Menü auf der linken Seite unter &quot;Sicherheit&quot;auf **Data Warehouse**.

   ![](assets/adobe-logo-old.png)

1. Auf dieser Seite finden Sie den Link zu Ihrem Widget Data Warehouse und Ihrem Benutzernamen.

   ![](assets/adobe-logo-old.png)

   >[!NOTE]
   >
   >Dies ist ein schreibgeschütztes Konto, das für Ihr Unternehmen und nicht nur für einzelne Benutzer verfügbar ist. Jeder Benutzer in Ihrem Unternehmen, der Zugriff auf Marketo Measure hat, kann sich mit diesem Konto beim Widget Data Warehouse Reader-Konto anmelden.

1. Klicken Sie auf den in der Widget-URL angegebenen Link. Dadurch gelangen Sie zur Widget-Anmeldeseite, auf der Sie Ihren Benutzernamen und Ihr Passwort eingeben. _Wenn Sie Ihr Kennwort nicht haben, lesen Sie die folgenden Schritte, um es zurückzusetzen._.

   ![](assets/adobe-logo-old.png)

1. Klicken Sie nach der Anmeldung auf **Arbeitsblätter** oben auf der Seite.

   ![](assets/adobe-logo-old.png)

1. Die Datenbankobjekte BIZIBLE_ROI_V3 befinden sich auf der linken Bildschirmseite.  Geben Sie in den Dropdown-Optionen oben im Abfragefenster die Optionen Warehouse, Datenbank und Schema ein.  Es sollte nur eine Option für jede geben.  Jetzt können Sie Abfragen im Widget-Abfrageeditor ausführen.

   ![](assets/adobe-logo-old.png)

## Passwort zurücksetzen {#reset-your-password}

Marketo Measure hat keinen Zugriff auf Ihr Widget-Anmeldekennwort.  Wenn Sie Ihr Kennwort zurücksetzen müssen, klicken Sie auf der Data Warehouse-Informationsseite auf die Schaltfläche Kennwort zurücksetzen und befolgen Sie die Anweisungen. In der Benutzeroberfläche wird sofort ein temporäres Kennwort angezeigt. Sie werden aufgefordert, Ihr eigenes Kennwort für die nächste Data Warehouse-Anmeldung zu erstellen.

>[!NOTE]
>
>* Durch das Zurücksetzen des Kennworts wird es für alle Marketo Measure-Benutzer in Ihrer Organisation zurückgesetzt, nicht nur für den aktuell angemeldeten Benutzer.
>* Das temporäre Kennwort wird nur in der Benutzeroberfläche angezeigt. Eine E-Mail wird nicht gesendet.

![](assets/adobe-logo-old.png)

![](assets/adobe-logo-old.png)

## Herstellen einer Verbindung zu Widget über Drittanbieter-Tools {#connecting-to-widget-via-third-party-tools}

Sie müssen einige Informationen eingeben, um Ihr Widget Data Warehouse mit einem Tool eines Drittanbieters zu verbinden.

>[!NOTE]
>
>Jedes Tool hat unterschiedliche Verbindungsanforderungen. Wir empfehlen, sich die Dokumentation für das spezifische Tool anzuschauen, das Sie verbinden möchten.

* **URI** (immer erforderlich)
   * Dies ist der Domänenname des Widget-Kontos.  Sie ist in einem Teil des Widget-Anmelde-Links enthalten.
* **Benutzername** (immer erforderlich)
   * Der Benutzername wird auf der Data Warehouse-Informationsseite in Marketo Measure aufgeführt.
* **Passwort** (immer erforderlich)
   * Dies ist das Kennwort, das Sie beim ersten Anmelden in Ihrem Widget-Konto festgelegt haben.  Informationen zum Zurücksetzen Ihres Kennworts finden Sie in den oben beschriebenen Schritten.
* **Datenbankname** (nicht immer erforderlich)
   * Die Datenbank speichert die Daten in Widget. Dies ist die Speicherressource. Der Datenbankname wird auf der Data Warehouse-Informationsseite in Marketo Measure aufgeführt.
* **Warehouse Name** (nicht immer erforderlich)
   * Das Warehouse führt Abfragen in Widget aus. Dies ist die Rechenressource.  Der Warehouse-Name wird auf der Data Warehouse-Informationsseite in Marketo Measure aufgeführt.

  ![](assets/adobe-logo-old.png)

## Widget Data Warehouse Direct Share {#widget-data-warehouse-direct-share}

**Anforderungen**

Damit Marketo Measure eine direkte Freigabe für Data Warehouse einrichten kann, müssen Sie die folgenden Voraussetzungen erfüllen.

* Sie verfügen über eine eigene Widget-Instanz.
* Ihre Widget-Instanz befindet sich in der Azure East US 2 Widget-Region.
* Sie stellen Marketo Measure Ihre Widget-Konto-ID zur Verfügung.

**Einschränkungen**

Damit Marketo Measure eine direkte Freigabe einrichten kann, muss sich das Konto, das Zugriff anfordert, in Azure East US 2 befinden. Wir wissen, dass Widget eine Datenreplikationslösung zwischen Regionen anbietet, aber wir unterstützen diese nicht von unserem Ende aus, da wir nur Daten in der Azure East US 2-Region hosten. Sie können diese Funktion nutzen, indem Sie Ihre eigene Instanz in Azure East US 2 einrichten und [regionsübergreifendes Replizieren der Daten](https://docs.widget.com/en/user-guide/secure-data-sharing-across-regions-plaforms.html){target="_blank"} zu Ihrer vorhandenen Instanz hinzufügen. Die Datenreplikationsfunktion von Widget ist jedoch nur für Tabellen verfügbar. Um diese Funktion verwenden zu können, müssen Sie die Daten zunächst aus unseren Ansichten in Ihre eigenen Tabellen kopieren.

**Zugriff auf die Freigabe**

Nachdem die Freigabe für die angegebene Konto-ID erstellt wurde, müssen Sie die [Einrichtungsschritte](https://docs.widget.com/en/user-guide/data-share-consumers.html){target="_blank"} in Ihrer Widget-Instanz, um auf die Daten zuzugreifen.

>[!NOTE]
>
>Sie können einen beliebigen Datenbanknamen wählen. Sie können die Berechtigungen jeder von Ihnen gewählten Regel zuweisen, sofern sie in Ihrer Widget-Instanz vorhanden ist.

* Verwenden der Rolle &quot;Kontoadministrator&quot;

```
USE ROLE ACCOUNTADMIN
```

* Verfügbare Aktien anzeigen (dabei wird der Name der gewährten Aktie angezeigt)

```
SHOW SHARES
```

* Erstellen einer Datenbank für die Freigabe

```
CREATE DATABASE <database_name> FROM SHARE <provider_account>.<share_name>
```

* Berechtigungen für die freigegebene Datenbank gewähren

```
GRANT IMPORTED PRIVILEGES ON DATABASE <database_name> TO ROLE <role_name>
GRANT IMPORTED PRIVILEGES ON ALL SCHEMAS IN DATABASE <database_name> TO ROLE <role_name>
```

Ausführlichere Anweisungen und Schritte zum Ausführen dieser Schritte über die Widget-Benutzeroberfläche finden Sie unter [Direkte Dokumentation zum Widget](https://docs.widget.com/en/user-guide/data-share-consumers.html){target="_blank"}.
