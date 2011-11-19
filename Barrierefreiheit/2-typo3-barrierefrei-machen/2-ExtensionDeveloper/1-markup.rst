Markup
######

Eine der ersten Grundregeln für Webdesign und Entwicklung ist es ein angemessenes Markup des Outputs entsprechend der technologischen Spezifikation zu haben. Technologische Spezifikation definiert die Bedeutung und korrekten Umgang mit den Eigenschaften der Technologie. Verwendet man diese Eigenschaften wie sie von der Spezifikation beschrieben sind, garantiert, dass User Agents, eingeschlossen Hilfstechnologien, in der Lage sein werden Repräsentationen der Eigenschaften anzuzeigen, die mit der Intention des Autors übereinstimmen und miteinander operabel sind. Diese technologische Spezifikation ist meistens von der Dokumenten Typ Declaration festgelegt.

WCAG 2.0 ist eine Empfehlung und beschreibt nur HTML 4.01 und XHTML 1.0. HTML 4.01 ist die neueste Version von HTML, die spezifische barrierefreie Eigenschaften anbietet und wird von vielen User Agents unterstützt. XHTML 1.0 bietet die gleichen Eigenschaften an wie HTML 4.01, außer dass es eine XML Struktur verwendet und einen strengeren Syntax als die HTML Struktur hat. WCAG 2.0 unterstützt keine ältere Version dieser Technologien, weil diese nicht als ausgereift betrachtet werden und/oder nicht von vielen User Agents unterstützt werden. Dies beinhaltet XHTML 1.1 und HTML5.

HTML5 ist immernoch ein Entwurf und wird es wahrscheinlich noch eine Weile bleiben bevor es zu einer Empfehlung weiter geht. XHTML 1.1 ist seit 2001 eine Empfehlung und wurde 2010 einer zweiten Revision unterzogen. Es scheint, als würde das W3C denken, dass diese Spezifikation immernoch  genug und gut unterstützt wird von User Agents.

Wie auch immer, dies bedeutet nicht, dass Sie diese Spezifikation nicht benutzen können. HTML5 wurde mit dem Gedanken einer besseren Semantik und Barrierefreiheit entwickelt.


Document Type Declaration
*************************

Obwohl die DTD in TYPO3 konfigurierbar ist, hat sich der Kern nicht um ein geeignetes Markup gekümmert bis Version 4.7. Um mehr spezifisch zu sein, der ganze Output war XHTML. Ungültige Tags, wie z.B. img, input, br und hr, bekamen immer ihren Schluss-Slash, sogar, wenn DTD als HTML 4.0 Transitional spezifiert war, was eigentlich der Standard Dokumententyp in TYPO3 ist.

No config.doctype set: HTML 4.0 Transitional:

::

   <img src="myimage.jpg" alt="My Image" />

which should be:

::

   <img src="myimage.jpg" alt="My Image">

Attribute folgten auch nicht den Regeln eines Dokumententyps. Zum Beispiel ist das Zielattribut nicht erlaubt für die meisten XHTML Spezifikationen, außer XHTML 1.0 Frameset, aber wurde trotzdem hinzugefügt.

Wenn man barrierefreie Erweiterungen schreibt, müssen Sie bei diesem Thema aufpassen! Das Markup sollte komplett den Auflagen der DTD entsprechen.

Templating
==========

Die meisten Erweiterungen kommen mit vordefinierten (X)HTML Templates. Die Erweiterungsentwickler entscheiden, welche Spezifikation bei diesem Template eingesetzt wird und meistens wird das XHTML sein.

Weil HTML5 spät gefördert wurde, sollten Sie in Betracht ziehen Templates in verschiedenen Dokumententypen abzuliefern, so dass Sie vollen Vorteil aus der HTML5 Semantik schöpfen können. Dies wird dem TYPO3-Integrator helfen, wenn er nicht das Markup des Templates ändern muss, weil die DTD, die er für die Webseite gewählt hat, nicht mit Ihrer Erweiterungstemplate DTD übereinstimmt.   

Um die config.doctype Settings in Typoscript zu kontrollieren, können Sie dies benutzen:


::

   TSFE:config|config|doctype

Dies wird Ihnen den Wert, den Sie in die config.doctpy eingegeben haben, geben. Sie können das kontrollieren, indem Sie Konditionen verwenden, wenn es Statements oder Fälle sind.

Wenn Sie Zielattribute verwenden in TypoScript, können Sie schauen, ob die DTD Frames zulässt.

::

   TSFE:dtdAllowsFrames

This will return TRUE or FALSE.

Coding
======

Der TYPO3 Kern verwendet keine Templates für Frontend Output. Alles in (X)HTML ist in PHP generiert. Dies passiert auch häufig in Erweiterungen, weil manche Probleme nicht mit Templates gelöst werden können.

Die oberen Settings können auch in PHP verwendet werden:

::

   $GLOBALS['TSFE']->config['config']['doctype']
   $GLOBALS['TSFE']->dtdAllowsFrames

Es werden die gleichen Werte herauskommen, wie oben schon erwähnt.
