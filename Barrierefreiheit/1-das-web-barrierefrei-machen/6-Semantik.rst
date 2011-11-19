Semantik
#########

Jeder, der heute eine eigene HTML Page erstellt, sollte anstreben sein Markup semantisch korrekt zu machen.

Was ist semantisches HTML?
**********************

Semantik ist die Studie von Bedeutung: Wie Bedeutung geschaffen und mit Zeichen angewandt wird. "Warum meint X X?" ist eine Frage der Semantik.

HTML ist die Markup-Sprache, die wir nutzen, um Webseiten zu schreiben. Es wird von Standardwebbrowsern verstanden, sowie Dutzenden von anderen Typen von "user agents", einschließlich Mobiltelefonen, Suchmaschinen-Crawlern, Hörbrowsern, etc.

HTML besteht aus 2 Typen von Dingen:

- Tags
- Textinhalt

Ein paar Tags können eigenen Inhalt bereitstellen (wie Bilder, Flashfilme, oder Metadaten), aber die meisten HTML Tags werden benutzt, um Struktur auf Inhalt anzuwenden.

Semantisches HTML, oder "semantisch richtiges HTML", ist HTML so dargestellt, dass die Tags, die dazu da sind Inhalt zu strukturieren, ausgewählt und passend zur Bedeutung des Inhalts angewendet werden.

Zum Beispiel, wenn Sie wollen, dass Ihr HTML semantisch-korrekt ist
 - Ein <p></p> Paragraph Tag Paar sollte nur verwendet werden, um einen Paragraph darzustellen (welches ein strukturelles Konzept ist). Es sollte nie verwendet werden, um freien Raum auf einer Webseite darzustellen. Verwenden Sie niemals  <p> Tags, um leeren Raum darzustellen!
 - Die HTML Tags <b></b> (für bold) und <i></i> (für italic) sollten nie verwendet werden, weil diese Format definieren, nicht die Struktur des Inhalts. Verwenden Sie stattdessen als Ersatz <strong></strong> und <em></em> (emphasis), welche automatisch Text in bold und italic umwandeln (aber eventuell nicht in allen Browsern), während die Tags zusätzlich dem Inhalt Bedeutung geben. 

Einfache Benutzung
******************

Zuerst einmal, semantisches HTML ist sauberes HTML. Es ist viel schneller zu lesen und zu bearbeiten, wenn es nicht mit extra Tags und Inlinestyling übersät ist. Sauberes Markup spart Zeit und Geld, wenn andere Leute damit Arbeiten müssen, wie zum Beispiel, wenn ein Entwickler Ihr Template in ein Content-Management-System oder andere Webapplikationen implementieren muss.

Ein andere Vorteil ist, dass Ihre HTML Dateien kleiner sind und schneller laden.