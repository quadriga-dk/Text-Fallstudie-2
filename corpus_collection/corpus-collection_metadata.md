(corpus-collection_metadata)=
# Metadaten
```{admonition} Feinlernziel(e) dieses Kapitels
:class: lernziele
Sie sind mit der Idee von Metadaten vertraut und kennen basale Metadatenschemata für Korpora und Korpus-Elemente.
```

Metadaten sind Daten über Daten. Sie liefern kontextuelle Informationen, die helfen, die Bedeutung, Herkunft, Struktur und Nutzungsmöglichkeiten eines Datensatzes besser zu verstehen. In den Digital Humanities sind Metadaten unerlässlich, um die Volltextkorpora systematisch zu organisieren, auffindbar zu machen und deren inhaltliche und strukturelle Qualität zu sichern.

**Metadatenschemata**

Es gibt verschiedene Metadatenschemata, die für unterschiedliche Anforderungen entwickelt wurden. Sie unterscheiden sich vor allem darin, was sie beschreiben: rein deskriptive Angaben über eine Ressource (z.B. Titel, Autor:in, Datum), die Struktur und das Layout eines Dokuments, oder auch die inhaltliche Auszeichnung des Textes selbst (z.B. Personen, Orte, Textabschnitte). Zu den bekanntesten Schemata gehören:

1. **<a href="https://www.dublincore.org/specifications/dublin-core/dces/" class="external-link" target="_blank">Dublin Core</a>**: Ein einfaches und disziplinübergreifendes Schema mit 15 flachen Elementen wie Titel, Autor:in, Thema und Datum. Vorteil ist die einfache Anwendbarkeit; Nachteil ist, dass sich damit weder die interne Struktur eines Dokuments noch dessen Textinhalt erfassen lässt.
2. **<a href="https://tei-c.org/" class="external-link" target="_blank">TEI (Text Encoding Initiative)</a>**: Speziell für Texte entwickelt. TEI beschreibt eine Ressource nicht nur deskriptiv im [`<teiHeader>`](https://tei-c.org/release/doc/tei-p5-doc/de/html/ref-teiHeader.html), sondern erlaubt zusätzlich, den Text selbst inhaltlich auszuzeichnen (z.B. Personen, Orte) sowie dessen Struktur und Layout festzuhalten (z.B. Absätze, Seitenumbrüche, Faksimiles). Vorteil ist entsprechend der große Umfang; Nachteil ist der damit verbundene höhere Aufwand bei der Erstellung.
3. **<a href="https://www.loc.gov/standards/mods/" class="external-link" target="_blank">MODS (Metadata Object Description Schema)</a>**: Von der Library of Congress entwickelt. MODS bietet gegenüber Dublin Core deutlich granularere, teils verschachtelte Felder, bleibt aber wie Dublin Core rein deskriptiv und zeichnet weder Textinhalt noch Layout aus. Vorteil ist die höhere Präzision bei bibliographischen Angaben; Nachteil ist der höhere Erstellungsaufwand im Vergleich zu Dublin Core.
4. **<a href="https://www.loc.gov/standards/mets/" class="external-link" target="_blank">METS (Metadata Encoding and Transmission Standard)</a>**: Ein Containerformat, das die Struktur eines aus mehreren Dateien bestehenden digitalen Objekts (z.B. die Seiten eines digitalisierten Buchs) beschreibt und dabei deskriptive Metadaten, häufig in Form von eingebettetem Dublin Core oder MODS, mit administrativen Angaben verknüpft. Vorteil ist die Eignung für komplexe, mehrteilige Objekte; Nachteil ist, dass METS nur die Verpackung, nicht den Inhalt der Texte selbst beschreibt.

Die folgende Tabelle fasst die Unterschiede zusammen:

| Schema | Was wird beschrieben? | Detailgrad | Typischer Einsatz |
| --- | --- | --- | --- |
| Dublin Core | Deskriptive Metadaten einer Ressource | Niedrig (15 flache Elemente) | Schneller, disziplinübergreifender Überblick |
| MODS | Deskriptive Metadaten, v.a. bibliographisch | Mittel bis hoch (verschachtelte Felder) | Bibliothekskataloge, bibliographische Beschreibungen |
| METS | Struktur/Verpackung eines digitalen Objekts, inkl. eingebetteter Metadaten | Hoch (Containerformat) | Digitalisate aus mehreren Dateien (z.B. gescannte Bücher) |
| TEI | Deskriptive Metadaten, inhaltliche Auszeichnung des Textes und dessen Struktur/Layout | Sehr hoch | Editionen, inhaltlich annotierte Textkorpora |

Die Schnittmengen dieser drei Dimensionen (deskriptive Metadaten, Struktur/Layout, inhaltliche Auszeichnung) lassen sich auch grafisch darstellen:

```{figure} ../assets/images/metadata_schemata_venn.svg
---
name: Schnittmengen der Metadatenschemata
---
Dublin Core und MODS decken ausschließlich deskriptive Metadaten ab. METS verknüpft die Struktur eines digitalen Objekts mit eingebetteten deskriptiven Metadaten. TEI deckt als einziges der vier Schemata alle drei Dimensionen ab: deskriptive Metadaten, Struktur/Layout und inhaltliche Auszeichnung des Textes.
```

## Metadaten zur Beschreibung eines Korpus

Bei der Beschreibung eines gesamten Korpus sind die Metadaten entscheidend, um den Kontext, den Umfang und die Struktur des Korpus zu dokumentieren. Wichtige Aspekte sind unter anderem:

- **Titel und Beschreibung**: Um das Korpus eindeutig zu identifizieren und dessen Inhalt zu beschreiben.
- **Ersteller:innen und/oder Herausgeber:innen**: Angaben zu den Personen oder Institutionen, die das Korpus erstellt und veröffentlicht haben.
- **Datum**: Zeitangaben zur Erstellung und Veröffentlichung des Korpus.
- **Umfang und Format**: Informationen über die Anzahl der enthaltenen Dokumente und deren Dateiformate.
- **Sprache**: Die im Korpus vertretenen Sprachen.
- **Thematik und Schlagworte**: Stichworte, die die inhaltlichen Schwerpunkte des Korpus beschreiben.

**Beispiel unter Verwendung Dublin Core**

Ein beispielhaftes Metadaten-Set für ein Korpus könnte unter Verwendung von Dublin Core so aussehen:

- **<a href="https://www.dublincore.org/specifications/dublin-core/dcmi-terms/elements11/title/" class="external-link" target="_blank">DC.title</a>**: "Korpus der Pressemitteilungen des Lands Berlin von 2011-2024"
- **<a href="https://www.dublincore.org/specifications/dublin-core/dcmi-terms/elements11/description/" class="external-link" target="_blank">DC.description</a>**: "Eine Sammlung der digital veröffentlichen Pressemitteilungen publiziert über die Website berlin.de aus den Jahren 2011 bis 2024"
- **<a href="https://www.dublincore.org/specifications/dublin-core/dcmi-terms/elements11/creator/" class="external-link" target="_blank">DC.creator</a>**: "Henny Sluyter-Gäthje, Daniil Skorinkin, Peer Trilcke für QUADRIGA. Berlin-Brandenburgische Datenkompetenzzentrum für Digital Humanities und Verwaltungswissenschaft"
- **<a href="https://www.dublincore.org/specifications/dublin-core/dcmi-terms/elements11/publisher/" class="external-link" target="_blank">DC.publisher</a>**: "<a href="https://www.berlin.de" class="external-link" target="_blank">www.berlin.de</a>" 
- **<a href="https://www.dublincore.org/specifications/dublin-core/dcmi-terms/elements11/date/" class="external-link" target="_blank">DC.date</a>**: "2025-04-04"
- **<a href="https://www.dublincore.org/specifications/dublin-core/dcmi-terms/elements11/format/" class="external-link" target="_blank">DC.format</a>**: "HTML, TXT"
- **<a href="https://www.dublincore.org/specifications/dublin-core/dcmi-terms/elements11/language/" class="external-link" target="_blank">DC.language</a>**: "Deutsch"
- **<a href="https://www.dublincore.org/specifications/dublin-core/dcmi-terms/elements11/subject/" class="external-link" target="_blank">DC.subject</a>**: "Verwaltung, Öffentlichkeitsarbeit"
- **<a href="https://www.dublincore.org/specifications/dublin-core/dcmi-terms/elements11/coverage/" class="external-link" target="_blank">DC.coverage</a>**: "21. Jahrhundert, Deutschland"

## Metadaten für einzelne Korpus-Elemente

Für einzelne Elemente eines Korpus, wie beispielsweise einzelne Artikel oder Dokumente, sind spezifische Metadaten notwendig, um diese präzise zu identifizieren und zu kontextualisieren. Wichtige Metadaten umfassen hier z.B.:

- **Titel und Autor:innen**: Um das Dokument eindeutig zu identifizieren.
- **Datum der Veröffentlichung**: Für zeitliche Einordnung.
- **Quelle**: Angaben zur ursprünglichen Publikation oder Fundort.
- **Sprache**: Die im Dokument verwendete Sprache.
- **Identifier**: Ein eindeutiger Identifikator wie eine DOI oder eine andere Art von Kennung.

**Beispiel unter Verwendung von Dublin Core**

Für eine einzelne Pressemitteilung könnten die Metadaten so aussehen:

- **<a href="https://www.dublincore.org/specifications/dublin-core/dcmi-terms/elements11/title/" class="external-link" target="_blank">DC.title</a>**: "Straßenfest auf dem Hermann-Ehlers-Platz am 03.05.2024 zum 'Aktionstag BUNT VERBINDET'"
- **<a href="https://www.dublincore.org/specifications/dublin-core/dcmi-terms/elements11/creator/" class="external-link" target="_blank">DC.creator</a>**: "N.N."
- **<a href="https://www.dublincore.org/specifications/dublin-core/dcmi-terms/elements11/date/" class="external-link" target="_blank">DC.date</a>**: "2024-04-19"
- **<a href="https://www.dublincore.org/specifications/dublin-core/dcmi-terms/elements11/publisher/" class="external-link" target="_blank">DC.publisher</a>**: "Bezirksamt Steglitz-Zehlendorf"
- **<a href="https://www.dublincore.org/specifications/dublin-core/dcmi-terms/elements11/subject/" class="external-link" target="_blank">DC.subject</a>**: "Gleichstellung"
- **<a href="https://www.dublincore.org/specifications/dublin-core/dcmi-terms/elements11/coverage/" class="external-link" target="_blank">DC.coverage</a>**: "2024, Berlin"
- **<a href="https://www.dublincore.org/specifications/dublin-core/dcmi-terms/elements11/language/" class="external-link" target="_blank">DC.language</a>**: "Deutsch"
- **<a href="https://www.dublincore.org/specifications/dublin-core/dcmi-terms/elements11/language/" class="external-link" target="_blank">DC.source</a>**: "https://www.berlin.de/ba-steglitz-zehlendorf/aktuelles/pressemitteilungen/2024/pressemitteilung.1438914.php"
- **<a href="https://www.dublincore.org/specifications/dublin-core/dcmi-terms/elements11/identifier/" class="external-link" target="_blank">DC.identifier</a>**: "30281"

Durch die sorgfältige Erfassung und Verwaltung von Metadaten auf beiden Ebenen – sowohl für das gesamte Korpus als auch für einzelne Elemente – wird die Nutzbarkeit und Nachnutzbarkeit von Forschungsdaten in den Digital Humanities erheblich verbessert. Dies trägt zur besseren Auffindbarkeit, Nachvollziehbarkeit und langfristigen Erhaltung der Daten bei.
