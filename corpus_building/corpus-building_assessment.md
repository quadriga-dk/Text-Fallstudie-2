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
        "question": "Welche Schritte sind beim praktischen Korpusaufbau durch Massenscraping notwendig? Wählen Sie alle zutreffenden Aussagen.",
        "type": "multiple_choice",
        "answers": [
            {
                "answer": "Untersuchung der HTML-Struktur der Zielwebsite (z.B. mit dem Browser-Inspektor)",
                "correct": True,
                "feedback": """✓ Korrekt! Die Strukturanalyse ist der erste Schritt: Sie dient der Identifikation relevanter HTML-Elemente, der Bestimmung von CSS-Selektoren und dem Verständnis des Seitenaufbaus und bildet damit die Basis für die Implementierung."""
            },
            {
                "answer": "Extraktion von Links zu allen relevanten Einzelseiten",
                "correct": True,
                "feedback": """✓ Korrekt! Link-Extraktion ist essentiell: Dabei werden alle URLs aus Übersichtsseiten gesammelt, oft aus Tabellen oder Listen, was die Basis für das systematische Crawling bildet und die Navigation durch das gesamte Korpus ermöglicht."""
            },
            {
                "answer": "Scraping der Einzelseiten mit Speicherung von HTML und bereinigtem Text",
                "correct": True,
                "feedback": """✓ Korrekt! Doppelte Speicherung ist sinnvoll: HTML dient der Nachvollziehbarkeit und Re-Analyse, bereinigter Text der direkten Textanalyse, wodurch verschiedene Nutzungsszenarien ermöglicht werden – dies ist Best Practice beim Korpusaufbau."""
            },
            {
                "answer": "Sofortige manuelle Korrektur jeder extrahierten Seite",
                "correct": False,
                "feedback": """× Nicht korrekt. Bei Massenscraping ist Automatisierung das Ziel, da manuelle Korrektur bei 50.000+ Dokumenten unmöglich ist; die Qualitätskontrolle erfolgt durch Stichproben, und eine Nachbearbeitung findet nur bei systematischen Problemen statt."""
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
        "question": "Welche Rolle spielt BeautifulSoup beim praktischen Korpusaufbau? Wählen Sie alle zutreffenden Aussagen.",
        "type": "multiple_choice",
        "answers": [
            {
                "answer": "BeautifulSoup ermöglicht das Parsen von HTML-Dokumenten zu einem navigierbaren Parse-Tree",
                "correct": True,
                "feedback": """✓ Korrekt! Das ist die Kernfunktion: die Umwandlung von HTML-String in eine Baum-Struktur, die Navigation durch das DOM ermöglicht und die Basis für die Element-Suche bildet, etwa mit Parsern wie 'lxml' oder 'html.parser'."""
            },
            {
                "answer": "BeautifulSoup bietet Methoden wie select() und find() zur Extraktion spezifischer Elemente",
                "correct": True,
                "feedback": """✓ Korrekt! Diese Methoden sind zentral: select() nutzt CSS-Selektoren, find() findet einzelne Elemente und find_all() findet mehrere Elemente, was eine flexible Element-Auswahl ermöglicht."""
            },
            {
                "answer": "BeautifulSoup kann Text aus HTML-Elementen extrahieren (z.B. mit get_text())",
                "correct": True,
                "feedback": """✓ Korrekt! Textextraktion ist wichtig: get_text() liefert nur Text ohne Tags, mit strip=True lassen sich Leerzeichen entfernen und mit get_text(' ') ein Separator angeben, was die Basis für saubere Textdaten bildet."""
            },
            {
                "answer": "BeautifulSoup führt automatisch HTTP-Requests durch",
                "correct": False,
                "feedback": """× Nicht korrekt. Es gibt eine klare Aufgabenteilung: HTTP-Requests übernimmt die requests-Bibliothek, HTML-Parsing übernimmt BeautifulSoup, beide arbeiten zusammen, und diese Trennung ermöglicht Flexibilität."""
            }
        ]
    }
]
display_quiz(question2, colors=colors.jupyterquiz)
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
        "question": "Warum ist die Implementierung von Retry-Logik und Sleep-Intervallen beim Massenscraping wichtig? Wählen Sie alle zutreffenden Aussagen.",
        "type": "multiple_choice",
        "answers": [
            {
                "answer": "Temporäre Netzwerkfehler können durch wiederholte Versuche überwunden werden",
                "correct": True,
                "feedback": """✓ Korrekt! Netzwerk ist nicht immer stabil: DNS-Fehler können vorübergehend sein, Timeouts können auftreten und Verbindungsabbrüche sind möglich, weshalb mehrere Versuche die Erfolgsrate erhöhen."""
            },
            {
                "answer": "Sleep-Intervalle verhindern Überlastung des Servers und mögliche Blockierungen",
                "correct": True,
                "feedback": """✓ Korrekt! Das ist serverfreundliches Verhalten: Es vermeidet zu hohe Last, respektiert Rate Limits und verhindert IP-Sperrung (429 Too Many Requests) und ist zudem ethisch geboten."""
            },
            {
                "answer": "Bei HTTP-Status 404 oder 410 sollte kein Retry durchgeführt werden",
                "correct": True,
                "feedback": """✓ Korrekt! Bei permanenten vs. temporären Fehlern gilt: 404 Not Found bedeutet, dass die Seite nicht existiert, und 410 Gone bedeutet, dass die Seite entfernt wurde – beide sind dauerhaft, sodass kein Retry sinnvoll ist. 5xx- und 429-Fehler sind dagegen temporär, weshalb hier ein Retry sinnvoll ist."""
            },
            {
                "answer": "Retry-Logik und Sleep-Intervalle sind nur für große Projekte relevant",
                "correct": False,
                "feedback": """× Nicht korrekt. Das ist immer wichtig: Auch bei kleinen Projekten können Fehler auftreten, es handelt sich um Best Practice unabhängig von der Größe, es geht um Stabilität und Zuverlässigkeit sowie um ethische Verantwortung."""
            }
        ]
    }
]
display_quiz(question3, colors=colors.jupyterquiz)
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
        "question": "Welche Scraping-Methode eignet sich für folgende Szenarien am besten? Wählen Sie alle zutreffenden Aussagen.",
        "type": "multiple_choice",
        "answers": [
            {
                "answer": "Für statische Übersichtsseiten mit Links zu Einzelartikeln eignet sich requests + BeautifulSoup",
                "correct": True,
                "feedback": """✓ Korrekt! Diese Kombination ist optimal für statisches HTML ohne JavaScript und klar strukturierte Seiten (z.B. Tabellen) sowie für das systematische Durchlaufen von Links, wie im Kapitel am Beispiel von Pressemitteilungen gezeigt."""
            },
            {
                "answer": "Wenn Inhalte erst beim Scrollen nachgeladen werden, ist Selenium notwendig",
                "correct": True,
                "feedback": """✓ Korrekt! Selenium eignet sich für dynamische Inhalte, da JavaScript-Ausführung erforderlich ist, Benutzerinteraktionen simuliert werden müssen und Inhalte nachgeladen werden, während requests nur den initialen HTML-Code sehen würde."""
            },
            {
                "answer": "Für mehrere tausend verlinkte Seiten mit ähnlicher Struktur ist scrapy effizienter als requests",
                "correct": True,
                "feedback": """✓ Korrekt! Scrapy bietet Vorteile wie integriertes Link-Following, paralleles Crawling, robustes Error-Handling und eine bessere Performance bei großen Projekten."""
            },
            {
                "answer": "requests + BeautifulSoup kann auch JavaScript-generierte Inhalte problemlos extrahieren",
                "correct": False,
                "feedback": """× Nicht korrekt. Wichtige Einschränkung: requests sieht nur den initialen HTML-Code, JavaScript wird NICHT ausgeführt und dynamische Inhalte fehlen daher – für JavaScript ist Selenium erforderlich."""
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

question5 = [
    {
        "question": "Warum sollten Metadaten parallel zum Scraping-Prozess systematisch erfasst und gespeichert werden? Wählen Sie alle zutreffenden Aussagen.",
        "type": "multiple_choice",
        "answers": [
            {
                "answer": "Bei Unterbrechung des Scraping-Prozesses gehen keine Informationen verloren",
                "correct": True,
                "feedback": """✓ Korrekt! Das dient der Absicherung gegen Abbrüche: Scraping kann Stunden oder Tage dauern, Netzwerkprobleme können auftreten, laufende CSV-Speicherung sichert den Fortschritt, und eine Wiederaufnahme an letzter Stelle wird möglich."""
            },
            {
                "answer": "Metadaten ermöglichen spätere Analysen wie Zeitreihen und Quellenvergleiche",
                "correct": True,
                "feedback": """✓ Korrekt! Der analytische Wert zeigt sich darin, dass das Datum Zeitreihenanalysen ermöglicht, Quelle/Ressort den Vergleich verschiedener Absender erlaubt, die URL die Rückverfolgbarkeit sichert und die Länge Verteilungsanalysen ermöglicht."""
            },
            {
                "answer": "Metadaten helfen bei der Identifikation von Lücken oder Problemen im Korpus",
                "correct": True,
                "feedback": """✓ Korrekt! Zur Qualitätskontrolle gehören die Übersicht über erfasste Dokumente, die Erkennung fehlender IDs, das Debugging bei Problemen und die Vollständigkeitsprüfung."""
            },
            {
                "answer": "Metadaten sollten erst nach Abschluss des gesamten Scraping-Prozesses erstellt werden",
                "correct": False,
                "feedback": """× Nicht korrekt. Parallele Erfassung ist besser: Sie schützt vor Datenverlust bei Abbruch, bietet eine laufende Übersicht über den Fortschritt und ermöglicht eine frühzeitige Problemerkennung – inkrementelle Speicherung ist hier Best Practice."""
            }
        ]
    }
]
display_quiz(question5, colors=colors.jupyterquiz)
```

## Frage 6

```{code-cell} ipython3
:tags: [remove-input]
import sys
sys.path.append("../quadriga")
from assessment import DragDropQuiz

quiz = DragDropQuiz()

quiz.create_matching_quiz(
    title="Ordnen Sie die Schritte des Korpusaufbaus in die richtige Reihenfolge:",
    descriptions=[
        "Untersuchung der HTML-Struktur der Übersichtsseite",
        "Scraping der Einzelseiten mit HTTP-Requests",
        "Extraktion aller Links zu Einzelseiten",
        "Extraktion und Speicherung von Text und Metadaten"
    ],
    options=["3", "1", "4", "2"],
    correct_mapping={
        "Untersuchung der HTML-Struktur der Übersichtsseite": "1",
        "Extraktion aller Links zu Einzelseiten": "2",
        "Scraping der Einzelseiten mit HTTP-Requests": "3",
        "Extraktion und Speicherung von Text und Metadaten": "4"
    }
)
```

## Frage 7

**Szenario:** Sie untersuchen eine Nachrichten-Website und finden folgende HTML-Struktur auf der Übersichtsseite:

```html
<table>
  <tbody>
    <tr>
      <td>15.01.2024</td>
      <td><a href="/artikel/12345.html">Neuer Stadtrat gewählt</a></td>
      <td>Rathaus</td>
    </tr>
    <tr>
      <td>14.01.2024</td>
      <td><a href="/artikel/12344.html">Haushalt beschlossen</a></td>
      <td>Finanzen</td>
    </tr>
  </tbody>
</table>
```

**Aufgaben:**
1. Welchen CSS-Selektor würden Sie verwenden, um alle Tabellenzeilen zu finden?
2. Wie würden Sie aus einer Zeile das Datum, den Titel und den Link extrahieren?
3. Wie würden Sie aus dem relativen Link "/artikel/12345.html" eine vollständige URL machen?
4. Welche Metadaten würden Sie für jeden Artikel erfassen?

```{code-cell} ipython3
:tags: [remove-input]
import sys
sys.path.append("../quadriga")
from assessment import create_answer_box

create_answer_box('corpus-building-1')
```

````{admonition} Musterlösung
:class: solution, dropdown

**Musterlösung:**

**1. CSS-Selektor für Tabellenzeilen:**

```python
from bs4 import BeautifulSoup
soup = BeautifulSoup(html_string)
rows = soup.select("table tbody tr")
# oder: soup.select("tbody tr")
# oder: soup.find_all("tr")
```

**Erklärung:**
- `table tbody tr`: Findet alle `<tr>`-Elemente innerhalb von `<tbody>` innerhalb von `<table>`
- Spezifischer Selektor verhindert Fehlextr aktionen
- `select()` gibt eine Liste aller passenden Elemente zurück

---

**2. Extraktion von Datum, Titel und Link:**

```python
for tr in rows:
    # Alle Zellen der Zeile holen
    cells = tr.find_all("td")
    
    # Sicherheitscheck
    if len(cells) < 3:
        continue
    
    # Datum aus erster Zelle
    datum = cells[0].get_text(strip=True)
    
    # Titel und Link aus zweiter Zelle
    anchor = cells[1].find("a", href=True)
    if anchor:
        titel = anchor.get_text(strip=True)
        relative_url = anchor["href"]  # oder: anchor.get("href")
    
    # Quelle aus dritter Zelle
    quelle = cells[2].get_text(strip=True)
```

**Wichtige Methoden:**
- `find_all("td")`: Findet alle Zellen
- `get_text(strip=True)`: Extrahiert Text, entfernt Leerzeichen
- `find("a", href=True)`: Findet Link, nur wenn href vorhanden
- `anchor["href"]`: Zugriff auf Attribut

---

**3. Relative zu absoluter URL:**

**Methode A: Manuelle Konkatenation**
```python
base_url = "https://www.nachrichtenportal.de"
relative_url = "/artikel/12345.html"
vollstaendige_url = base_url + relative_url
# Ergebnis: "https://www.nachrichtenportal.de/artikel/12345.html"
```

**Methode B: urllib.parse.urljoin (empfohlen)**
```python
from urllib.parse import urljoin

base_url = "https://www.nachrichtenportal.de"
relative_url = "/artikel/12345.html"
vollstaendige_url = urljoin(base_url, relative_url)
# Ergebnis: "https://www.nachrichtenportal.de/artikel/12345.html"
```

**Vorteil von urljoin:**
- Behandelt verschiedene URL-Formate korrekt
- Berücksichtigt Protokoll und Domain
- Funktioniert auch mit vollständigen URLs (gibt sie unverändert zurück)

---

**4. Zu erfassende Metadaten:**

**Essentiell:**
- **ID:** Eindeutige Kennung (z.B. aus URL: "12345")
- **URL:** Vollständige Artikel-URL
- **Datum:** Veröffentlichungsdatum ("15.01.2024")
- **Titel:** Artikelüberschrift ("Neuer Stadtrat gewählt")
- **Quelle:** Ressort/Abteilung ("Rathaus")

**Zusätzlich empfohlen:**
- **Dateiname (HTML):** Wo wurde das Original gespeichert
- **Dateiname (TXT):** Wo wurde der bereinigte Text gespeichert
- **Scraping-Zeitpunkt:** Wann wurde der Artikel erfasst
- **Text-Länge:** Anzahl Tokens/Wörter (für Analysen)
- **HTTP-Status:** War der Abruf erfolgreich

**Speicherformat (CSV):**
```csv
DC.identifier,DC.source,DC.date,DC.title,DC.publisher,html_file,txt_file,scraped_at,n_tokens
12345,https://...,15.01.2024,Neuer Stadtrat gewählt,Rathaus,12345.html,12345.txt,2024-01-20,385
12344,https://...,14.01.2024,Haushalt beschlossen,Finanzen,12344.html,12344.txt,2024-01-20,412
```

**Code-Beispiel:**
```python
records = []

for tr in rows:
    cells = tr.find_all("td")
    if len(cells) < 3:
        continue
    
    datum = cells[0].get_text(strip=True)
    anchor = cells[1].find("a", href=True)
    if not anchor:
        continue
    
    titel = anchor.get_text(strip=True)
    relative_url = anchor["href"]
    quelle = cells[2].get_text(strip=True)
    
    # ID aus URL extrahieren
    uid = relative_url.split("/")[-1].split(".")[0]  # "12345"
    
    # Vollständige URL
    vollstaendige_url = urljoin(base_url, relative_url)
    
    # Metadaten sammeln
    records.append({
        'DC.identifier': uid,
        'DC.source': vollstaendige_url,
        'DC.date': datum,
        'DC.title': titel,
        'DC.publisher': quelle,
        'html_file': f"{uid}.html",
        'txt_file': f"{uid}.txt"
    })

```
In CSV speichern:

```python
import pandas as pd
df = pd.DataFrame(records)
df.to_csv('metadata.csv', index=False, encoding='utf-8')
```
````