---
jupytext:
  formats: md:myst
  text_representation:
    extension: .md
    format_name: myst
---

# 🏆Selbsttest: Wissen und Praxis

````{admonition} Hinweis
:class: hinweis
Diese Übungsaufgaben dienen Ihrer Selbsteinschätzung und helfen Ihnen, das im Kapitel Gelernte zu reflektieren.

Sie können die Fragen in beliebiger Reihenfolge beantworten und auch mehrfach versuchen. 

**So funktioniert es:**
- Wählen Sie bei jeder Frage die Antwort(en), die Sie für richtig halten
- Lesen Sie das Feedback zu den einzelnen Antwortoptionen sorgfältig durch
- Die Erklärungen helfen Ihnen, Ihr Verständnis zu vertiefen – auch bei korrekten Antworten 

Es erfolgt keine Bewertung oder Speicherung Ihrer Ergebnisse. Nutzen Sie dieses Assessment, um Wissenslücken zu identifizieren und gegebenenfalls die entsprechenden Abschnitte des Kapitels noch einmal zu bearbeiten. 

**Geschätzte Zeit**: 15–25 min.

Viel Erfolg!
````

## Frage 1

```{code-cell} ipython3
:tags: [remove-input]
from jupyterquiz import display_quiz

import sys
sys.path.append("..")
from quadriga import colors

question1 = [
    {
        "question": "Welche Aussagen über Parameter auf Wortebene zur Berechnung der Textkomplexität sind korrekt? Wählen Sie alle zutreffenden Aussagen.",
        "type": "multiple_choice",
        "answers": [
            {
                "answer": "Die Anzahl der Buchstaben auf 100 Wörter berücksichtigt die Gleichverteilung der Textschwierigkeit",
                "correct": True,
                "feedback": """✓ Korrekt! Wichtige Differenzierung: Es geht nicht nur um die absolute Wortlänge, der Text wird dabei in Abschnitte unterteilt, und es wird die Konsistenz der Schwierigkeit gemessen. Dies wird im Coleman-Liau-Index verwendet und unterscheidet sich von der einfachen durchschnittlichen Wortlänge."""
            },
            {
                "answer": "Wörter mit mehr als drei Silben gelten in den meisten Indexe als schwer",
                "correct": True,
                "feedback": """✓ Korrekt! Standard-Schwellenwert: 1-2 Silben gelten als leicht, 3 und mehr Silben gelten als schwer. Dies wird in der Wiener Sachtextformel verwendet, ist sprachabhängig (Silbentrennung) und ein wichtiger Parameter für die Komplexität."""
            },
            {
                "answer": "Die absolute Wortlänge in Buchstaben ist aussagekräftiger als die Silbenzahl",
                "correct": False,
                "feedback": """× Nicht generell korrekt. Wichtige Unterscheidung: Beide haben Vor- und Nachteile, die Silbenzahl ist sprachabhängig und näher an der Aussprache, während die Buchstabenzahl sprachunabhängig und einfacher zu berechnen ist. Der ARI nutzt Buchstaben, Flesch nutzt Silben, und es besteht keine klare Überlegenheit."""
            },
            {
                "answer": "Schwierige Wörter werden immer über ein vordefiniertes Wörterbuch ermittelt, nie über Wortlänge oder Silbenzahl",
                "correct": False,
                "feedback": """× Nicht korrekt. Verschiedene Ansätze: Die Wiener Sachtextformel ist wörterbuch-basiert, andere Indexe arbeiten über Länge beziehungsweise Silben. Beide Methoden existieren parallel, das Wörterbuch ist EIN Ansatz, nicht der einzige."""
            }
        ]
    }
]
display_quiz(question1, colors=colors.jupyterquiz)
```

## Frage 2

```{code-cell} ipython3
:tags: [remove-input]
from jupyterquiz import display_quiz

import sys
sys.path.append("..")
from quadriga import colors

question2 = [
    {
        "question": "Welche Aussagen über Parameter auf Satzebene zur Berechnung der Textkomplexität sind korrekt? Wählen Sie alle zutreffenden Aussagen.",
        "type": "multiple_choice",
        "answers": [
            {
                "answer": "Die Anzahl der Sätze auf 100 Wörter ist ein indirektes Maß für die Satzlänge",
                "correct": True,
                "feedback": """✓ Korrekt! Clevere Umkehrung: Mehr Sätze pro 100 Wörter bedeuten kürzere Sätze, weniger Sätze pro 100 Wörter bedeuten längere Sätze. Dies wird im Coleman-Liau-Index verwendet, die Normalisierung ermöglicht Vergleichbarkeit und bietet eine alternative Perspektive zur direkten Satzlänge."""
            },
            {
                "answer": "Der Durchschnitt wird berechnet, indem man die Längen aller Sätze summiert und durch die Anzahl der Sätze teilt",
                "correct": True,
                "feedback": """✓ Korrekt! Standardberechnung: Die Summe aller Satzlängen wird durch die Anzahl der Sätze geteilt, dies glättet Extremwerte und liefert einen repräsentativen Wert für den gesamten Text. Es wird in Flesch, Wiener und ARI verwendet und bildet die Basis für die meisten Berechnungen."""
            },
            {
                "answer": "Kürzere Sätze führen immer zu einem niedrigeren Textkomplexitätsscore in allen Indexe",
                "correct": False,
                "feedback": """× Nicht präzise genug. Wichtige Nuance: Die Richtung hängt vom Index ab, bei Flesch bedeutet ein höherer Score einen leichteren Text (kürzere Sätze), bei Wiener/ARI bedeutet ein niedrigerer Score einen leichteren Text (kürzere Sätze). Dies ist nicht einheitlich über alle Indexe, die Beziehung ist konsistent, aber die Skalen unterscheiden sich."""
            },
            {
                "answer": "Die maximale Satzlänge im Text ist wichtiger als die durchschnittliche Satzlänge",
                "correct": False,
                "feedback": """× Nicht korrekt. Standard-Praxis: Der Durchschnitt ist der Standard-Parameter, das Maximum würde eine Verzerrung erzeugen, da ein einzelner langer Satz nicht repräsentativ ist. Indexe verwenden durchschnittliche Werte, weil diese robuster gegenüber Ausreißern sind."""
            }
        ]
    }
]
display_quiz(question2, colors=colors.jupyterquiz)
```

## Frage 3

```{code-cell} ipython3
:tags: [remove-input]
import sys
sys.path.append("../quadriga")
from assessment import DragDropQuiz

quiz = DragDropQuiz()

quiz.create_matching_quiz(
    title="Ordnen Sie die Lesbarkeitsindizes den passenden Beschreibungen zu:",
    descriptions=[
        "Am weitesten verbreitet, operiert auf Satzlänge und Silbenanzahl",
        "Speziell für deutsche Sachtexte entwickelt, nutzt schwierige Wörter",
        "Operiert rein auf Längenmaßen (Zeichen, Wörter, Sätze)",
        "Basiert auf Buchstaben und Sätzen pro 100 Wörter"
    ],
    options=["Flesch-Lesbarkeitsindex", "Wiener Sachtextformel", "Automated Readability Index (ARI)", "Coleman-Liau-Index", "SMOG-Index"],
    correct_mapping={
        "Am weitesten verbreitet, operiert auf Satzlänge und Silbenanzahl": "Flesch-Lesbarkeitsindex",
        "Speziell für deutsche Sachtexte entwickelt, nutzt schwierige Wörter": "Wiener Sachtextformel",
        "Operiert rein auf Längenmaßen (Zeichen, Wörter, Sätze)": "Automated Readability Index (ARI)",
        "Basiert auf Buchstaben und Sätzen pro 100 Wörter": "Coleman-Liau-Index"
    }
)
```

## Frage 4

```{code-cell} ipython3
:tags: [remove-input]
from jupyterquiz import display_quiz

import sys
sys.path.append("..")
from quadriga import colors

question4 = [
    {
        "question": "Was ist die korrekteste Aussage über die Interpretation von Lesbarkeitsindizes?",
        "type": "multiple_choice",
        "answers": [
            {
                "answer": "Die meisten Scores lassen sich in eine Klassenstufe oder Bildungsniveau übersetzen, wobei ein niedriger Score meist einen schweren Text und ein hoher Score einen leichten Text bedeutet",
                "correct": False,
                "feedback": """× Teilweise korrekt, aber umgekehrt! Wichtige Korrektur: Ein niedriger Score bedeutet bei den meisten Indexen einen leichteren Text, ein hoher Score bedeutet einen schwereren Text. Flesch kann je nach Version variieren, die Richtung ist entscheidend!"""
            },
            {
                "answer": "Die meisten Scores lassen sich in eine Klassenstufe übersetzen, und ein niedriger Score bedeutet meist einen leichten Text",
                "correct": True,
                "feedback": """✓ Korrekt! Das ist die Standardinterpretation: Ein niedriger Score bedeutet einen leichteren Text, ein hoher Score einen schwereren Text. Dies ermöglicht eine Klassenstufen-Zuordnung (z.B. 5. Klasse bis Uni) und ist praktisch für die Zielgruppenbestimmung; wichtig ist dabei, dass sich die Skalen zwischen den Indexen unterscheiden!"""
            },
            {
                "answer": "Alle Lesbarkeitsindizes verwenden dieselbe Skala von 0-100, was den Vergleich erleichtert",
                "correct": False,
                "feedback": """× Nicht korrekt. Wichtiger Hinweis: Es gibt unterschiedliche Skalen, etwa Flesch (0-180), Wiener (4-15) und ARI (1-14+), die NICHT direkt vergleichbar sind. Dies ist wichtig für die korrekte Interpretation, denn jeder Index hat eine eigene Normierung."""
            },
            {
                "answer": "Höhere Textkomplexität bedeutet immer bessere Textqualität, unabhängig von der Zielgruppe",
                "correct": False,
                "feedback": """× Nicht korrekt. Wichtige Differenzierung: Komplexität ist nicht gleich Qualität, sondern zielgruppenabhängig. Barrierefreiheit erfordert oft eine niedrige Komplexität, und einfache Texte können durchaus hochwertig sein."""
            }
        ]
    }
]
display_quiz(question4, colors=colors.jupyterquiz)
```

## Frage 5

```{code-cell} ipython3
:tags: [remove-input]
from jupyterquiz import display_quiz

import sys
sys.path.append("..")
from quadriga import colors

question6 = [
    {
        "question": "Was ist der Hauptvorteil von Liniendiagrammen gegenüber Balkendiagrammen für die Darstellung zeitlicher Entwicklungen?",
        "type": "multiple_choice",
        "answers": [
            {
                "answer": "Liniendiagramme zeigen Häufigkeiten in diskreten Zeitintervallen besser",
                "correct": False,
                "feedback": """× Nicht korrekt. Das ist tatsächlich umgekehrt: Balkendiagramme eignen sich gut für diskrete Intervalle, während Liniendiagramme besser für kontinuierliche Entwicklungen geeignet sind. Für Häufigkeiten in Intervallen sind daher Balken besser geeignet, für zeitliche Trends dagegen Linien."""
            },
            {
                "answer": "Liniendiagramme ermöglichen die bessere Erkennung von Trends und Mustern über Zeit, da die Verbindung zwischen Zeitpunkten visualisiert wird",
                "correct": True,
                "feedback": """✓ Korrekt! Das ist der zentrale Vorteil: Die Kontinuität wird sichtbar gemacht, Trends sind leicht erkennbar (steigend/fallend) und Minima sowie Maxima werden deutlich. Verbindungslinien zeigen die Entwicklung und sind ideal für diachrone Analysen."""
            },
            {
                "answer": "Liniendiagramme können keine Zeitachse auf der X-Achse darstellen",
                "correct": False,
                "feedback": """× Nicht korrekt. Im Gegenteil: Die X-Achse wird typischerweise für die Zeit verwendet, was eine natürliche chronologische Darstellung ermöglicht. Verschiedene Zeiteinheiten sind möglich, dies ist Standard für Zeitreihen."""
            },
            {
                "answer": "Liniendiagramme zeigen einzelne Datenpunkte genauer als Balkendiagramme",
                "correct": False,
                "feedback": """× Nicht der Hauptvorteil. Wichtig: Beide zeigen Datenpunkte, die Genauigkeit ist ähnlich. Der Hauptvorteil liegt in der Trendvisualisierung, Verbindungslinien sind das zentrale Element."""
            }
        ]
    }
]
display_quiz(question6, colors=colors.jupyterquiz)
```

## Frage 6

```{code-cell} ipython3
:tags: [remove-input]
from jupyterquiz import display_quiz

import sys
sys.path.append("..")
from quadriga import colors

question7 = [
    {
        "question": "Wie wird eine diachrone Analyse der Textkomplexität durchgeführt? Wählen Sie alle zutreffenden Aussagen.",
        "type": "multiple_choice",
        "answers": [
            {
                "answer": "Textkomplexität wird für jede Pressemitteilung einzeln berechnet",
                "correct": True,
                "feedback": """✓ Korrekt! Individuelle Berechnung: Jeder Text erhält einen eigenen Score, der die Basis für die weitere Aggregation bildet. Dies ermöglicht eine detaillierte Analyse und ist ein notwendiger erster Schritt."""
            },
            {
                "answer": "Die Werte werden dann über Zeiteinheiten akkumuliert (z.B. Wochen, Monate, Jahre)",
                "correct": True,
                "feedback": """✓ Korrekt! Zeitliche Aggregation: Die Gruppierung erfolgt nach Zeitabschnitten, wobei eine unterschiedliche Granularität möglich ist. Dies glättet Einzelausreißer und ermöglicht die Erkennung von Mustern."""
            },
            {
                "answer": "Für jede Zeiteinheit wird der Durchschnitt der Textkomplexitätsmaße berechnet",
                "correct": True,
                "feedback": """✓ Korrekt! Durchschnittsbildung: Sie liefert einen repräsentativen Wert pro Zeiteinheit und ermöglicht die Vergleichbarkeit zwischen Perioden. Sie reduziert Rauschen und bildet die Basis für die Visualisierung."""
            },
            {
                "answer": "Nur der höchste Wert jeder Zeiteinheit wird betrachtet",
                "correct": False,
                "feedback": """× Nicht korrekt. Durchschnitt vs. Maximum: Der Durchschnitt ist repräsentativer, nur das Maximum zu betrachten würde eine Verzerrung erzeugen. Alle Werte sollten berücksichtigt werden, Standard ist daher die Mittelwertbildung."""
            }
        ]
    }
]
display_quiz(question7, colors=colors.jupyterquiz)
```

## Frage 7

**Szenario:** Sie analysieren ein Korpus von Zeitungsartikeln aus den Jahren 2010-2024. Nach Berechnung des Flesch-Index und Visualisierung in einem Liniendiagramm stellen Sie fest:
- 2010-2015: Scores zwischen 70-75 (mittelschwer)
- 2015-2020: Scores zwischen 60-65 (durchschnittlich)  
- 2020-2024: Scores zwischen 50-55 (anspruchsvoll)

**Aufgaben:**
1. Wie interpretieren Sie diese Entwicklung?
2. Was könnte diese Entwicklung für die Barrierefreiheit der Texte bedeuten?
3. Welche weiteren Analysen würden Sie vorschlagen?
4. Würden Sie dieselbe Entwicklung auch mit anderen Lesbarkeitsindizes überprüfen? Warum?

```{code-cell} ipython3
:tags: [remove-input]
import sys
sys.path.append("../quadriga")
from assessment import create_answer_box

create_answer_box('corpus-analysis-2')
```

````{admonition} Musterlösung
:class: solution, dropdown

**Musterlösung:**

**1. Interpretation der Entwicklung:**

Die Daten zeigen einen **klaren Abwärtstrend** der Flesch-Scores über 14 Jahre:
- **2010-2015:** 70-75 (mittelschwer, 7.-8. Klasse)
- **2015-2020:** 60-65 (durchschnittlich, 8.-9. Klasse)
- **2020-2024:** 50-55 (anspruchsvoll, 10.-12. Klasse)

**Interpretation:**
- **Steigende Textkomplexität** über die Zeit
- Durchschnittlich ca. 5 Punkte pro 5-Jahres-Periode
- Von Mittelstufen- zu Oberstufen-Niveau
- **Kontinuierlicher Trend**, keine sprunghaften Veränderungen

**Mögliche Ursachen:**
- Zunehmende Fachsprache
- Längere Sätze und komplexere Satzstrukturen
- Mehr mehrsilbige Wörter
- Thematische Verschiebungen (komplexere Themen?)

---

**2. Bedeutung für die Barrierefreiheit:**

**Negative Entwicklung für Barrierefreiheit:**

- **Abnehmende Zugänglichkeit:** Texte werden schwerer verständlich
- **Kleinere Zielgruppe:** Von breiter Öffentlichkeit (7.-8. Klasse) zu gebildeteren Lesern (10.-12. Klasse)
- **Barrieren steigen:** 
  - Für Menschen mit Lernschwierigkeiten
  - Für Menschen mit geringer formaler Bildung
  - Für Nicht-Muttersprachler
  - Für jüngere Leser

**Konsequenzen:**
- **Informationszugang** wird eingeschränkt
- **Demokratische Teilhabe** erschwert
- **Digitale Kluft** könnte vergrößert werden
- Widerspruch zu Zielen der **Leichten/Einfachen Sprache**

**Empfehlungen:**
- Bewusste Vereinfachung anstreben
- Schulungen für Redakteure
- Style Guides für verständliche Sprache
- Parallele Versionen in Leichter Sprache

---

**3. Vorgeschlagene weitere Analysen:**

**A) Detailanalyse der Parameter:**
- Welche spezifischen Parameter treiben die Komplexität?
- Sind es hauptsächlich:
  - Längere Sätze? → Durchschnittliche Satzlänge über Zeit
  - Mehr Silben? → Silbenzahl pro Wort über Zeit
  - Schwierigere Wörter? → Anteil langer/schwieriger Wörter
- Dies hilft, gezielte Verbesserungen zu identifizieren

**B) Thematische Analyse:**
- Unterscheiden sich verschiedene Themenbereiche?
- Politik vs. Kultur vs. Verwaltung
- Korrelation zwischen Thema und Komplexität?

**C) Vergleich mit anderen Quellen:**
- Wie entwickelt sich die Komplexität bei anderen Zeitungen?
- Ist dies ein allgemeiner Trend oder spezifisch?
- Benchmarking mit Qualitäts- vs. Boulevardzeitungen

**D) Saisonale/zyklische Muster:**
- Gibt es wiederkehrende Muster?
- Wahljahre komplexer?
- Ferienzeiten einfacher?

**E) Autorschaft:**
- Unterschiede zwischen Redakteuren?
- Ressorts mit konsistent höherer/niedrigerer Komplexität?

---

**4. Überprüfung mit anderen Indexe:**

**JA, definitiv!** Und zwar aus folgenden Gründen:

**Validierung der Ergebnisse:**
- **Flesch-Index allein** könnte Artefakt sein
- **Mehrere Indexe** erhöhen Vertrauenswürdigkeit
- Wenn alle Indexe denselben Trend zeigen → starke Evidenz
- Wenn Indexe divergieren → weitere Untersuchung nötig

**Unterschiedliche Perspektiven:**
- **Flesch:** Silben + Satzlänge
- **Wiener Sachtextformel:** Schwierige Wörter + Satzlänge
- **ARI:** Reine Längenmaße
- **Coleman-Liau:** Buchstaben pro 100 Wörter
- Jeder Index betont andere Aspekte

**Robustheit:**
- Nicht alle Indexe messen exakt dasselbe
- Konvergenz mehrerer Indexe = robuster Befund
- Divergenz = differenzierteres Bild

**Praktische Durchführung:**
```python
# Alle vier Indexe berechnen
df['flesch'] = df['text'].apply(calculate_flesch)
df['wiener'] = df['text'].apply(calculate_wiener)
df['ari'] = df['text'].apply(calculate_ari)
df['coleman_liau'] = df['text'].apply(calculate_coleman_liau)

# Zeitliche Entwicklung für alle
for measure in ['flesch', 'wiener', 'ari', 'coleman_liau']:
    plot_over_time(df, measure)
```

**Erwartung:**
- **Alle Indexe sollten** sinkende Lesbarkeit zeigen (steigenden Score bei den meisten)
- **Stärke des Trends** könnte variieren
- **Interpretation** wird durch Konvergenz gestützt

---

**Zusammenfassung:**

Die Analyse zeigt eine problematische Entwicklung hinsichtlich Barrierefreiheit. Eine umfassende Validierung mit multiplen Indexe und tiefergehende Analysen der Ursachen sind empfehlenswert, um fundierte Empfehlungen für barriereärmere Kommunikation zu geben.
````