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

**Geschätzte Zeit**: 20–25 min.

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
        "question": "Was versteht man unter 'Operationalisierung' im Kontext der Digital Humanities? Wählen Sie alle zutreffenden Aussagen.",
        "type": "multiple_choice",
        "answers": [
            {
                "answer": "Die Entwicklung eines Erkennungs- oder Messverfahrens für ein theoretisches Konzept",
                "correct": True,
                "feedback": """✓ Korrekt! Operationalisierung bezeichnet genau diesen Prozess: Theoretische Konzepte werden messbar gemacht, es wird ein konkretes Verfahren entwickelt, dies ermöglicht empirische Überprüfung und ist essentiell für quantitative Analysen."""
            },
            {
                "answer": "Die Brücke zwischen qualitativen Fragestellungen und quantitativen Methoden",
                "correct": True,
                "feedback": """✓ Korrekt! Die Operationalisierung ist tatsächlich diese Brücke: Sie verbindet 'numbers' mit 'meaning', ermöglicht quantitative Analyse qualitativer Fragen, ist zentral für Digital Humanities-Projekte und macht geisteswissenschaftliche Konzepte messbar."""
            },
            {
                "answer": "Die technische Implementierung von Analysealgorithmen",
                "correct": False,
                "feedback": """× Nicht korrekt. Die technische Implementierung ist ein späterer Schritt: Die Operationalisierung findet VOR der technischen Umsetzung statt, sie definiert WAS gemessen werden soll, die Implementierung beschäftigt sich mit dem WIE, und die Operationalisierung ist konzeptionelle Arbeit."""
            },
            {
                "answer": "Die Dokumentation der verwendeten Software und Tools",
                "correct": False,
                "feedback": """× Nicht korrekt. Dokumentation ist wichtig, aber nicht Operationalisierung: Die Operationalisierung definiert Messverfahren, die Dokumentation beschreibt die Umsetzung, beides sind getrennte Schritte im Forschungsprozess, und die Operationalisierung ist konzeptionell, während die Dokumentation deskriptiv ist."""
            },
            {
                "answer": "Ein Prozess, der immer eindeutig und unstrittig ist",
                "correct": False,
                "feedback": """× Nicht korrekt. Operationalisierung ist diskutabel: Verschiedene Operationalisierungen sind möglich, die Wahl muss begründet und reflektiert werden, Grenzen und Beschränkungen müssen erkannt werden, und dies ist Teil der wissenschaftlichen Reflexion."""
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
        "question": "Welche Aussagen zum Konzept der 'Leichten Sprache' und kommunikativen Barrierearmut sind korrekt? Wählen Sie alle zutreffenden Aussagen.",
        "type": "multiple_choice",
        "answers": [
            {
                "answer": "Leichte Sprache ist seit der Ratifizierung der UN-Behindertenrechtskonvention 2009 in Deutschland rechtlich relevant",
                "correct": True,
                "feedback": """✓ Korrekt! Die UN-Behindertenrechtskonvention wurde 2009 in Deutschland ratifiziert, ist verbindliches Recht, beinhaltet die Verpflichtung zur barrierefreien Kommunikation und gab der Leichten Sprache rechtliche Bedeutung."""
            },
            {
                "answer": "Kommunikative Barrierearmut ist ein binäres Konzept: Entweder eine Kommunikation ist barrierefrei oder nicht",
                "correct": False,
                "feedback": """× Nicht korrekt. Barrierearmut ist graduell: Sprache kann mehr oder weniger verständlich sein, es gibt verschiedene Grade der Komplexität, es handelt sich nicht um ein Entweder-Oder, sondern um ein Kontinuum, und dies ermöglicht die Messung von Veränderungen."""
            },
            {
                "answer": "Leichte Sprache bezieht sich nur auf die Wortebene (z.B. Vermeidung von Fremdwörtern)",
                "correct": False,
                "feedback": """× Nicht korrekt. Leichte Sprache umfasst mehrere Ebenen: die Wortebene (geläufige Wörter, keine Fremdwörter), die Satzebene (Verbalstil, einfache Strukturen) und die Textebene (Gliederung, Zusammenfassungen); alle Ebenen tragen zur Verständlichkeit bei."""
            },
            {
                "answer": "Die gesellschaftliche Aufmerksamkeit für Leichte Sprache hat in den letzten Jahren zugenommen",
                "correct": True,
                "feedback": """✓ Korrekt! Dies zeigt sich beispielsweise in der Zunahme des Begriffs im Google Books-Korpus, in der Entwicklung von Regelwerken und Standards, in der DIN SPEC von März 2025 und in vermehrten Angeboten von Behörden."""
            },
            {
                "answer": "Leichte Sprache betrifft ausschließlich Menschen mit Behinderungen",
                "correct": False,
                "feedback": """× Nicht korrekt. Leichte Sprache hat breitere Relevanz: Sie betrifft Grundfragen gesellschaftlicher Teilhabe, ist relevant für verschiedene Zielgruppen, fördert allgemeine Verständlichkeit und ist nicht auf eine Gruppe beschränkt."""
            }
        ]
    }
]
display_quiz(question2, colors=colors.jupyterquiz )
```

## Frage 3

```{code-cell} ipython3
:tags: [remove-input]
from jupyterquiz import display_quiz

import sys
sys.path.append("..")
from quadriga import colors

question3 = [
    {
        "question": "Welche Aussagen zu Lesbarkeitsindizes treffen zu? Wählen Sie alle zutreffenden Aussagen.",
        "type": "multiple_choice",
        "answers": [
            {
                "answer": "Lesbarkeitsindizes nutzen häufig durchschnittliche Wortlänge und Satzlänge als Parameter",
                "correct": True,
                "feedback": """✓ Korrekt! Diese Parameter sind zentral für viele Lesbarkeitsindizes, lassen sich objektiv messen, korrelieren mit Textkomplexität und werden auch in der Leichte-Sprache-Forschung verwendet."""
            },
            {
                "answer": "Lesbarkeitsindizes erfassen alle Aspekte der Leichten Sprache vollständig",
                "correct": False,
                "feedback": """× Nicht korrekt. Lesbarkeitsindizes sind begrenzt: Sie erfassen nur ausgewählte Indikatoren, Metaphern, Fremdwörter etc. werden oft nicht berücksichtigt, die Textebene (Gliederung) ist schwer messbar, und die Operationalisierung wählt bewusst ein Set aus Indikatoren."""
            },
            {
                "answer": "Steigende Werte in Lesbarkeitsindizes bedeuten immer höhere Verständlichkeit",
                "correct": False,
                "feedback": """× Nicht korrekt. Die Interpretation hängt vom Index ab: Manche Indexe messen Komplexität (höher bedeutet schwieriger), andere messen Lesbarkeit (höher bedeutet leichter), die Interpretation muss jeweils definiert werden, und in unserer Fallstudie bedeutet höhere Komplexität weniger Barrierefreiheit."""
            },
            {
                "answer": "Lesbarkeitsindizes ermöglichen die Messung zeitlicher Entwicklungen in Textkomplexität",
                "correct": True,
                "feedback": """✓ Korrekt! Dies ist zentral für unsere Fragestellung: Quantitative Werte können über Zeit verglichen werden, Trends lassen sich statistisch erfassen, Veränderungen werden messbar, und dies ist die Grundlage für die Beantwortung unserer Forschungsfrage."""
            },
            {
                "answer": "Lesbarkeitsindizes sind die einzige Möglichkeit, Textkomplexität zu operationalisieren",
                "correct": False,
                "feedback": """× Nicht korrekt. Es gibt verschiedene Ansätze: Lesbarkeitsindizes sind eine mögliche Operationalisierung, andere Indikatoren wären denkbar (z.B. Fremdwortanteil), die Wahl muss begründet werden, und alternative Operationalisierungen sind legitim."""
            }
        ]
    }
]
display_quiz(question3, colors=colors.jupyterquiz )
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
        "question": "Welches der folgenden Kriterien war NICHT ausschlaggebend für die Wahl der Pressemitteilungen des Berliner Senats als Korpus?",
        "type": "multiple_choice",
        "answers": [
            {
                "answer": "Öffentliche Zugänglichkeit und maschinelle Aggregierbarkeit",
                "correct": False,
                "feedback": """× Dies war ein wichtiges Kriterium: Pressemitteilungen sind online verfügbar, systematisches Scraping ist möglich, dies ist notwendig für den Korpusaufbau, und es ist eines der vier definierten Kriterien."""
            },
            {
                "answer": "Funktion als Kommunikation der Behörden mit der Öffentlichkeit",
                "correct": False,
                "feedback": """× Dies war zentral für die Auswahl: Pressemitteilungen sind öffentliche Kommunikation, richten sich an Bürger:innen, sind repräsentativ für Behördenkommunikation und sind eines der vier definierten Kriterien."""
            },
            {
                "answer": "Homogenität der Textsorte",
                "correct": False,
                "feedback": """× Dies war ein wichtiges Kriterium: Es vermeidet Verzerrungen durch unterschiedliche Konventionen, ermöglicht valide Vergleiche über Zeit, Pressemitteilungen folgen ähnlichen Mustern, und es ist eines der vier definierten Kriterien."""
            },
            {
                "answer": "Maximale Länge der Einzeltexte",
                "correct": True,
                "feedback": """✓ Korrekt! Die Textlänge war KEIN definiertes Kriterium: Die vier Kriterien waren Zugänglichkeit, Kommunikationsfunktion, Homogenität und zeitliche Situierbarkeit, die Textlänge spielt für die Analyse mit Lesbarkeitsindizes keine ausschlaggebende Rolle, und kurze wie lange Texte können beide analysiert werden."""
            },
            {
                "answer": "Präzise zeitliche Situierbarkeit der Einzeltexte",
                "correct": False,
                "feedback": """× Dies war essentiell: Pressemitteilungen haben klare Publikationsdaten, dies ermöglicht die Analyse zeitlicher Entwicklungen, ist zentral für die Forschungsfrage und eines der vier definierten Kriterien."""
            }
        ]
    }
]
display_quiz(question4, colors=colors.jupyterquiz )
```

## Frage 5

```{code-cell} ipython3
:tags: [remove-input]
import sys
sys.path.append("../quadriga")
from assessment import DragDropQuiz

quiz = DragDropQuiz()

quiz.create_matching_quiz(
    title="Ordnen Sie die folgenden Empfehlungen für Leichte Sprache der entsprechenden Ebene zu:",
    descriptions=[
        "Verwenden geläufiger Wörter, Vermeiden von Fremdwörtern",
        "Eher Verbalstil, Vermeiden von Negationen",
        "Klare Absatzgliederung, vorangestellte Zusammenfassung"
    ],
    options=["Wortebene", "Satzebene", "Textebene", "Silbenebene"],
    correct_mapping={
        "Verwenden geläufiger Wörter, Vermeiden von Fremdwörtern": "Wortebene",
        "Eher Verbalstil, Vermeiden von Negationen": "Satzebene",
        "Klare Absatzgliederung, vorangestellte Zusammenfassung": "Textebene"
    }
)
```

## Frage 6

**Szenario:** Ein Forschungsteam möchte untersuchen, ob wissenschaftliche Zeitschriften in den letzten 20 Jahren verständlicher geworden sind. Sie planen, dies anhand von Abstracts zu untersuchen.

**Ihre Aufgabe:** Skizzieren Sie eine mögliche Operationalisierung dieser Fragestellung. Berücksichtigen Sie dabei:
1. Die Wahl des Korpus und Begründung
2. Die Auswahl geeigneter Messverfahren
3. Potenzielle Einschränkungen Ihrer Operationalisierung

```{code-cell} ipython3
:tags: [remove-input]
import sys
sys.path.append("../quadriga")
from assessment import create_answer_box

create_answer_box('research-question-1')
```

````{admonition} Musterlösung
:class: solution, dropdown

**Musterlösung:**

**1. Korpus:**
- Abstracts aus repräsentativen wissenschaftlichen Zeitschriften
- Zeitraum: 2005-2025 (20 Jahre)
- Auswahl nach Disziplinen (z.B. je 3-5 Zeitschriften pro Fachgebiet)
- Begründung: 
  - Abstracts sind homogene Textsorte
  - Zeitlich präzise datierbar
  - Öffentlich zugänglich
  - Repräsentativ für wissenschaftliche Kommunikation

**2. Messverfahren:**
- Lesbarkeitsindizes (z.B. Flesch Reading Ease, LIX)
- Durchschnittliche Wort- und Satzlänge
- Eventuell: Anteil an Fachwörtern (falls operationalisierbar)
- Begründung:
  - Objektiv messbar
  - Zeitliche Vergleiche möglich
  - Etablierte Verfahren

**3. Einschränkungen:**
- Lesbarkeitsindizes erfassen nicht alle Aspekte von Verständlichkeit
- Disziplinäre Unterschiede müssen berücksichtigt werden
- Abstracts repräsentieren nicht den gesamten Artikel
- Verständlichkeit ist kontextabhängig (Fachpublikum vs. Laien)
- Alternative Operationalisierungen wären möglich und legitim

**Wichtig:**
- Transparente Dokumentation der Entscheidungen
- Reflexion der Grenzen
- Begründung der Auswahlkriterien
````

## Frage 7

```{code-cell} ipython3
:tags: [remove-input]
from jupyterquiz import display_quiz

import sys
sys.path.append("..")
from quadriga import colors

question7 = [
    {
        "question": "Welche Aussagen zur Reflexion von Operationalisierungen in Digital Humanities-Projekten sind zutreffend? Wählen Sie alle korrekten Aussagen.",
        "type": "multiple_choice",
        "answers": [
            {
                "answer": "Die Reflexion der Grenzen und Beschränkungen der eigenen Operationalisierung ist essentieller Bestandteil von DH-Projekten",
                "correct": True,
                "feedback": """✓ Korrekt! Wissenschaftliche Reflexion bedeutet Bewusstsein für die Grenzen der eigenen Methode, transparente Dokumentation von Entscheidungen und Diskussion alternativer Ansätze, und ist Teil der wissenschaftlichen Integrität."""
            },
            {
                "answer": "Jede Operationalisierung ist diskutabel und könnte auch anders erfolgen",
                "correct": True,
                "feedback": """✓ Korrekt! Dies ist wichtig zu verstehen: Es gibt selten die eine 'richtige' Operationalisierung, verschiedene Ansätze haben unterschiedliche Stärken, die Wahl muss begründet werden, und wissenschaftlicher Diskurs ist erwünscht."""
            },
            {
                "answer": "Quantitative Methoden erfassen alle Aspekte qualitativer Phänomene vollständig",
                "correct": False,
                "feedback": """× Nicht korrekt. Dies ist eine wichtige Einsicht: Quantifizierung bedeutet immer Reduktion, nicht alle Aspekte sind messbar, qualitative Dimensionen können verloren gehen, und deshalb ist Reflexion so wichtig."""
            },
            {
                "answer": "Die Operationalisierung sollte nur dann reflektiert werden, wenn die Ergebnisse unerwartet sind",
                "correct": False,
                "feedback": """× Nicht korrekt. Reflexion ist immer notwendig: Sie ist unabhängig von den Ergebnissen, Teil des Forschungsprozesses von Anfang an, stärkt die wissenschaftliche Qualität und ermöglicht informierte Interpretation."""
            },
            {
                "answer": "Eine gute Operationalisierung macht die Forschungsfrage für quantitative Analyse adressierbar",
                "correct": True,
                "feedback": """✓ Korrekt! Das ist die Kernfunktion: Sie verbindet qualitative Fragen mit quantitativen Methoden, macht abstrakte Konzepte messbar und ermöglicht empirische Überprüfung, nach dem Prinzip 'from numbers to meaning'."""
            },
            {
                "answer": "Einschränkungen der Operationalisierung bedeuten, dass die Forschung wertlos ist",
                "correct": False,
                "feedback": """× Nicht korrekt. Wichtige Differenzierung: Jede Operationalisierung hat Grenzen, dies schmälert jedoch nicht den Wert der Forschung, wichtig ist die bewusste Reflexion, und Transparenz über Grenzen erhöht die wissenschaftliche Qualität."""
            }
        ]
    }
]
display_quiz(question7, colors=colors.jupyterquiz )
```

## Frage 8

```{code-cell} ipython3
:tags: [remove-input]
import sys
sys.path.append("../quadriga")
from assessment import DragDropQuiz

quiz = DragDropQuiz()

quiz.create_matching_quiz(
    title="Ordnen Sie die folgenden Schritte zur Operationalisierung der Forschungsfrage in die richtige Reihenfolge:",
    descriptions=[
        "Definition des Korpus",
        "Formulierung der Forschungsfrage",
        "Auswahl geeigneter Messverfahren",
        "Reflexion der Grenzen der Operationalisierung",
        "Definition des zu messenden Konzepts"
    ],
    options=["3", "1", "5", "2", "4"],
    correct_mapping={
        "Formulierung der Forschungsfrage": "1",
        "Definition des zu messenden Konzepts": "2",
        "Auswahl geeigneter Messverfahren": "3",
        "Definition des Korpus": "4",
        "Reflexion der Grenzen der Operationalisierung": "5"
    }
)
```

## Frage 9

**Kritische Reflexion:** Bewerten Sie die folgende Operationalisierung kritisch:

*"Um die Entwicklung der Barrierearmut in der Behördenkommunikation zu untersuchen, werden alle Texte der Berliner Senatsverwaltung aus den letzten 50 Jahren gesammelt und mit einem einzelnen Lesbarkeitsindex analysiert. Wenn der Index niedriger wird, ist die Kommunikation barriereärmer geworden."*

**Ihre Aufgabe:** Identifizieren Sie mindestens vier problematische Aspekte dieser Operationalisierung und schlagen Sie Verbesserungen vor.

```{code-cell} ipython3
:tags: [remove-input]
import sys
sys.path.append("../quadriga")
from assessment import create_answer_box

create_answer_box('research-question-2')
```

````{admonition} Musterlösung
:class: solution, dropdown

**Musterlösung - Problematische Aspekte und Verbesserungsvorschläge:**

**1. "Alle Texte" - zu heterogen:**
- Problem: Verschiedene Textsorten (Pressemitteilungen, Formulare, Berichte) haben unterschiedliche Konventionen
- Verbesserung: Beschränkung auf eine homogene Textsorte (z.B. nur Pressemitteilungen)
- Begründung: Vermeidet Verzerrungen durch Textsorten-Konventionen

**2. "50 Jahre" - praktisch problematisch:**
- Problem: Digitale Verfügbarkeit für ältere Texte unklar, sehr großes Datenvolumen
- Verbesserung: Fokussierung auf einen relevanten, gut dokumentierten Zeitraum (z.B. seit 2011)
- Begründung: Praktikabilität und Nachvollziehbarkeit

**3. "Einzelner Lesbarkeitsindex" - zu eng:**
- Problem: Ein Index erfasst nur ausgewählte Aspekte der Komplexität
- Verbesserung: Verwendung mehrerer Indexe zur Triangulation
- Begründung: Robustere Ergebnisse, umfassendere Erfassung

**4. "Niedriger = barriereärmer" - zu simpel:**
- Problem: 
  - Interpretation hängt vom spezifischen Index ab
  - Kausale Schlussfolgerung ohne Begründung
  - Keine Reflexion alternativer Erklärungen
- Verbesserung: 
  - Klare Definition der Interpretation für den gewählten Index
  - Vorsichtige Formulierung (Korrelation, nicht Kausalität)
  - Diskussion möglicher Störfaktoren

**5. Fehlende Reflexion:**
- Problem: Keine Diskussion der Grenzen und alternativen Ansätze
- Verbesserung: Explizite Reflexion über:
  - Was erfasst wird und was nicht
  - Welche Annahmen getroffen werden
  - Welche alternativen Operationalisierungen möglich wären
  - Welche Einschränkungen die Interpretation beeinflussen

**Allgemeine Verbesserung:**
Eine wissenschaftlich fundierte Operationalisierung sollte transparent, begründet und reflektiert sein, mit klaren Kriterien für Korpusauswahl und Messmethodik.
````

## Frage 10

```{code-cell} ipython3
:tags: [remove-input]
from jupyterquiz import display_quiz

import sys
sys.path.append("..")
from quadriga import colors

question10 = [
    {
        "question": """Ein Forschungsteam möchte untersuchen, ob sich die "Emotionalität" politischer Reden im Bundestag über die Zeit verändert hat. Welche der folgenden Operationalisierungen wäre am sinnvollsten?""",
        "type": "multiple_choice",
        "answers": [
            {
                "answer": "Auszählen aller Wörter mit Ausrufezeichen in den Protokollen",
                "correct": False,
                "feedback": """× Zu eng gefasst: Dies erfasst nur einen sehr spezifischen Aspekt, Interpunktion ist nicht immer zuverlässig transkribiert, Emotionalität äußert sich vielfältiger, und wichtige Dimensionen würden übersehen."""
            },
            {
                "answer": "Messung positiver/negativer Emotionen und Analyse emotionaler Wörter mittels Sentimentanalyse-Tools",
                "correct": True,
                "feedback": """✓ Gute Operationalisierung, weil Sentimentanalyse ein etabliertes Verfahren ist, verschiedene emotionale Dimensionen erfasst, quantitativ messbar und über Zeit vergleichbar ist und durch weitere Indikatoren ergänzt werden kann; trotzdem müssen Grenzen reflektiert werden (z.B. Kontextabhängigkeit, Ironie)."""
            },
            {
                "answer": "Befragung von Politiker:innen, wie emotional sie ihre Reden empfinden",
                "correct": False,
                "feedback": """× Nicht für diese Fragestellung geeignet: Es liefert subjektive Einschätzungen statt objektiver Messung, eine retrospektive Befragung über lange Zeiträume ist unmöglich, es gibt keine Vergleichbarkeit über Jahrzehnte, und es passt nicht zum quantitativen Methodenparadigma der Korpusanalyse."""
            },
            {
                "answer": "Zählen der Zwischenrufe und Reaktionen im Protokoll",
                "correct": False,
                "feedback": """× Misst etwas anderes: Dies erfasst Reaktionen des Publikums, nicht die Emotionalität der Rede selbst, die Protokollierung von Zwischenrufen kann sich über Zeit ändern, es ist nur ein indirekter Indikator, und es könnte ergänzend interessant sein, aber nicht als Hauptoperationalisierung."""
            },
            {
                "answer": "Messung der Lautstärke in Audioaufnahmen",
                "correct": False,
                "feedback": """× Praktisch problematisch: Audioaufnahmen sind nicht für alle Zeiträume verfügbar, die Aufnahmequalität variiert stark, Lautstärke entspricht nicht Emotionalität, und es handelt sich um eine technische statt inhaltliche Messung."""
            }
        ]
    }
]
display_quiz(question10, colors=colors.jupyterquiz )
```