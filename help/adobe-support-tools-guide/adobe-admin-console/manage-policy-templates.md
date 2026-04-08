---
title: Verwalten von Richtlinienvorlagen in der Global Admin Console
description: Erfahren Sie, wie globale Administratoren Richtlinienvorlagen direkt oder indirekt von der Organisation, in der sie in der Global Admin Console gespeichert sind, auf jede untergeordnete Organisation anwenden können.
feature-set: Experience Cloud Services
solution: Admin Console
feature: Admin Console
product_v2:
  - id: f7bdf6be-dd3b-4d2d-ac52-0e62ed0d3102
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
exl-id: e4dc5c35-1323-4894-bd47-b31c61a864bc
source-git-commit: ad324036dbeb2a54855349321b2ba33405d2c075
workflow-type: tm+mt
source-wordcount: 705
ht-degree: 0%

---

# Verwalten von Richtlinienvorlagen in der Global Admin Console

**Gilt für:** Enterprise

Erfahren Sie, wie globale Administratoren Richtlinienvorlagen direkt oder indirekt von der Organisation, in der sie in der Global Admin Console gespeichert sind, auf jede untergeordnete Organisation anwenden können.

>[!NOTE]
>
>Wählen Sie in der [Global Admin Console](https://helpx.adobe.com/enterprise/global-admin-console/adopt-global-administration.html) eine Organisation aus, die bearbeitet werden soll, und navigieren Sie zur Registerkarte **Richtlinienvorlagen**, um die Einrichtung zu optimieren und eine unternehmensübergreifende konsistente Richtlinienverwaltung zu erleichtern.
>
> [Bei Global Admin Console anmelden](https://global-admin-console.adobe.com/)

## Funktionsweise von Richtlinienvorlagen

Richtlinienvorlagen werden in einer Organisation gespeichert und sind für alle globalen Administratoren dieser Organisation sichtbar. Nach der Anwendung werden die Einträge aus der Richtlinienvorlage in jeder Organisation einzeln festgelegt. Wenn eine Richtlinienvorlage auf eine Organisation angewendet wird, werden alle Einträge in der Richtlinienvorlage auf die Richtlinien der Organisation angewendet und ersetzen vorhandene Richtlinienwerte.

### Gesperrtes Richtlinienverhalten

Aktualisierungen gesperrter Richtlinien werden nur durchgeführt, wenn der Benutzer, der die Aktualisierung anwendet, ein globaler Administrator der Organisation ist, der durch das Symbol **[!UICONTROL Gesperrt nach]** der zu aktualisierenden Richtlinie angegeben wird.

Wenn der Benutzer, der die Vorlage anwendet, berechtigt ist, die Richtlinie zu entsperren, übernimmt die Richtlinie die Werte aus der angewendeten Vorlage (gesperrt oder entsperrt). Wenn die Vorlage angibt, dass die Sperre unverändert bleiben soll, bleibt der Wert der Sperre in der Richtlinie unverändert.

### Wichtiger Hinweis zum Speichern

>[!NOTE]
>
>Im Gegensatz zu anderen Änderungen, die in Global Admin Console vorgenommen wurden, werden Änderungen an Richtlinienvorlagen sofort wirksam, ohne den Prozess **[!UICONTROL Ausstehende Änderungen überprüfen - Übermitteln]** müssen. Um ausstehende Änderungen in Organisationen zu implementieren, auf die die Richtlinienvorlage angewendet wird, ist jedoch [Übermittlung](https://helpx.adobe.com/enterprise/global-admin-console/execute-jobs.html) erforderlich.

## Erstellen einer Richtlinienvorlage

1. Wählen Sie in der [Global Admin Console](https://global-admin-console.adobe.com/) eine zu bearbeitende Organisation aus und navigieren Sie dann zur Registerkarte **[!UICONTROL Richtlinienvorlagen]** .
1. Wählen Sie **[!UICONTROL Vorlage erstellen]**.<br>
   ![pic1](./assets/DXSKB-3209-1-ga_14.png)
   <br>
1. Geben **[!UICONTROL im Dialogfeld]** Richtlinienvorlage erstellen“ den **Namen** und **Beschreibung** für die Richtlinienvorlage ein.<br>Der Name der Richtlinienvorlage darf maximal 100 Zeichen lang sein.
1. Wählen Sie die Richtlinien aus, die in die Vorlage aufgenommen werden sollen.
1. Legen Sie Werte für die ausgewählten Richtlinien fest (siehe [Festlegen von Richtlinienwerten](#setting-policy-values) unten).
1. Wählen Sie **[!UICONTROL Speichern]** aus.

### Festlegen von Richtlinienwerten {#setting-policy-values}

Konfigurieren Sie für jede in der Vorlage enthaltene Richtlinie zwei Einstellungen:

* **Erlaubt/Nicht erlaubt** Stellen Sie den Schieberegler auf den gewünschten Wert ein. Weitere Informationen [Richtliniendetails](https://helpx.adobe.com/enterprise/global-admin-console/update-policies.html#policy-details).
* **Wert sperren** Ändern Sie den Sperrstatus der Richtlinie mithilfe einer der folgenden Optionen:
   * **lock** - Die Richtlinie wird nach Anwendung der Vorlage gesperrt.
   * **Entsperren** - Die Richtlinie wird nach Anwendung der Vorlage entsperrt.
   * **unverändert beibehalten** - Der Sperrstatus der Richtlinie bleibt gleich wie vor der Anwendung der Vorlage.<br>
     ![pic2](./assets/DXSKB-3209-2-policy-template.png)
<br>

## Anwenden einer Vorlage auf Organisationen

1. Wählen Sie in der [Global Admin Console](https://global-admin-console.adobe.com/) eine zu bearbeitende Organisation aus und navigieren Sie dann zur Registerkarte **[!UICONTROL Richtlinienvorlagen]** .
1. Wählen Sie das Symbol **[!UICONTROL Weitere Optionen]** ![Weitere Optionen](./assets/manage-product-profiles_more-options.png) für die entsprechende Richtlinienvorlage aus und wählen Sie **[!UICONTROL Vorlage auf Organisation anwenden]**.<br>
   ![pic3](./assets/DXSKB-3209-3-ga_15.png)
   <br>
1. Wählen Sie die Organisationen aus, auf die Sie die Vorlage anwenden möchten. Sie können mehrere Organisationen auswählen.<br>
   ![pic4](./assets/DXSKB-3209-4-bulk-apply-template.png)
   <br>
1. Wählen Sie **[!UICONTROL Vorlage anwenden]** aus.
1. Um ausstehende Änderungen in Organisationen zu implementieren, auf die die Richtlinienvorlage angewendet wird, wählen Sie **[!UICONTROL Ausstehende Änderungen überprüfen]**. Wählen Sie nach der Überprüfung **[!UICONTROL Änderungen übermitteln]** aus, um [auszuführen](https://helpx.adobe.com/enterprise/global-admin-console/execute-jobs.html).

Wenn alle Richtlinienwerte in den von Ihnen ausgewählten Organisationen bereits mit den Werten in der Vorlage übereinstimmen, wird eine Meldung angezeigt, die besagt, dass keine Änderungen vorgenommen wurden. Außerdem wird **[!UICONTROL Ausstehende Änderungen überprüfen]** nicht aktiviert, wenn keine anderen ausstehenden Änderungen vorhanden sind.

## Bearbeiten einer Vorlage

1. Wählen Sie in der [Global Admin Console](https://global-admin-console.adobe.com/) eine zu bearbeitende Organisation aus und navigieren Sie dann zur Registerkarte **[!UICONTROL Richtlinienvorlagen]** .
1. Wählen Sie das Symbol **[!UICONTROL Weitere Optionen]** ![Weitere Optionen](./assets/manage-product-profiles_more-options.png) für die entsprechende Vorlage aus und klicken Sie auf **[!UICONTROL Vorlage bearbeiten]**.<br>
   ![pic5](./assets/DXSKB-3209-5-ga_15-1.png)
   <br>
1. Aktualisieren Sie die Richtlinienvorlage und wählen Sie **[!UICONTROL Jetzt aktualisieren]**.
1. Um ausstehende Änderungen in Organisationen zu implementieren, auf die die Richtlinienvorlage angewendet wird, wählen Sie **[!UICONTROL Ausstehende Änderungen überprüfen]**. Wählen Sie nach der Überprüfung **[!UICONTROL Änderungen übermitteln]** aus, um [auszuführen](https://helpx.adobe.com/enterprise/global-admin-console/execute-jobs.html).

## Löschen einer Vorlage

1. Wählen Sie in der [Global Admin Console](https://global-admin-console.adobe.com/) eine zu bearbeitende Organisation aus und navigieren Sie dann zur Registerkarte **[!UICONTROL Richtlinienvorlagen]** .
1. Wählen Sie das Symbol **[!UICONTROL Weitere Optionen]** ![Weitere Optionen](./assets/manage-product-profiles_more-options.png) für die entsprechende Vorlage und wählen Sie **[!UICONTROL Vorlage löschen]**.<br>
   ![pic6](./assets/DXSKB-3209-6-ga_15-2.png)
   <br>
1. Wählen *im* angezeigten Dialogfeld „Ja“ aus.
