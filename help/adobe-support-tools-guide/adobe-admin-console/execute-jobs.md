---
title: Ausstehende Aufträge ausführen
description: Erfahren Sie, wie Sie ausstehende Aufträge in der Adobe Admin Console ausführen, um sicherzustellen, dass alle Änderungen auf Ihr Unternehmen angewendet werden.
exl-id: 9b8c1a2e-5f3d-4c6a-9b7e-1a2b3c4d5e6f
source-git-commit: 7e2f0623a334ca2541b468629d4f14846eaefe79
workflow-type: tm+mt
source-wordcount: '498'
ht-degree: 0%

---


# Ausstehende Aufträge ausführen

Diese Funktion gilt für Unternehmen, die die [[!DNL Global Admin Console]](https://global-admin-console.adobe.com/) verwenden.

- Die Änderungen in der [[!DNL Global Admin Console]](https://global-admin-console.adobe.com/) werden in zwei Phasen abgeschlossen:

   1. **Phase bearbeiten**: Änderungen an Organisationen vornehmen oder Produkte zuordnen.
   2. **Ausführungsphase**: Ausstehende Änderungen überprüfen und ausführen, damit sie wirksam werden.

- Um sicherzustellen, dass alle in der [[!DNL Global Admin Console]](https://helpx.adobe.com/enterprise/global-admin-console/adopt-global-administration.html) vorgenommenen Änderungen implementiert sind und wirksam werden, wählen Sie die Registerkarte [[!UICONTROL Auftragsausführung]] und fahren Sie mit der Ausführung der ausstehenden Änderungen fort.

  Beim [[!DNL Global Admin Console]](https://global-admin-console.adobe.com/) anmelden

## Persistenz und Sichtbarkeit von Änderungen

### Persistenz ändern

- Sie können sich abmelden und später zurückkehren, ohne ausstehende Änderungen zu verlieren.
- Nicht ausgeführte Änderungen:
   - werden nach 30 Tagen verworfen.
   - werden gelöscht, wenn die Sitzung beendet wird, z. B. wenn die Browser-Registerkarte oder das Fenster geschlossen wird.

> [!NOTE]
> Führen Sie wichtige Änderungen umgehend aus, um sicherzustellen, dass sie erfolgreich angewendet werden.

### Mehrere Administratoren und Konflikte

- Zwei Administratoren, die in derselben Organisation arbeiten:
   - Sehen Sie nicht die nicht ausgeführten Änderungen der anderen Seite.
   - Änderungen nur anzeigen nach:
      - Ausführung und
      - Aktualisieren der Anzeige oder erneutes Anmelden.
- Nicht ausgeführte Änderungen können mit bereits ausgeführten Änderungen in Konflikt stehen.

### Konfliktbehandlung

Konflikte werden gemeldet:
- Zur Ausführungszeit oder
- Wenn Daten aktualisiert werden (z. B. nach der Abmeldung und der erneuten Anmeldung).

## Ausstehende Änderungen ausführen

Als globaler Administrator können Sie ausstehende Änderungen auf der Registerkarte [Auftragsausführung] überprüfen  ausführen.

### Schritte zum Ausführen von Änderungen

1. Melden Sie sich bei [[!DNL Global Admin Console]] an.
2. Wählen Sie die Registerkarte [!UICONTROL Auftragsausführung] im linken Navigationsbereich aus.
3. Überprüfen Sie die ausstehenden Änderungen.
4. Wählen Sie [[!UICONTROL Änderungen einreichen]] aus, um sie auszuführen.

Nachdem Sie den Auftrag gesendet haben:

- Der Auftrag gelangt in die Ausführungswarteschlange.
- Der Status ist [[!UICONTROL Ausstehend] während der Ausführung des Auftrags.
- Adobe empfiehlt, nur jeweils einen Auftrag auszuführen, um die Ausführung vorherzusagen und die Fehlerbehebung zu vereinfachen.

> [!IMPORTANT]
> Wenn während der Ausführung ein Fehler auftritt, müssen alle Änderungen, die nicht erfolgreich angewendet wurden, erneut eingegeben und gesendet werden.

### Langfristige Zuteilungen

Wenn eine Produktzuordnung länger als 12 Stunden dauert:
- Der Vorgang ist als [[!UICONTROL Fehlgeschlagen] gekennzeichnet.
- Alle nachfolgenden ausstehenden Aufgaben in diesem Auftrag werden nicht ausgeführt.

![Pending-Jobs](assets/pending-jobs.png)

## Abbrechen eines laufenden Auftrags

Sie können einen aktuell ausgeführten Auftrag über die Registerkarte [[!UICONTROL Auftragsausführung]] abbrechen.

### Schritte zum Abbrechen eines laufenden Auftrags

1. Melden Sie sich bei [[!DNL Global Admin Console]] an.
2. Wählen Sie [[!UICONTROL Auftragsausführung]] aus.
3. Wählen Sie [[!UICONTROL Laufenden Auftrag abbrechen]].

### Abbruchverhalten

1. Der Vorgang wird am Ende des aktuellen Schritts angehalten.
2. Der Vorgang endet nicht mitten in einem Schritt.
3. Einige Schritte können Minuten oder Stunden dauern.
4. Während dieser Zeit kann der Auftrag im Status [[!UICONTROL Abbrechen] verbleiben.

> [!NOTE]
> Planen Sie Abbrüche mit dem Wissen, dass der Abschluss des aktuellen Schritts sich erheblich verzögern kann, wenn der Auftrag beendet wird.

## Vorgangsverlauf anzeigen

- So zeigen Sie die in den letzten 30 Tagen ausgeführten Aufträge an:

   1. Melden Sie sich bei [[!DNL Global Admin Console]] an.
   2. Wählen Sie [[!UICONTROL Auftragsausführung]] aus.
   3. Scrollen Sie nach unten auf der Seite.
   4. Wählen Sie [[!UICONTROL Letzte Aufträge]].

- Anzeige „Letzte Aufträge“:
   - Übermittelt **Vorgangsbefehle**.
   - **Fehler** und **Warnungen** im Zusammenhang mit der Ausführung.

> [!NOTE]
> Nachfolgende Umbenennungen oder Löschungen verwandter Objekte **beeinflussen nicht** wie Befehle im Vorgangsverlauf angezeigt werden. Der Verlauf spiegelt den Status zum Zeitpunkt der Übermittlung wider.
