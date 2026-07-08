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

**Geschätzte Zeit**: XX

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
        "question": "Welche der folgenden Aussagen beschreiben korrekt die wesentlichen Merkmale eines Korpus in den Digital Humanities? Wählen Sie alle zutreffenden Aussagen.",
        "type": "multiple_choice",
        "answers": [
            {
                "answer": "Eine Sammlung von maschinenlesbaren Textdokumenten",
                "correct": True,
                "feedback": """✓ Korrekt! Die Maschinenlesbarkeit ist ein zentrales Merkmal von DH-Korpora, da sie die computergestützte Analyse ermöglicht. Dies unterscheidet DH-Korpora von traditionellen Textsammlungen und ist Voraussetzung für quantitative Analysen."""
            },
            {
                "answer": "Eine nach bestimmten Kriterien zusammengestellte Textsammlung",
                "correct": True,
                "feedback": """✓ Korrekt! Die kriteriengeleitete Zusammenstellung ist essentiell für wissenschaftliche Korpora. Die Kriterien müssen dabei transparent dokumentiert sein, zur Forschungsfrage passen und systematisch angewendet werden."""
            },
            {
                "answer": "Eine Sammlung, die nur digitalisierte Bücher enthält",
                "correct": False,
                "feedback": """× Nicht korrekt. Korpora können verschiedene Arten von Texten enthalten, etwa Zeitungsartikel (wie in unserer Fallstudie), literarische Texte, Dokumente oder andere Textformen. Die Art der Texte wird durch die Forschungsfrage bestimmt, nicht durch das Format."""
            },
            {
                "answer": "Eine Textsammlung, die spezifischen Forschungszwecken dient",
                "correct": True,
                "feedback": """✓ Korrekt! Die Zweckgebundenheit ist ein wichtiges Merkmal: Das Korpus wird für bestimmte Forschungsfragen zusammengestellt, die Forschungszwecke bestimmen die Auswahlkriterien und die Zweckbindung beeinflusst auch die Art der Aufbereitung der Texte."""
            },
            {
                "answer": "Eine beliebige Sammlung von digitalisierten Texten",
                "correct": False,
                "feedback": """× Nicht korrekt. Eine beliebige Sammlung erfüllt nicht die wissenschaftlichen Anforderungen an ein Korpus: Es fehlen systematische Auswahlkriterien, die Zusammenstellung ist nicht durch Forschungsfragen motiviert und eine methodisch fundierte Analyse wäre nicht möglich."""
            },
            {
                "answer": "Eine Sammlung, die immer alle verfügbaren Texte zu einem Thema enthalten muss",
                "correct": False,
                "feedback": """× Nicht korrekt. Vollständigkeit ist nur eine mögliche Strategie des Korpusaufbaus: Wie im Text erläutert, gibt es verschiedene Strategien (z.B. repräsentative Stichproben), die Vollständigkeit ist nur bei klar begrenzten, kleinen Untersuchungsbereichen sinnvoll und die Strategie der Korpuserstellung richtet sich nach der Forschungsfrage und praktischen Erwägungen."""
            }
        ]
    }
]
display_quiz(question1, colors=colors.jupyterquiz  )
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
        "question": "Was ist ein Referenzkorpus?",
        "type": "multiple_choice",
        "answers": [
            {
                "answer": "Ein Korpus, das besonders darauf ausgelegt wurde, für eine bestimmte Domäne repräsentativ zu sein",
                "correct": True,
                "feedback": """✓ Korrekt! Referenzkorpora sind spezielle Korpora, bei denen besondere Aufmerksamkeit auf Repräsentativität gelegt wird, die als Vergleichsgrundlage für andere Studien dienen, meist sorgfältig nach wissenschaftlichen Kriterien zusammengestellt werden und wichtig für die Standardisierung in der Forschung sind."""
            },
            {
                "answer": "Ein Korpus, das alle verfügbaren Texte einer Sprache enthält",
                "correct": False,
                "feedback": """× Nicht korrekt. Ein Referenzkorpus muss nicht vollständig sein, fokussiert auf Repräsentativität statt Vollständigkeit, wird gezielt zusammengestellt und soll eine Domäne abbilden, statt alles zu sammeln."""
            },
            {
                "answer": "Ein Korpus, das als Vergleichsgrundlage für linguistische Studien dient",
                "correct": True,
                "feedback": """✓ Korrekt! Das ist eine wichtige Funktion: Es dient als Standard für Vergleiche, ermöglicht Aussagen über typische Sprachverwendung, ist Basis für normative Beschreibungen und wichtig für die Vergleichbarkeit von Studien."""
            },
            {
                "answer": "Ein Korpus, das nur aus veröffentlichten wissenschaftlichen Texten besteht",
                "correct": False,
                "feedback": """× Nicht korrekt. Referenzkorpora können verschiedene Textsorten enthalten und werden nach Domäne definiert, nicht nach Textsorte – ein Referenzkorpus für gesprochene Sprache enthält beispielsweise keine wissenschaftlichen Texte, denn die Zusammensetzung hängt vom Zweck ab."""
            }
        ]
    }
]
display_quiz(question2, colors=colors.jupyterquiz  )
```

## Frage 3

```{code-cell} ipython3
:tags: [remove-input]
import sys
sys.path.append("../quadriga")
from assessment import DragDropQuiz

quiz = DragDropQuiz()

quiz.create_matching_quiz(
    title="Ordnen Sie die Korpustypen den entsprechenden Definitionen zu:",
    descriptions=[
        "Umfasst alle verfügbaren Textobjekte zu einem spezifischen Gegenstandsbereich",
        "Auswahl, die durch zufällige Stichprobenziehung die Variabilität der Grundgesamtheit abbildet",
        "Gezielt nach Kriterien zusammengestellte Auswahl, die alle wesentlichen Merkmale gleichmäßig abdeckt",
        "Sammlung, deren Auswahl nur durch die Verfügbarkeit von Daten geleitet wird"
    ],
    options=["Vollständiges Korpus", "Repräsentative Stichprobe", "Balanciertes Korpus", "Opportunistisches Korpus", "Referenzkorpus"],
    correct_mapping={
        "Umfasst alle verfügbaren Textobjekte zu einem spezifischen Gegenstandsbereich": "Vollständiges Korpus",
        "Auswahl, die durch zufällige Stichprobenziehung die Variabilität der Grundgesamtheit abbildet": "Repräsentative Stichprobe",
        "Gezielt nach Kriterien zusammengestellte Auswahl, die alle wesentlichen Merkmale gleichmäßig abdeckt": "Balanciertes Korpus",
        "Sammlung, deren Auswahl nur durch die Verfügbarkeit von Daten geleitet wird": "Opportunistisches Korpus"
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
        "question": "Welche Voraussetzungen muss ein Korpus erfüllen, um als repräsentative Stichprobe zu gelten?",
        "type": "multiple_choice",
        "answers": [
            {
                "answer": "Die Grundgesamtheit muss bekannt und gut dokumentiert sein",
                "correct": True,
                "feedback": """✓ Korrekt! Ohne bekannte Grundgesamtheit kann keine Repräsentativität berechnet werden, sind keine validen statistischen Aussagen möglich, fehlt die Grundlage für eine zufällige Auswahl und kann die Stichprobenqualität nicht bewertet werden."""
            },
            {
                "answer": "Die Auswahl der Datensätze muss zufällig erfolgen",
                "correct": True,
                "feedback": """✓ Korrekt! Zufällige Auswahl ist essentiell: Sie vermeidet systematische Verzerrungen, ermöglicht statistische Inferenz, ist Grundlage für Repräsentativität und wissenschaftlicher Standard für Stichproben."""
            },
            {
                "answer": "Das Korpus muss alle verfügbaren Texte enthalten",
                "correct": False,
                "feedback": """× Nicht korrekt. Eine repräsentative Stichprobe ist definitionsgemäß eine Teilmenge, muss nicht vollständig sein und bildet die Grundgesamtheit statistisch ab – Vollständigkeit würde stattdessen ein vollständiges Korpus erfordern."""
            },
            {
                "answer": "Die Texte müssen nach subjektiven Qualitätskriterien ausgewählt werden",
                "correct": False,
                "feedback": """× Nicht korrekt. Bei repräsentativen Stichproben erfolgt die Auswahl ZUFÄLLIG, nicht nach Qualität, da subjektive Kriterien Verzerrungen einführen würden – Ziel ist statistische Repräsentativität, während Qualitätskriterien zu anderen Strategien gehören."""
            }
        ]
    }
]
display_quiz(question4, colors=colors.jupyterquiz  )
```

## Frage 5

```{code-cell} ipython3
:tags: [remove-input]
from jupyterquiz import display_quiz

import sys
sys.path.append("..")
from quadriga import colors

question5 = [
    {
        "question": "Für welche der folgenden Forschungsvorhaben wäre ein balanciertes Korpus die beste Wahl?",
        "type": "multiple_choice",
        "answers": [
            {
                "answer": "Analyse der Entwicklung literarischer Gattungen über verschiedene Jahrzehnte",
                "correct": True,
                "feedback": """✓ Korrekt! Ein balanciertes Korpus ist ideal, weil verschiedene Jahrzehnte gleichmäßig vertreten sein sollen, Entwicklungen und Unterschiede analysiert werden, eine gezielte Auswahl nach Kriterien (Zeit, Gattung) erfolgt und statistische Korrelationen vermieden werden können."""
            },
            {
                "answer": "Vollständige Erfassung aller Werke eines einzelnen Autors",
                "correct": False,
                "feedback": """× Nicht die beste Wahl. Hierfür wäre ein vollständiges Korpus geeignet: Alle verfügbaren Werke werden gesammelt, der Gegenstandsbereich ist klar begrenzt und es wird keine Auswahl, sondern Vollständigkeit angestrebt."""
            },
            {
                "answer": "Erste explorative Studie in einem wenig erschlossenen Forschungsbereich",
                "correct": False,
                "feedback": """× Nicht die beste Wahl. Hierfür wäre ein opportunistisches Korpus geeignet: die Sammlung verfügbarer Daten dient der ersten Exploration, klare Auswahlkriterien sind noch nicht möglich und eine Balancierung setzt Wissen über die Domäne voraus."""
            },
            {
                "answer": "Studie über Sprachvariation in verschiedenen Textsorten und Registern",
                "correct": True,
                "feedback": """✓ Korrekt! Ein balanciertes Korpus passt, weil verschiedene Textsorten gleichmäßig vertreten sein sollen, Variation systematisch erfasst werden soll, eine gezielte Auswahl nach Kriterien (Textsorte, Register) erfolgt und Unterschiede analysiert werden sollen."""
            }
        ]
    }
]
display_quiz(question5, colors=colors.jupyterquiz  )
```

## Frage 6

```{code-cell} ipython3
:tags: [remove-input]
from jupyterquiz import display_quiz

import sys
sys.path.append("..")
from quadriga import colors

question6 = [
    {
        "question": "Welche Aussagen zu Metadaten treffen zu?",
        "type": "multiple_choice",
        "answers": [
            {
                "answer": "Metadaten sind Daten über Daten",
                "correct": True,
                "feedback": """✓ Korrekt! Dies ist die grundlegende Definition: Metadaten beschreiben andere Daten, liefern kontextuelle Informationen, helfen beim Verstehen und Organisieren von Daten und sind essentiell für die Nachnutzbarkeit."""
            },
            {
                "answer": "Metadaten sind in den Digital Humanities unwichtig, da die Texte selbst im Fokus stehen",
                "correct": False,
                "feedback": """× Nicht korrekt. Metadaten sind essentiell: Sie ermöglichen systematische Organisation, machen Korpora auffindbar, sichern inhaltliche und strukturelle Qualität und sind unverzichtbar für wissenschaftliche Arbeit."""
            },
            {
                "answer": "Metadaten helfen bei der Bedeutung, Herkunft, Struktur und Nutzungsmöglichkeiten eines Datensatzes",
                "correct": True,
                "feedback": """✓ Korrekt! Metadaten erfüllen mehrere Funktionen: Kontextualisierung (Bedeutung, Herkunft), Strukturierung (Organisation der Daten), Nutzung (wie können Daten verwendet werden) und Qualitätssicherung."""
            },
            {
                "answer": "Für Metadaten gibt es nur ein einziges, universell verwendetes Schema",
                "correct": False,
                "feedback": """× Nicht korrekt. Es gibt verschiedene Schemata: Dublin Core (einfach und universell), TEI (spezialisiert auf Texte), MODS (bibliographische Informationen) und METS (Digitalisate und deren Übertragung) – jedes Schema ist für spezifische Anforderungen gedacht."""
            }
        ]
    }
]
display_quiz(question6, colors=colors.jupyterquiz  )
```

## Frage 7

```{code-cell} ipython3
:tags: [remove-input]
import sys
sys.path.append("../quadriga")
from assessment import DragDropQuiz

quiz = DragDropQuiz()

quiz.create_matching_quiz(
    title="Ordnen Sie die Metadatenschemata den entsprechenden Beschreibungen zu:",
    descriptions=[
        "Einfaches Schema mit 15 grundlegenden Elementen wie Titel, Autor und Datum",
        "Spezialisiert auf Textauszeichnung mit detaillierten Richtlinien und teiHeader",
        "Umfangreiche Beschreibung für bibliographische Informationen",
        "Standard zur Kodierung und Übertragung von Digitalisaten"
    ],
    options=["Dublin Core", "TEI", "MODS", "METS", "MARC"],
    correct_mapping={
        "Einfaches Schema mit 15 grundlegenden Elementen wie Titel, Autor und Datum": "Dublin Core",
        "Spezialisiert auf Textauszeichnung mit detaillierten Richtlinien und teiHeader": "TEI",
        "Umfangreiche Beschreibung für bibliographische Informationen": "MODS",
        "Standard zur Kodierung und Übertragung von Digitalisaten": "METS"
    }
)
```

## Frage 8

```{code-cell} ipython3
:tags: [remove-input]
from jupyterquiz import display_quiz

import sys
sys.path.append("..")
from quadriga import colors

question8 = [
    {
        "question": "Welche Metadaten-Elemente sind typischerweise für die Beschreibung eines GESAMTEN Korpus relevant?",
        "type": "multiple_choice",
        "answers": [
            {
                "answer": "Titel und Beschreibung des Korpus",
                "correct": True,
                "feedback": """✓ Korrekt! Auf Korpusebene wichtig sind die eindeutige Identifikation des gesamten Korpus, die Beschreibung des Inhalts und Umfangs, der Kontext der Sammlung und grundlegende Information für Nutzer."""
            },
            {
                "answer": "Umfang und Format der enthaltenen Dokumente",
                "correct": True,
                "feedback": """✓ Korrekt! Wichtig für das Gesamtkorpus sind die Anzahl der Dokumente, die verwendeten Dateiformate, die Gesamtgröße der Sammlung und technische Spezifikationen."""
            },
            {
                "answer": "Spezifischer Publikationsort jedes einzelnen Dokuments",
                "correct": False,
                "feedback": """× Nicht auf Korpusebene. Dies ist ein elementspezifisches Metadatum, das zur Beschreibung einzelner Dokumente gehört, zu detailliert für die Korpusebene ist und Teil der Dokument-Metadaten bildet."""
            },
            {
                "answer": "Ersteller:innen und Herausgeber:innen des Korpus",
                "correct": True,
                "feedback": """✓ Korrekt! Wichtig auf Korpusebene ist, wer das Korpus zusammengestellt hat, sowie institutionelle Verantwortung, Zitierfähigkeit und Nachvollziehbarkeit."""
            },
            {
                "answer": "Datum der Erstellung und Veröffentlichung des Korpus",
                "correct": True,
                "feedback": """✓ Korrekt! Zeitangaben sind wichtig für Versionierung, Aktualität der Sammlung, wissenschaftliche Dokumentation und Nachnutzbarkeit."""
            }
        ]
    }
]
display_quiz(question8, colors=colors.jupyterquiz  )
```

## Frage 9

**Szenario:** Sie möchten ein Korpus der Wahlprogramme deutscher Parteien von 1949 bis 2025 aufbauen, um die Entwicklung politischer Themen zu analysieren.

**Ihre Aufgabe:** 
1. Welche Korpus-Strategie würden Sie wählen und warum?
2. Skizzieren Sie mindestens 5 relevante Metadaten-Elemente (auf Korpusebene UND Dokumentebene)
3. Begründen Sie Ihre Entscheidungen

```{code-cell} ipython3
:tags: [remove-input]
import sys
sys.path.append("../quadriga")
from assessment import create_answer_box

create_answer_box('corpus-1')
```

````{admonition} Musterlösung
:class: solution, dropdown

**Musterlösung:**

**1. Korpus-Strategie:**

**Vollständiges Korpus** wäre die beste Wahl, weil:
- Klar definierter und begrenzter Gegenstandsbereich (Wahlprogramme etablierter Parteien)
- Relativ überschaubare Anzahl an Dokumenten (ca. 20 Bundestagswahlen × durchschnittlich 5-7 Parteien)
- Alle Dokumente sind bzw. sollten verfügbar sein
- Vollständigkeit ermöglicht umfassende Analyse der Entwicklung
- Keine Notwendigkeit für Stichprobenziehung

Alternative: **Balanciertes Korpus** (falls Vollständigkeit nicht möglich):
- Ausgewählte Wahlperioden gleichmäßig verteilt
- Alle relevanten Parteien repräsentiert
- Verschiedene politische Phasen abgedeckt

**2. Metadaten-Elemente:**

**Auf Korpusebene:**
- **DC.title**: "Korpus deutscher Wahlprogramme 1949-2025"
- **DC.description**: "Sammlung der Wahlprogramme aller im Bundestag vertretenen Parteien von 1949 bis 2025"
- **DC.creator**: [Name/Institution]
- **DC.date**: [Erstellungsdatum des Korpus]
- **DC.coverage**: "1949-2025, Deutschland, Bundestagswahlen"
- **DC.format**: "PDF, TXT"
- **DC.language**: "Deutsch"

**Auf Dokumentebene:**
- **DC.title**: "Wahlprogramm [Parteiname] zur Bundestagswahl [Jahr]"
- **DC.creator**: [Parteiname]
- **DC.date**: [Veröffentlichungsdatum]
- **DC.publisher**: [Parteiname oder -zentrale]
- **DC.subject**: "Wahlprogramm, Bundestagswahl, [spezifische Themen]"
- **DC.identifier**: [eindeutige ID, z.B. "BTW_2021_SPD"]
- **DC.source**: [URL oder Archivquelle]

**3. Begründungen:**

- **Vollständigkeit**: Ermöglicht umfassende diachrone Analyse ohne Lücken
- **Metadaten auf zwei Ebenen**: Korpus- und Dokumentebene für verschiedene Analysezwecke
- **Zeitliche Einordnung**: Essentiell für Entwicklungsanalyse
- **Partei-Information**: Ermöglicht Vergleiche zwischen Parteien
- **Eindeutige Identifikatoren**: Wichtig für Referenzierung und Nachnutzung
- **Coverage auf Korpusebene**: Gibt Gesamtrahmen an
- **Subject auf Dokumentebene**: Ermöglicht thematische Filterung
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
        "question": "Warum ist die Reflexion über Korpusaufbau und -grenzen ein unabdingbarer Bestandteil von Digital Humanities-Projekten?",
        "type": "multiple_choice",
        "answers": [
            {
                "answer": "Weil die Strategie und Kriterien des Korpusaufbaus darüber entscheiden, welche Forschungsfragen sinnvoll beantwortet werden können",
                "correct": True,
                "feedback": """✓ Korrekt! Das ist zentral: Das Korpus bestimmt die Reichweite der Ergebnisse, nicht alle Fragen sind mit jedem Korpus beantwortbar, die Zusammenstellung hat methodische Konsequenzen und wissenschaftliche Ehrlichkeit erfordert diese Reflexion."""
            },
            {
                "answer": "Weil mit dem Korpusaufbau das epistemische Objekt der Forschung konstruiert wird",
                "correct": True,
                "feedback": """✓ Korrekt! Wichtige erkenntnistheoretische Einsicht: Das Korpus ist nicht neutral, Auswahlentscheidungen prägen Forschungsergebnisse, die Konstruktion des Forschungsgegenstands ist ein bewusster Akt und beeinflusst, was überhaupt erkennbar ist."""
            },
            {
                "answer": "Weil Reflexion Zeit spart und den Forschungsprozess beschleunigt",
                "correct": False,
                "feedback": """× Nicht der Hauptgrund. Reflexion nimmt Zeit in Anspruch, ist methodisch notwendig statt aus Effizienzgründen erforderlich, dient der wissenschaftlichen Qualität und kann den Prozess sogar verlangsamen, ihn dabei aber verbessern."""
            },
            {
                "answer": "Weil ohne Reflexion die korpusbedingten Grenzen der Analyseergebnisse nicht erkannt werden",
                "correct": True,
                "feedback": """✓ Korrekt! Kritische Selbstreflexion ist wichtig: Sie vermeidet Übergeneralisierung, macht Grenzen der Aussagen transparent, ermöglicht angemessene Interpretation und ist Teil wissenschaftlicher Integrität."""
            },
            {
                "answer": "Weil nur durch Reflexion garantiert werden kann, dass alle Texte einer Domäne erfasst werden",
                "correct": False,
                "feedback": """× Nicht korrekt. Reflexion garantiert keine Vollständigkeit, Vollständigkeit ist nicht immer das Ziel, Reflexion hilft dabei, bewusste Entscheidungen zu treffen, und fokussiert auf Angemessenheit statt auf Vollständigkeit."""
            }
        ]
    }
]
display_quiz(question10, colors=colors.jupyterquiz  )
```

## Frage 11

```{code-cell} ipython3
:tags: [remove-input]
import sys
sys.path.append("../quadriga")
from assessment import DragDropQuiz

quiz = DragDropQuiz()

quiz.create_matching_quiz(
    title="Ordnen Sie die folgenden Schritte beim Korpusaufbau in die richtige Reihenfolge:",
    descriptions=[
        "Definition der Metadatenstruktur für Korpus und Elemente",
        "Entwicklung des Korpuskonzepts und der Forschungsfrage",
        "Festlegung der Korpus-Strategie (vollständig, repräsentativ, balanciert, opportunistisch)",
        "Sammlung und Aufbereitung der Texte",
        "Reflexion der Korpusgrenzen und deren Auswirkungen auf Analyseergebnisse"
    ],
    options=["5", "3", "1", "4", "2"],
    correct_mapping={
        "Entwicklung des Korpuskonzepts und der Forschungsfrage": "1",
        "Festlegung der Korpus-Strategie (vollständig, repräsentativ, balanciert, opportunistisch)": "2",
        "Definition der Metadatenstruktur für Korpus und Elemente": "3",
        "Sammlung und Aufbereitung der Texte": "4",
        "Reflexion der Korpusgrenzen und deren Auswirkungen auf Analyseergebnisse": "5"
    }
)
```
