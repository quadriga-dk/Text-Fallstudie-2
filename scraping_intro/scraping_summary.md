(scraping-intro_summary)=
# Resümee
```{admonition} Key points des Kapitels
:class: keypoint

**Webkommunnikation**

Bei der Aufrufen von Websites gibt es einen Client (Ihr Computer), der bei einem Server mittels HTTP-Request eine Website anfragt und vom Server eine HTTP-Response zurückbekommt. Der Request besteht aus einer Request-Methode (meistens GET oder POST) und einer URL. Die HTTP-Response besteht aus einem Status-Code, eine Metainformation über den Erfolg der Anfrage (z.B. 200 für OK), einem Header mit Metainformation zu der Antwort und einem Body, in dem der eigentlich Inhalt der Website geschickt wird. 

**Webscraping**

Um eine oder mehrere Websites automatisiert abzufragen, können unterschiedliche Scraping-Methoden eingesetzt werden. Abhängig davon, ob Websites nur aus statischen oder auch aus dynamischen Inhalten bestehen, muss die entsprechende Scraping-Methode gewählt werden. Statische Websites bestehen aus HTML-Dokumenten, die in dieser Form vom Server zum Client geschickt werden. Bei dynamischen Websites werden die Inhalte erst bei der Abfrage erstellt, meist durch JavasSript. 
Für Abfragen von einzelnen, statischen Websites eignet sich die Python-Bibliothek `requests`. Wenn automatisiert Links auf Websites gefolgt werden soll, ist die Bibliothek `scrapy` eine gute Wahl. Sobald mit dynamischen Inhalten interagiert werden muss, ist es sinnvoll, `selenium` zu verwenden. 

```
