Wie Sie Ihre TYPO3 Webseite barrierefrei machen
################################################

Eine Webseite barrierefrei machen kann einfach oder komplex sein, dies hängt von vielen Faktoren ab, wie zum Beispiel dem Inhaltstyp, die Größe, die Komplexität der Seite und die Entwicklerwerkzeuge und Umwelt.

Viele barrierefreie Eigenschaften sind leicht zu implementieren, wenn Sie von Anfang an bei der Webseitenentwicklung oder Umgestaltung eingeplant sind. Diese unzugänglichen Webseiten können signifikanten Aufwand benötigen, besonders Seiten, die nicht korrekt mit Standard X(HTML) markup geschrieben wurden und Seiten mit bestimmten Inhaltstypen wie Multimedia.

Seit TYPO3 4.7 gibt es die Inhaltselemente css_styled_content (außer FORM und SEARCH), um ein geeignetes Markup zu verwenden, egal was für ein Dokumententyp ausgewählt ist. Zum Beispiel beinhalten Void Tags (zum Beispiel selbstschließend) einen Schluss-Slash, wenn eine XHTML Dokumententyp verwendet wird, aber nicht, wenn ein HTML Dokumententyp verwendet wird. Attribute werden nur verwendet, wenn sie vom Dokumententyp erlaubt werden.

Dieses Dokument wird Ihnen Wege aufzeigen, die Integratoren, Erweiterungsentwickler und Editoren helfen werden, die Richtlinien zur Barrierefreiheit umzusetzen.

.. toctree::
   :maxdepth: 2

   2-ExtensionDeveloper/Index
   3-Editor/Index