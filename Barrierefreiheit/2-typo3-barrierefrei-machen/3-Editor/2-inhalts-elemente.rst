Inhalts Elemente
################

Die Dokumente ":doc:`../../1-MakingWebAccessible/2-principles`" und ":doc:`1-four-easy-tips`" decken die meisten der Barrierefreiheitspunkte ab, auf die man als Editor achten sollten. Jedoch gibt es ein paar TYPO3 Inhalts Elemente, die besondere Aufmerksamkeit brauchen:

Bilder
******

Unter dem Tab "Bilder" gibt es einen Abschnitt der "Barrierefreiheit" heißt. Dieser Abschnitt gibt Ihnen alle Felder, die für Barrierefreiheit verwendet werden können.

.. figure:: /Images/2-MakingTypo3Accessible/3-Editor/figure-2-3-1-1.png
      :align: center

      Figure 2-3-1-1: Images tab with Accessibility section

Alternative Beschreibung
  Fügen Sie für jedes Bild alternativen Text ein, einen pro Linie, der das Bild beschreibt, außer es hat keine Bedeutung. 
  Die alternative Beschreibung ist dazu bestimmt kurz zu sein.
Titel
  Die Titelattribute repräsentieren beratende Informationen für die Elemente, wie zum Beispiel für eine Kurzinfo. 
  Bei einem Link könnte das eine Beschreibung für die Zielquelle; bei einem Bild, könnte es den Namen des Fotografen 
  enthalten oder eine Beschreibung des Bildes; bei einem Paragraph kann es eine Fussnote oder ein Kommentar zum Text 
  ein; bei einem Zitat kann es weitere Information über die Quelle sein, usw. Das Wertvolle ist der Text. Titel für 
  Bilder sind nicht so wichtig, wie die alternativen Beschreibungen. Die Barrierefreiheit von Titelattributen ist der 
  unvorhersehbaren Kombination von schlechter Browserunterstützung, schlechten Screenreadern und schlechten Autoren 
  zum Opfer gefallen. Geben Sie nie die gleichen Informationen in die Felder von alternativer Beschreibung und Titel ein. 
Lange Beschreibungs-URLs
  In manchen Fällen ist ein Bild zu komplex, um es nur in ein paar Worten zu beschreiben. Diagramme und Schaubilder 
  sind erstklassige Beispiele dafür. Obwohl es nicht scheint, dass es ein Limit für die Länge eines alternativen 
  Textes gibt, ist die Beschreibung dazu gedacht kurz zu sein. Darum würde es ein Missbrauch des Attributes sein 
  mehr als ein paar Worte zu schreiben oder höchstens ein paar kurze Sätze. Die Antwort darauf ist einen kurzen 
  alternativen Beschreibungstext des Bildes bereit zu stellen und dann eine längere Beschreibung auf einer anderen Seite.

Bilder & Texte
**************

Dieser Link führt Sie zu `Bilder`_.

Tabellen
********

Der Zweck einer Tabelle ist Informationen in einem Raster oder Matrix zu präsentieren und Spalten und Reihen zu haben, die die Bedeutung der Informationen im Raster vermitteln. Wenn Screenreader direkt durch die Tabellen lesen, kann es leicht passieren, dass man den Faden verliert, besonders bei großen Tabellen. 

Um eine Tabelle barrierefrei zu machen, muss es das korrekte HTML Markup haben. Dann können sich User mit Screenreadern in Tabellen von Zeile zu Zeile navigieren und werden die Spalten und Reihenüberschriften ausgesprochen hören.

Hier sehen Sie, wie der Barrierefreiheitsabschnitt für das Inhalts Element "Tabelle" aussieht:

.. figure:: /Images/2-MakingTypo3Accessible/3-Editor/figure-2-3-1-2.png
      :align: center

      Figure 2-3-1-2: Table tab with Accessibility section

Tabellentitel (Table Caption)
  Tabellen sollten einen Titel oder eine Überschrift haben. Es ist nicht absolut notwendig für die Barrierefreiheit, aber trotzdem eine gute Übung.
Tabellenbeschreibung (Table Summary)
  Eine Tabellenbeschreibung ist keine Voraussetzung für einfache Tabellen, aber kann das Verständnis von komplexeren 
  Tabellen steigern bei Leuten, die Screenreader benutzen. Zum Beispiel kann man wichtige Elemente einer Tabelle 
  hervorheben und so dem User dadurch helfen nach was für Daten er in der Tabelle schauen muss.
Benutzen Sie die Tabellenfusszeile (Table Footer)
  Das Fusszeilen Element der Tabelle wird verwendet, um der Tabellenfusszeile, eine Beschreibung zu geben, zum Beispiel 
  die Summe aller Zeilen. Diesen nicht zu benutzen stellt kein Problem für die Barrierefreiheit dar. Es kann helfen, 
  wichtige Informationen hervorzuheben. 
Position der Tabellenkopfzeile (Table Header)
  Der erste Schritt eine barrierefreie Tabelle zu erstellen ist Reihen und Spaltenkopfzeilen zu benennen.
Keine CSS Styles für Tabellen
  Hat nichts mit Barrierefreiheit zu tun.
Weitere CSS Klasse
  Hat nichts mit Barrierefreiheit zu tun.

Dateienlinks
**********

Abhängig vom "Layout" Setting, welches man im "Appearance" Tab finden kann, wird ein Vorschau-Icon vor dem Dateienlink angezeigt. Dies ist ein Bild. Bilder brauchen eine alternative Beschreibung, wie unter 'Bilder' beschrieben, außer das Bild hat absolut keine Bedeutung. TYPO3 wird die automatische Beschreibung automatisch füllen, außer Sie überschreiben es mit dem Feld "Alternative Beschreibung für Icons/Thumbnails" im "Allgemein" Tab.

Menü/Sitemap
************

Aus Navigationsgründen ist es wichtig dem Menüpunkt einen Titel zuzuweisen. Der Titel wird dem User helfen sich in dem Menü zurecht zu finden. Ist das Menü nicht relevant für den User, sollte es die Möglichkeit geben, das Menü auszulassen. Dieser Punkt wird im "Barrierefreihet" Abschnitt im Tab "Allgemein" abgedeckt.

.. figure:: /Images/2-MakingTypo3Accessible/3-Editor/figure-2-3-1-3.png
      :align: center

      Figure 2-3-1-3: Accessibility section

Menüblocktitel (Mene block title)
  Der Titel gibt dem User Informationen über die Navigation, wie zum Beispiel "Hauptnavigation" oder "Kommende Veranstaltungen."
Fügen Sie einen Link zum Umgehungsnavigationsblock hinzu
  Dies wird am Anfang des Menüs/Navigation einen Link hinzufügen, um diesen Punkt auszulassen und zum nächsten zu gehen.
Linktext für Umgehungsnavigationsblock
  Ist es leer, verwendet TYPO3 Standardtext für den Link, um den Navigationsblock zu umgehen, wie zum Beispiel "Umgehe Navigation". 
  Sie können den Standardtext überschreiben.