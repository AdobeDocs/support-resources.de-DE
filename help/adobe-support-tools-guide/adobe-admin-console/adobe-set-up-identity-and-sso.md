---
title: Einrichten von Identität und Single Sign-on
description: Erfahren Sie, wie Systemadministratoren von Unternehmen Benutzeridentitäten und Single Sign-on (SSO) in der Adobe Admin Console mithilfe von Adobe ID, Enterprise ID oder Federated ID einrichten können.
feature-set: Experience Cloud Services
solution: Admin Console
feature: Admin Console
source-git-commit: 0c2992946f1cdbbcfb44a2baf37888bd05b2253b
workflow-type: tm+mt
source-wordcount: '870'
ht-degree: 1%

---

# Einrichten von Identität und Single Sign-on

**Gilt für:** Enterprise

Erfahren Sie, wie Sie in der Adobe Admin Console eine Identität einrichten. Vergleichen Sie Adobe ID, Enterprise ID und Federated ID und konfigurieren Sie Single Sign-On (SSO) für einen sicheren Zugriff auf Adobe-Apps.

Konfigurieren Sie die Identität und richten Sie Single Sign-On (SSO) ein, damit sich [&#x200B; Mitarbeiter mit &#x200B;](https://adminconsole.adobe.com/settings/) Unternehmensanmeldedaten anmelden können.

Im Folgenden finden Sie das Video-Tutorial zum Einrichten [Identity and SSO (YouTube)](https://youtu.be/V57lU4zaSBs).

## Schlüsselbegriffe und Konzepte

### Verzeichnis

Ein Verzeichnis in der Admin Console ist eine Entität, die Ressourcen wie Benutzende und Richtlinien wie Authentifizierung enthält. Diese Verzeichnisse ähneln LDAP oder Active Directories.

### Identitätsanbieter (IdP)

Ein Identitätsanbieter (IdP) ist der Identitätsanbieter Ihres Unternehmens, z. B.:

- Active Directory
- Microsoft Azure
- Ping
- Okta
- Gemeinsam
- Shibboleth

### Beteiligte Rollen

| Rolle | Verantwortlichkeit |
|------|----------------|
| Systemadministrator | Arbeitet mit IdP-Verzeichnis-Managern und DNS-Managern zusammen, um Identitäten in der Admin Console einzurichten. |
| DNS-Manager | Aktualisiert DNS-Token zur Validierung des Domain-Besitzes. |
| Identity Provider-Ordner-Manager (IdP) | Verarbeitet das IdP-Portal und die zugehörigen Connectoren. |

### Adobe ID

Wird vom Endbenutzer erstellt, erworben und verwaltet. Adobe führt die Authentifizierung durch, und der Endbenutzer verwaltet die Identität. Je nach [Speichermodell](https://helpx.adobe.com/de/enterprise/using/storage-for-business.html) behalten Benutzer oder Unternehmen die Kontrolle über Dateien und Daten.

Für Organisationen, die auf das Speichermodell des Unternehmens aktualisiert wurden, werden Assets und Daten von der Organisation gesteuert. Für Organisationen, die nicht aktualisiert wurden, ist die Person für Adobe ID-Assets verantwortlich und kontrolliert diese.

### Enterprise ID

Wird von einer Organisation erstellt, verwaltet und befindet sich im Besitz einer Organisation. Adobe hostet die Enterprise ID und führt die Authentifizierung durch, das Unternehmen verwaltet jedoch die Enterprise ID. Administratoren erstellen eine Enterprise ID und stellen sie einem Benutzer aus. Administratoren können den Zugriff auf Produkte und Services sperren, indem sie das Konto übernehmen oder die Enterprise ID löschen, um den Zugriff auf zugehörige Daten dauerhaft zu blockieren. Um mehr zu erfahren, klicken Sie [hier](https://helpx.adobe.com/de/enterprise/using/setup-enterprise-id.html).

### Federated ID

Wird von einer Organisation erstellt und ist im Besitz dieser Organisation und über einen Verbund mit dem Unternehmensverzeichnis verknüpft. Das Unternehmen verwaltet Anmeldeinformationen und verarbeitet Single Sign-On über einen SAML2 Identity Provider (IdP).

Im Folgenden finden Sie einige Anforderungen und Szenarien, in denen Federated IDs empfohlen werden:

- Wenn Sie Benutzer basierend auf dem Unternehmensverzeichnis Ihrer Organisation bereitstellen möchten.
- Wenn Sie die Benutzerauthentifizierung verwalten möchten.
- Wenn Sie eine strikte Kontrolle über Apps und Services behalten müssen, die einem Benutzer zur Verfügung stehen.

## Einrichten der Identität ohne einmaliges Anmelden

Sie können Adobe ID oder Enterprise ID verwenden, wenn Ihr Unternehmen SSO derzeit nicht in anderen Programmen verwendet.

## Verwenden von Adobe ID

Adobe aktualisiert alle Unternehmen auf das [Speichermodell für Unternehmen](https://helpx.adobe.com/de/enterprise/using/storage-for-business.html). Dadurch erhält Ihr Unternehmen mehr Kontrolle über die Assets und Daten Ihrer Benutzer.

Erste Schritte mit dem [Hinzufügen von Benutzern](https://helpx.adobe.com/de/enterprise/using/users.html) zur Admin Console.

## Einrichten von Identitäten mit Enterprise ID

Sie können ein Enterprise ID-Verzeichnis einrichten, wenn Sie ohne SSO mehr Kontrolle über die Daten Ihrer Benutzer haben möchten. Nur Administratoren erstellen eine Enterprise ID und stellen sie einem Benutzer aus.

Unter [Einrichten einer Organisation mit Enterprise ID](https://helpx.adobe.com/de/enterprise/using/setup-enterprise-id.html) finden Sie die Anforderungen und Schritte zum Erstellen von Enterprise ID-Verzeichnissen.

## Einrichten der Identität mit Single Sign-on

Sie müssen die Benutzeridentität mit Federated ID-Konten einrichten, um SSO verwenden zu können.

Federated IDs werden empfohlen, wenn:

- Sie müssen die einem Benutzer zur Verfügung stehenden Apps und Dienste streng kontrollieren.
- Sie die Benutzerauthentifizierung verwalten möchten.
- Sie möchten Benutzer basierend auf dem Unternehmensverzeichnis Ihrer Organisation bereitstellen.

## Einrichten einer neuen SSO-Integration

Sie können gängige Identitätsanbieter wie Microsoft Azure AD, Google oder andere SAML-basierte IDs verwenden, um SSO zwischen Ihrem Unternehmen und Adobe-Produkten einzurichten.

**Azure AD** (empfohlen) - [Einrichten von SSO und Benutzersynchronisierung mit dem Azure AD-Connector](https://helpx.adobe.com/de/enterprise/using/sso-setup-azure.html)

**Other SAML IdP** - [Einrichten von SSO mit anderen SAML-Anbietern](https://helpx.adobe.com/de/enterprise/using/create-directory.html)

**Google** (empfohlen) - [Einrichten von SSO und Benutzersynchronisierung mit dem Google-Connector](https://helpx.adobe.com/de/enterprise/using/setup-sso-google.html)

## Vorhandenes SSO-Setup verwalten

Nachdem SSO zwischen Ihrem Unternehmen und Adobe eingerichtet wurde, können Sie das Setup wie folgt verwalten und ändern.

Erfahren Sie, wie Sie Ihre Domains und Verzeichnisse verwalten:

- [Verwalten von &#x200B;](https://helpx.adobe.com/de/enterprise/using/users.html) und [Gruppen](https://helpx.adobe.com/enterprise/using/user-groups..HTML)
- [Verknüpfen von Domains mit &#x200B;](https://helpx.adobe.com/de/enterprise/using/add-domains-directories.html#link-domains-to-directoies), um den Benutzerzugriff auf Apps, Services und Einstellungen zu steuern
- [Verzeichnisvertrauen verwalten](https://helpx.adobe.com/de/enterprise/using/directory-trust.html) um Domains zu verwenden, die von einer anderen Organisation beansprucht werden

Erfahren Sie, wie Sie Ihren Identitätsanbieter ändern:

- [Ändern des &#x200B;](https://helpx.adobe.com/de/enterprise/using/migrate-authentication-provider.html), ohne die Arbeit der Benutzer zu stören
- [Verschieben von Domains über Verzeichnisse hinweg](https://helpx.adobe.com/de/enterprise/using/manage-domains-directories.html#move-domains-across-directories)
- [Ältere Verzeichnisbenutzer entfernen](https://helpx.adobe.com/de/enterprise/using/manage-directory-users.html)
- [Löschen alter/nicht beanspruchter Domains und leerer Ordner](https://helpx.adobe.com/de/enterprise/using/manage-domains-directories.html#delete)

## Fehler und häufige Fragen

Lösungen für häufige Fragen und Fehler beim Einrichten und Verwalten von SSO:

### Azure AD - Häufig gestellte Fragen und Fehlerbehebung

#### Häufig gestellte Fragen (FAQ)

- [Häufig gestellte Fragen zum Azure AD-Connector](https://helpx.adobe.com/de/enterprise/using/azure-ad-connector-faq.html)
- [Löschen von Verzeichnissen und Domains](https://helpx.adobe.com/de/enterprise/using/sso-setup-azure.html#Deletedirectoriesandremovedomains)

#### Fehlerbehebung

- [Benutzern wurde der Zugriff verweigert](https://helpx.adobe.com/de/enterprise/using/sso-setup-azure.html#sync-issues)
- [Synchronisierungsprobleme](https://helpx.adobe.com/de/enterprise/using/sso-setup-azure.html#sync-issues)

### Andere SAML-IDs - Häufig gestellte Fragen und Fehlerbehebung

#### Häufig gestellte Fragen (FAQ)

[Häufig gestellte Fragen zur SAML-Integration](https://helpx.adobe.com/de/enterprise/using/sso-faq.html)

#### Fehlerbehebung

- [Allgemeine SSO-](https://helpx.adobe.com/de/enterprise/kb/tshoot-fed-id.html)
- [&#x200B; Fehler „Zugriff verweigert“](https://helpx.adobe.com/de/enterprise/kb/tshoot-fed-id.html#Error_Access_Denied_logging_in)
- [&#x200B; Fehler „Ein anderer Benutzer ist derzeit angemeldet“](https://helpx.adobe.com/de/enterprise/kb/tshoot-fed-id.html#ErrorAnotheruseriscurrentlyloggedin)
- [Durchführen einer SAML-Verfolgung](https://helpx.adobe.com/de/enterprise/kb/perform-a-saml-trace.html)

### Google - Häufig gestellte Fragen

- [Häufig gestellte Fragen zum Google-Connector](https://helpx.adobe.com/de/enterprise/using/google-federation-faq.html)
- [Löschen von Verzeichnissen und Domains](https://helpx.adobe.com/de/enterprise/using/setup-sso-google.html#Deletedirectoriesandremovedomains)

## Reden Sie mit

Um mit anderen Administratoren zusammenzuarbeiten, Fragen zu stellen und mit ihnen zu chatten, verwenden Sie die [Enterprise und Teams Community](https://www.adobe.com/go/entcom_de).

## Rechtliche Hinweise und Datenschutz

- [Rechtliche Hinweise](https://helpx.adobe.com/de/legal/legal-notices.html)
- [Online-Datenschutzrichtlinie](https://www.adobe.com/de/privacy.html)
