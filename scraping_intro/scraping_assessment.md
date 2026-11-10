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

**Geschätzte Zeit**: 5–10 min.

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
        "question": "Welche Komponenten sind an einem HTTP-Request beteiligt? Wählen Sie alle zutreffenden Aussagen.",
        "type": "multiple_choice",
        "answers": [
            {
                "answer": "Der Client sendet eine Anfrage an den Server",
                "correct": True,
                "feedback": """✓ Korrekt! Der Client ist Ihr Computer oder Browser, initiiert die Kommunikation, sendet den HTTP-Request und wartet auf die Antwort des Servers."""
            },
            {
                "answer": "Die URL (Uniform Resource Locator) spezifiziert die gewünschte Ressource",
                "correct": True,
                "feedback": """✓ Korrekt! Die URL ist die Webadresse, enthält Protokoll, Domain, Pfad und ggf. Parameter und identifiziert die angeforderte Ressource, zum Beispiel https://www.berlin.de/rbmskzl/."""
            },
            {
                "answer": "Die Request-Methode (z.B. GET oder POST) gibt an, welche Aktion erwartet wird",
                "correct": True,
                "feedback": """✓ Korrekt! Die Request-Methode definiert die Art der Anfrage und ist wichtig für die Server-Verarbeitung: Bei GET werden Daten angefordert, ohne sie zu verändern, bei POST werden Daten an den Server gesendet."""
            },
            {
                "answer": "Der Server ist derjenige, der die Anfrage stellt",
                "correct": False,
                "feedback": """× Nicht korrekt. Wichtige Unterscheidung: Der CLIENT stellt die Anfrage, der SERVER empfängt die Anfrage und antwortet dann mit einer Response, denn Client und Server haben unterschiedliche Rollen."""
            }
        ]
    }
]
display_quiz(question1, colors=colors.jupyterquiz   )
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
        "question": "Was ist der Unterschied zwischen einem GET- und einem POST-Request? Wählen Sie alle zutreffenden Aussagen.",
        "type": "multiple_choice",
        "answers": [
            {
                "answer": "GET-Requests fordern Daten an, ohne sie zu verändern",
                "correct": True,
                "feedback": """✓ Korrekt! GET-Requests rufen nur Daten ab, ohne Veränderungen am Server vorzunehmen, sind vergleichbar mit dem Bestellen aus einem Katalog und sind Standard für Webseiten-Aufrufe."""
            },
            {
                "answer": "POST-Requests senden Daten an den Server",
                "correct": True,
                "feedback": """✓ Korrekt! POST-Requests übermitteln Daten zum Server, zum Beispiel Formulardaten oder Login-Informationen, sind vergleichbar mit dem Zurücksenden eines ausgefüllten Formulars, und die Daten sind dabei nicht in der URL sichtbar."""
            },
            {
                "answer": "GET-Requests sind in der URL sichtbar, POST-Requests nicht",
                "correct": True,
                "feedback": """✓ Korrekt! Das ist ein wichtiger Unterschied: Bei GET stehen Parameter in der URL (z.B. ?suche=Begriff), bei POST stehen die Daten im Request-Body, was bei sensiblen Daten einen Sicherheitsaspekt darstellt, weshalb POST für Passwörter etc. besser geeignet ist."""
            },
            {
                "answer": "GET und POST sind völlig identisch in ihrer Funktion",
                "correct": False,
                "feedback": """× Nicht korrekt. Sie haben unterschiedliche Zwecke: GET dient dem Abrufen von Daten, POST dem Senden von Daten, und beide unterscheiden sich in Anwendungsfällen und Sicherheitsaspekten."""
            }
        ]
    }
]
display_quiz(question2, colors=colors.jupyterquiz   )
```

## Frage 3

```{code-cell} ipython3
:tags: [remove-input]
import sys
sys.path.append("../quadriga")
from assessment import DragDropQuiz

quiz = DragDropQuiz()

quiz.create_matching_quiz(
    title="Ordnen Sie die HTTP-Statuscodes den richtigen Bedeutungen zu:",
    descriptions=[
        "Anfrage erfolgreich, hier sind die gewünschten Daten",
        "Die angeforderte Seite existiert nicht",
        "Zugriff verweigert",
        "Interner Server-Fehler"
    ],
    options=["200 (OK)", "404 (Not Found)", "403 (Forbidden)", "500 (Internal Server Error)", "301 (Moved Permanently)"],
    correct_mapping={
        "Anfrage erfolgreich, hier sind die gewünschten Daten": "200 (OK)",
        "Die angeforderte Seite existiert nicht": "404 (Not Found)",
        "Zugriff verweigert": "403 (Forbidden)",
        "Interner Server-Fehler": "500 (Internal Server Error)"
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
        "question": "Welche Komponenten enthält eine HTTP-Response? Wählen Sie alle zutreffenden Aussagen.",
        "type": "multiple_choice",
        "answers": [
            {
                "answer": "Einen Statuscode zur Information über den Erfolg der Anfrage",
                "correct": True,
                "feedback": """✓ Korrekt! Der Statuscode informiert über Erfolg oder Misserfolg, ist eine dreistellige Zahl (z.B. 200, 404), deren erste Stelle die Kategorie angibt, und ermöglicht so eine Fehlerbehandlung."""
            },
            {
                "answer": "Einen Response-Header mit Metainformationen über die Antwort",
                "correct": True,
                "feedback": """✓ Korrekt! Der Response-Header enthält Metainformationen, z.B. Content-Type, Datum und Server-Info, die für die Verarbeitung wichtig sind, aber nicht den eigentlichen Inhalt darstellen."""
            },
            {
                "answer": "Einen Response-Body mit dem eigentlichen Inhalt",
                "correct": True,
                "feedback": """✓ Korrekt! Der Response-Body enthält den eigentlichen Inhalt, meist HTML-Code für Webseiten, kann aber auch Bilder, JSON oder PDFs enthalten, also das, was Sie tatsächlich sehen möchten."""
            },
            {
                "answer": "Die URL der nächsten zu besuchenden Seite",
                "correct": False,
                "feedback": """× Nicht standardmäßig. Die Response enthält die angeforderten Daten, aber keine automatische nächste URL; Links können zwar im HTML-Body enthalten sein, jedoch nicht als Standard-Komponente."""
            }
        ]
    }
]
display_quiz(question4, colors=colors.jupyterquiz   )
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
        "question": "Was ist der Unterschied zwischen statischen und dynamischen Websites? Wählen Sie alle zutreffenden Aussagen.",
        "type": "multiple_choice",
        "answers": [
            {
                "answer": "Statische Websites sind fertige Dokumente, die unverändert vom Server gesendet werden",
                "correct": True,
                "feedback": """✓ Korrekt! Statische Websites liegen fertig vor und werden unverändert gesendet, ähnlich wie ein Buch aus der Bibliothek, wobei alle Inhalte bereits im HTML-Code enthalten sind."""
            },
            {
                "answer": "Dynamische Websites werden erst bei der Anfrage zusammengestellt",
                "correct": True,
                "feedback": """✓ Korrekt! Dynamische Websites werden on-demand erstellt, oft mit JavaScript, wobei Inhalte nachgeladen werden, ähnlich wie ein Koch, der auf Bestellung kocht."""
            },
            {
                "answer": "Statische Websites können leicht mit einfachen Scraping-Methoden extrahiert werden",
                "correct": True,
                "feedback": """✓ Korrekt! Das ist ein Vorteil für Scraping: Alle Inhalte stehen direkt im HTML, oft reicht einfaches requests, ein Browser ist nicht nötig, und das Vorgehen ist schneller und einfacher."""
            },
            {
                "answer": "Dynamische Websites benötigen keine speziellen Scraping-Methoden",
                "correct": False,
                "feedback": """× Nicht korrekt. Dynamische Websites benötigen fortgeschrittene Methoden, oft ist Selenium erforderlich, eine Browser-Simulation ist nötig, und JavaScript muss ausgeführt werden."""
            }
        ]
    }
]
display_quiz(question5, colors=colors.jupyterquiz   )
```

## Frage 6


```{code-cell} ipython3
:tags: [remove-input]
import sys
sys.path.append("../quadriga")
from assessment import DragDropQuiz

quiz = DragDropQuiz()

quiz.create_matching_quiz(
    title="Ordnen Sie die Python-Bibliotheken für Web-Scraping den passenden Beschreibungen zu:",
    descriptions=[
        "Einfache HTTP-Anfragen für einzelne statische Webseiten",
        "Effizientes Crawlen und Folgen von Links über mehrere Seiten",
        "Simulation von Benutzerinteraktionen und Ausführung von JavaScript"
    ],
    options=["requests", "scrapy", "selenium", "beautifulsoup"],
    correct_mapping={
        "Einfache HTTP-Anfragen für einzelne statische Webseiten": "requests",
        "Effizientes Crawlen und Folgen von Links über mehrere Seiten": "scrapy",
        "Simulation von Benutzerinteraktionen und Ausführung von JavaScript": "selenium"
    }
)
```

## Frage 7

```{code-cell} ipython3
:tags: [remove-input]
from jupyterquiz import display_quiz

import sys
sys.path.append("..")
from quadriga import colors

question7 = [
    {
        "question": "Welche Aussagen zu den Vor- und Nachteilen der Scraping-Methode 'requests' treffen zu? Wählen Sie alle zutreffenden Aussagen.",
        "type": "multiple_choice",
        "answers": [
            {
                "answer": "Einfach zu implementieren und geringer Ressourcenverbrauch",
                "correct": True,
                "feedback": """✓ Korrekt! Vorteile von requests sind die sehr einfache Syntax, der geringe Bedarf an Rechenleistung, die Geschwindigkeit und die gute Eignung für Einsteiger."""
            },
            {
                "answer": "Ausreichend für einfache Scraping-Aufgaben mit statischen Seiten",
                "correct": True,
                "feedback": """✓ Korrekt! Der Anwendungsbereich umfasst statische Seiten, das Abrufen einzelner Seiten sowie Fälle, in denen HTML direkt verfügbar ist und keine komplexen Interaktionen nötig sind."""
            },
            {
                "answer": "Kann automatisch Links folgen und mehrere Seiten durchsuchen",
                "correct": False,
                "feedback": """× Nicht korrekt. Das ist ein Nachteil: Es können nur einzelne Seiten abgerufen werden, eine automatische Navigation fehlt, für mehrere Seiten eignet sich scrapy besser, und eine manuelle Programmierung ist nötig."""
            },
            {
                "answer": "Geeignet für dynamisch generierte Inhalte mit JavaScript",
                "correct": False,
                "feedback": """× Nicht korrekt. Das ist ein Nachteil: Es werden nur statische Inhalte erfasst, JavaScript wird nicht ausgeführt, für dynamische Inhalte ist selenium nötig, und es wird nur der ursprüngliche HTML-Code gesehen."""
            }
        ]
    }
]
display_quiz(question7, colors=colors.jupyterquiz   )
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
        "question": "Wann sollte man Selenium anstelle von requests oder scrapy verwenden? Wählen Sie alle zutreffenden Aussagen.",
        "type": "multiple_choice",
        "answers": [
            {
                "answer": "Wenn Inhalte dynamisch mittels JavaScript geladen werden",
                "correct": True,
                "feedback": """✓ Korrekt! Selenium ist nötig für JavaScript-generierte Inhalte, dynamisches Nachladen, interaktive Elemente und Single Page Applications."""
            },
            {
                "answer": "Wenn Benutzerinteraktionen simuliert werden müssen (z.B. Klicken, Scrollen)",
                "correct": True,
                "feedback": """✓ Korrekt! Selenium kann Buttons klicken, Formulare ausfüllen und scrollen und dabei wie ein menschlicher Nutzer agieren."""
            },
            {
                "answer": "Wenn man eine einfache statische Webseite abrufen möchte",
                "correct": False,
                "feedback": """× Nicht optimal. Für statische Seiten ist requests ausreichend, Selenium wäre overkill, da es zu ressourcenintensiv und zu langsam für einfache Aufgaben ist."""
            },
            {
                "answer": "Wenn Geschwindigkeit und geringer Ressourcenverbrauch wichtig sind",
                "correct": False,
                "feedback": """× Nicht korrekt. Selenium ist deutlich langsamer, benötigt mehr Ressourcen und startet einen echten Browser; für Geschwindigkeit eignen sich requests oder scrapy besser."""
            }
        ]
    }
]
display_quiz(question8, colors=colors.jupyterquiz   )
```

## Frage 9

```{code-cell} ipython3
:tags: [remove-input]
from jupyterquiz import display_quiz

import sys
sys.path.append("..")
from quadriga import colors

question10 = [
    {
        "question": "Welche ethischen und rechtlichen Aspekte müssen beim Web-Scraping beachtet werden? Wählen Sie alle zutreffenden Aussagen.",
        "type": "multiple_choice",
        "answers": [
            {
                "answer": "Die robots.txt-Datei einer Website sollte beachtet werden",
                "correct": True,
                "feedback": """✓ Korrekt! Die robots.txt gibt Scraping-Richtlinien vor, zeigt, welche Bereiche erlaubt sind, sollte respektiert werden und liegt meist unter example.com/robots.txt."""
            },
            {
                "answer": "Angemessene Wartezeiten zwischen Anfragen sollten eingehalten werden",
                "correct": True,
                "feedback": """✓ Korrekt! Wartezeiten vermeiden Serverüberlastung, zeigen respektvolles Verhalten, liegen typisch bei 1-2 Sekunden zwischen Requests und verhindern, dass das Scraping als Angriff wahrgenommen wird."""
            },
            {
                "answer": "Persönliche Daten dürfen ohne Einwilligung gesammelt werden, wenn sie öffentlich sind",
                "correct": False,
                "feedback": """× Nicht korrekt! Der Datenschutz muss beachtet werden: Auch öffentliche Daten unterliegen dem Datenschutz, die DSGVO muss beachtet werden, eine Einwilligung ist oft erforderlich, und besondere Vorsicht ist bei personenbezogenen Daten geboten."""
            },
            {
                "answer": "Urheberrecht und Nutzungsbedingungen der Websites müssen beachtet werden",
                "correct": True,
                "feedback": """✓ Korrekt! Zu den rechtlichen Aspekten gehört, dass das Urheberrecht auch im Web gilt, die Terms of Service gelesen werden sollten und nicht jede öffentliche Information genutzt werden darf; bei Unsicherheit sollte rechtliche Beratung eingeholt werden."""
            }
        ]
    }
]
display_quiz(question10, colors=colors.jupyterquiz   )
```