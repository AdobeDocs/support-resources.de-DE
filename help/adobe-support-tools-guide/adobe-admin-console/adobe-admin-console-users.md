---
title: Adobe Admin Console-Benutzer
description: Planen Sie Ihre Strategie für die Benutzerverwaltung in Adobe Admin Console - fügen Sie Administratoren und Endbenutzer hinzu, wählen Sie eine Benutzerverwaltungsmethode aus und weisen Sie Lizenzen zu.
feature-set: Experience Cloud Services
solution: Admin Console
feature: Admin Console
source-git-commit: d92f4190b68a480409f4126a877de3469ed836f0
workflow-type: tm+mt
source-wordcount: '842'
ht-degree: 4%

---

# Adobe Admin Console-Benutzer

Gilt für Unternehmen und Teams.

Mit einem dieser Probleme konfrontiert? Wählen Sie ein Problem aus, um die Lösung anzuzeigen.

- [Verwalten von Administratorrollen](https://helpx.adobe.com/de/enterprise/using/admin-roles.html)
- [Probleme beim Herunterladen und Installieren](https://helpx.adobe.com/de/download-install.html)
- [Enterprise ID-Benutzerkennwort zurücksetzen](https://helpx.adobe.com/de/enterprise/kb/enterprise-id-faq.html#faq)
- [Beheben von Federated ID-Fehlern](https://helpx.adobe.com/de/enterprise/kb/tshoot-fed-id.html)
- [Benutzer löschen oder gelöschten Benutzer wiederherstellen](https://helpx.adobe.com/de/enterprise/using/manage-directory-users.html)

**Adobe Admin Console - Benutzer** — [Auf YouTube ansehen](https://youtu.be/w8b36YX2TEM)

## Gründe für das Hinzufügen von Benutzern zu Adobe Admin Console

>[!NOTE]
>
>Nachdem Sie als Administrator auf der Adobe Admin Console Ihren [Identitätstyp](https://helpx.adobe.com/de/enterprise/using/identity.html) und [Identität einrichten](https://helpx.adobe.com/de/enterprise/using/set-up-identity.html) ausgewählt haben, besteht Ihre nächste Aufgabe darin, Benutzer zur Admin Console hinzuzufügen.

Adobe Enterprise und Teams definieren im Großen und Ganzen zwei Benutzertypen:

### Administratoren (Administratoren)

Unternehmens- oder Team-Administratoren führen administrative Aufgaben für die Admin Console durch. Sie können Administratoren hinzufügen, um eine flexible Verwaltungshierarchie zu definieren, die eine differenzierte Verwaltung des Zugriffs, der Verwendung und anderer Verwaltungsaufgaben von Adobe-Produkten ermöglicht.

Alle Administratoren müssen der Admin Console hinzugefügt werden. Beim Hinzufügen dieser Berechtigungen basieren die Administratorrechte auf ihren [Administratorrollen](https://helpx.adobe.com/de/enterprise/using/admin-roles.html).

### Endbenutzer

Endbenutzer sind die Benutzer in Ihrem Unternehmen oder Ihrer Institution, die die Adobe-Produkte und -Services nutzen, die Ihr Unternehmen oder Ihre Institution im Rahmen der Vereinbarung mit Adobe erhalten hat.

## Festlegen einer Benutzerverwaltungsstrategie

Je nach Ihren Anforderungen können Sie Benutzer hinzufügen, entfernen oder aktualisieren *einzeln* oder eine der verfügbaren *Massen-Upload-Methoden*. Verwenden Sie die folgende Matrix als Anleitung zur Planung Ihrer Benutzerverwaltung.

>[!NOTE]
>
>Wenn Sie neu bei Adobe Enterprise oder Teams sind, empfehlen wir, diese Tabelle durchzugehen, bevor Sie mit der Benutzerverwaltung in Admin Console beginnen. Bestehende Kundinnen und Kunden können dies verwenden, insbesondere wenn sie planen, von einem Identitätstyp zu einem anderen zu migrieren (siehe [Identitätstyp bearbeiten](https://helpx.adobe.com/de/enterprise/using/switch-user-identity.html)).

<table>
<thead>
<tr>
<th scope="col"></th>
<th scope="col"><strong>Individuell (Admin Console)</strong></th>
<th scope="col"><strong>CSV-Massen-Upload (Admin Console)</strong></th>
<th scope="col"><strong>Azure-/Google-Connectoren</strong></th>
<th scope="col"><strong>Tool zur Benutzersynchronisierung</strong></th>
<th scope="col"><strong>User Management-REST-API</strong></th>
</tr>
</thead>
<tbody>
<tr>
<th scope="row"><strong>Gilt für</strong></th>
<td colspan="2">Adobe-Teams und Unternehmenskunden</td>
<td colspan="3">Adobe Enterprise-Kunden</td>
</tr>
<tr>
<th scope="row"><strong>Beschreibung</strong></th>
<td>Verwalten Sie Benutzende einzeln in der Admin Console.</td>
<td>Verwalten Sie Benutzende mit CSV-Datei, die in die Admin Console hochgeladen wurde.</td>
<td>Verwalten Sie Benutzer (und Gruppen) basierend auf Ihrem bestehenden Azure AD-Portal oder Google-Verbund.</td>
<td colspan="2">Verwalten Sie Benutzer (und Gruppen) basierend auf dem LDAP Ihres Unternehmens.</td>
</tr>
<tr>
<th scope="row"><strong>Benutzer hinzufügen</strong></th>
<td>Registerkarte <strong>Benutzer</strong> in <strong>Admin Console</strong>. <a href="https://helpx.adobe.com/de/enterprise/using/manage-users-individually.html#add-users">Weitere Informationen</a>.</td>
<td>Verwenden Sie <strong>Benutzer nach CSV hinzufügen</strong> in <strong>Admin Console</strong>. <a href="https://helpx.adobe.com/de/enterprise/using/bulk-upload-users.html">Weitere Informationen</a>. <em>(Standard-CSV-Vorlage verwenden.)</em></td>
<td>Benutzer in <a href="https://helpx.adobe.com/de/enterprise/using/sso-setup-azure.html">Azure</a> oder <a href="https://helpx.adobe.com/de/enterprise/using/setup-sso-google.html">Google </a>. Oder über <strong>Admin Console</strong>.</td>
<td colspan="2">Benutzer sollten zum LDAP Ihres Unternehmens hinzugefügt werden.</td>
</tr>
<tr>
<th scope="row"><strong>Benutzer entfernen</strong></th>
<td>Benutzer in <strong>Admin Console auswählen und </strong>. <a href="https://helpx.adobe.com/de/enterprise/using/manage-users-individually.html#remove-users">Weitere Informationen</a>.</td>
<td>Wählen Sie <strong>Benutzer durch CSV entfernen</strong> auf der Registerkarte <strong>Benutzer</strong> von <strong>Admin Console</strong>. <a href="https://helpx.adobe.com/de/enterprise/using/bulk-upload-users.html#remove-users">Weitere Informationen</a>. <em>(Standard-CSV-Vorlage verwenden.)</em></td>
<td>Benutzende müssen in <a href="https://helpx.adobe.com/de/enterprise/using/sso-setup-azure.html">Azure</a> oder <a href="https://helpx.adobe.com/de/enterprise/using/setup-sso-google.html">Google entfernt </a>.</td>
<td colspan="2">Stellen Sie sicher, dass die Benutzerinformationen synchronisiert sind. <strong>Achtung:</strong> Benutzer, die nicht im LDAP Ihres Unternehmens sind, werden aus Admin Console entfernt.</td>
</tr>
<tr>
<th scope="row"><strong>Benutzerdetails bearbeiten</strong></th>
<td>Wählen Sie den Benutzer und dann <strong>Benutzerdetails bearbeiten</strong> in Admin Console aus. <a href="https://helpx.adobe.com/de/enterprise/using/manage-users-individually.html#edit-user-details">Weitere Informationen</a>.</td>
<td>Wählen Sie <strong>Benutzerdetails nach CSV bearbeiten</strong> auf der Registerkarte <strong>Benutzer</strong> von <strong>Admin Console</strong>. <a href="https://helpx.adobe.com/de/enterprise/using/bulk-upload-users.html#edit-user-details">Weitere Informationen</a>. <em>(Standard-CSV-Vorlage verwenden.)</em></td>
<td>Alle Benutzerinformationen müssen in <a href="https://helpx.adobe.com/de/enterprise/using/sso-setup-azure.html">Azure</a> oder <a href="https://helpx.adobe.com/de/enterprise/using/setup-sso-google.html">Google geändert </a>.</td>
<td colspan="2">Stellen Sie sicher, dass die Benutzerinformationen synchronisiert sind.</td>
</tr>
<tr>
<th scope="row"><strong>Unterstützte Identitätstypen</strong></th>
<td colspan="2">Alle</td>
<td>Federated ID</td>
<td colspan="2">Federated ID und Enterprise ID</td>
</tr>
<tr>
<th scope="row"><strong>Max. Updates pro Vorgang</strong></th>
<td>10</td>
<td>25.000 (<em>5.000 für optimale Leistung</em>)</td>
<td colspan="3">Unbegrenzt (Zuordnung zum LDAP Ihrer Organisation)</td>
</tr>
<tr>
<th scope="row"><strong>Erfordert</strong></th>
<td>Adobe Admin Console</td>
<td>Erstellen und Aktualisieren von CSV-Dateiformaten, vorzugsweise mit Microsoft Excel</td>
<td>Sie müssen einen Azure AD- oder Google-Verbund einrichten</td>

<td>
  <ul>
    <li>macOS Terminal oder Windows-Eingabeaufforderung</li>
    <li>Grundlagen zu LDAP</li>
  </ul>
</td>

<td>Grundkenntnisse einer Programmiersprache (wie Python) zur Verwendung von REST-APIs</td>
</tr>
<tr>
<th scope="row"><strong>Mehr dazu</strong></th>
<td><a href="https://helpx.adobe.com/de/enterprise/using/manage-users-individually.html">Verwalten einzelner Benutzer</a></td>

<td>
  <ul>
    <li>
      <a href="https://helpx.adobe.com/de/enterprise/using/bulk-upload-users.html">
        Benutzer verwalten | CSV-Massenupload
      </a>
    </li>
    <li>
      <a href="https://helpx.adobe.com/de/enterprise/kb/troubleshoot-bulk-user-csv-upload.html">
        Fehlerbehebung beim Massen-Benutzer-CSV-Upload
      </a>
    </li>
  </ul>
</td>

<td>
  <ul>
    <li>
      <a href="https://helpx.adobe.com/de/enterprise/using/sso-setup-azure.html">
        Azure AD-Connector
      </a>
    </li>
    <li>
      <a href="https://helpx.adobe.com/de/enterprise/using/setup-sso-google.html">
        Google Federation-Connector
      </a>
    </li>
  </ul>
</td>

<td>
  <ul>
    <li>
      <a href="https://adobe-apiplatform.github.io/user-sync.py/en/">
        Über die Benutzersynchronisierung
      </a>
    </li>
    <li>
      <a href="https://github.com/adobe-apiplatform/user-sync.py">
        Git-Repository
      </a>
    </li>
    <li>
      <a href="https://helpx.adobe.com/de/enterprise/using/user-sync.html">
        Schrittweise Anleitung
      </a>
    </li>
  </ul>
</td>
<td><a href="https://developer.adobe.com/umapi/">Über UMAPI</a></td>
</tr>
</tbody>
</table>

## Nächste Schritte

### Erstellen von Paketen

Nach dem Hinzufügen können Ihren Benutzern die ihnen zugewiesenen Apps und Services zugewiesen werden.

Weisen Sie Endbenutzern Lizenzen basierend auf Ihrer Lizenzierungsmethode zu:

- **Spezifische Benutzerlizenzierung:** Fügen Sie diese Benutzer zu **Produkten** ([für Teams](https://helpx.adobe.com/de/enterprise/using/assign-licenses-to-teams-users.html)) oder **Produktprofilen** ([für Unternehmen](https://helpx.adobe.com/de/enterprise/using/manage-product-profiles.html)) hinzu, um ihnen Berechtigungen für Adobe-Produkte und -Services zu erteilen. Weitere Informationen finden Sie unter [&#x200B; von benannten Benutzerlizenzierungspaketen &#x200B;](https://helpx.adobe.com/de/enterprise/using/create-nul-packages.html) &quot;[&quot; &#x200B;](https://helpx.adobe.com/de/enterprise/using/manage-product-profiles.html#create-product-profile).
- **Lizenzierung freigegebener Geräte:** [Hinzugefügte Benutzer](https://helpx.adobe.com/de/enterprise/using/sdl-deployment-guide.html#add-users-admin-console) können die konfigurierten freigegebenen Geräte verwenden, auf die nur Benutzer **Organisation) zugreifen**. Weitere Informationen finden Sie unter [Erstellen von SDL-Paketen](https://helpx.adobe.com/de/enterprise/using/create-sdl-packages.html).

### Bereitstellen von Paketen

Nachdem Sie das Paket erstellt haben, stellen Sie es mit einer der folgenden Methoden auf Ihren Client-Computern bereit:

- Doppelklicken Sie auf dem Client-Computer auf die Paketdatei (Windows oder macOS).
- Verwenden Sie die Windows-Eingabeaufforderung oder das macOS-Terminal.
- Verwenden Sie Tools von Drittanbietern:
   - [Microsoft Intune](https://helpx.adobe.com/de/enterprise/kb/deploy-packages-using-ms-intune.html)
   - [Microsoft System Center Configuration Manager (SCCM)](https://helpx.adobe.com/de/enterprise/kb/deploy-packages-using-sccm.html)
   - [Apple Remote Desktop (ARD)](https://helpx.adobe.com/de/enterprise/kb/deploy-packages-using-ard.html)
   - [JAMF Pro](https://helpx.adobe.com/de/enterprise/kb/deploy-packages-using-jamf-pro.html)
   - [Munki](https://helpx.adobe.com/de/enterprise/kb/deploy-packages-using-munki.html)

## Verwandtes Lesen

- [Benutzer verwalten | Individuell](https://helpx.adobe.com/de/enterprise/using/manage-users-individually.html)
- [Benutzer verwalten | CSV-Massen-Upload](https://helpx.adobe.com/de/enterprise/using/bulk-upload-users.html)
- [Verzeichnisbenutzer verwalten](https://helpx.adobe.com/de/enterprise/using/manage-directory-users.html)
- [Admin Console](https://helpx.adobe.com/de/enterprise/using/admin-console.html)
- [Zuweisen von Benutzern zu Produktprofilen (für Unternehmen und Institutionen)](https://helpx.adobe.com/de/enterprise/using/manage-product-profiles.html#assign-users)
- [Lizenzen Team-Benutzern zuweisen](https://helpx.adobe.com/de/enterprise/using/assign-licenses-to-teams-users.html)
- [Geschäftsspeichermodell](https://helpx.adobe.com/de/enterprise/kb/business-storage-model-introduction.html)