WAI-ARIA
########

WAI-ARIA, Accessible Rich Internet Applications Suite, definiert einen Weg, um Webinhalt und Applikationen barrierefrei für Menschen mit Behinderungen zugänglich zu machen. Es hilft besonders bei dynamischem Inhalt und fortgeschrittener Benutzeroberfläche, die mit Ajax, HTML, JavaScript und verwandten Technologien entwickelt wurde. Momentan ist eine bestimmte Funktionalität, die auf Webseiten genutzt wird, nicht verfügbar für Menschen mit Behinderungen, besonders Menschen, die auf einen Screenreader angewiesen sind oder keine Maus benutzen können. WAI-ARIA ist an diese Zugangsherausforderungen adressiert, zum Beispiel bei der Definition von neuen Funktionswegen von Hilfstechnologien. Mit WAI-ARIA können Entwickler fortgeschrittene Webapplikationen zugänglich und nutzbar für Menschen mit Behinderungen machen.

ARIA gehört nicht zu HTML5, es ist eine Spezifikation, die vom W3C geschrieben wurde und nutzt Attribute anstatt Elementen. Es ist konstruiert, um jegliche Auszeichnungssprache zu ergänzen, nicht nur HTML. Es kann auch mit SVG, Adobe's MXML und anderen genutzt werden.

ARIA Informationen zu HTML4 hinzuzufügen hilft der Barrierefreiheit, aber das HTML-Dokument wird nicht länger valide sein. Weil HTML5 immer noch in der Entwicklung ist, werden ARIA Attribute in HTML5 validiert sein. Nicht nur das, sondern auch bestimmte Korrespondenz zwischen den zwei Spezifizierungen in der HTML5 spec; manche Elemente haben eingebaute ARIA Rollen, die nicht überschritten werden können.

.. Anmerkung::

   Die Protocols and Formats Working Group (PFWG) veröffentlichte WAI-ARIA 1.0 als
   W3C Candidate Recommendation am 18 Januar 2011.

Ajax und verwandte Technologien zugänglich machen
*************************************************

Webseiten benutzen immer mehr fortgeschrittene und komplexere Benutzer-Interfacesteuerungen, wie zum Beispiel Baumstrukturen für die Webseiten-Navigation. Um eine barrierefreie Benutzer-Erfahrung für Menschen mit Behinderungen zu gewährleisten, müssen Hilfstechnologien in der Lage sein mit diesen Steuerungen zu interagieren. Wie auch immer, die Informationen, die die Hilfstechnologien brauchen, ist nicht mit den meisten Webtechnologien erhältlich.

Ein anderes Beispiel eines Zugangshindernisses ist die Drag-and-Drop Funktionalität, die für Benutzer, die sich nur mit der Tastatur auf der Webseite bewegen können, nicht nutzbar ist. Sogar relativ einfache Webseiten können Herausforderungen darstellen, wenn die Tastatur-Navigation viele Tastenschläge braucht.

Viele Webapplikationen, die mit Ajax, DHTML und anderen Technologien entwickeln wurden, stellen der Barrierefreiheit zusätzliche Herausforderungen. Zum Beispiel: Wenn sich der Inhalt einer Webseite auf Grund einer Useraktion oder zeitbasierten oder ereignisbasierten Updates verändert, neuer Inhalt ist vielleicht nicht zugänglich für Menschen, die blind sind, oder Menschen mit kognitiven Behinderungen, die einen Screenreader nutzen.

WAI-ARIA spricht diese Zugangsherausforderungen durch Definieren an, wie Informationen über diese Funktionaliät, Hilfstechnologien zur Verfügung gestellt werden. Mit WAI-ARIA kann eine fortgeschrittene Webapplikation zugänglich und nutzbar gemacht werden für Menschen mit Behinderungen.

Technische Lösungen
===================

Genauer gesagt stellt WAI-ARIA ein Gerüst bereit, das es möglich macht Attribute hinzuzufügen, um Merkmale für User-Interaktionen zu identifizieren, wie diese miteinander verknüpft sind und ihren aktuellen Status. WAI-ARIA beschreibt neue Navigationstechniken, um Regionen und gängige Webstrukturen wie Menüs, primären Inhalt, sekundären Inhalt, Bannerinformationen und andere Typen von Webstrukturen aufzuzeigen. Zum Beispiel können Entwickler mit WAI-ARIA Regionen von Webseiten identifizieren und es so Tastaturbenutzern einfacher ermöglichen, sich zwischen Regionen zu bewegen, anstatt viele Male Tab drücken.

WAI-ARIA beinhaltet auch Technologien, um Steuerungen abzubilden, Ajax live Regionen und Ereignisse zu APIs (accessibility applikation programming interfaces), einschließlich benutzerdefinierter Steuerung für Applikationen mit viel Text. WAI-ARIA Techniken lassen sich auf Widgets, Buttons, Drop-Down Listen, Kalenderfunktionen und Baumstrukturen anwenden (zum Beispiel erweiterbare Menüs) und Andere.

WAI-ARIA stellt Folgendes für Webautoren bereit:

- Funktionen, um das dargestellte Widget zu beschreiben, wie zum Beispiel "menu," "treeitem," "slider," und "progressmeter"
- Funktionen, um die Struktur der Webseite zu beschreiben, wie zum Beispiel Überschriften, Regionen und Tabellen (Raster)
- Eigenschaften, um den Status der Widgets zu beschreiben, wie zum Beispiel "checked" für eine Checkbox oder "haspopup" für ein Menü
- Eigenschaften, um live Regionen einer Webseite zu definieren, bei denen die Möglichkeit besteht, Updates zu bekommen (wie z.B. stock quotes), sowie eine Unterbrechungsstrategie für diese Updates. Zum Beispiel kritische Updates werden in einer Dialogalarmbox dargestellt und zufällige Updates werden innerhalb der Webseite auftauchen
- Eigenschaften für drag-and-drop die drag-Quellen beschreiben und drop-Ziele darstellen
- Ein Weg um Tastaturnavigation bereit zu stellen für Webobjekte und Ereignisse, wie zum Beispiel die oben erwähnten 