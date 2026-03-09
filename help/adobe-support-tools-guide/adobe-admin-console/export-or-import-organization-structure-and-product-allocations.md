---
title: Organisationsstruktur und Produktzuordnungen exportieren oder importieren
description: Erfahren Sie, wie globale Admins Organisationshierarchie- und Produktzuordnungsdaten in Global Admin Console mithilfe von JSON, CSV oder XLSX exportieren und importieren. Gilt für Unternehmen.
feature-set: Experience Cloud Services
solution: Admin Console
feature: Admin Console
source-git-commit: fe5b03e5886a43b55929a2bdba45da3c08ad0ab9
workflow-type: tm+mt
source-wordcount: '4423'
ht-degree: 3%

---


# Organisationsstruktur und Produktzuordnungen exportieren oder importieren

**Gilt für:** Enterprise

Erfahren Sie, wie globale Administratoren die Organisations- und Produktverwaltung mit Export- und Importfunktionen in der Global Admin Console optimieren können.

Greifen Sie auf die **[!UICONTROL Organisationen]** in der [Global Admin Console zu](https://helpx.adobe.com/enterprise/global-admin-console/adopt-global-administration.html) um die Organisationsstruktur zu exportieren oder zu importieren. Gehen Sie zur Registerkarte **[!UICONTROL Produktzuordnung]** für Zuordnungsdaten. Verwenden Sie das Symbol **[!UICONTROL Weitere Optionen]** **⋮**, um Export oder Import auszuwählen. [Melden Sie sich bei Global Admin Console an](https://global-admin-console.adobe.com).

## Exportieren der Organisationsstruktur

Als [globaler Administrator](https://helpx.adobe.com/enterprise/global-admin-console/manage-administrators.html) können Sie die Organisationshierarchie exportieren. Sie können eine JSON-, CSV- oder XLSX-Darstellung der gesamten Organisationshierarchie oder einer Untergruppe davon herunterladen. Sie können diese Daten dann zur Analyse oder Änderung verwenden.

Das ausgewählte Exportformat wirkt sich auf die Struktur der exportierten Daten aus:

- CSV-Format - Ermöglicht den Export von jeweils nur einer Art von Daten. Beim Exportieren von Produktprofilen im CSV-Format werden die Profile und Ressourcen zu einer Tabelle zusammengefasst. Für das Produktprofil gibt es mehrere Einträge, einen für jede Ressource.
- XLSX-Format - Ergibt, dass jedes Organisationsdetail in einem separaten Blatt angezeigt wird. Datensätze sind zwischen den verschiedenen Objekttypen durch eine Referenz-ID verbunden. In einigen Fällen kann es mehrere Zeilen für ein bestimmtes Objekt geben (z. B. Ressourcenobjekte, wenn ein Satz von Werten mit einer bestimmten Ressource verknüpft ist).
- JSON-Format - Das flexibelste. Es können strukturelle Beziehungen zwischen exportierten Objekten genutzt werden (z. B. erscheinen Produkte in einer Organisation direkt im Organisationselement). Dieselben Felder werden in alle drei Formate exportiert, aber einige Werte im JSON-Format sind redundant.

### Zu exportierende Schritte

1. Melden Sie sich bei der [Global Admin Console](https://global-admin-console.adobe.com/) an. Verwenden **[!UICONTROL auf der Registerkarte]** Organisationen“ die Organisationsauswahl, um die Organisationshierarchie auszuwählen, in die Sie exportieren möchten. Daten für alle Organisationen in der Hierarchie werden exportiert.
2. Wählen Sie das ⋮ **[!UICONTROL Weitere Optionen]** und dann **[!UICONTROL Exportieren]** aus.

   ![Organisationsstruktur exportieren](./assets/export-org-structure.png)

3. Wählen **[!UICONTROL Dialogfeld „Exportieren]** aus, was exportiert werden soll und in welchem Format die Daten exportiert werden sollen.

   ![Dialogfeld &quot;Admin Console-Export“](./assets/export-12.png)

4. Wählen Sie **[!UICONTROL Exportieren]** aus. Es kann mehrere Minuten dauern, bis die Exportdatei erstellt ist. Um den Bericht herunterzuladen, gehen Sie nach Abschluss des Vorgangs zu **[!UICONTROL Global Admin Console]** > **[!UICONTROL Insights]** > **[!UICONTROL Berichte exportieren]**.

&#x200B;> [!NOTE]
>
> JSON-Dateien werden im ZIP-Format exportiert. Sie können sie mithilfe eines ZIP-Dienstprogramms oder der ZIP-Funktionen des Betriebssystems öffnen.

Nach dem Herunterladen der Datei können Sie die Daten bearbeiten und dann wieder importieren. Die importierten Aktualisierungen werden in der Global Admin Console so angezeigt, als hätten Sie die Daten manuell bearbeitet.

## Organisationsstruktur importieren

Als [globaler Administrator](https://helpx.adobe.com/enterprise/global-admin-console/manage-administrators.html) können Sie potenziell geänderte Daten importieren. Beim Hochladen werden die neuen Daten mit den aktuellen Daten verglichen und alle Änderungen werden auf die Organisationshierarchie angewendet. Alle Importvorgänge werden mit der aktualisierten Kopie der Organisationshierarchie durchgeführt. Wenn Sie ausstehende Änderungen haben, werden die Importänderungen zusätzlich zu den ausstehenden Änderungen in der Hierarchie hinzugefügt.

### Importschritte

1. Melden Sie sich bei der [Global Admin Console](https://global-admin-console.adobe.com) an. Verwenden **[!UICONTROL auf der Registerkarte]** Organisationen“ die Organisationsauswahl, um die Organisationshierarchie auszuwählen, in der Sie den Import durchführen möchten.
2. Wählen Sie das Symbol **[!UICONTROL Weitere Optionen]** **⋮** und dann **[!UICONTROL Importieren]** aus. Je nach Größe und Komplexität der Importdatei kann die Verarbeitung einige Sekunden bis mehrere Minuten dauern.
3. Wählen Sie **[!UICONTROL Datei auswählen]** und wählen Sie eine JSON-, CSV- oder XLSX-Datei zum Hochladen aus. Bei CSV-Dateien kann jeweils nur ein Organisationsdetail importiert werden, während der Import von Produkten nicht unterstützt wird. Die importierten Änderungen erscheinen so, als hätten Sie die Daten manuell bearbeitet.
4. Wählen Sie **[!UICONTROL Schließen]** aus.
5. Wählen **[!UICONTROL Ausstehende Änderungen überprüfen]** aus. Wählen Sie dann **[!UICONTROL Änderungen übermitteln]** aus, um [&#x200B; auszuführen](https://helpx.adobe.com/enterprise/global-admin-console/execute-jobs.html). Vor dem Ausführen der Änderungen werden die ausstehenden Aktionen auf dieselbe Weise angezeigt wie bei manuellen Bearbeitungen in der Global Admin Console.

## Schemata exportieren und importieren

Beim Importieren von Daten mithilfe einer CSV-Datei können die Felder in jeder beliebigen Reihenfolge angezeigt werden, müssen jedoch immer mit ihrer Kopfzeile übereinstimmen.

Beim Importieren von Daten müssen Sie für jedes Element einen Vorgang angeben. Der Vorgang kann einer der folgenden sein:

- Aktualisieren: zeigt eine Bearbeitung an.
- Erstellen: gibt das Erstellen eines neuen Objekts an (z. B. Organisation, Benutzergruppe oder Administrator).
- Löschen: gibt das Löschen eines Objekts an (z. B. Organisation, Benutzergruppe oder Administrator).

Eingabedateien ohne oder leeres Operationsfeld werden ignoriert.

### Organisationen

<table>
  <tr>
    <th>Feldname</th>
    <th>Beschreibung</th>
    <th>Anmerkungen</th>
  </tr>

<tr>
    <td>id</td>
    <td>
      Organisations-ID.<br><br>
      Beim Hinzufügen einer neuen Organisation kann dies leer oder auf eine Platzhalterkennung festgelegt sein, z. B. .
      new_org_1. Die Platzhalterkennung wird in Fällen verwendet, in denen andere importierte Einträge verweisen müssen
      für diese Organisation. Nach der Erstellung wird eine tatsächliche Organisations-ID zugewiesen, die alle ersetzt
      Verwendung der Platzhalter-Organisations-ID.
    </td>
    <td>Kann bei operation=create auf einen temporären Wert gesetzt werden</td>
  </tr>

<tr>
    <td>name</td>
    <td>
      Einfacher Name der Organisation. Mindestlänge 4, max. 100.
      Namen können UTF-8-Zeichen mit bis zu 3 Byte enthalten,
      4-Byte-Zeichen werden nicht unterstützt.
    </td>
    <td>
      Kann festgelegt oder aktualisiert werden, wenn operation=create bzw. operation=update gilt
    </td>
  </tr>

<tr>
    <td>Länder-Code</td>
    <td>Länder- oder Regionscode</td>
    <td>
      Muss bei operation=create festgelegt werden, kann bei operation=update aktualisiert werden
    </td>
  </tr>

<tr>
    <td>type</td>
    <td>Art der Organisation</td>
    <td>Schreibgeschützt</td>
  </tr>

<tr>
    <td>parentOrgId</td>
    <td>
      ID der übergeordneten Organisation. Leer für Stammorganisation.
      Bei der Aktualisierung gelten erhebliche Einschränkungen, einschließlich der Tatsache, dass sich neue übergeordnete Elemente in derselben Hierarchie befinden und
      die Produkte haben, die in der Organisation vorhanden sind.
    </td>
    <td>
      Kann festgelegt oder aktualisiert werden, wenn operation=create bzw. operation=update gilt
    </td>
  </tr>

<tr>
    <td>adminCount</td>
    <td>Anzahl der Administratoren</td>
    <td>Schreibgeschützt</td>
  </tr>

<tr>
    <td>domainCount</td>
    <td>Anzahl der Domains</td>
    <td>Schreibgeschützt</td>
  </tr>

<tr>
    <td>userCount</td>
    <td>Anzahl der Benutzer</td>
    <td>Schreibgeschützt</td>
  </tr>

<tr>
    <td>userGroupCount</td>
    <td>Anzahl der Benutzergruppen</td>
    <td>Schreibgeschützt</td>
  </tr>

<tr>
    <td>Admins</td>
    <td>Satz von Admin-Objekten, die Administratoren für diese Organisation darstellen</td>
    <td rowspan="6">
      Fehlt möglicherweise, wenn für den Export nicht ausgewählt. Es wird in XLSX-Dateien auf einer separaten Registerkarte angezeigt.
    </td>
  </tr>

<tr>
    <td>Domains</td>
    <td>Satz von Domain-Objekten, die Domains in dieser Organisation darstellen</td>
  </tr>

<tr>
    <td>Produkte</td>
    <td>Satz von Produktobjekten, die Produkte in dieser Organisation darstellen</td>
  </tr>

<tr>
    <td>productProfile</td>
    <td>Satz von Produktprofilobjekten, die Produktprofile in dieser Organisation darstellen</td>
  </tr>

<tr>
    <td>userGroups</td>
    <td>Satz von Benutzergruppenobjekten, die Benutzergruppen in dieser Organisation repräsentieren</td>
  </tr>

<tr>
    <td>orgPolicies</td>
    <td>Richtlinien und ihre Werte repräsentierende Struktur</td>
  </tr>

<tr>
    <td>Betrieb</td>
    <td>
      Leer, Erstellen, Aktualisieren oder Löschen. Beim Datenimport zu ergreifende Aktion
    </td>
    <td>Immer leer beim Exportieren.</td>
  </tr>
</table>


**Importanforderungen:**

- Zum Aktualisieren oder Löschen muss orgId auf eine vorhandene Organisation in Ihrer Hierarchie verweisen.
- Wenn Sie eine neue Organisation erstellen, können Sie das Feld orgId leer lassen oder auf eine eindeutige ID festlegen, die Sie erstellen können (z. B. new-1 oder new-2). Diese ID kann verwendet werden, um auf die zu erstellende Organisation zu verweisen.
- Ländercode muss gültig sein.
- Die orgId für *Update*- und *Delete*-Vorgang sollte bereits in der Organisationshierarchie vorhanden sein.
- orgId, die als *Löschen* markiert ist, sollte nicht als übergeordnete orgId für Organisationen mit *Aktualisieren* oder *Erstellen* ausgewählt werden.
- Untergeordnete Organisationen derselben Ebene und desselben übergeordneten Elements sollten nicht dieselben orgNames haben.
- Zum Erstellen einer Organisation oder Aktualisieren eines Organisationsnamens darf der Name der Organisation nicht mit dem Namen eines vorhandenen untergeordneten Elements desselben übergeordneten Elements übereinstimmen.

### Admins

<table>
  <tr>
    <th>Feldname</th>
    <th>Beschreibung</th>
    <th>Verwenden von </th>
  </tr>

<tr>
    <td>orgId</td>
    <td>Verweis auf die Organisation, in der sich der Administrator befindet.</td>
    <td>Wird als Referenz verwendet, um enthaltende oder verknüpfte Objekte zu finden.</td>
  </tr>

<tr>
    <td>firstName</td>
    <td>
     Vorname des Admin-Benutzers.
Vor- und Nachname für Adobe ID-Benutzer können durch einen vom Benutzer eingegebenen Wert ersetzt werden, wenn der Benutzer die Einladung annimmt.
    </td>
    <td rowspan="4">
      Kann festgelegt oder aktualisiert werden, wenn operation=create bzw. operation=update gilt
    </td>
  </tr>

<tr>
    <td>lastName</td>
    <td>Nachname des Admin-Benutzers</td>
  </tr>

<tr>
    <td>email</td>
    <td>Admin-Benutzer-E-Mail-Adresse. Dies ist ein Primärschlüssel für den Benutzer und muss eindeutig sein.</td>
  </tr>

<tr>
    <td>Länder-Code</td>
    <td>
Länder- oder Regionscode, in dem der Benutzer tätig ist. Gilt nur für Federated ID- und Enterprise ID-Typen.
    </td>
  </tr>

<tr>
    <td>userType</td>
    <td>Entweder "Adobe ID", "Enterprise ID" oder "Federated ID".</td>
    <td>Schreibgeschützt</td>
  </tr>

<tr>
    <td>adminType</td>
    <td>ENTWEDER „GLOBAL ADMIN“, „GLOBAL VIEWER“, „SYSTEM ADMIN“, „USER GROUP ADMIN“, „PRODUCT ADMIN“, „PRODUCT PROFILE ADMIN“, „DEPLOYMENT ADMIN“ ODER „STORAGE_ADMIN“.</td>
    <td rowspan="4">Kann festgelegt werden, wenn operation=Create</td>
  </tr>

<tr>
    <td>groupId</td>
    <td>Gruppen-ID der Gruppe, für die dieser Benutzer ein Administrator ist. Nur für Benutzergruppen- und Produktprofil-Administrierende relevant.</td>

</tr>

<tr>
    <td>licenseId</td>
    <td>Produktlizenz-ID des Produkts, für das dieser Benutzer Administrator ist. Nur für Produkt-Admins relevant.</td>

</tr>

<tr>
    <td>domain</td>
    <td>Domain-Name des Benutzers, wenn keine E-Mail-Domain verwendet wird</td>

</tr>

<tr>
    <td>userName</td>
    <td>Benutzername des Benutzers, wenn keine E-Mail-Adresse verwendet wird</td>
    <td></td>
  </tr>

<tr>
    <td>Betrieb</td>
    <td>Leer, Erstellen, Aktualisieren oder Löschen. Beim Datenimport zu ergreifende Aktion</td>
    <td></td>
  </tr>
</table>


**Importanforderungen:**

- orgId, email, adminType und userType müssen gültige Werte enthalten.
- countryCode muss gültig sein.
- Wenn der Benutzer bereits vorhanden ist und aktualisiert wird, muss der userType dem Benutzer entsprechen.
- Überprüfen Sie, ob in der Organisation doppelte E-Mail-Adressen vorhanden sind.

### Produktprofile

Exporte und Importe von Produktprofilen bestehen aus zwei Teilen: den Produktprofildetails und einem Satz von Ressourcen, die mit dem Produktprofil verknüpft sind. Diese Ressourcen identifizieren Dienste, die konfiguriert werden können, in der Regel nur, um sie zu aktivieren oder zu deaktivieren.

- Die Ressourcenobjekte sind im Produktprofil im JSON-Format verschachtelt.
- Bei Verwendung von CSV oder XLSX mit Produktprofilen werden die Profile und Ressourcen zu einer Tabelle zusammengefasst. Für das Produktprofil sind mehrere Einträge vorhanden, einer für jede Ressource.
- Das Feld „Ausgewählt“ in der Ressource steuert, ob der Service aktiviert ist.
- Beim Importieren von Produktprofilen muss es einen Vorgang Erstellen oder Aktualisieren für das Produktprofil selbst und für alle Ressourcenobjekte geben, die aktualisiert oder erstellt werden sollen.


<table>
  <tr>
    <th>Feldname</th>
    <th>Beschreibung</th>
    <th>Verwenden von </th>
  </tr>

<tr>
    <td>productProfileId</td>
    <td>
     <br><br>
      Kennung des Produktprofils
Der Platzhalterwert kann beim Erstellen verwendet werden, damit andere Objekte auf das neue Profil verweisen können.
    </td>
    <td>Kann bei operation=create auf einen temporären Wert gesetzt werden</td>
  </tr>

<tr>
    <td>productProfileName</td>
    <td>
     Name des Produktprofils. Es kann sich nicht um ein Duplikat anderer Produktprofile oder Benutzergruppen in derselben Organisation handeln.
    </td>
    <td rowspan="2">
   Kann festgelegt oder aktualisiert werden, wenn operation=create bzw. operation=update gilt
    </td>
  </tr>

<tr>
    <td>productProfileDescription</td>
    <td>Textbeschreibung des Produktprofils</td>
  </tr>

<tr>
    <td>licenseId</td>
    <td>Lizenz-ID-Verweis auf das Produkt</td>
    <td rowspan="2"> Wird als Referenz verwendet, um ein enthaltenes oder verknüpftes Objekt zu finden
    </td>
  </tr>

<tr>
    <td>orgId</td>
    <td>
Organisation, die die Benutzergruppe enthält
    </td>
  </tr>

<tr>
    <td>Benachrichtigungen</td>
    <td>Mit True oder False wird angegeben, ob eine E-Mail-Benachrichtigung an Benutzer gesendet werden soll, wenn sie diesem Produktprofil hinzugefügt oder daraus entfernt werden</td>
    <td>Kann festgelegt oder aktualisiert werden, wenn operation=create bzw. operation=update gilt</td>
  </tr>

<tr>
    <td>Ressourcen</td>
    <td> Array von Ressourcen, die mit diesem Produktprofil verknüpft sind.
Das Feld Ressourcen ist nur für das JSON-Format vorhanden. Für das CSV- und XLSX-Format werden Ressourcen mit den folgenden zusätzlichen Feldern dargestellt: resourceName, resourceId, resourceDescription, icon, selected, quota, resourceType. Einzelheiten zu diesen Feldern finden Sie unter [Produkte und Ressourcen](#products-and-resources).
Wenn das Produktprofil mehr als eine Ressource hat, sind mehrere Zeilen vorhanden, eine für jede Ressource. Die anderen Felder haben für jede Ressource dieselben Werte. </td>
    <td></td>
  </tr>

<tr>
    <td>Betrieb</td>
    <td>Leer, Erstellen, Aktualisieren oder Löschen. Beim Datenimport zu ergreifende Aktion</td>  
    <td></td>
  </tr>
</table>



**Importanforderungen:**

- productProfileId, licenseId und orgId müssen gültige Werte haben.
- Beim Erstellen eines Produktprofils muss der productProfileName ein gültiger Name sein und darf keinen anderen Produktprofilnamen oder Benutzergruppennamen in derselben Organisation duplizieren.
- Das Kontingentfeld muss einen gültigen Wert für den Einheitentyp haben. Dies ist numerisch oder „unbegrenzt“, wenn resourceType=QUOTA oder andernfalls leer ist.
- Das Benachrichtigungsfeld muss „true“ oder „false“ sein.
- Validieren Sie für CSV- und XLSX-Importe productProfileId. Alle Einträge müssen dieselbe orgId, licenseId und productProfileName aufweisen.
- Überprüfen Sie doppelten productProfileName in der Eingabedatei und in der Organisation.
- Profile, die aktualisiert und gelöscht werden sollen, müssen in der Organisation vorhanden sein.
- Ressourcen, die aktualisiert und gelöscht (deaktiviert) werden sollen, müssen im Profil vorhanden sein.
- Stellen Sie Folgendes sicher, damit Profile erstellt werden können:
   - Die orgId sollte eine neue Organisation oder eine vorhandene Organisation sein.
   - Die licenseId sollte ein neues oder ein vorhandenes Produkt sein.
   - Überprüfen Sie die Ressourcen für das Profil.

### Ressourcen in Produktprofilen


<table>
  <tr>
    <th>Feldname</th>
    <th>Beschreibung</th>
    <th>Verwenden von </th>
  </tr>

<tr>
    <td>resourceName</td>
    <td>
     Name der Ressource
    </td>
    <td>Schreibgeschützt</td>
  </tr>

<tr>
    <td>resourceId</td>
    <td>
   Ressourcenkennung
    </td>
    <td>
   Schreibgeschützt
    </td>
  </tr>

<tr>
    <td>resourceDescription</td>
    <td>Textbeschreibung der Ressource</td>
    <td>Schreibgeschützt</td>
  </tr>

<tr>
    <td>icon</td>
    <td>URL zum Bild für Ressource</td>
    <td> Schreibgeschützt</td>
  </tr>

<tr>
    <td>ausgewählt</td>
    <td>Für einen Konfigurationseintrag, ob die Funktion aktiviert ist. Dieses Feld ist nur in JSON vorhanden.</td>
    <td rowspan ="2">Kann festgelegt oder aktualisiert werden, wenn operation=create bzw. operation=update gilt.</td>
  </tr>

<tr>
    <td>Kontingent</td>
    <td>Menge der primären Ressource, die Benutzern über dieses Produktprofil ausgegeben werden kann. Dieses Feld ist nur in JSON vorhanden.</td>
    <td></td>
  </tr>

<tr>
    <td>resourceType</td>
    <td> Wenn vorhanden, ist der Wert SERVICE. Es zeigt an, dass diese Ressource einen Service darstellt, der basierend auf dem Wert des ausgewählten Felds aktiviert oder deaktiviert werden kann. Dieses Feld ist nur in JSON vorhanden.</td>
    <td>Schreibgeschützt</td>
  </tr>

<tr>
    <td>Betrieb</td>
    <td>Leer, Erstellen, Aktualisieren oder Löschen. Beim Datenimport zu ergreifende Aktion</td>  
    <td></td>
  </tr>
</table>

**Importanforderungen:**

- Das Vorgangsfeld für Ressourcen wird ignoriert, wenn für das Produktprofil, zu dem sie gehören, Vorgänge auf *Löschen* oder *Erstellen* eingestellt sind.
- Es sollte keine Ressource zum Löschen markiert werden; dies ist ein ungültiger Vorgang.
- Damit Produktprofile erstellt werden können, sollte die Anzahl der Ressourcen mit der Anzahl der Ressourcen des Quellproduktprofils übereinstimmen.
- Für Ressourcen mit *Aktualisieren*-Vorgang muss die Ressource im Produktprofil vorhanden sein.

### Benutzergruppen

<table>
  <tr>
    <th>Feldname</th>
    <th>Beschreibung</th>
    <th>Verwenden von </th>
  </tr>

<tr>
    <td>userGroupId</td>
    <td>
Kennung der Benutzergruppe
Der Platzhalterwert kann beim Erstellen verwendet werden, damit andere Objekte auf die neue Benutzergruppe verweisen können.
    </td>
    <td>Kann bei operation=create auf einen temporären Wert gesetzt werden</td>
  </tr>

<tr>
    <td>userGroupName</td>
    <td> Name der Benutzergruppe</td>
    <td rowspan="2"> Kann festgelegt oder aktualisiert werden, wenn operation=create bzw. operation=update gilt</td>
  </tr>

<tr>
    <td>userGroupDescription</td>
    <td>Textbeschreibung der Benutzergruppe</td>
    <td></td>
  </tr>

<tr>
    <td>userCount</td>
    <td>Anzahl der Benutzer in Benutzergruppe</td>
    <td>Schreibgeschützt</td>
  </tr>

<tr>
    <td>Profile</td>
    <td>Array von Produktprofil-IDs, mit denen die Benutzergruppe verknüpft ist.
XLSX hat eine Zeile pro Wert mit denselben Werten für andere Felder.</td>
    <td>Kann festgelegt oder aktualisiert werden, wenn operation=create bzw. operation=update gilt</td>
  </tr>

<tr>
    <td>orgId</td>
    <td>Organisation, die die Benutzergruppe enthält.</td>
    <td>Wird als Referenz verwendet, um ein enthaltenes oder verknüpftes Objekt zu finden.</td>
  </tr>

<tr>
    <td>Betrieb</td>
    <td>Leer, Erstellen, Aktualisieren oder Löschen. Beim Datenimport zu ergreifende Aktion</td>
    <td></td>
  </tr>
</table>



**Importanforderungen:**

- orgId muss auf eine bestehende Organisation oder eine Organisation verweisen, die im selben Import erstellt wird.
- userGroupId muss für die Aktualisierung oder Löschung auf eine vorhandene Gruppe verweisen und kann eine ID sein, die Sie für neue Benutzergruppen definieren.
- Für die Aktualisierung oder Erstellung darf userGroupName nicht leer sein und darf keinen anderen Benutzergruppen- oder Produktprofilnamen in derselben Organisation duplizieren.
- Stellen Sie sicher, dass userGroupName in der Eingabedatei und in der Organisation nicht dupliziert ist.
- Zu aktualisierende und zu löschende Benutzergruppen müssen in der Organisation vorhanden sein.
- Das Profil, das aus der Benutzergruppe entfernt werden soll, muss in der Benutzergruppe vorhanden sein. Aktualisierungsvorgänge können nicht für das Profil einer Benutzergruppe durchgeführt werden.
- Stellen Sie Folgendes sicher, damit Benutzergruppen erstellt werden können:
   - Die orgId sollte eine neue Organisation oder eine vorhandene Organisation sein.
   - Die LicenseId sollte ggf. ein neues oder ein vorhandenes Produkt sein.
   - Die productProfileId sollte ein neues Produktprofil oder ein vorhandenes Produktprofil sein.

### Domains

Die Domain-Informationen enthalten schreibgeschützte Informationen zu den in den einzelnen Organisationen verfügbaren Domains. Diese Daten können nicht bearbeitet werden.


| Feldname | Beschreibung | Verwenden von  |
| ------------- | ----------------------------------------------------------------------------------------- | ------------------------------------------------------------- |
| orgId | Verweis auf die Organisation, in der diese Domain aufgeführt ist | Wird als Referenz verwendet, um enthaltende oder verknüpfte Objekte zu finden. |
| domainName | Name der Domain (z. B. adobe.com). | Schreibgeschützt |
| directoryName | Name des Verzeichnisses, in dem die Domain aufgeführt ist | Schreibgeschützt |
| directoryType | Einer von Federated ID oder Enterprise ID. | Schreibgeschützt |
| domainStatus | entweder „AKTIV“, „RESERVIERT“, „NICHT BEANSPRUCHT“, „BEANSPRUCHT“, „VALIDIERT“, „ZURÜCKGEZOGEN“, „ABGELAUFEN“. | Schreibgeschützt |


### Produkte und Ressourcen {#products-and-resources}

In XLSX-Dateien gibt es zwei Blätter - eine für Produkte und eine für die Ressourcen. In JSON werden Ressourcenobjekte im Produktobjekt verschachtelt.

**Produkte**


| Feldname | Beschreibung | Verwenden von  |
| ------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------- |
| licenseId | Kennung, die das Produkt identifiziert. Jedes Produkt verfügt über eine eindeutige Lizenzkennung in der Organisation, in der es aufgeführt ist. Wenn Sie ein neues Produkt hinzufügen, kann dies leer sein oder eine Platzhalterkennung verwenden (z. B. new_product_1). Nach der Erstellung wird eine tatsächliche Lizenzkennung zugewiesen, die alle Verwendungen der Platzhalter-Lizenzkennung ersetzt. | Kann bei operation=create auf einen temporären Wert gesetzt werden |
| productName | Name des Produkts | Schreibgeschützt |
| productDescription | Textbeschreibung des Produkts | Schreibgeschützt |
| allowOverallocation | Boolescher Wert, der angibt, ob eine Überallokation dieser Produktinstanz zulässig ist. Überzuordnung bezieht sich auf die Möglichkeit, einer untergeordneten Organisation mehr Mengen zu gewähren als Ihnen gewährt wurden. | Kann festgelegt oder aktualisiert werden, wenn operation=create bzw. operation=update gilt |
| icon | URL des Produktsymbols | Schreibgeschützt |
| sourceLicenseId | Lizenzkennung der Produktinstanz in der Organisation, der dieses Produkt zugeordnet wurde. Der Wert ist null, wenn es sich bei dieser Instanz nicht um ein zugewiesenes Produkt, sondern um ein gekauftes Produkt handelt. | Kann festgelegt werden, wenn operation=Create |
| productId | Kennung des Produkts | Schreibgeschützt |
| orgId | Kennung der Organisation, die diese Produktinstanz enthält | Wird als Referenz verwendet, um ein enthaltenes oder verknüpftes Objekt zu finden |
| neu verteilbar | Boolescher Wert, der angibt, ob dieses Produkt über Ressourcen verfügt, die untergeordneten Organisationen gewährt werden können. | Schreibgeschützt |
| Ressourcen | Objekt, das einen Satz von Ressourcenobjekten enthält, die die Ressourcen und Einstellungen in diesem Produkt darstellen |                                                                               |
| Betrieb | Leer, Erstellen, Aktualisieren oder Löschen. Beim Datenimport zu ergreifende Aktion |                                                                               |


**Importanforderungen:**

- Für die Erstellung muss licenseId eine eindeutige ID sein, die Sie erstellen.
- Für die Aktualisierung muss licenseId die ID eines vorhandenen Produkts in der angegebenen Organisation sein.
- orgId muss auf eine vorhandene Organisation verweisen oder auf eine Organisation, die im selben Importvorgang erstellt wird.
- Für die Erstellung muss sourceLicenseId auf ein vorhandenes Produkt oder auf die ID verweisen, die Sie für ein Produkt definiert haben, das im selben Importvorgang erstellt wird.
- licenseId und sourceLicenseId sollten für Produkte mit dem Vorgang *Erstellen* nicht identisch sein.
- Validieren Sie die Organisationen von Produkten. Die Organisation sollte eine neue sein oder bereits in der Organisationshierarchie vorhanden sein.
- Für *Vorgang* Aktualisieren“ und *Löschen* sollte das Produkt bereits in der Organisationshierarchie vorhanden sein.
- licenseId, die als *Löschen* markiert ist, sollte nicht als sourceLicenseId von Produkten mit *Erstellen* und *Aktualisieren* verwendet werden.
- Überprüfen Sie bei Produkten mit *Erstellen*-Vorgang, ob die sourceLicenseId in der übergeordneten Organisation vorhanden sein muss.

**Ressourcen für Produkte**

Ressourcenobjekte können in Produkten und in Produktprofilen angezeigt werden.


| Feldname | Beschreibung | Verwenden von  |
| ------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------- |
| resourceName | Name der Ressource | Schreibgeschützt |
| resourceId | Ressourcenkennung | Schreibgeschützt |
| resourceDescription | Textbeschreibung der Ressource | Schreibgeschützt |
| icon | URL zum Bild für Ressource | Schreibgeschützt |
| productName | Name des Produkts, zu dem diese Ressource gehört. | Schreibgeschützt |
| licenseId | Lizenzkennung (Produktinstanz) des Produkts, zu dem diese Ressource gehört. | Wird als Referenz verwendet, um ein enthaltenes oder verknüpftes Objekt zu finden |
| grantedQuantity | Gewährte Menge dieser Ressource: Menge der Ressourcen, die diese Organisation lokal verwenden oder untergeordneten Organisationen zuordnen kann. | Kann festgelegt oder aktualisiert werden, wenn operation=create bzw. operation=update gilt |
| Einheit | Name der Einheit der Menge, für die die Finanzhilfe gewährt wurde. | Schreibgeschützt |
| currentQuantity | Aktuelle nutzbare Menge in dieser Organisation. Dies ist die zugewiesene Menge abzüglich der den untergeordneten Organisationen zugewiesenen Ressourcen. Dies ist der Wert, der in der Admin Console für dieses Produkt/diese Ressource angezeigt wird. | Schreibgeschützt |
| provisionedQuantity | Tatsächlich bereitgestellte Menge: kann kleiner als „grant“ oder „current“ sein, kann kleiner als „currentQuantity“ sein, wenn eine Begrenzung vorhanden ist. | Schreibgeschützt |
| Betrieb | Leer, Erstellen, Aktualisieren oder Löschen. Beim Datenimport zu ergreifende Aktion |                                                                               |


**Importanforderungen:**

Das Feld Vorgang für Ressourcen wird ignoriert, wenn für das Produkt, zu dem sie gehören, Vorgänge auf *Löschen* oder *Erstellen* eingestellt sind.
- Es sollte keine Ressource zum Löschen markiert werden; dies ist ein ungültiger Vorgang.
- Für zu erstellende Produkte sollte die Anzahl der Ressourcen mit der Anzahl der Ressourcen des Quellprodukts übereinstimmen.
- Für Ressourcen mit *Aktualisieren*-Vorgang muss die Ressource im Produkt vorhanden sein.

## Importieren und Exportieren von Produktzuordnungsdaten

Als [globaler Administrator](https://helpx.adobe.com/enterprise/global-admin-console/manage-administrators.html) können Sie die Produktzuordnungsdaten als JSON- oder CSV-Datei exportieren. Anschließend können Sie diese Daten bearbeiten und zum Importieren der Änderungen hochladen. Beim Hochladen der potenziell geänderten Daten werden die neuen Daten mit den aktuellen Daten verglichen und alle Änderungen werden auf die Produktzuordnungsdaten angewendet. Sie können dann die ausstehenden Änderungen überprüfen und übermitteln, damit sie wirksam werden.

## Exportieren des Produktzuordnungsmodells

Gehen Sie wie folgt vor, um das Produktzuordnungsmodell zu exportieren:

1. Melden Sie sich bei der [Global Admin Console](https://global-admin-console.adobe.com/) an und navigieren Sie zur Registerkarte **[!UICONTROL Produktzuordnung]** .
2. Wählen Sie das ⋮ **[!UICONTROL Weitere Optionen]** und dann **[!UICONTROL CSV exportieren]** oder **[!UICONTROL JSON exportieren]**. Ihre Datei wird heruntergeladen. [Weitere Informationen](#export-and-import-formats-for-product-allocation) über die Exportformate.

## Produkt-Zuordnungsmodell importieren

Sie können Daten exportieren, ändern und dann die geänderte Datei importieren. Gehen Sie wie folgt vor, um das Produktzuordnungsmodell zu importieren:

1. Melden Sie sich bei der [Global Admin Console](https://global-admin-console.adobe.com/) an und navigieren Sie zur Registerkarte **[!UICONTROL Produktzuordnung]** .
2. Wählen Sie das ⋮ **[!UICONTROL Weitere Optionen]** und dann **[!UICONTROL Importieren]** aus.
3. JSON- oder CSV-Datei zum Hochladen auswählen.
4. Wählen **[!UICONTROL Ausstehende Änderungen überprüfen]** aus. Wählen Sie nach Überprüfung der Änderungen **[!UICONTROL Änderungen übermitteln]** aus, um [&#x200B; Änderungen &#x200B;](https://helpx.adobe.com/enterprise/global-admin-console/execute-jobs.html).

## Export- und Importformate für die Produktzuordnung

Die Export- und Importformate sind identisch. Beim Importieren im CSV-Format können die Felder in jeder beliebigen Reihenfolge angezeigt werden, sie müssen jedoch mit der Kopfzeile übereinstimmen. Beim Importieren im JSON-Format können die Felder in beliebiger Reihenfolge angezeigt werden.

Sie müssen den Vorgang beim Importieren von Produktzuordnungsdaten angeben. Der Vorgang kann einer der folgenden sein:

- Aktualisieren: zeigt eine Bearbeitung an (Änderung an „grantedQuantity“, „allowOverAllocation“-Werte).
- Erstellen: gibt an, dass der angegebenen Organisation eine Produktressource hinzugefügt werden soll.
- Löschen: gibt das Löschen des Produkts an.

Wenn kein -Vorgang angegeben ist, treten keine Änderungen auf, wenn Daten für diese Zeile in CSV oder das -Objekt in JSON importiert werden.

In der exportierten Datei gibt es eine Zeile oder einen Datensatz für jede Produktressource. Einige Produkte verfügen über mehr als eine Ressource.

Wenn ein Produkt mehr als eine Ressource hat, können Aktualisierungsvorgänge auf unabhängige Ressourcen angewendet werden, ein Löschvorgang löscht das Produkt einschließlich aller Ressourcen aus einer Organisation, und ein Erstellungsvorgang benötigt einen Datensatz für jede der Ressourcen in der Importdatei, damit die richtige Menge jeder dieser Ressourcen angegeben werden kann. Das Feld allowOverAllocation ist produktweit und es spielt keine Rolle, in welcher Ressource ein Update für dieses Feld vorhanden ist.

### Beschreibung der Header


| Feldname | Beschreibung | Verwenden von  |
| --------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------- |
| productName | Name des Produkts. | Schreibgeschützt |
| licenseId | Kennung eines Produkts (eindeutig für ein Produkt in einer Organisation). Wenn Sie ein neues Produkt hinzufügen, kann dies leer sein oder auf eine Platzhalterkennung (z. B. new_product_1) festgelegt werden. Die Platzhalterkennung wird in Fällen verwendet, in denen andere importierte Einträge auf dieses Produkt verweisen müssen. Nach der Erstellung wird eine tatsächliche Lizenzkennung zugewiesen, die alle Verwendungen der Platzhalter-Lizenzkennung ersetzt. | Kann festgelegt werden, wenn operation=Create |
| sourceLicenseId | Kennung des übergeordneten Produkts. Sie ist leer oder null, wenn dies einen Kauf anstelle einer Zuordnung darstellt. | Kann festgelegt werden, wenn operation=Create |
| productId | Kennung, die diese Produktklasse identifiziert. Diese ID wird von Produkten desselben Typs gemeinsam genutzt und unterscheidet sich von der licenseId, die eine Instanz dieses Produkts angibt. | Schreibgeschützt |
| resourceName | Name dieser Produktressource. Beispiel: Benutzerlizenzen. | Schreibgeschützt |
| resourceId | Kennung, die diese Produktressource identifiziert. | Kann festgelegt werden, wenn operation=Create |
| orgPathName | Pfadname der Organisation, in der sich diese Produktressource befindet. Durch &quot;/&quot; getrennte Segmente | Schreibgeschützt |
| orgName | Einfacher Name der Organisation, die diese Produktressource enthält. Dies ist das letzte Segment des orgPathName. | Schreibgeschützt |
| orgId | Organisations-ID der Organisation, die diese Produktressource enthält. | Kann festgelegt werden, wenn operation=Create |
| grantedQuantity | Anzahl der Einheiten der Ressourcenmenge, die dieser Organisation von der übergeordneten Organisation gewährt wurde, oder der gekaufte Betrag, wenn dieser Produktressourceneintrag einen Kauf darstellt. Dieses Feld kann aktualisiert werden, mit Ausnahme von gekauften Produkten oder Stammzuweisungen, die der globale Administrator nicht ändern darf. | Kann aktualisiert werden, wenn operation=Update oder operation=Create |
| Einheit | Name der Ressourceneinheit. Beispiel: Benutzer. | Schreibgeschützt |
| totalAllokations | Summe der Zuwendungen an untergeordnete Organisationen dieser Organisation für diese Produktressource. Dieser Wert umfasst die direkten Zuschüsse an unmittelbare Kinder sowie die Überallokationen dieser Organisationen. Wenn diese Organisation beispielsweise einem untergeordneten Element 10 und diesem untergeordneten Element 25 zuweist, wären die Gesamtzuweisungen 25: die 10 für das untergeordnete Element plus ein Überschuss von 15 für dieses untergeordnete Element. | Schreibgeschützt |
| Zuschuss | Betrag, um den die Gesamtzahl der Zuweisungen die zugeteilte Menge übersteigt. Wenn totalAllokations den Wert grantedQuantity nicht überschreitet, ist dieser Wert null oder null. | Schreibgeschützt |
| localLicensingQuantity | Betrag dieser Ressource, der dieser Organisation für die Verwendung überlassen wurde, nachdem die den untergeordneten Elementen zugewiesene Menge abgezogen wurde. Dies ist der Betrag, der in der Admin Console als verfügbar angezeigt wird. Dieser Wert kann null sein, ist jedoch nie negativ, selbst wenn diese Organisation ihren untergeordneten Elementen Ressourcen überlastet hat. | Schreibgeschützt |
| localUsage | Anzahl der Einheiten der in dieser Organisation verwendeten Ressource. Wenn Sie beispielsweise eine Benutzerlizenz an einen Benutzer delegieren, zählt dies als eine Nutzungseinheit. | Schreibgeschützt |
| totalUsage | Anzahl der Einheiten der von dieser Organisation verwendeten Ressource und aller untergeordneten Elemente. Dies zeigt die Verwendung dieser Ressource in dem Teil der Organisationshierarchie, der auf dieser Organisation basiert. | Schreibgeschützt |
| useOverage | Betrag der gesamten Nutzung über die Gewährung der Organisation (Organisation und untergeordnete Elemente haben mehr der Ressource verwendet als verfügbar). Zeigt einen Wert ungleich null an, wenn „totalUsage“ die „localLicensingQuantity“ überschreitet. | Schreibgeschützt |
| allowOverAllocation | Gibt an, ob Benutzende Kindern mehr Ressourcen gewähren dürfen, obwohl keine weiteren Ressourcen zu gewähren sind (zulässig, trotz Gewährungsüberschuss). Dieser Wert gilt für alle Ressourcen dieses Produkts. Wenn versucht wird, die allowOverallocation für mehr als eine Ressource desselben Produkts auf verschiedene Werte zu aktualisieren, ist das Ergebnis zufällig. | Kann aktualisiert werden, wenn operation=update |
| isPurchasedProduct | „true“, wenn das Produkt ein Kaufprodukt ist (nicht von übergeordneter Seite zugeordnet). Dies entspricht sourceLicenseId mit einem leeren Wert. | Schreibgeschützt |
| neu verteilbar | „true“, wenn das Produkt untergeordneten Elementen zugewiesen werden kann. „false“ bedeutet, dass das Produkt nur in der Organisation verfügbar ist, in der es angezeigt wird, und dass Ressourcen nicht einer anderen Organisation zugewiesen werden können. | Schreibgeschützt |
| Betrieb | Leer, Erstellen, Aktualisieren oder Löschen. Beim Datenimport zu ergreifende Aktion |                                                          |


**Einfuhrbestimmungen**

**Datenvalidierung**

- Das Vorgangsfeld muss einen gültigen Vorgang haben.
- Die Produktimportdaten müssen über Eigenschaften und Werte für erforderliche Felder verfügen.
- Die Eigenschaften der Produktimportdaten müssen vom richtigen Typ sein.
- Das Produktrichtlinienfeld (overallocation) darf für verschiedene Ressourcen nicht angegeben werden.
- Das Feld grantedQuantity:
   - Kann nicht in &quot;*&quot; geändert werden* wenn es nicht bereits &quot;*&quot;*.
   - Muss eine nicht negative Ganzzahl oder der Zeichenfolgenwert (unlimited *sein*

**Berechtigungs-/barrierefreie Validierung**

- Die mit den Importdaten verknüpfte Organisation muss vorhanden sein. Stellen Sie bei einer Aktualisierung sicher, dass das mit den Importdaten verknüpfte Produkt und die Ressource tatsächlich vorhanden sind.

**Produktvalidierung hinzufügen**

- SourceLicenseId muss vorhanden sein.
- Die mit dem neuen Produkt verknüpfte Organisation muss vorhanden sein.
- Das erstellte Produkt darf nicht vorhanden sein (Produkt mit derselben Lizenz-ID).
- Die Ressourcen, die einem zu erstellenden Produkt zugeordnet sind, müssen über eine entsprechende productId verfügen, die mit diesem Produkt übereinstimmt.

