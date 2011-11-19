Trennen Sie immer Style von Inhalt
##################################

HTML Tags sollten nie für die Gestaltung verwendet werden - das ist die Arbeit von CSS (Cascading Style Sheets).

Sofern Sie nicht mit HTML markup durch Medien und nicht Ihren Webbrowser interagiert haben, scheint es nicht offensichtlich, dass Ihre Webseiten ein Leben außerhalb des Browserfensters haben, aber sie tun das sehr oft. Webseiten können von Menschen und Maschinen auf viele verschiedene Wege konsumiert werden!

Wenn Sie visuelle Aspekte (z.B. Style) von der eigentlichen Bedeutung eines Dokuments trennen, werden Sie mit einem Dokument enden, welches immer das Gleiche meint. Die Art, wie es dargestellt oder konsumiert wird, kann variieren. Eine bekannte Technik, die von Webdesignern verwendet wird, ist verschiedenen Stylesheets für verschiedene Medien zu verwenden. Zum Beispiel können Sie ein bestimmtes Stylesheet  nur verwenden, wenn ein Dokument auf auf Papier gedruckt ist, ein anderes wenn es auf dem Bildschirm angeschaut wird und wieder ein anderes, wenn von einem Browser mit Screenreader zugegriffen wird.

Ein Text-to-Screen Reader versteht auch die Tags <strong> oder <em>, aber er behandelt Textoutput mit diesen Tags sehr verschieden von dem, wie es ein visueller Browser tun würde. Der TTS (Text-to-Screen Reader) passt Ton und Volumen an, anstatt Kontrast oder Textstyle, welches dieselbe Bedeutung übermittelt, aber durch ein anderes Medium.

Vermeiden Sie Inline Styles
****************************

Ein Inline Style verliert viele der Vorteile von Stylesheets durch das Vermischen von Inhalt mit Präsentation. Es wird meistens verwendet, wenn man eine Formatierung an ein einziges Element in einer Webseite anwendet. Weil sie die spezifischsten im Cascade sind, können Sie Dinge überschreiben ohne, dass Sie es wollten und können nicht überschrieben werden, wenn Sie nicht das richtige Attribut verwenden. Inline Styles sind schwer zu pflegen.

   Anmerkung::

   Manche staatlichen Richtlinien zur Barrierefreiheit, wie z.B. die holländischen "Webrichtlijnen", 
   die überhaupt keine Inline Styles erlauben.

Der TYPO3 Kern bietet eine Methode an, die es ermöglicht, Inline Styles in eine temporäres, externes Stylesheet zu packen. Anstatt es zu Schreiben.

::

   <div style="width: 200px;">Content</div>

Sie können Folgendes in Ihrer Erweiterung verwenden:

::

   $plugin = 'tx_yourplugin.';
   $selector = '.width200';
   $declaration = 'width: 200px;';

   $GLOBALS['TSFE']->tmpl->setup['plugin.'][$plugin]['_CSS_PAGE_STYLE'][$selector] = $selector . ' { ' . $declaration . ' }';

Dies wird eine extra Linie zum temporären Stylesheet der Seite hinzufügen. Das temporäre Stylesheet "/typo3temp/stylesheet_xxx.css", in dem xxx ein Hash-Zeichenkette ist, ist meisten das Gleiche für jede Seite. Wenn extra Styles für jede Seite hinzugefügt werden, wird das Stylesheet mit diesen zusätzlichen Informationen geschrieben und bekommt einen anderen Namen, indem es eine andere Hash-Zeichenkette verwendet.

Ihr Container kann jetzt eine Klasse für Weite verwenden.

::

   <div class="width200">Content</div>

