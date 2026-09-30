---
title: Best Practices und Stabilität
description: Best Practices und Stabilitätsempfehlungen, die Adobe Commerce-Händlern bei der Vorbereitung ihrer Umgebungen auf Ereignisse mit hohem Traffic-Aufkommen wie die Weihnachtszeit helfen.
feature-set: Commerce
feature: Support
solution: Commerce
role: Developer, Admin, Leader
TQID: 'https://experienceleague.adobe.com/iA6ioGYYgQSotPrPqujDBdRcjBLUQXMGXfwlcSMGjkM'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: cdfd3bc1-dc23-5cf0-b965-d3c0c55cde67
    internal-label: Best Practices
  - id: 5a951749-fac9-5bc7-9a98-ebe4ff066437
    internal-label: Cloud
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
subfeature_v2:
  - id: 3c398179-d35a-51ba-b317-6c5b95feef5e
    internal-label: Logs
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
source-git-commit: 71589dd124714805fbf844540fb2d272433631ee
workflow-type: tm+mt
source-wordcount: '861'
ht-degree: 4%
---

# Best Practices und Stabilität

Dieser Abschnitt enthält technische Empfehlungen zur Vorbereitung von Adobe Commerce-Umgebungen - sowohl Commerce auf Cloud-Infrastrukturen als auch On-Premise - auf Ereignisse mit hohem Traffic-Aufkommen wie die Weihnachtszeit.

>[!NOTE]
>
>Die mit **(nur Cloud) gekennzeichneten** gelten für Commerce in der Cloud-Infrastruktur. Die meisten anderen Empfehlungen gelten auch für lokale Bereitstellungen.

## Aktualisieren auf die neueste Version von Adobe Commerce {#upgrade-to-latest-version-of-adobe-commerce}

Stellen Sie sicher, dass Ihre Site nicht mit einer nicht unterstützten Version von Adobe Commerce verwendet wird, da dies die Leistung Ihrer Site beeinträchtigen und die Anfälligkeit für Sicherheitsprobleme erhöhen kann. Führen Sie ein Upgrade auf die neueste Version von Adobe Commerce durch, um sicher und bereit für die Weihnachtssaison zu sein.

Die [neueste Version](https://experienceleague.adobe.com/de/docs/commerce-operations/release/notes/overview) von Adobe Commerce enthält viele [wichtige Sicherheitskorrekturen](https://experienceleague.adobe.com/en/docs/commerce-operations/release/notes/security-patches/overview) einschließlich Verbesserungen und behobener Probleme, von denen Ihr Projekt profitieren wird, wenn Sie von einer früheren Version aktualisieren.

Weitere Informationen zu nicht unterstützten Versionen von Adobe Commerce finden Sie in der [Adobe Commerce-Lebenszyklusrichtlinie](https://experienceleague.adobe.com/de/docs/commerce-operations/release/planning/lifecycle-policy).

## Installieren des neuesten ECE-Tools und Quality Patch Tools (QPT) {#install-latest-ece-tools-and-quality-patch-tool-qpt}

Stellen Sie sicher, dass das neueste `ece-tools` und seine abhängigen Module mithilfe des `--with-dependencies` installiert werden, damit alle erforderlichen Cloud-Patches ordnungsgemäß für Ihre Adobe Commerce-Version installiert werden. Anweisungen hierzu finden Sie [Aktualisieren des Pakets ECE-Tools](https://experienceleague.adobe.com/en/docs/commerce-on-cloud/user-guide/dev-tools/ece-tools/update-package).

Überprüfen Sie die im Quality Patches Tool verfügbare Patch-Liste und stellen Sie sicher, dass die mit Ihrer Adobe Commerce-Version kompatiblen Leistungs-Patches angewendet wurden. Siehe [Quality Patches Tool: Nach Patches suchen](https://experienceleague.adobe.com/de/docs/commerce-operations/tools/quality-patches-tool/patches-available-in-qpt/patches-available-in-qpt-tool-overview).

>[!NOTE]
>
>QPT ist sowohl für Adobe Commerce in der Cloud-Infrastruktur als auch für On-Premise-Installationen verfügbar. Installation und Verwendungsbefehle unterscheiden sich zwischen den beiden - für Cloud-Lösungen ist QPT im Paket ECE-Tools enthalten.

## Überprüfen und Bereinigen von Protokolldateien {#review-and-clean-log-files}

Überprüfen Sie die Protokolldateien in der Cloud-Umgebung (z. B. die Anwendungsprotokolldateien unter `~/var/log`) und identifizieren Sie alle häufig protokollierten Datensätze, die in die standardmäßigen oder benutzerdefinierten Protokolldateien geschrieben werden. Weitere Informationen finden Sie unter [Protokolle anzeigen und verwalten](https://experienceleague.adobe.com/en/docs/commerce-on-cloud/user-guide/develop/test/log-locations).

* Überprüfen Sie die folgenden standardmäßigen Protokolldateien und beheben Sie wiederkehrende Fehler: `~/var/log`, `~/var/log/exception.log`, `~/var/log/support_report.log`, `~/var/log/system.log`, `~/var/report`.
* Entfernen Sie Debug-Protokolle, die zuvor zur Fehlerbehebung bei früheren Problemen hinzugefügt wurden.

Diese Protokolle sind auch in [!DNL New Relic] verfügbar. Siehe [New Relic-Protokollverwaltung](https://experienceleague.adobe.com/en/docs/commerce-on-cloud/user-guide/monitor/new-relic/log-management).

## Überwachen des Festplattenwachstums {#monitor-disk-size-growth}

Ihre Adobe Commerce in der Cloud-Infrastruktur verfügt über zwei Hauptfestplatten-Volumes. Überwachen Sie diese Volumes, um sicherzustellen, dass sie bei starkem Traffic über ausreichend freien Speicherplatz verfügen. Adobe Commerce gibt eine Warnung aus, wenn eines der beiden Volumes eine Auslastung von über 70 % erreicht.

* `/mnt/shared` (freigegebene Dateien, einschließlich Protokolle und Mediendateien)
* `/data/mysql` (Datenbankvolume)

Weitere Informationen finden Sie unter [Speicherplatz verwalten](https://experienceleague.adobe.com/en/docs/commerce-on-cloud/user-guide/develop/storage/manage-disk-space).

## Überprüfen der langsamsten Datenbankanfragen {#review-slowest-database-requests}

Es ist wichtig, die zeitaufwendigsten Datenbanktransaktionen in [!DNL New Relic] regelmäßig zu überwachen und zu überprüfen. Deutlich langsame Abfragen und Komponenten untersuchen.

* **Überprüfen Sie die zeitaufwendigsten Transaktionen:** Gehen Sie zu **[!UICONTROL New Relic]** > **[!UICONTROL APM und Services]** > wählen Sie Umgebung > **[!UICONTROL Datenbanken]** und sortieren Sie dann nach den meisten zeitaufwendigen Transaktionen.

* **Überprüfen Sie das MySQL-Protokoll für langsame Abfragen:** Überprüfen Sie die `mysql-slow.log` für langsame Abfragen, die vom System aufgezeichnet werden. Diese Protokolle sind auch in [!DNL New Relic] verfügbar: Wechseln Sie zu **[!UICONTROL New Relic]** > **[!UICONTROL Protokolle]** und filtern Sie nach `filePath:"/var/log/mysql/mysql-slow.log"`.

Überprüfen Sie die [!DNL MySQL] Protokolle für langsame Abfragen regelmäßig, um sicherzustellen, dass langsame Abfragen nicht häufig ausgeführt werden. Schritte zum Beheben von Abfragen, die Sie als problematisch identifizieren, finden Sie unter [Beheben von Datenbankleistungsproblemen](https://experienceleague.adobe.com/en/docs/commerce-operations/implementation-playbook/best-practices/maintenance/resolve-database-performance-issues).

## Konfigurieren von Cron-Aufträgen {#configure-cron-jobs}

Alle asynchronen Vorgänge in Commerce werden mit dem Linux-Cron-Befehl ausgeführt.

Commerce hängt von der richtigen Cron-Auftragskonfiguration für wichtige Systemfunktionen ab, einschließlich der Indizierung und Warteschlangenverbrauchervorgänge. Wenn die Einrichtung nicht ordnungsgemäß erfolgt, funktioniert Commerce nicht wie erwartet.

Es ist wichtig, dass Commerce cron korrekt eingerichtet und konfiguriert ist, indem der entsprechende Unix-Benutzer in der crontab-Unix-Datei verwendet wird. Jeder Unix-Benutzer hat seine eigene crontab-Datei. Dies ist die Konfiguration, die zum Ausführen von Cron-Aufträgen für diesen Benutzer verwendet wird. Anweisungen hierzu finden Sie [Konfigurieren und Ausführen von Cron-Aufträgen](https://experienceleague.adobe.com/en/docs/commerce-operations/configuration-guide/cli/configure-cron-jobs).

Das `dev/tools/cron.sh` kann nicht mehr ausgeführt werden, da es entfernt wurde.

## Optimieren der Client-seitigen Einstellungen {#optimize-client-side-settings}

Um die Reaktionsfähigkeit Ihrer Commerce-Instanz zu verbessern, konfigurieren Sie die folgenden Einstellungen unter **[!UICONTROL Stores]** > **[!UICONTROL Configuration]** > **[!UICONTROL Advanced]** > **[!UICONTROL Developer]**, die nur im Entwicklermodus verfügbar sind:

* **[!UICONTROL Rastereinstellungen]** > **[!UICONTROL Asynchrone Indizierung]**: *[!UICONTROL Aktivieren]*
* **[!UICONTROL CSS-Einstellungen]** — **[!UICONTROL Minimieren von CSS-Dateien]**: *[!UICONTROL Ja]*
* **[!UICONTROL JavaScript-Einstellungen]** — **[!UICONTROL JavaScript-Dateien minimieren]**: *[!UICONTROL Ja]*
* **[!UICONTROL JavaScript-Einstellungen]** — **[!UICONTROL JavaScript-Bundle aktivieren]**: *[!UICONTROL Ja]* (standardmäßig nicht aktiviert)
* **[!UICONTROL Vorlageneinstellungen]** — **[!UICONTROL HTML minimieren]**: *[!UICONTROL Ja]*

Da Adobe Commerce in Cloud immer im Produktionsmodus ausgeführt wird, legen Sie stattdessen jede Option in der Befehlszeile fest - z. B. `bin/magento config:set --lock-config dev/css/minify_files 1` - und übertragen Sie dann die resultierende `app/etc/config.php` und stellen Sie sie erneut bereit. Eine vollständige Liste der CLI-Pfade finden Sie unter [Ressourcendateien optimieren](https://experienceleague.adobe.com/en/docs/commerce-operations/implementation-playbook/best-practices/development/optimize-css-js-files).
