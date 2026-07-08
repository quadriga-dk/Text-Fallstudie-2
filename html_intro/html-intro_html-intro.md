(html-intro_html-intro)=
# Einführung in HTML

HTML (HyperText Markup Language) ist die Grundsprache des Internets. Sie wird verwendet, um Webseiten zu strukturieren und Inhalte wie Text, Bilder und Links darzustellen. Die Bausteine der HTML-Sprache sind HTML-Elemente.

```{figure} ../book_images/html_tag_anatomy.png
---
height:
name: HTML-Element
---
Der Aufbau eines einfachen HTML-Elements
```

## Die Grundstruktur einer HTML-Seite
Jede HTML-Datei beginnt mit der Deklaration `<!DOCTYPE html>`, die dem Browser mitteilt, um welchen Dokumenttyp es sich handelt. Für HTML5 sieht die grundlegende Struktur so aus:

```html
<!DOCTYPE html>
<html>
<head>
    <title>Meine erste Webseite</title>
</head>
<body>
    <h1>Willkommen!</h1>
    <p>Dies ist ein einfacher Absatz.</p>
</body>
</html>
```

- `<html>`: Der Hauptcontainer für die gesamte Seite.
- `<head>`: Enthält Metainformationen und den Titel der Seite.
- `<title>`: Legt den Titel der Webseite fest.
- `<body>`: Enthält den sichtbaren Inhalt der Seite.

## Wichtige HTML-Elemente
HTML besteht aus verschiedenen Elementen, die durch Tags (`<tag>` und `</tag>`) gekennzeichnet sind.

### a) Überschriften und Absätze
- `<h1>`, `<h2>`, ..., `<h6>`: Überschriften unterschiedlicher Größe.
- `<p>`: Ein Absatz.

```html
<h1>Überschrift 1</h1>
<h2>Überschrift 2</h2>
<p>Dies ist ein Absatz.</p>
```

### b) Links und Bilder
- `<a href="URL">Text</a>`: Erstellt einen Link.
- `<img src="bild.jpg" alt="Beschreibung">`: Fügt ein Bild ein.

```html
<a href="https://www.example.com">Besuche Example</a>
<img src="bild.jpg" alt="Beispielbild">
```

### HTML-Attribute

HTML-Tags können Attribute enthalten, die zusätzliche Informationen bereitstellen. Ein Attribut wird im Start-Tag angegeben und besteht aus einem Namen und einem Wert:

```html
<tagname attributname="wert">Inhalt</tagname>
```

Beispiele:

```html
<a href="https://www.example.com" target="_blank">Öffne Link in neuem Tab</a>
<img src="bild.jpg" alt="Beispielbild" width="300">
```

Häufig verwendete Attribute sind:

* `href` bei Links
* `src`, `alt`, `width`, `height` bei Bildern
* `id`, `class` zur Identifizierung und Gestaltung per CSS

## Listen und Tabellen

### a) Ungeordnete und geordnete Listen
- `<ul>`: Eine Liste mit Punkten.
- `<ol>`: Eine nummerierte Liste.
- `<li>`: Ein Listenelement.

```html
<ul>
    <li>Erstes Element</li>
    <li>Zweites Element</li>
</ul>
```

### b) Tabellen
- `<table>`: Erstellt eine Tabelle.
- `<tr>`: Erstellt eine Zeile.
- `<td>`: Erstellt eine Zelle.
- `<th>`: Erstellt eine Kopfzelle.

```html
<table>
    <tr>
        <th>Name</th>
        <th>Alter</th>
    </tr>
    <tr>
        <td>Max</td>
        <td>25</td>
    </tr>
</table>
```

## Hierarchische Struktur in HTML

HTML-Dokumente bestehen aus verschachtelten (nested) Elementen. Das bedeutet, dass Tags innerhalb anderer Tags liegen können. Diese hierarchische Struktur bildet einen sogenannten DOM-Baum (Document Object Model), der von Browsern oder Programmen zum Analysieren und Verarbeiten genutzt wird.

Beispiel:

```html
<div>
    <h2>Überschrift</h2>
    <p>Ein Absatz mit <a href="#">einem Link</a> darin.</p>
</div>
```

Hier liegt das `<a>`-Element innerhalb des `<p>`-Elements, und beide liegen wiederum im `<div>`-Element. Solche Strukturen sind wichtig, um Webseiten korrekt zu gestalten und um beim Scraping gezielt Inhalte auszuwählen.

## HTML und CSS
HTML strukturiert die Inhalte, für das Design (Farben, Schriften, Abstände, Layout) wird hingegen CSS (Cascading Style Sheets) verwendet. CSS kann auf drei Arten mit einem HTML-Dokument verbunden werden:

- **Inline** als `style`-Attribut direkt an einem einzelnen Element, z. B. `<p style="color: red;">…</p>`.
- **Intern** im Kopf des Dokuments innerhalb eines `<style>`-Elements (siehe Beispiel unten).
- **Extern** in einer separaten `.css`-Datei, die über ein `<link>`-Element eingebunden wird, z. B. `<link rel="stylesheet" href="styles.css">`. Das Auslagern in eine eigene Datei ist bei größeren Websites üblich, weil sich dieselben Stilregeln so für viele Seiten wiederverwenden lassen.

Im folgenden Beispiel werden die Stilregeln innerhalb eines `<style>`-Elements definiert. Sogenannte **Selektoren** geben dabei an, welche HTML-Elemente gestaltet werden sollen – hier alle `body`- und `h1`-Elemente:

```html
<style>
    body { background-color: lightblue; }
    h1 { color: darkblue; }
</style>
```

Für das Web Scraping sind vor allem die Selektoren relevant: Mit ihnen lassen sich Elemente gezielt ansprechen – nach demselben Prinzip werden später beim Scraping die zu extrahierenden Inhalte ausgewählt. Eine ausführlichere Einführung in CSS bietet <a href="https://wiki.selfhtml.org/wiki/CSS" class="external-link" target="_blank">SELFHTML</a>.

## Fazit
HTML ist einfach zu lernen und bildet die Grundlage jeder Webseite. Mit HTML kann man Texte, Bilder, Links, Tabellen und mehr darstellen. CSS ist ein wichtiger Bestandteil des Webdesigns. Um Websites zu scrapen und automatisch Daten aus dem Web zu extrahieren, sind HTML-Kenntnisse besonders wichtig.

### Video: eine 3-minütige HTML-Einführung von W3C

<iframe width="560" height="315" src="https://www.youtube.com/embed/it1rTvBcfRg?si=eGiQ0_jPRctkv2MV&amp;start=10" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
