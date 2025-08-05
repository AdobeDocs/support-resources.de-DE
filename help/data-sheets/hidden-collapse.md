---
title: Fehlerabschnitte reduzieren
description: Reduzierbare Abschnitte von UGP-13446 werden nicht gerendert, möglicherweise aufgrund von eingebetteten Seitenregisterkarten
hide: true
hidefromtoc: true
source-git-commit: f2d8eb9125df5f542c1ed075348586965f4adaad
workflow-type: tm+mt
source-wordcount: '428'
ht-degree: 7%

---

# Reduzierbare Abschnitte

<http://jira.corp.adobe.com/browse/UGP-13446> Reduzierbare Abschnitte von UGP-13446 werden nicht gerendert, möglicherweise aufgrund von eingebetteten Seitenregisterkarten

## Beispiele

Erste mit Seiten-Registerkarten, zweite ohne

### Option 2: Mit Seitenregisterkarten

+++ Manuelle Hotfix-Installation für 6.5.18.0 - 6.5.22.0

**Schritt 1: Herunterladen und Extrahieren des Hotfix-Pakets**

- Laden Sie [Hotfix für 6.5.18.0 - 6.5.22](https://www.adobe.com) vom Adobe Software Distribution-Portal herunter.
- Lokal extrahieren

**Schritt 2: Navigieren Sie zum richtigen Versionsordner**

- Gehen Sie je nach in Ihrer Umgebung installierter Service Pack-Version in den entsprechenden Ordner.

  Beispiel: Der Ordner für Service Pack 20 lautet:

  ```
  <extracted-hotfix>/SP20/
  ```

**Schritt 3: Suchen Sie das Bereitstellungsverzeichnis**

- Wechseln Sie auf Ihrem AEM Forms on JEE-Server zu:

  ```
  [AEM installation directory]/deploy
  ```

  Beispiel: `adobe/adobe-experience-manager-forms/deploy`



**Schritt 4: Aktualisieren und ersetzen Sie die EAR-Dateien**

>[!BEGINTABS]

>[!TAB JBoss]

1. `adobe-core-jboss.ear` öffnen und `adminui.war` ersetzen durch

   ```
   adobe-xxe-configuration-hotfix/SP[version]/jboss/adminui.war
   ```

   Beispiel: `adobe-xxe-configuration-hotfix/SP20/jboss/adminui.war`

1. Wechseln Sie innerhalb des `adobe-core-jboss.ear` zum Ordner `lib/` und ersetzen Sie `adobe-uisupport.jar` durch:

   ```
   adobe-xxe-configuration-hotfix/SP[version]/adobe-uisupport.jar
   ```

   Beispiel: `adobe-xxe-configuration-hotfix/SP20/adobe-uisupport.jar`

1. Rettet das OHR. Sicherstellen, dass Änderungen ordnungsgemäß gespeichert werden.


1. `adobe-edcserver-jboss.ear` ersetzen durch

   ```
   adobe-xxe-configuration-hotfix/SP[version]/jboss/adobe-edcserver-jboss.ear
   ```

   Beispiel: `adobe-xxe-configuration-hotfix/SP20/jboss/adobe-edcserver-jboss.ear`

1. `adobe-forms-jboss.ear` ersetzen durch

   ```
   adobe-xxe-configuration-hotfix/SP[version]/jboss/adobe-forms-jboss.ear
   ```

   Beispiel: `adobe-xxe-configuration-hotfix/SP20/jboss/adobe-forms-jboss.ear`



>[!TAB WebLogic]

1. `adobe-core-weblogic.ear` öffnen und `adminui.war` ersetzen durch

   ```
   adobe-xxe-configuration-hotfix/SP[version]/weblogic/adminui.war
   ```

   Beispiel: `adobe-xxe-configuration-hotfix/SP20/weblogic/adminui.war`

1. Ersetzen Sie innerhalb des `adobe-core-weblogic.ear` `adobe-uisupport.jar` durch:

   ```
   adobe-xxe-configuration-hotfix/SP[version]/adobe-uisupport.jar
   ```

   Beispiel: `adobe-xxe-configuration-hotfix/SP20/adobe-uisupport.jar`

1. Rettet das OHR. Sicherstellen, dass Änderungen ordnungsgemäß gespeichert werden.


1. `adobe-edcserver-weblogic.ear` ersetzen durch

   ```
   adobe-xxe-configuration-hotfix/SP[version]/weblogic/adobe-edcserver-weblogic.ear
   ```

   Beispiel: `adobe-xxe-configuration-hotfix/SP20/weblogic/adobe-edcserver-weblogic.ear`

1. `adobe-forms-weblogic.ear` ersetzen durch

   ```
   adobe-xxe-configuration-hotfix/SP[version]/weblogic/adobe-forms-weblogic.ear
   ```

   Beispiel: `adobe-xxe-configuration-hotfix/SP20/weblogic/adobe-forms-weblogic.ear`

>[!TAB WebSphere]

1. `adobe-core-websphere.ear` öffnen und `adminui.war` ersetzen durch

   ```
   adobe-xxe-configuration-hotfix/SP[version]/websphere/adminui.war
   ```

   Beispiel: `adobe-xxe-configuration-hotfix/SP20/websphere/adminui.war`

1. Ersetzen Sie innerhalb des `adobe-core-websphere.ear` `adobe-uisupport.jar` durch:

   ```
   adobe-xxe-configuration-hotfix/SP[version]/adobe-uisupport.jar
   ```

   Beispiel: `adobe-xxe-configuration-hotfix/SP20/adobe-uisupport.jar`

1. Rettet das OHR. Sicherstellen, dass Änderungen ordnungsgemäß gespeichert werden.


1. `adobe-edcserver-websphere.ear` ersetzen durch

   ```
   adobe-xxe-configuration-hotfix/SP[version]/websphere/adobe-edcserver-websphere.ear
   ```

   Beispiel: `adobe-xxe-configuration-hotfix/SP20/websphere/adobe-edcserver-websphere.ear`

1. `adobe-forms-websphere.ear` ersetzen durch

   ```
   adobe-xxe-configuration-hotfix/SP[version]/websphere/adobe-forms-websphere.ear
   ```

   Beispiel: `adobe-xxe-configuration-hotfix/SP20/websphere/adobe-forms-websphere.ear`

>[!ENDTABS]



**Schritt 5: Aktualisieren `adobe-rightsmanagement-<appserver>-dsc.jar`Datei mit**

```
adobe-xxe-configuration-hotfix/SP[version]/<appserver>/adobe-rightsmanagement-<appserver>-dsc.jar
```

Beispiel: `adobe-xxe-configuration-hotfix/SP20/jboss/adobe-rightsmanagement-jboss-dsc.jar`

**Schritt 6: Zusätzliche Konfiguration für Document Security auf WebSphere und WebLogic**:

Wenn Sie Document Security (früher Rights Management) verwenden, legen Sie die folgende Java-Systemeigenschaft (JVM-Argument) fest, bevor Sie den AEM Forms-Server starten:

```
-Dcom.adobe.forms.jee.services.allowDoctypeDeclaration=true
```


**Schritt 7: Führen Sie Configuration Manager erneut aus**

- Starten Sie den Configuration Manager, um die aktualisierte EAR-Datei erneut bereitzustellen und den Hotfix anzuwenden

+++

### Option 2: Ohne Seitenregisterkarten

+++ Manuelle Hotfix-Installation für 6.5.18.0 - 6.5.22.0

**Schritt 1: Herunterladen und Extrahieren des Hotfix-Pakets**

- Laden Sie [Hotfix für 6.5.18.0 - 6.5.22](https://www.adobe.com) vom Adobe Software Distribution-Portal herunter.
- Lokal extrahieren

**Schritt 2: Navigieren Sie zum richtigen Versionsordner**

- Gehen Sie je nach in Ihrer Umgebung installierter Service Pack-Version in den entsprechenden Ordner.

  Beispiel: Der Ordner für Service Pack 20 lautet:

  ```
  <extracted-hotfix>/SP20/
  ```

**Schritt 3: Suchen Sie das Bereitstellungsverzeichnis**

- Wechseln Sie auf Ihrem AEM Forms on JEE-Server zu:

  ```
  [AEM installation directory]/deploy
  ```

  Beispiel: `adobe/adobe-experience-manager-forms/deploy`



**Schritt 4: Aktualisieren und ersetzen Sie die EAR-Dateien**

Seitenregisterkarten gelöscht

**Schritt 5: Aktualisieren `adobe-rightsmanagement-<appserver>-dsc.jar`Datei mit**

```
adobe-xxe-configuration-hotfix/SP[version]/<appserver>/adobe-rightsmanagement-<appserver>-dsc.jar
```

Beispiel: `adobe-xxe-configuration-hotfix/SP20/jboss/adobe-rightsmanagement-jboss-dsc.jar`

**Schritt 6: Zusätzliche Konfiguration für Document Security auf WebSphere und WebLogic**:

Wenn Sie Document Security (früher Rights Management) verwenden, legen Sie die folgende Java-Systemeigenschaft (JVM-Argument) fest, bevor Sie den AEM Forms-Server starten:

```
-Dcom.adobe.forms.jee.services.allowDoctypeDeclaration=true
```


**Schritt 7: Führen Sie Configuration Manager erneut aus**

- Starten Sie den Configuration Manager, um die aktualisierte EAR-Datei erneut bereitzustellen und den Hotfix anzuwenden

+++

Flosse
