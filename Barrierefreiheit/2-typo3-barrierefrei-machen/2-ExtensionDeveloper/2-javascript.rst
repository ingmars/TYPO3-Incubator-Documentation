Javascript
##########

JavaScript erlaubt Entwicklern vermehrt Interaktionen hinzuzufügen, Informationen zu verarbeiten und webbasierten Inhalt zu kontrollieren. JavaScript kann aber auch ein Problem für die Barrierefreiheit darstellen, indem es die Navigation durch Tastatur oder Hilfstechnologien einschränkt, Inhalt oder Funktionalität präsentiert, welcher nicht für Hilfstechnologien zugänglich ist, Benutzerkontrolle limitiert über automatische Inhaltsänderungen und die normale Funktionalität der Browser modifiziert.

Wenn Sie mit Problemen der Barrierefreiheit in JavaScript konfrontiert werden, müssen Sie eines der folgenden Dinge tun:

- Stellen Sie sicher, dass JavaScript direkt zugänglich ist
- Stellen Sie barrierefreie, nicht-JavaScript Alternativen bereit

JavaScript wird häufig für kosmetische oder ander Inhaltsänderungen verwendet, welche nicht die Barrierefreihet beeinträchtigen. Inhalt, der für die Seite mit JavaScript geschrieben wurde ist barrierefrei, wenn:

- Gerätunabhängige Vorgänge verwendet werden
- JavaScriptfähiger Inhalt und Funktionalität barrierefrei für Hilfstechnologien ist
- Scripted Seiten und Elemente sind navigierbar mit der Tastatur sind
- Die normale Browserfunktionalität ist nicht modifiziert auf eine Art, welche vielleicht Verwirrung oder Unzugänglichkeit verursachen könnte
- Eine barrierefreie Alternative ist bereitgestellt, wenn JavaScript nicht auf natürliche Weise zugänglich gemacht werden kann

Sollte ich überhaupt JavaScript benutzen?
*****************************************

Natürlich solltest Du! Stell Dir eine Web 2.0 Webseite ohne JavaScript vor. Die meisten Hilfstechnologien wissen, wie man JavaScript behandeln muss. WAI-ARIA hilft besonders mit dynamischem Inhalt und fortgeschrittenen Benutzer Interface Steuerung, die mit Ajax, HTML, JavaScript und verwandten anderen Technologien entwickelt wurden.

JavaScript Alternativen
***********************

Es gibt viele Möglichkeiten, um Alternativen für JavaScript darzustellen. Neuere Versionen von CSS lassen viel Verhalten von JavaScript zu, welches einzigst durch die Kopie des CSS stattfindet. Drop-Down Menüs, Navigationsbalken und interaktive Bilder können alle entwickelt werden ohne sich auf JavaScript zu verlassen. Wie auch immer, die Implementierung von CSS über die Browser und Hilfstechnologien ist variabel und problematsich. Wenn JavaScript selbst nicht natürlich zugänglich gemacht werden kann, müssen Sie barrierefreie Alternativen bereitstellen. Dies kann durch Kopieren oder Ersetzen des JavaScript Verhaltens mit Prozessen auf der Server-Seite. Sie können auch <noscript> Inhalt bereitstellen, welcher zugänglich gemacht wird, wenn JavaScript deaktiviert und nicht zugänglich zu dem Enduser ist.

