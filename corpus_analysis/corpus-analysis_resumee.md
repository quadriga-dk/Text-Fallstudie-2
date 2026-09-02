# Resümee

```{admonition} Kernpunkte des Kapitels
:class: keypoint

**Textkomplexität**
Es gibt verschiedene Textkomplexitätsmaße, die unterschiedliche Parameter zur Berechnung der Textkomplexität oder Lesbarkeit eines Textes einsetzen. Die Parameter lassen sich aufteilen in die Wort- und die Satzebene. Die meisten Scores lassen sich in eine Klassenstufe übersetzen. Wichtig: Die Indizes unterscheiden sich in ihrer Richtung – beim Flesch-Index bedeutet ein höherer Score eine leichtere Lesbarkeit, bei den meisten anderen Indexen (ARI, Coleman-Liau, Wiener Sachtextformel) bedeutet ein höherer Score eine schwerere Lesbarkeit.

**Berechnung der Textkomplexität**
Wir haben vier Maße zur Berechnung der Textkomplexität angewendet: Flesch (am weitesten verbreitet, operiert auf Satzlänge und Silbenanzahl), Wiener Sachtextformel (auf Deutsch ausgelegt, operiert auf Satzlänge und Anteil von schwierigen Wörtern), Automated Readability Score (operiert rein auf Längenmaßen) und Coleman-Liau (operiert auf der Gleichmäßigkeit der Textschwierigkeit).
Die Maße haben wir mittels Python auf die Pressemitteilungen angewendet.

**Analyse und Visualisierung**
Die Analyse der Maße über Zeit hat gezeigt, dass alle Maße denselben Trend anzeigen: Die Pressemitteilungen werden über die Zeit komplexer, die Barrierefreiheit somit verringert.
```
