---
title: Zuweisen von Produkten zu untergeordneten Organisationen mithilfe der Global Admin Console
description: Erfahren Sie, wie globale Administratoren Ressourcen an untergeordnete Organisationen verteilen können, um eine effektive Ressourcenverwaltung und Benutzerzuweisung innerhalb jeder Organisation zu ermöglichen.
Feature-set: Experience Cloud Services
Solution: Admin Console
Feature: Admin Console
source-git-commit: 943ddbe1e049e77d502e2da393f7588b10a7a58b
workflow-type: tm+mt
source-wordcount: '1050'
ht-degree: 0%

---

# Zuweisen von Produkten zu untergeordneten Organisationen mithilfe der Global Admin Console

Gilt für Unternehmen.

Erfahren Sie, wie globale Administratoren Ressourcen an untergeordnete Organisationen verteilen können, um eine effektive Ressourcenverwaltung und Benutzerzuweisung innerhalb jeder Organisation zu ermöglichen.

Wechseln Sie in der [Global Admin Console](https://helpx.adobe.com/enterprise/global-admin-console/adopt-global-administration.html) zur Registerkarte **[!UICONTROL Produktzuordnung]** und wählen Sie ein Produkt aus, das untergeordneten Organisationen zugeordnet werden soll.

Melden Sie sich bei der [Global Admin Console](https://adminconsole.adobe.com/support) an.

>[!NOTE]
>
>**[!UICONTROL Produktzuordnung]** ist nur für Verträge mit Enterprise Term License Agreement (ETLA) verfügbar.

Teil der unternehmensübergreifenden Verteilung und Verwaltung von Adobe-Produkten ist die Aufteilung erworbener Ressourcen in Ressourcenzuteilungen innerhalb der zu verwaltenden Organisationen. Sie können die Verwaltung von Produktressourcen an andere Organisationen verteilen, indem Sie die gesamte Ressource oder einen Teil davon bereitstellen. Es können nicht alle Ressourcen aller Produkte zugewiesen werden. Einige Produkte können nicht an andere Organisationen verteilt werden. Solche Produkte werden auf der Registerkarte **[!UICONTROL Produktzuordnung]** angezeigt, verfügen jedoch über keine Steuerelemente, um sie anderen Organisationen hinzuzufügen.

>[!WARNING]
>
>Sie können einer untergeordneten Organisation keine Produkte aus einem Vertrag zuordnen, der **abgelaufen** oder wenn sich die Organisation im Status **inaktiv** befindet. Erfahren Sie mehr über [Vertragsablauf](https://helpx.adobe.com/enterprise/using/contract-expiry.html) oder wenden Sie sich an den Administrator Ihres Unternehmens, um zu verhindern, dass Benutzende in der untergeordneten Organisation den Zugriff auf ihre Adobe-Programme und -Services verlieren.

## Pool-Speicher

Dies gilt für Kunden, die über eine Registerkarte „Speicherung“ in ihrer Admin Console verfügen. Wenn keine Registerkarte „Speicher“ angezeigt wird, wurde Ihr Admin Console noch nicht auf das Enterprise-Speichermodell aktualisiert. Nach der Migration Ihrer Organisation werden die folgenden Änderungen angezeigt:

- Globale Administratoren erhalten Zugriff auf das Speicherkontingent und die Nutzung in der gesamten Hierarchie und können über die Registerkarte **[!UICONTROL Produktzuweisung]** in der [Global Admin Console](https://adminconsole.adobe.com/) Speicher Organisationen zuweisen.
- Systemadministratoren und Speicheradministratoren haben die volle Kontrolle über die Speichersysteme im gesamten Unternehmen und können diese anzeigen. Sie können den Speicher mithilfe der Registerkarte **[!UICONTROL Speicher]** in der [Adobe Admin Console &#x200B;](https://adminconsole.adobe.com/) und verwalten.

Mit den Aktualisierungen des Adobe Creative Cloud-Speichers sind die Speicherkontingente für Endbenutzer bis hin zur vom Unternehmen erworbenen Speichermenge flexibel. [Weitere Informationen](https://helpx.adobe.com/enterprise/using/manage-adobe-storage.html).

## Produkte zuordnen

Die **[!UICONTROL Produktzuordnung]** in der Global Admin Console zeigt Zuordnungseinheiten für Produkte an, die in der Unternehmenshierarchie gekauft wurden. Als [globaler Administrator](https://helpx.adobe.com/enterprise/global-admin-console/manage-administrators.html#admins) können Sie diese Produktressourcen einer anderen Organisation im Organisationsbaum zuordnen und die zuzuordnende Menge angeben. Als [globaler Betrachter](https://helpx.adobe.com/enterprise/global-admin-console/manage-administrators.html#admins) können Sie die Daten anzeigen und exportieren, jedoch keine Aktualisierungen vornehmen.

Gehen Sie wie folgt vor, um einer Organisation Produkte zuzuweisen:

1. Melden Sie sich bei der [Global Admin Console](https://global-admin-console.adobe.com) an und gehen Sie zu **[!UICONTROL Produktzuordnung]**.
1. Wählen Sie ein Produkt aus der Dropdown-Liste aus, um zu sehen, wie es den verschiedenen Organisationen zugeordnet ist.\
   Wenn eine Organisation das Produkt derzeit nicht hat, wird das **[!UICONTROL Hinzufügen +]** angezeigt.

   >[ !NHinweis]
   >
   >Wenn die untergeordnete Organisation bereits über einen Kaufvertrag verfügt, kann die Produktzuordnung von der übergeordneten Organisation zu dieser untergeordneten Organisation eingeschränkt sein. [Weitere Informationen](https://helpx.adobe.com/enterprise/global-admin-console/allocate-products.html#limited-product-allocation).

1. Um das Produkt zuzuordnen, wählen Sie das Symbol **[!UICONTROL Hinzufügen +]** für die entsprechende Organisation aus.\
   Einige Produkte enthalten mehr als eine zuweisbare Ressource. In diesem Fall werden im Dialogfeld mehrere Ressourcen aufgelistet und Sie müssen für jede Ressource Werte angeben. Adobe Stock kann beispielsweise Adobe Stock-Bildguthaben und Premium-Guthaben enthalten.
   ![Adobe Stock-Bilder](/help/adobe-support-tools-guide/assets/adobe-stock-images.png)
1. Geben Sie im angezeigten Dialogfeld die Produktmenge an.
1. Wählen Sie **[!UICONTROL Speichern]** aus.
1. Um eine Überallokation einer Ressource zuzulassen oder zu verbieten, wählen Sie den entsprechenden Umschalter aus.
   ![Überallokation](/help/adobe-support-tools-guide/assets/overallocation.png)
1. Wählen Sie **[!UICONTROL Ausstehende Änderungen überprüfen]**, nachdem Sie die Ressourcenzuweisung abgeschlossen haben. Wählen Sie nach der Überprüfung **[!UICONTROL Änderungen übermitteln]** aus, um [auszuführen](https://helpx.adobe.com/enterprise/global-admin-console/execute-jobs.html).

## Zuweisen und Verteilen von Adobe Acrobat Sign-Benutzerlizenzen oder -Transaktionen

Mit der Global Admin Console können Sie Acrobat Sign-Benutzerlizenzen oder -Transaktionen über die gesamte Unternehmenshierarchie hinweg zuweisen und verteilen. Jedes Unternehmen in der Hierarchie, dem Acrobat Sign-Lizenzen oder Transaktionen zugeordnet sind, erstellt ein eigenes Acrobat Sign-Konto.

- Jedes erstellte Acrobat Sign-Konto ist in Bezug auf Administration und Inhalt unabhängig und isoliert.
- Jedes Acrobat Sign-Konto kennt keine anderen Acrobat Sign-Konten (z. B. in übergeordneten oder Schwesterorganisationen).

Weitere Informationen zum [Verwalten von Adobe Acrobat Sign in der Admin Console](https://helpx.adobe.com/enterprise/using/adobe-sign-for-enterprise.html).

Um Authentifizierungs-Add-ons wie Knowledge-based Authentication (KBA) und Phone Authentication (PA) zu verwalten, wenden Sie sich an Ihren Adobe-Support-Mitarbeiter oder Customer Success Manager.


## Einschränkungen bei der Produktzuweisung

Die Zuordnung von einer übergeordneten Organisation zu einer untergeordneten Organisation ist in den folgenden Fällen beschränkt:

- Wenn beide Organisationen unterschiedliche Verträge haben und das Produkt, das Sie zuweisen möchten, in beiden vorhanden ist, ist das Mischen desselben Angebots zwischen Verträgen nicht zulässig.
- Wenn beide Unternehmen denselben Vertrag haben, können Sie die Genehmigung zur Zuordnung des Produkts anfordern, indem Sie sich an Ihren Adobe-Support-Mitarbeiter wenden oder [einen Support-](https://helpx.adobe.com/enterprise/using/support-for-enterprise.html) einreichen) und angeben, dass **[!UICONTROL Produktzuweisung]** in Global Admin Console blockiert ist.

## Überallokation

Als [globaler Administrator](https://helpx.adobe.com/enterprise/global-admin-console/manage-administrators.html#admins) können Sie eine Überallokation von Ressourcen zulassen.

Eine Zuordnung [Richtlinie](https://helpx.adobe.com/enterprise/global-admin-console/update-policies.html#update-policies), die mit dem Produkt und der Organisation verknüpft ist, gibt an, ob eine Überallokation zulässig ist.

Durch die Überallokation können einer untergeordneten Organisation mehr Produktressourcen zugewiesen werden, als in der übergeordneten Organisation verfügbar sind. Dies ist nützlich, wenn die Zuweisungen Näherungswerte sind und der Administrator nicht damit belastet werden möchte, dass die Ressourcenzuweisungen addiert bleiben.
Wenn die übermäßige Zuordnung für eine Produktressource in einer Organisation deaktiviert ist, darf die Summe der untergeordneten Gewährungen nicht höher sein als die übergeordnete Gewährung. Anfragen zum Überschreiben einer Ressource, bei der die Überzuordnung deaktiviert ist, werden nicht ausgeführt.
Wenn der Umschalter Überallokation von Aktiviert auf Deaktiviert umgeschaltet wird, müssen die Gewährungswerte angepasst werden, um eine Überallokation zu vermeiden, bevor Gewährungsaktualisierungen ausgeführt werden können, wenn eine Überallokation in den Gewährungsmengen einer Ressource vorhanden ist.

![Überallokation](/help/adobe-support-tools-guide/assets/overallocation.png)

## Abgelaufene Verträge in der Hierarchie

Sie können keine Produkte aus einem abgelaufenen ETLA-Vertrag einer untergeordneten Organisation zuordnen. In-App-Banner und -Benachrichtigungen wie die folgenden auf den Seiten **[!UICONTROL Übersicht]** und **[!UICONTROL Produktzuweisung]** geben deutlich an, wann der Vertrag für eine oder mehrere untergeordnete Organisationen abläuft, abgelaufen ist oder inaktiv ist.

![Produktzuordnung](/help/adobe-support-tools-guide/assets/product-allocation.png)

>[ !IWichtig]
>
>Sobald ein ETLA-Vertrag, der Teil der Hierarchie ist, inaktiv ist, werden die Produkte aus den Seiten **[!UICONTROL Übersicht]** und **[!UICONTROL Produktzuordnung]** entfernt.

[Erfahren Sie mehr über &#x200B;](https://helpx.adobe.com/enterprise/using/contract-expiry.html), oder wenden Sie sich an den Administrator Ihres Unternehmens, um zu verhindern, dass Benutzende in der untergeordneten Organisation den Zugriff auf ihre Adobe-Programme und -Services verlieren.
