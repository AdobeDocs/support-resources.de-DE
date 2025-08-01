---
title: Tag-Bibliotheken
description: Die Tag-Bibliotheken Granite, CQ und Sling bieten Ihnen Zugriff auf bestimmte Funktionen, die im JSP-Skript Ihrer Vorlagen und Komponenten verwendet werden können
contentOwner: Guillaume Carlino
products: SG_EXPERIENCEMANAGER/6.5/SITES
topic-tags: platform
content-type: reference
solution: Experience Manager, Experience Manager Sites
hide: true
hidefromtoc: true
role: Developer
exl-id: d024b7e9-1e8e-4aa3-bbb8-7bc92d143a1f
source-git-commit: 3128bd389ee7998736993f7b17c9ac53d146e929
workflow-type: tm+mt
source-wordcount: '2458'
ht-degree: 0%

---

# Tag-Bibliotheken{#tag-libraries}

Die Tag-Bibliotheken Granite, CQ und Sling bieten Ihnen Zugriff auf bestimmte Funktionen, die im JSP-Skript Ihrer Vorlagen und Komponenten verwendet werden können.

## **Fettschrift**

Dies ist oben eine kühne Überschrift.

Freitag, 31. Juli 2025

## *Kursiv gedruckte*

Dies ist eine kursiv gedruckte Überschrift.

## Granite-Tag-Bibliothek {#granite-tag-library}

Die Granite-Tag-Bibliothek enthält hilfreiche Funktionen.

Wenn Sie das JSP-Skript einer Granite-UI-Komponente entwickeln, wird empfohlen, folgenden Code am Anfang des Skripts einzuschließen:

```xml
<%@include file="/libs/granite/ui/global.jsp"%>
```

Die globale Bibliothek deklariert auch die Sling-Bibliothek.

```xml
<%@taglib prefix="sling" uri="https://sling.apache.org/taglibs/sling" %>
```

### &lt;ui:includeClientLib> {#ui-includeclientlib}

Das `<ui:includeClientLib>`-Tag enthält eine AEM-HTML-Client-Bibliothek, bei der es sich um eine JS-, CSS- oder Design-Bibliothek handeln kann. Für mehrere Einschlüsse verschiedener Typen, z. B. js und css, muss dieses Tag mehrmals in der JSP verwendet werden. Dieses Tag ist ein praktischer Wrapper für die ` [com.adobe.granite.ui.clientlibs.HtmlLibraryManager](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/reference-materials/javadoc/com/adobe/granite/ui/clientlibs/HtmlLibraryManager.html)`-Service-Schnittstelle .

Sie weist die folgenden Attribute auf:

**categories** - Eine durch Kommas getrennte Liste der Client-Bibliothekskategorien. Dies umfasst alle JavaScript- und CSS-Bibliotheken für die angegebenen Kategorien. Der Design-Name wird aus der Anfrage extrahiert.

Entspricht: `com.adobe.granite.ui.clientlibs.HtmlLibraryManager#writeIncludes`

**theme** - Eine durch Kommas getrennte Liste der Client-Bibliothekskategorien. Dies umfasst alle designbezogenen Bibliotheken (CSS und JS) für die jeweiligen Kategorien. Der Design-Name wird aus der Anfrage extrahiert.

Entspricht: `com.adobe.granite.ui.clientlibs.HtmlLibraryManager#writeThemeInclude`

**js** - Eine durch Kommas getrennte Liste der Client-Bibliothekskategorien. Dies umfasst alle JavaScript-Bibliotheken für die angegebenen Kategorien.

Entspricht: `com.adobe.granite.ui.clientlibs.HtmlLibraryManager#writeJsInclude`

**css** - Eine durch Kommas getrennte Liste der Client-Bibliothekskategorien. Dies umfasst alle CSS-Bibliotheken für die angegebenen Kategorien.

Entspricht: `com.adobe.granite.ui.clientlibs.HtmlLibraryManager#writeCssInclude`

**themed** - Ein Flag, das angibt, ob nur designbezogene oder nicht designbezogene Bibliotheken enthalten sein sollen. Wenn ausgelassen, sind beide Sätze enthalten. Gilt nur für reine JS- oder CSS-Includes (nicht für Kategorien oder Design-Includes).

Das `<ui:includeClientLib>`-Tag kann in einem JSP-Code wie folgt verwendet werden:

```xml
<%-- all: js + theme (theme-js + css) --%>
<ui:includeClientLib categories="cq.wcm.edit" />

<%-- only js libs --%>
<ui:includeClientLib js="cq.collab.calendar, cq.security" />

<%-- theme only (theme-js + css) --%>
<ui:includeClientLib theme="cq.collab.calendar, cq.security" />

<%-- css only --%>
<ui:includeClientLib css="cq.collab.calendar, cq.security" />
```

## CQ Tag Library {#cq-tag-library}

Die CQ-Tag-Bibliothek enthält hilfreiche Funktionen.

Um die CQ-Tag-Bibliothek in Ihrem Skript zu verwenden, muss das Skript mit dem folgenden Code beginnen:

```xml
<%@taglib prefix="cq" uri="https://www.day.com/taglibs/cq/1.0" %>
```

>[!NOTE]
>
>Wenn die `/libs/foundation/global.jsp` Datei im Skript enthalten ist, wird die Tag-Bibliothek automatisch deklariert.

Wenn Sie das JSP-Skript einer AEM-Komponente entwickeln, sollten Sie folgenden Code am Anfang des Skripts einfügen:

```xml
<%@include file="/libs/foundation/global.jsp"%>
```

Er deklariert die Tag-Bibliotheken Sling, CQ und JSTL und macht die regelmäßig verwendeten Skriptobjekte verfügbar, die durch das Tag [`<cq:defineObjects />`](#amp-lt-cq-defineobjects) definiert sind. Dies verkürzt und vereinfacht den JSP-Code Ihrer Komponente.

### &lt;cq:text> {#cq-text}

Das `<cq:text>`-Tag ist ein Hilfe-Tag, das Komponententext in JSP ausgibt.

Sie weist die folgenden optionalen Attribute auf:

**property** - Name der zu verwendenden Eigenschaft. Der Name ist relativ zur aktuellen Ressource.

**value** - Der für die Ausgabe zu verwendende Wert. Wenn dieses Attribut vorhanden ist, wird die Verwendung des Attributs „property“ überschrieben.

**oldValue** - Der für die diff-Ausgabe zu verwendende Wert. Wenn dieses Attribut vorhanden ist, wird die Verwendung des Attributs „property“ überschrieben.

**escapeXml** - Definiert, ob die Zeichen &lt;, >, &amp;, &#39; und &quot; in der daraus entstehenden Zeichenfolge in ihre entsprechenden Zeichenentitäts-Codes umgewandelt werden sollen. Der Standardwert ist „false“. Der Escape-Vorgang wird nach der optionalen Formatierung angewendet.

**format** - Optionales java.text.Format für die Formatierung des Textes.

**noDiff** - Unterdrückt die Berechnung einer diff-Ausgabe, auch wenn eine diff-Information vorhanden ist.

**tagClass** - CSS-Klassenname eines Elements, das eine nicht leere Ausgabe umgibt. Wenn leer, wird kein Element hinzugefügt.

**tagName** - Name des Elements, das eine nicht leere Ausgabe umgibt. Standardmäßig ist DIV eingestellt.

**placeholder** - Standardwert, der im Bearbeitungsmodus für null oder leeren Text verwendet wird, d. h. der Platzhalter. Die Standardprüfung wird nach der optionalen Formatierung und dem Escape-Vorgang durchgeführt, d. h. sie wird unverändert in die Ausgabe geschrieben. Standardwert ist:

`<div><span class="cq-text-placeholder">&para;</span></div>`

**default** - Standardwert, der für null oder leeren Text verwendet werden soll. Die Standardprüfung wird nach der optionalen Formatierung und dem Maskieren durchgeführt, d. h. sie wird unverändert in die Ausgabe geschrieben.

Beispiele für die Verwendung des `<cq:text>`-Tags in JSP:

```xml
<cq:text property="jcr:title" tagName="h2"/>
<cq:text property="jcr:description" tagName="p"/>

<cq:text value="<%= listItem.getTitle() %>" tagName="h4" placeholder="" />
<cq:text value="<%= listItem.getDescription() %>" tagName="p" placeholder=""/>

<cq:text property="jcr:title" value="<%= title %>" tagName="h3"/><%
    } else if (type.equals("link")) {
        %><cq:text property="jcr:title" value="<%= "\u00bb " + title %>" tagName="p" tagClass="link"/><%
    } else if (type.equals("extralarge")) {
        %><cq:text property="jcr:title" value="<%= title %>" tagName="h1"/><%
    } else {
        %><cq:text property="jcr:title" value="<%= title %>" tagName="h2"/><%

<cq:text property="jcr:description" placeholder="" tagName="small"/>

<cq:text property="tableData"
               escapeXml="false"
               placeholder="<img src=\"/libs/cq/ui/resources/0.gif\" class=\"cq-table-placeholder\" alt=\"\">"
    />

<cq:text property="text"/>

<cq:text property="image/jcr:description" placeholder="" tagName="small"/>
<cq:text property="text" tagClass="text"/>
```

### &lt;cq:setContentBundle> {#cq-setcontentbundle}

Das Tag `<cq:setContentBundle>` erstellt einen i18n-Lokalisierungskontext und speichert ihn in der `javax.servlet.jsp.jstl.fmt.localizationContext` Konfigurationsvariablen .

Sie weist die folgenden Attribute auf:

**language**: Die Sprache des Gebietsschemas, für das das Ressourcenpaket abgerufen werden soll.

**source** - Die Quelle, aus der das Gebietsschema übernommen werden soll. Sie kann auf einen der folgenden Werte eingestellt werden:

* **static**: Das Gebietsschema wird vom Attribut `language` übernommen, falls verfügbar, andernfalls vom standardmäßigen Server-Gebietsschema.

* **page**: Das Gebietsschema wird von der Sprache der aktuellen Seite oder Ressource übernommen, falls verfügbar, andernfalls vom Attribut `language`, falls verfügbar, oder andernfalls vom standardmäßigen Server-Gebietsschema.

* **request**: Das Gebietsschema wird vom angeforderten Gebietsschema (`request.getLocale()`) übernommen.

* **auto**: Das Gebietsschema wird vom Attribut `language` übernommen, falls verfügbar, andernfalls von der Sprache der aktuellen Seite oder Ressource, falls verfügbar, andernfalls von der Anfrage.

Wenn das `source` nicht festgelegt ist:

* Wenn das Attribut `language` festgelegt ist, ist für das Attribut `source` standardmäßig &quot;`static`.

* Wenn das Attribut `language` nicht festgelegt ist, ist für das Attribut `source` standardmäßig `auto`.

Das „Inhaltspaket“ kann von standardmäßigen JSTL-`<fmt:message>`-Tags verwendet werden. Nachrichten werden anhand von Schlüsseln in zweifacher Reihenfolge nachgeschlagen:

1. Zunächst werden die JCR-Eigenschaften der zugrunde liegenden Ressource, die gerendert wird, nach Übersetzungen durchsucht. Auf diese Weise können Sie ein einfaches Komponentendialogfeld definieren, um diese Werte zu bearbeiten.
1. Wenn der Knoten keine Eigenschaft mit dem exakt gleichen Namen wie das Schlüsselwort enthält, wird ein Ressourcenpaket aus der Sling-Anfrage geladen ( `SlingHttpServletRequest.getResourceBundle(Locale)`). Die Sprache oder das Gebietsschema für dieses Bundle wird durch die Sprach- und Quellattribute des `<cq:setContentBundle>`-Tags definiert.

Das `<cq:setContentBundle>`-Tag kann in einem JSP-Code wie folgt verwendet werden.

Für Seiten, die ihre Sprache definieren:

```xml
... %><cq:setContentBundle source="page"/><%  %>
<div class="error"><fmt:message key="Hello"/>
</div> ...
```

Für vom Benutzer personalisierte Seiten:

```xml
... %><cq:setContentBundle scope="request"/><% %>
<div class="error"><fmt:message key="Hello"/>
</div> ...
```

### &lt;cq:include> {#cq-include}

Das Tag `<cq:include>` fügt eine Ressource in die aktuelle Seite ein.

Sie weist die folgenden Attribute auf:

**flush**

* Ein boolescher Wert, der definiert, ob die Ausgabe vor dem Einschließen des Ziels geleert werden soll.

**path**

* Der Pfad zum Ressourcenobjekt, das in die aktuelle Anfrageverarbeitung aufgenommen werden soll. Wenn dieser Pfad relativ ist, wird er an den Pfad der aktuellen Ressource angehängt, deren Skript die angegebene Ressource enthält. „path“ und „resourceType“ oder „script“ müssen angegeben werden.

**resourceType**

* Der Ressourcentyp der einzuschließenden Ressource. Wenn der Ressourcentyp festgelegt ist, muss der Pfad der exakte Pfad zu einem Ressourcenobjekt sein: In diesem Fall wird das Hinzufügen von Parametern, Selektoren und Erweiterungen zum Pfad nicht unterstützt.
* Wenn die einzuschließende Ressource mit dem Pfadattribut angegeben wird, das nicht in eine Ressource aufgelöst werden kann, kann das Tag ein synthetisches Ressourcenobjekt aus dem Pfad und diesem Ressourcentyp erstellen.
* „path“ und „resourceType“ oder „script“ müssen angegeben werden.

**script**

* Das einzuschließende JSP-Skript. „path“ und „resourceType“ oder „script“ müssen angegeben werden.

**ignoreComponentHierarchy**

* Ein boolescher Wert, der steuert, ob die Komponentenhierarchie für die Skriptauflösung ignoriert werden soll. Wenn „true“, werden nur die Suchpfade berücksichtigt.

**Beispiel:**

```xml
<%@taglib prefix="cq" uri="https://www.day.com/taglibs/cq/1.0" %><%
%><div class="center">
    <cq:include path="trail" resourceType="foundation/components/breadcrumb" />
    <cq:include path="title" resourceType="foundation/components/title" />
    <cq:include script="redirect.jsp"/>
    <cq:include path="par" resourceType="foundation/components/parsys" />
</div>
```

Sollen `<%@ include file="myScript.jsp" %>` oder `<cq:include script="myScript.jsp" %>` verwendet werden, um ein Skript einzufügen?

* Die `<%@ include file="myScript.jsp" %>`-Direktive informiert den JSP-Compiler, dass er eine vollständige Datei in die aktuelle Datei einfügen soll. Es ist, als ob der Inhalt der eingeschlossenen Datei direkt in die Originaldatei eingefügt würde.
* Mit dem `<cq:include script="myScript.jsp">`-Tag wird die Datei zur Laufzeit eingebunden.

Sollten Sie `<cq:include>` oder `<sling:include>` verwenden?

* Bei der Entwicklung von AEM-Komponenten empfiehlt Adobe die Verwendung von `<cq:include>`.
* `<cq:include>` können Sie Skriptdateien bei Verwendung des script-Attributs direkt anhand ihres Namens einbeziehen. Dabei werden Komponenten- und Ressourcentypvererbung berücksichtigt. Diese ist häufig einfacher als die strikte Einhaltung der Skriptauflösung von Sling mithilfe von Selektoren und Erweiterungen.

### &lt;cq:includeClientLib> {#cq-includeclientlib}

>[!CAUTION]
>
>`<cq:includeClientLib>` Seit AEM 5.6 nicht mehr unterstützt. Stattdessen sollte `<ui:includeClientLib>` verwendet werden.

Das `<cq:includeClientLib>`-Tag enthält eine AEM-HTML-Client-Bibliothek, bei der es sich um eine JS-, CSS- oder Design-Bibliothek handeln kann. Für mehrere Einschlüsse verschiedener Typen, z. B. js und css, muss dieses Tag mehrmals in der JSP verwendet werden. Dieses Tag ist ein praktischer Wrapper für die `com.day.cq.widget.HtmlLibraryManager`-Service-Schnittstelle .

Sie weist die folgenden Attribute auf:

**categories** - Eine durch Kommas getrennte Liste der Client-Bibliothekskategorien. Dies umfasst alle JavaScript- und CSS-Bibliotheken für die angegebenen Kategorien. Der Design-Name wird aus der Anfrage extrahiert.

Entspricht: `com.day.cq.widget.HtmlLibraryManager#writeIncludes`

**theme** - Eine durch Kommas getrennte Liste der Client-Bibliothekskategorien. Dies umfasst alle designbezogenen Bibliotheken (CSS und JS) für die jeweiligen Kategorien. Der Design-Name wird aus der Anfrage extrahiert.

Entspricht: `com.day.cq.widget.HtmlLibraryManager#`writeThemeInclude

**js** - Eine durch Kommas getrennte Liste der Client-Bibliothekskategorien. Dies umfasst alle JavaScript-Bibliotheken für die angegebenen Kategorien.

Entspricht: `com.day.cq.widget.HtmlLibraryManager#writeJsInclude`

**css** - Eine durch Kommas getrennte Liste der Client-Bibliothekskategorien. Dies umfasst alle CSS-Bibliotheken für die angegebenen Kategorien.

Entspricht: `com.day.cq.widget.HtmlLibraryManager#writeCssInclude`

**themed** - Ein Flag, das angibt, ob nur designbezogene oder nicht designbezogene Bibliotheken enthalten sein sollen. Wenn ausgelassen, sind beide Sätze enthalten. Gilt nur für reine JS- oder CSS-Includes (nicht für Kategorien oder Design-Includes).

Das `<cq:includeClientLib>`-Tag kann in einem JSP-Code wie folgt verwendet werden:

```xml
<%-- all: js + theme (theme-js + css) --%>
<cq:includeClientLib categories="cq.wcm.edit" />

<%-- only js libs --%>
<cq:includeClientLib js="cq.collab.calendar, cq.security" />

<%-- theme only (theme-js + css) --%>
<cq:includeClientLib theme="cq.collab.calendar, cq.security" />

<%-- css only --%>
<cq:includeClientLib css="cq.collab.calendar, cq.security" />
```

### &lt;cq:defineObjects> {#cq-defineobjects}

Das Tag `<cq:defineObjects>` macht die folgenden, regelmäßig verwendeten Skriptobjekte verfügbar, auf die der Entwickler verweisen kann. Darüber hinaus werden die Objekte verfügbar gemacht, die durch das Tag [`<sling:defineObjects>`](#amp-lt-sling-defineobjects) definiert sind.

**componentContext**

* Das aktuelle Komponentenkontextobjekt der Anfrage (com.day.cq.wcm.api.components.ComponentContext-Schnittstelle).

**Komponente**

* Das aktuelle AEM-Komponentenobjekt der aktuellen Ressource (com.day.cq.wcm.api.components.Component-Schnittstelle).

**currentDesign**

* Das aktuelle Design-Objekt der aktuellen Seite (com.day.cq.wcm.api.designer.Design-Schnittstelle).

**currentPage**

* das aktuelle AEM WCM-Seitenobjekt (com.day.cq.wcm.api.Page-Schnittstelle).

**currentStyle**

* Das aktuelle Stilobjekt der aktuellen Zelle (com.day.cq.wcm.api.designer.Style-Schnittstelle).

**designer**

* Das Designer-Objekt, das zum Zugreifen auf Entwurfsinformationen verwendet wird (com.day.cq.wcm.api.designer.Designer-Schnittstelle).

**editContext**

* Bearbeiten Sie das Kontextobjekt der AEM-Komponente (com.day.cq.wcm.api.components.EditContext-Schnittstelle).

**pageManager**

* das Seiten-Manager-Objekt für Vorgänge auf Seitenebene (com.day.cq.wcm.api.PageManager-Schnittstelle).

**pageProperties**

* das Seiteneigenschaftenobjekt der aktuellen Seite (org.apache.sling.api.resource.ValueMap).

**Eigenschaften**

* das Eigenschaftenobjekt der aktuellen Ressource (org.apache.sling.api.resource.ValueMap).

**resourceDesign**

* das Design-Objekt der Ressourcenseite (com.day.cq.wcm.api.designer.Design-Schnittstelle).

**resourcePage**

* das Ressourcen-Seitenobjekt (com.day.cq.wcm.api.Page-Schnittstelle).
* Sie weist die folgenden Attribute auf:

**requestName**

* Von Sling geerbt

**responseName**

* Von Sling geerbt

**resourceName**

* Von Sling geerbt

**nodeName**

* Von Sling geerbt

**logName**

* Von Sling geerbt

**resourceResolverName**

* Von Sling geerbt

**slingName**

* Von Sling geerbt

**componentContextName**

* Spezifisch für WCM

**editContextName**

* Spezifisch für WCM

**propertiesName**

* Spezifisch für WCM

**pageManagerName**

* Spezifisch für WCM

**currentPageName**

* Spezifisch für WCM

**resourcePageName**

* Spezifisch für WCM

**pagePropertiesName**

* Spezifisch für WCM

**componentName**

* Spezifisch für WCM

**designerName**

* Spezifisch für WCM

**currentDesignName**

* Spezifisch für WCM

**resourceDesignName**

* Spezifisch für WCM

**currentStyleName**

* Spezifisch für WCM

**Beispiel**

```xml
<%@page session="false" contentType="text/html; charset=utf-8" %><%
%><%@ page import="com.day.cq.wcm.api.WCMMode" %><%
%><%@taglib prefix="cq" uri="https://www.day.com/taglibs/cq/1.0" %><%
%><cq:defineObjects/>
```

>[!NOTE]
>
>Wenn die `/libs/foundation/global.jsp`-Datei im Skript enthalten ist, wird das `<cq:defineObjects />`-Tag automatisch eingefügt.

### &lt;cq:requestURL> {#cq-requesturl}

Das Tag `<cq:requestURL>` schreibt die aktuelle Anforderungs-URL in JspWriter. Die beiden Tags [`<cq:addParam>`](#amp-lt-cq-addparam) und [`<cq:removeParam>`](#amp-lt-cq-removeparam) und können innerhalb dieses Tags verwendet werden, um die aktuelle Anforderungs-URL zu ändern, bevor sie geschrieben wird.

Damit können Sie Links zur aktuellen Seite mit unterschiedlichen Parametern erstellen. Beispielsweise können Sie damit die Anfrage transformieren:

`mypage.html?mode=view&query=something` in `mypage.html?query=something`.

Die Verwendung von `addParam` oder `removeParam` ändert nur das Auftreten des angegebenen Parameters, alle anderen Parameter sind nicht betroffen.

`<cq:requestURL>` weist kein Attribut auf.

Beispiele:

```xml
<a href="<cq:requestURL><cq:removeParam name="language"/></cq:requestURL>">remove filter</a>
```

```xml
<a title="filter results" href="<cq:requestURL><cq:addParam name="language" value="${bucket.value}"/></cq:requestURL>">${label} (${bucket.count})</a>
```

### &lt;cq:addParam> {#cq-addparam}

Das Tag `<cq:addParam>` fügt einen Anforderungsparameter mit dem angegebenen Namen und Wert zum umschließenden Tag [`<cq:requestURL>`](#amp-lt-cq-requesturl) hinzu.

Sie weist die folgenden Attribute auf:

**name**

* Name des hinzuzufügenden Parameters

**value**

* Wert des hinzuzufügenden Parameters

**Beispiel:**

```xml
<a title="filter results" href="<cq:requestURL><cq:addParam name="language" value="${bucket.value}"/></cq:requestURL>">${label} (${bucket.count})</a>
```

### &lt;cq:removeParam> {#cq-removeparam}

Das `<cq:removeParam>`-Tag entfernt einen Anforderungsparameter mit dem angegebenen Namen und Wert aus dem umschließenden [`<cq:requestURL>`](#amp-lt-cq-requesturl)-Tag. Wenn kein Wert angegeben wird, werden alle Parameter mit dem angegebenen Namen entfernt.

Sie weist die folgenden Attribute auf:

**name**

* Name des zu entfernenden Parameters

Beispiel:

```xml
<a href="<cq:requestURL><cq:removeParam name="language"/></cq:requestURL>">remove filter</a>
```

## Sling-Tag-Bibliothek {#sling-tag-library}

Die Sling-Tag-Bibliothek enthält hilfreiche Sling-Funktionen.

Wenn Sie die Sling-Tag-Bibliothek in Ihrem Skript verwenden, muss das Skript mit dem folgenden Code beginnen:

```xml
<%@ taglib prefix="sling" uri="https://sling.apache.org/taglibs/sling/1.0" %>
```

>[!NOTE]
>
>Wenn die `/libs/foundation/global.jsp` Datei im Skript enthalten ist, wird die Tag-Bibliothek von Sling automatisch deklariert.

### &lt;sling:include> {#sling-include}

Das Tag `<sling:include>` fügt eine Ressource in die aktuelle Seite ein.

Sie weist die folgenden Attribute auf:

**flush**

* Ein boolescher Wert, der definiert, ob die Ausgabe vor dem Einschließen des Ziels geleert werden soll.

**Ressource**

* Das Ressourcenobjekt, das in die aktuelle Anfrageverarbeitung eingeschlossen werden soll. Es muss entweder eine Ressource oder ein Pfad angegeben werden. Wenn beide angegeben sind, hat die Ressource Vorrang.

**path**

* Der Pfad zum Ressourcenobjekt, das in die aktuelle Anfrageverarbeitung aufgenommen werden soll. Wenn dieser Pfad relativ ist, wird er an den Pfad der aktuellen Ressource angehängt, deren Skript die angegebene Ressource enthält. Es muss entweder eine Ressource oder ein Pfad angegeben werden. Wenn beide angegeben sind, hat die Ressource Vorrang.

**resourceType**

* Der Ressourcentyp der einzuschließenden Ressource. Wenn der Ressourcentyp festgelegt ist, muss der Pfad der exakte Pfad zu einem Ressourcenobjekt sein: In diesem Fall wird das Hinzufügen von Parametern, Selektoren und Erweiterungen zum Pfad nicht unterstützt.
* Wenn die einzuschließende Ressource mit dem Pfadattribut angegeben wird, das nicht in eine Ressource aufgelöst werden kann, kann das Tag ein synthetisches Ressourcenobjekt aus dem Pfad und diesem Ressourcentyp erstellen.

**replaceSelectors**

* Beim Versenden werden die Selektoren durch den Wert dieses Attributs ersetzt.

**addSelectors**

* Beim Versenden wird der Wert dieses Attributs zu den Selektoren hinzugefügt.

**replaceSuffix**

* Beim Versand wird das Suffix durch den Wert dieses Attributs ersetzt.

>[!NOTE]
>
>Die Auflösung der Ressource und des Skripts, das im `<sling:include>`-Tag enthalten ist, ist dieselbe wie bei einer normalen URL-Auflösung in Sling. Standardmäßig werden die Selektoren, die Erweiterung usw. aus der aktuellen Anfrage auch für das enthaltene Skript verwendet. Sie können durch die Tag-Attribute geändert werden: Beispielsweise ermöglicht `replaceSelectors="foo.bar"` das Überschreiben der Selektoren.

Beispiele:

```xml
<div class="item"><sling:include path="<%= pathtoinclude %>"/></div>
```

```xml
<sling:include resource="<%= par %>"/>
```

```xml
<sling:include addSelectors="spool"/>
```

```xml
<sling:include resource="<%= par %>" resourceType="<%= newType %>"/>
```

```xml
<sling:include resource="<%= par %>" resourceType="<%= newType %>"/>
```

```xml
<sling:include replaceSelectors="content" />
```

### &lt;sling:defineObjects> {#sling-defineobjects}

Das Tag `<sling:defineObjects>` macht die folgenden, regelmäßig verwendeten Skriptobjekte verfügbar, auf die der Entwickler verweisen kann:

**slingRequest**

* SlingHttpServletRequest-Objekt, das Zugriff auf die HTTP-Anfrage-Header-Informationen bietet, die Standard-HttpServletRequest erweitert und Zugriff auf Sling-spezifische Elemente wie Ressource, Pfadinformationen und Selektor bietet.

**slingResponse**

* SlingHttpServletResponse-Objekt, das Zugriff auf die vom Server erstellte HTTP-Antwort bietet. Dies ist dasselbe wie die HttpServletResponse, von der aus sie erweitert wird.**Anfrage**
* Das standardmäßige JSP-Anfrageobjekt, das eine reine HttpServletRequest ist.**response**
* Das standardmäßige JSP-Antwortobjekt, das eine reine HttpServletResponse ist.

**resourceResolver**

* Das aktuelle ResourceResolver-Objekt. Es ist dasselbe wie slingRequest.getResourceResolver()

.**sling**

* Ein SlingScriptHelper-Objekt, das praktische Methoden für Skripte enthält, vor allem sling.include(&#39;/some/other/resource&#39;) zum Einschließen der Antworten anderer Ressourcen in diese Antwort (z. B. Einbetten von Kopfzeilen-HTML-Ausschnitten) und sling.getService(foo.bar.Service.class) zum Abrufen der in Sling verfügbaren OSGi-Dienste (Klassennotation abhängig von Skriptsprache).

**Ressource**

* das aktuelle zu verarbeitende Ressourcenobjekt, abhängig von der URL der Anfrage. Es ist dasselbe wie slingRequest.getResource().

**currentNode**

* Wenn die aktuelle Ressource auf einen JCR-Knoten verweist (was normalerweise in Sling der Fall ist), gewährt dies direkten Zugriff auf das Node-Objekt. Andernfalls ist dieses Objekt nicht definiert.

**log**

* Stellt einen SLF4J-Logger für die Protokollierung im Sling-Protokollsystem aus Skripten bereit, z. B. log.info(„Executing my script„).

* Sie weist die folgenden Attribute auf:

**requestName**

**responseName**

**nodeName**

l **ogName resourceResolverName**

**slingName**

**Beispiel:**

```xml
<%@page session="false" %><%
%><%@page import="com.day.cq.wcm.foundation.forms.ValidationHelper"%><%
%><%@taglib prefix="sling" uri="https://sling.apache.org/taglibs/sling/1.0" %><%
%><sling:defineObjects/>
```

## JSTL-Tag-Bibliothek {#jstl-tag-library}

Die [JavaServer Pages Standard Tag Library](https://www.oracle.com/java/technologies/java-server-tag-library.html) enthält viele nützliche und standardmäßige Tags. Die Tag-Bibliotheken für Kern, Formatierung und Funktionen werden durch die `/libs/foundation/global.jsp` definiert, wie im folgenden Ausschnitt gezeigt.

### Auszug aus /libs/foundation/global.jsp {#extract-of-libs-foundation-global-jsp}

```xml
<%@taglib prefix="c" uri="https://java.sun.com/jsp/jstl/core" %>
<%@taglib prefix="fmt" uri="https://java.sun.com/jsp/jstl/fmt" %>
<%@taglib prefix="fn" uri="https://java.sun.com/jsp/jstl/functions" %>
```

Nach dem Importieren der `/libs/foundation/global.jsp`-Datei wie zuvor beschrieben können Sie die Präfixe `c`, `fmt` und `fn` verwenden, um auf diese Tag-Bibliotheken zuzugreifen. Die offizielle Dokumentation der JSTL ist verfügbar unter [Das Java™ EE 5-Tutorial - standardmäßige Tag-Bibliothek JavaServer Pages](https://docs.oracle.com/javaee/5/tutorial/doc/bnakc.html).
