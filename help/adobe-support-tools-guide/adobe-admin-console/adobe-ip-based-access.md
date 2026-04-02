---
title: Produktzugriff nach IP-Adressen einschränken
description: Verwenden Sie den IP-basierten Zugriff, um den Benutzerzugriff auf Adobe-Produkte zu steuern und die Verwendung auf genehmigte öffentliche IP-Bereiche zu beschränken.
feature-set: Experience Cloud Services
solution: Admin Console
feature: Admin Console
source-git-commit: 879a936ea110084c03df6003494f88831561d3c2
workflow-type: tm+mt
source-wordcount: '482'
ht-degree: 1%

---


# Produktzugriff nach IP-Adressen einschränken

Gilt für Unternehmen.

Verwenden Sie den IP-basierten Zugriff, um den Zugriff Ihrer Benutzer auf Adobe-Produkte zu steuern und eine unbefugte Verwendung von nicht aufgelisteten öffentlichen IP-Adressen zu verhindern.

Wechseln Sie zu [Admin Console](https://adminconsole.adobe.com/settings/identity), um der Adobes **IP-basierter Zugriff** vertrauenswürdige öffentliche IP-Adressen für die sichere Verwendung von auf die Zulassungsliste setzen-Anwendungen und -Services hinzuzufügen.

## Vorteile des IP-basierten Zugriffs

Die IP-basierte Zugriffssteuerung verwendet eine IP-Adresse, um die Verwendung von Adobe-Produkten von zufälligen öffentlichen IP-Adressen zu beschränken. Der IP-basierte Zugriff gilt für alle Ordner und die zugehörigen Produkte in Ihrer Adobe Admin Console.

Sie können der Liste **Zulässige IP-Adressen** vertrauenswürdige öffentliche IPs hinzufügen, um Benutzer daran zu hindern,

- Zugriff auf Produkte von öffentlichen IPs außerhalb der zulässigen IP-Bereiche
- Anmeldung bei Adobe [Benutzerprofilen](https://helpx.adobe.com/de/enterprise/using/manage-adobe-profiles.html) von öffentlichen IPs außerhalb der zulässigen IP-Bereiche
- Benutzerprofile in Web-Apps außerhalb der zulässigen IP-Bereiche wechseln

  ![Organisationsstruktur exportieren](./assets/ip-based-access.avif)

## IP-basierten Zugriff aktivieren

### Wichtige Überlegungen

>[ !IWichtige Überlegungen]
>
>- Administratoren müssen zunächst ihre eigene öffentliche IP-Adresse hinzufügen und erst dann andere IP-Bereiche hinzufügen. Andernfalls kann ein Fehler auftreten.
>- Der IP-basierte Zugriff gilt nicht für private IP-Adressen.

Sie können bis zu 150 verschiedene öffentliche IP-Bereiche nur im CIDR-Format hinzufügen.

Führen Sie die folgenden Schritte aus, um den IP-basierten Zugriff in Ihrer Adobe Admin Console zu aktivieren:

1. Wechseln Sie zum Abschnitt **[[!UICONTROL Adobe Admin Console-]](https://adminconsole.adobe.com/settings/identity)**.
2. Wählen und erweitern Sie **[!UICONTROL Datenschutz und Sicherheit]** im Auswahlmenü und klicken Sie dann auf **[!UICONTROL Authentifizierungseinstellungen]**.
3. Klicken Sie im Abschnitt **[!UICONTROL IP-basierter Zugriff]** auf die Schaltfläche **[!UICONTROL IP-Adresse hinzufügen]**.
4. Im Fenster **[!UICONTROL IP-Adresse hinzufügen]**:
   - Geben Sie die öffentlichen IP-Adressen oder den CIDR-Block ein, der Ihrer Zulassungsliste hinzugefügt werden soll.
   - Mehrere IP-Adressen mit Kommas trennen.
   - Wählen Sie **[!UICONTROL Speichern]** aus.

   Derzeit wird nur das IPv4-Format unterstützt. Im Folgenden finden Sie einige Beispiele:
   - IP v4-Adresse: 1.3.4.6
   - IP v4-Subnetzadresse: 1.2.0.0/24

Ihre IP-Adressen werden innerhalb weniger Minuten hinzugefügt. Zugewiesene Benutzer sehen die Einschränkung, wenn sie das nächste Mal versuchen, sich anzumelden oder Profile außerhalb der zulässigen öffentlichen IP-Adressen zu wechseln. Es wird empfohlen, die Benutzer vorab über diese Änderung zu informieren.

Sie können jede aufgelistete IP-Adresse bearbeiten oder entfernen, indem Sie die Optionen Bearbeiten oder Löschen neben jedem Eintrag auswählen.

>[!NOTE]
>
>- Wenn der IP-basierte Zugriff aktiviert ist, **keine erzwungene Abmeldung**. Benutzer sind nur betroffen, wenn sie versuchen, beim Anmelden oder beim Wechsel des Profils im Web das eingeschränkte Profil auszuwählen.
>- Wenn Sie ein gesichertes Web-Gateway verwenden, stellen Sie sicher, dass der gesamte Traffic durch dieses geleitet wird. Anzeigen der [Liste der zuzulassen](https://helpx.adobe.com/de/enterprise/kb/network-endpoints.html) damit Adobe-Programme und -Services ordnungsgemäß funktionieren.
>- Wenn Sie von der Admin Console gesperrt wurden, weil Sie eine ungültige IP-Adresse eingegeben haben, wenden Sie sich an die [Adobe-Kundenunterstützung](https://helpx.adobe.com/de/enterprise/using/support-for-enterprise.html).

## Reden Sie mit

Um mit anderen Administratoren zusammenzuarbeiten, Fragen zu stellen und mit ihnen zu chatten, besuchen Sie unsere [Enterprise and Teams Community](https://www.adobe.com/go/entcom_de).
