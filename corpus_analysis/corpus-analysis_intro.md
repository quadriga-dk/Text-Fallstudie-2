(corpus-analysis_intro)=
# Korpusanalyse 
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
```{admonition} Groblernziel dieses Kapitels
:class: lernziele
Sie können die auf einem Korpus ausgeführte Berechnung der Textkomplexität erklären und die Ergebnisse interpretieren.
```

Nachdem wir im vorherigem Kapitel ein Korpus gescraped und aus den HTML-Dokumenten den Text extrahiert haben, analysieren wir das Textkorpus in diesem Kapitel in Hinblick auf die Textkomplexität.

```{figure} ../assets/images/flow-chart_corpus-analysis.png
---
name: Flussdiagramm der Fallstudie – Korpusanalyse
---
Flussdiagramm der Fallstudie, das aktuelle Arbeitspaket ist hevorgehoben.
```

Dafür wird:
1. Konzeptionell in die Analyse der Textkomplexität und die verschiedenen Arten der Berechnung eingeführt (Kapitel [Textkomplexität](corpus-analysis_text_complexity))
2. Die Textkomplexität auf dem Korpus mit verschiedenen Algorithmen berechnet (Notebook [`corpus-analysis_analysis.ipynb`](corpus-analysis_analysis.ipynb))
3. Die errechnete Textkomplexität über Zeit visuell durch ein Liniendiagramm dargestellt. Das Diagramm bietet die Möglichkeit, die Ergebnisse unterschiedlich granular (Woche, Monat, Jahr) darzustellen (Kapitel [Analyse und Visualisierung](corpus-analysis_visualisation))
4. Das Diagramm interpretiert (Notebook [`corpus-analysis_visualization.ipynb`](corpus-analysis_visualization.ipynb))

