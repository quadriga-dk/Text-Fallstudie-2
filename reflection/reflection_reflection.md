(reflection_reflection)=
# Reflexion
````{margin}
```{admonition} Fragen oder Feedback 
:class: frage-feedback

<a href="https://github.com/quadriga-dk/Text-Fallstudie-2/issues/new?assignees=&labels=question&projects=&template=frage.yml" class="external-link" target="_blank">
    Stellen Sie eine Frage
</a> <br>
<a href="https://github.com/quadriga-dk/Text-Fallstudie-2/issues/new?assignees=&labels=feedback&projects=&template=feedback.yml" class="external-link" target="_blank">
    Geben Sie uns Feedback
</a>

Mit Ihren Rückmeldungen können wir unser interaktives Lehrbuch gezielt an Ihre Bedürfnisse anpassen.

```
````

Mit der Analyse der Textkomplexität haben wir den in dieser Fallstudie entwickelten Meßvorgang abgeschlossen. Ausgehend von der Forschungsfrage, *wie sich die kommunikative Barrierearmut des Berliner Senats im Zeitraum von 2011 bis 2024 entwickelt*, haben wir das Konzept der Barrierearmut über die Leichte Sprache an Lesbarkeitsindizes gekoppelt, ein Korpus der Pressemitteilungen der Berliner Exekutive aufgebaut und die Textkomplexität über die Zeit ausgewertet. Die vier verwendeten Maße deuten dabei übereinstimmend auf eine zunehmende Textkomplexität hin. Zu beachten ist, dass ein hoher Flesch-Wert für eine leichtere Lesbarkeit steht (er sinkt über die Zeit), ein hoher Wert der drei übrigen Maße dagegen für eine schwerere (sie steigen). Gemessen an unserer Operationalisierung ist die Kommunikation des Senats also nicht barriereärmer, sondern eher barrierereicher geworden.

Dieser Befund bedarf allerdings der Einordnung. Ein Ergebnis ist nur so tragfähig wie die Operationalisierung, die ihm zugrunde liegt, und jede Operationalisierung in den Digital Humanities ist, wie wir bereits im Kapitel [Operationalisierung](research-question_operationalization) angemerkt haben, diskutabel. Wir treten daher zum Abschluss einen Schritt zurück und reflektieren Reichweite und Grenzen unseres Vorgehens.

## Kritische Bewertung: Reichweite und Grenzen

**1. Lesbarkeit ist nicht gleich Leichte Sprache.** Wir haben kommunikative Barrierearmut an das Konzept der Leichten Sprache gekoppelt und dieses über Lesbarkeitsindizes messbar gemacht. Leichte Sprache umfasst auf Wort-, Satz- und Textebene jedoch sehr viel mehr Merkmale, als in diese Indizes eingehen: den Verzicht auf Fremd- und Fachwörter, das Vermeiden von Negationen und komplexen Nominalphrasen, eine klare Absatzgliederung, vorangestellte Zusammenfassungen und vieles mehr. Die von uns genutzten Indizes beruhen dagegen im Kern auf der durchschnittlichen Wort- und Satzlänge {cite:p}`dubay_principles_2004`. Das sind leicht zu berechnende, aber grobe Näherungen: Sie korrelieren mit Verständlichkeit, sind aber nicht mit ihr identisch. Ein kurzer Satz kann inhaltlich schwierig, ein langer Satz gut verständlich sein.

**2. Die Maße selbst haben Grenzen.** Lesbarkeitsindizes wurden überwiegend für das Englische entwickelt und nur teilweise auf das Deutsche angepasst (etwa Flesch in der Adaption von Amstad oder die Wiener Sachtextformel). Ihre Gewichtungen bleiben Konventionen, die ein komplexes Phänomen auf wenige Oberflächenmerkmale reduzieren. Dass alle vier Maße übereinstimmend auf eine zunehmende Komplexität hindeuten, macht unseren Befund robuster. Allerdings teilen sie auch dieselbe blinde Stelle: ihren Fokus auf Längenmerkmale.

**3. Das Korpus ist ein Ausschnitt.** Unsere Analyse beruht auf einer Quelle, einer Textsorte und nur auf den digital verfügbaren Pressemitteilungen der Berliner Exekutive. Pressemitteilungen richten sich zudem primär an Medien und Multiplikator:innen und nicht unmittelbar an alle Bürger:innen; eigens erstellte Angebote in Leichter Sprache bleiben außen vor. Der Befund lässt sich daher nicht ohne Weiteres auf „die" Behördenkommunikation insgesamt, auf andere Verwaltungsebenen oder auf andere Bundesländer übertragen.

**4. Vom Messwert zur Deutung: Korrelation ist keine Ursache.** Der diachrone Trend zeigt, *dass* sich etwas verändert, nicht *warum*. Eine steigende Textkomplexität kann auch inhaltliche Gründe haben, etwa komplexere Themen, zunehmende Fachlichkeit oder längere Meldungen, und muss keine kommunikative Absicht widerspiegeln. Unsere Maße trennen den sprachlichen Stil nicht vom behandelten Inhalt. Die Interpretation des Befunds, der Schritt „from numbers to meaning" {cite:p}`heuser_learning_2011`, bleibt eine genuin geisteswissenschaftliche Aufgabe, die über die reine Messung hinausgeht.

## Von den Zahlen zur Bedeutung

Diese Einschränkungen entwerten den Befund nicht, sie grenzen seine Reichweite ein. Forschung in den Digital Humanities bewegt sich in einem Spannungsfeld: Auf der einen Seite steht die Möglichkeit, Aussagen über menschlich nicht mehr lesbare Textmengen zu treffen; auf der anderen Seite die quantitative Unschärfe und die Reduktion, die jede Operationalisierung mit sich bringt. Der Wert eines solchen Vorgehens liegt weniger im einzelnen Messwert als in der transparenten, nachvollziehbaren und reproduzierbaren Kette von Entscheidungen, die von der Fragestellung über die Operationalisierung bis zur Analyse führt und damit kritisierbar und nachnutzbar wird.

Genau darin lag das Erkenntnisinteresse dieser Fallstudie: nicht allein im Ergebnis, dass die Pressemitteilungen des Berliner Senats sprachlich komplexer geworden sind, sondern im exemplarischen Nachvollzug, wie sich eine qualitative Fragestellung mit quantitativ-computationellen Methoden bearbeiten lässt und wo die Grenzen dieser Bearbeitung liegen.

```{admonition} Kernpunkte des Kapitels
:class: keypoint
- Der Befund (zunehmende Textkomplexität, also abnehmende Barrierearmut) gilt **im Rahmen unserer Operationalisierung**.
- Lesbarkeitsindizes sind eine grobe Näherung an das reichere Konzept der Leichten Sprache; sie messen vor allem Wort- und Satzlänge.
- Das Korpus ist ein Ausschnitt (eine Quelle, eine Textsorte); der Befund ist nicht unbesehen verallgemeinerbar.
- Ein Trend zeigt eine Entwicklung, nicht ihre Ursache; die Deutung bleibt eine geisteswissenschaftliche Aufgabe.
```

__Bibliographie__
```{bibliography}
:filter: docname in docnames
```