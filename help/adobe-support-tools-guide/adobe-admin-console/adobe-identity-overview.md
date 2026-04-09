---
title: Identitätsübersicht
description: Identitätstypen (Federated ID, Enterprise ID, Adobe ID und Personal Adobe ID) für Ihr Unternehmen verstehen und auswählen und den Benutzerzugriff in der Admin Console verwalten.
Feature-set: Experience Cloud Services
Solution: Admin Console
Feature: Admin Console
source-git-commit: c066e95c05f8e8a0953daecda9a220268d325f98
workflow-type: tm+mt
source-wordcount: '723'
ht-degree: 5%

---


# Identitätsübersicht

Gilt für Unternehmen und Teams.

Das Identitätsverwaltungssystem von Adobe hilft Admins beim Erstellen und Verwalten des Benutzerzugriffs auf Programme und Services. Adobe bietet diese Identitätstypen oder -konten an, um Benutzende zu authentifizieren und zu autorisieren.

## Identitätstypen in Adobe Admin Console

Identitätstypen ermöglichen dem Unternehmen verschiedene Ebenen der Kontrolle über die Konten und Daten der Benutzer. Die Auswahl des Identitätsmodells hat einen erheblichen Einfluss darauf, wie Assets in Ihrem Unternehmen gespeichert und freigegeben werden. Während Federated ID- und Enterprise ID-Modelle vom Unternehmen erstellt und verwaltet werden, werden Adobe-IDs vom Kontakt erstellt und verwaltet.

Die folgende Tabelle führt Sie bei der Auswahl des Identitätsmodells, das am besten zu Ihrer Organisation passt.

>[!NOTE]
>Wenn Ihr Unternehmen nicht auf das Unternehmensspeichermodell von Adobe aktualisiert wurde und Sie weiterhin Adobe-IDs für Einzelpersonen verwenden, lesen Sie die Beschreibung in der [Identitätstypen](https://helpx.adobe.com/de/enterprise/using/identity.html#using-personal-adobe-id) unten.

<table>
<thead>
<tr>
<th scope="col">Identitätstypen</th>

<th scope="col" style="text-align: center;">
  <img src="./assets/federated-id.png" alt="Federated ID-Symbol"><br>
  Federated ID
</th>
<th scope="col" style="text-align: center;">
  <img src="./assets/enterprise-id.png" alt="Enterprise ID"><br>
  Enterprise ID
</th>
<th scope="col" style="text-align: center;">
  <img src="./assets/adobe-id.png" alt="Adobe ID"><br>
  Adobe ID
</th>
</tr>
</thead>
<tbody>
<tr>
<th scope="row"><strong>Wichtige -Angebote</strong></th>
<td>Von der Organisation erstellt, verwaltet und in ihrem Besitz befindlich. Das Unternehmen verwaltet die Benutzeranmeldeinformationen und verwendet Single Sign-On (SSO) über einen SAML2 Identity Provider (IdP).</td>
<td>Von der Organisation erstellt, verwaltet und in ihrem Besitz befindlich. Das Unternehmen behält die exklusiven Rechte zum Erstellen von Benutzerkonten auf verifizierten Domains.</td>
<td>Wird vom Endbenutzer erstellt, erworben und verwaltet. Adobe führt die Authentifizierung durch, und der Endbenutzer verwaltet die Identität. Je nach <a href="https://helpx.adobe.com/de/enterprise/using/storage-for-business.html">Speichermodell</a> behalten Benutzer oder Unternehmen die Kontrolle über Dateien und Daten. Adobe ID-Konten werden auf nicht verifizierten, öffentlichen oder vertrauenswürdigen Domains erstellt. Siehe Nummer 2 des folgenden Anmerkungen.</td>
</tr>
<tr>
<th scope="row"><strong>Konto- und Dateneigentum</strong></th>
<td colspan="2">Eigentum und Kontrolle der Organisation</td>
<td>Unternehmen im Besitz für Unternehmensspeicher und Benutzer im Besitz für Benutzerspeicher</td>
</tr>
<tr>
<th scope="row"><strong>Sicherheit und Überwachung</strong></th>
<td colspan="2">
  <ul>
    <li>Auditprotokolle</li>
    <li>Inhaltsprotokolle</li>
    <li>Freigabebeschränkungen</li>
    <li>Authentifizierungseinstellungen des Unternehmens</li>
  </ul>
</td>

<td>
  <ul>
    <li>Inhaltsprotokolle</li>
    <li>Freigabebeschränkungen</li>
    <li>Passwortrichtlinie</li>
  </ul>
</td>

</tr>
<tr>
<th scope="row"><strong>Passwort zurücksetzen</strong></th>
<td colspan="2">Nicht unterstützt</td>
<td><a href="https://helpx.adobe.com/de/manage-account/using/change-or-reset-password.html">Passwort für das Konto zurücksetzen</a></td>
</tr>
<tr>
<th scope="row"><strong>Creative Cloud für Unternehmen und Document Cloud für Unternehmen</strong></th>
<td colspan="3">Unterstützt</td>
</tr>
<tr>
<th scope="row"><strong>Creative Cloud für Teams und Document Cloud für Teams</strong></th>
<td colspan="2">Nicht unterstützt</td>
<td>Unterstützt</td>
</tr>
<tr>
<th scope="row"><strong>Experience Cloud</strong></th>
<td colspan="3">Unterstützt</td>
</tr>
<tr>
<th scope="row"><strong>Empfohlen für</strong></th>
<td>
  <ul>
    <li>Organisationen, die bereits SSO oder SAML verwenden</li>
    <li>Bestehende Verzeichnisdienste (z. B. Google und Azure AD)</li>
    <li>Einfache Integration mit Services von Drittanbietern erfordern</li>
    <li>Kann den Besitz einer Domain nachweisen</li>
  </ul>
</td>
<td>
  <ul>
    <li>Kann den Besitz einer Domain nachweisen</li>
    <li>SSO nicht erforderlich</li>
  </ul>
</td>
<td>
  <ul>
    <li>Creative Cloud für Teams</li>
    <li>Das Unternehmen bevorzugt die Verwendung von Domains, deren Inhaber es nicht ist</li>
    <li>Öffentliche Domains (z. B. Hotmail, Gmail)</li>
    <li>Zugriff auf Apps wie Adobe Experience Manager Mobile</li>
  </ul>
</td>
</tr>
<tr>
<th scope="row"><strong>Erste Schritte</strong></th>
<td><a href="https://helpx.adobe.com/de/enterprise/using/set-up-identity.html">Einrichten der Identität</a></td>
<td><a href="https://helpx.adobe.com/de/enterprise/using/add-domains-directories.html#claim-domains">Domains beanspruchen</a></td>
<td><a href="https://helpx.adobe.com/de/enterprise/using/users.html#add-users">Benutzerin oder Benutzer hinzufügen</a></td>
</tr>
</tbody>
</table>

>[!NOTE]
>
>1. Die Passwortrichtlinie für Creative Cloud für Teams ist dieselbe wie für Creative Cloud für Einzelpersonen.
>1. Adobe ID-Benutzer authentifizieren sich mit ihren Adobe ID-Anmeldeinformationen oder durch das Authentifizierungsmodell ihres eigenen Unternehmens (SSO, 2FA usw.). In solchen Fällen werden Benutzer zur SSO-Seite der verantwortlichen Organisation weitergeleitet. Nach der Authentifizierung müssen Benutzende möglicherweise [ein Geschäftsprofil auswählen](https://helpx.adobe.com/de/enterprise/kb/enterprise-id-faq.html#choose-profile).

## Verwenden von Personal Adobe IDs

Adobe aktualisiert alle Teams und Unternehmenskunden auf das Enterprise-Speichermodell von Adobe. In der folgenden Tabelle finden Sie Informationen dazu, ob Ihr Unternehmen über Benutzende verfügt, die persönliche Adobe-IDs verwenden, um auf Adobe-Apps und -Services ihres Unternehmens oder ihrer Schule zuzugreifen.

### Personal Adobe ID

<table>
<thead>
<tr>
<th scope="col">Identitätstyp</th>
</th>
<th scope="col" style="text-align: center;">
  <img src="./assets/personal-adobe-id.png" alt="Adobe ID"><br>
  Personal Adobe ID
</th>
</tr>
</thead>
<tbody>
<tr>
<th scope="row"><strong>Wichtige -Angebote</strong></th>
<td>Wird vom Endbenutzer erstellt, erworben und verwaltet. Adobe führt die Authentifizierung durch, und der Endbenutzer verwaltet die Identität.</td>
</tr>
<tr>
<th scope="row"><strong>Konto- und Dateneigentum</strong></th>
<td>benutzergesteuert</td>
</tr>
<tr>
<th scope="row"><strong>Sicherheit und Überwachung</strong></th>
<td>Passwortrichtlinie. Siehe Nummer 1 im folgenden Abschnitt.</td>
</tr>
<tr>
<th scope="row"><strong>Passwort zurücksetzen</strong></th>
<td><a href="https://helpx.adobe.com/de/manage-account/using/change-or-reset-password.html">Setzen Sie Ihr Kontokennwort zurück.</a> Siehe Nummer 2 im folgenden Abschnitt.</td>
</tr>
<tr>
<th scope="row"><strong>Creative Cloud für Unternehmen und Document Cloud für Unternehmen</strong></th>
<td>Unterstützt</td>
</tr>
<tr>
<th scope="row"><strong>Experience Cloud</strong></th>
<td>Unterstützt</td>
</tr>
<tr>
<th scope="row"><strong>Nur für verfügbar/Empfohlen für</strong></th>
<td>
  <ul>
    <li>Vor der Migration Onboarding von Unternehmens- und Unternehmensteams</li>
    <li>Creative Cloud für Teams</li>
    <li>Ich möchte Kontrolle in der Hand des Benutzers</li>
    <li>Zugriff auf Apps wie Digital Publishing Suite</li>
    <li>Benutzer besitzen Assets nach der Trennung von der Organisation</li>
  </ul>
</td>
</tr>
<tr>
<th scope="row"><strong>Erste Schritte</strong></th>
<td><a href="https://helpx.adobe.com/de/enterprise/using/users.html#add-users">Benutzerin oder Benutzer hinzufügen</a></td>
</tr>
</tbody>
</table>

>[!NOTE]
>
>1. Die Passwortrichtlinie für Creative Cloud für Teams ist dieselbe wie für Creative Cloud für Einzelpersonen.
>1. Bei Creative Cloud für Unternehmenskunden, die [Unternehmensspeicher](https://helpx.adobe.com/de/enterprise/using/manage-adobe-storage.html) verwenden, können Administratoren Adobe ID-Benutzer zur Admin Console hinzufügen, sie jedoch nicht zu Produktprofilen hinzufügen. Administratoren müssen Adobe ID-Benutzer zu einem anderen Identitätstyp migrieren.
>1. Es gibt einige Produkte und Services, z. B. die **Adobe-Lizenzierungs-Website, die nur Adobe ID**.

## Ähnliche Themen

- [Identität einrichten](https://helpx.adobe.com/de/enterprise/using/set-up-identity.html)
- [Benutzeridentität wechseln](https://helpx.adobe.com/de/enterprise/using/switch-user-identity.html)
- [Übersicht über Admin Console](https://helpx.adobe.com/enterprise/using/admin-console-overview.html)
- [Häufig gestellte Fragen zu Schulungen](https://helpx.adobe.com/enterprise/using/education-faq.html)
- [Benutzer hinzufügen und verwalten](https://helpx.adobe.com/de/enterprise/using/users.html)