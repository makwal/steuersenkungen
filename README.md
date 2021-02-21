# Wer im Aargau von Steuersenkungen profitiert

Die Aargauer Regierung und die bürgerlichen Parteien wollen den Spitzen-Gewinnsteuersatz für Firmen im Kanton Aargau von 18,6 auf 15,1 Prozent senken, um für Firmen attraktiv zu bleiben.

**These**

Die Firmensteuern sind im Kanton Aargau in den vergangenen zwei Jahrzehnten stärker gesunken als die Steuern für natürliche Personen. Dies, weil der Steuerwettbewerb um Firmen national und international spielt. Dadurch sind die Steuererträge der Einwohner für den Kanton wichtiger geworden im Vergleich zu jenen der Firmen.

**Thesen-Check**

Das Thema ist relevant, weil die grosse Mehrheit der Bürgerinnen und Bürger sowie der juristischen Personen steuerpflichtig ist. Ausserdem ist im Aargau derzeit eine politische Diskussion um die Senkung der Gewinnsteuern im Gang.

Journalistisch aufbereitete Steuervergleiche gibt es immer wieder. Meistens fokussieren sie aber entweder auf die juristischen oder die natürlichen Personen. Ein Beispiel, in dem beide Seiten vorkommen, findet sich bei der ["Berner Zeitung"](https://www.bernerzeitung.ch/so-haben-sich-die-steuerzahler-veraendert-899339702447).

Aufwand/Ertrag: Es gibt viele strukturierte Datensätze zu Steuerthemen. Der Aufwand für Datenbeschaffung und -reinigung sollte sich in Grenzen halten. Ertragsseitig ist mit einem Artikel zu einem aktuellen, relevanten und lesernahen Thema zu rechnen. Was den Code angeht, dürfte der Ertrag etwas geringer ausfallen, weil er wohl grösstenteils nicht wiederverwendet werden kann.

**Knackpunkt**

In der Fülle von Steuerdaten und -auswertungen ein geeignetes Datenset finden, das den Direktvergleich juristischer und natürlicher Personen ermöglicht.

**Briefing-Personen**

Jan Schüpbach, Senior Economist bei der Credit Suisse: "Dass die Steuern für juristische Personen in den letzten Jahren stärker gesenkt wurden als für natürliche, deckt sich mit meinen Beobachtungen."

Gespräch mit Roger Ammann, eidg. Steuerverwaltung, Autor des Berichts: "Unterschiede in der Steuerbelastung natürlicher und juristischer Personen 2004 – 2016"

*Kann man die Daten des Berichts für eine Gegenüberstellung der juristischen und natürlichen Steuerbelastungen über die Zeit verwenden?*

Ja, das kann man so machen.

*Müssen die Daten gewichtet werden?*

Man sollte eine Gewichtung machen. Und sonst muss man deklarieren, dass es sich um einen ungewichteten Mittelwert handelt, bei dem jeder Kanton mit dem gleichen Gewicht ins Rennen geht.

*Wie lässt sich der Unterschied der Steuerbelastung zum BAK Taxation Index erklären?*

Dort wird mit einer ganz anderen Methode gerechnet, mit einem investitionstheoretischen Ansatz. Der Index zieht auch die direkte Bundessteuer mit ein. Man kann die Zahlen des BAK Taxation Index nicht mit den Zahlen dieses Berichts vergleichen.

**Daten**

**Daten ESTV_1**

- [Code](https://github.com/makwal/steuersenkungen/blob/master/1_estv_steuerbelastung_2004-2016.ipynb)

Die Daten zur Entwicklung der Steuern natürlicher und juristischer Personen stammen aus einem Datenset, das der Eidgenössischen Steuerverwaltung 2018 als Grundlage für den Bericht "Unterschiede in der Steuerbelastung natürlicher und juristischer Personen 2004 - 2016" diente: https://www.estv.admin.ch/estv/de/home/allgemein/steuerpolitik/fachinformationen/berichte.html#-747570948

**Kurzbeschrieb der Datei [Daten/estv_steuerbelastung04-16_juristisch.xlsx](https://github.com/makwal/steuersenkungen/blob/master/Daten/estv_steuerbelastung04-16_juristisch.xlsx)**
Die Excel-Datei für die juristischen Personen enthält drei Tabellenblätter. In dieser Analyse wird nur mit dem ersten (Ordentlich) gearbeitet. Die ordentlich besteuerten Firmen machen den überwiegenden Anteil der juristischen Personen aus (im Aargau 2017 80 Prozent, siehe Daten/kanton_ag_steuern_juristische_personen.xlsx -> T1). Pro Kanton sind drei Firmentypen (1-3) mit unterschiedlicher Rendite aufgeführt. Um die Holdings zu integrieren, wäre eine Gewichtung in allen Kantonen nötig (die Holdings bezahlen teils sehr wenig Steuern). Das würde den Rahmen dieser Analyse sprengen. Das gleiche gilt für die Gewichtung zwischen den Kantonen. Jeder Kanton fliesst folglich zu gleichen Teilen in diese Analyse ein. Innerhalb der Kantone wurden die Daten allerdings vom Studienautor gewichtet. Zu den Daten ist wichtig zu wissen, dass sie die Steuerbelastungen durch Reingewinn und Kapitalsteuern (Kantons- und Gemeindesteuern) umfassen.

**Kurzbeschrieb der Datei [Daten/estv_steuerbelastung04-16_natürlich.xlsx](https://github.com/makwal/steuersenkungen/blob/master/Daten/estv_steuerbelastung04-16_nat%C3%BCrlich.xlsx)**
Die Excel-Datei für die natürlichen Personen ist fast gleich aufgebaut. In diese Analyse werden alle Haushaltstypen ausser das Tabellenblatt "Vermögen" einbezogen. Die Analyse fusst demnach auf den Steuerbelastungen für folgende Haushaltstypen:

- Alleinstehende Person ohne Kinder mit Einkommen aus unselbständiger Erwerbstätigkeit („Lediger“)
- Ehepaar ohne Kinder, mit Einkommen aus unselbständiger Erwerbstätigkeit nur eines Ehepartners („Verheiratetes Paar ohne Kinder“)
- Ehepaar mit 2 Kindern, mit Einkommen aus unselbständiger Erwerbstätigkeit nur eines Ehepartners („Verheiratetes Paar mit Kindern“)
- Ehepaar ohne Kinder, mit Renteneinkommen beider Ehepartner („Rentner-Ehepaar“)

Für jeden Haushaltstyp gibt es in den Daten Belastungswerte für folgende Brutto-Einkommensstufen: 50'000, 100'000, 200'000, 500'000 und 1 Million Franken. 

Weil es bei den Rentnern 2007 zu einer Änderung der Berechnungsmethode kam, kann für die Rentner nur der Zeitraum von 2008 bis 2016 berücksichtigt werden.

Zu den Daten ist wichtig zu wissen: "Den Berechnungen der Steuerbelastung liegen die in den Steuerjahren 2004 bis 2016 in den kantonalen Steuergesetzen festgehaltenen Tarife und Sozialabzüge der Einkommen- und Vermögensteuer sowie die für diese Jahre geltenden Steuerfüsse von Kanton, Gemeinde und Kirche zugrunde." (aus der Studie)

In beiden Dateien wird mit den Belastungswerten in Prozent gerechnet, nicht mit den absoluten Zahlen in Franken.

**Daten ESTV_2**

- [Datensatz](https://github.com/makwal/steuersenkungen/tree/master/Daten/estv_steuerrechner)
- [Code Scraper](https://github.com/makwal/steuersenkungen/blob/master/2_estv_scraper.ipynb)
- [Code Datenverarbeitung](https://github.com/makwal/steuersenkungen/blob/master/3_auswertung_estv_scraping.ipynb)

Die Daten ESTV_1 reichen nur bis ins Jahr 2016. Glücklicherweise verfügt die ESTV über einen Steuerrechner, mit welchem die natürlichen Steuerbelastungen für diesselben Haushaltsypen und Einkommen wie bei ESTV_1 für die Jahre 2016 bis 2020 generiert werden können. Die Daten reichen nur bis ins Jahr 2014 zurück, deshalb ist dies nur die sekundäre Datenquelle. https://swisstaxcalculator.estv.admin.ch/#/taxburden/income-wealth-tax

Die Seite wird mit Hilfe von Selenium gescraped. Es werden für jede Aargauer Gemeinde die jeweiligen Felder angewählt und das generierte Excel-File heruntergeladen.

Die Daten von ESTV_1 und ESTV_2 können nicht 1:1 miteinander verglichen werden, weil ESTV_2 zusätzlich die direkte Bundessteuer umfasst und weiterer wahrscheinlicher Unterschiede (wegen der unterschiedlichen Datenerhebungen).

**Daten ESTV_3**

- Daten [hier](https://github.com/makwal/steuersenkungen/blob/master/Daten/estv_juristische_2003-2020.csv) und [hier](https://github.com/makwal/steuersenkungen/blob/master/Daten/estv_steuersubstrat_gemeinden.xlsx)
- [Code](https://github.com/makwal/steuersenkungen/blob/master/4_estv_juristische_2020.ipynb)

Um auch für die juristischen Personen ein aktuelles Bild zu erhalten, wurden zusätzlich Daten aus dem ESTV-Bericht "Entwicklung der Unternehmenssteuerbelastung in der Schweiz von 2003 bis 2020: Analyse auf Gemeindeebene" beigezogen. Daraus werden die durchschnittlichen effektiven Steuersätze 2020 der Kantone visualisiert. Die Daten zur Studie sind auf der ESTV-Website auffindbar. Um die Gewichtung der Kantone wie in der Studie vornehmen zu können, musste ich bei der ESTV die Daten zum Steuersubstrat pro Gemeinde bestellen. Zum Bericht:
https://www.estv.admin.ch/estv/de/home/allgemein/steuerpolitik/fachinformationen/berichte.html#-768005854

**Daten Kanton AG**

- [Code](https://github.com/makwal/steuersenkungen/blob/master/5_kanton_ag_steuerertr%C3%A4ge.ipynb)

Die Daten zur Relevanz der Steuern juristischer und natürlicher Personen für die Erträge von Kanton und Gemeinden stammen vom Kanton Aargau

- [Juristische Personen](https://github.com/makwal/steuersenkungen/blob/master/Daten/kanton_ag_steuern_juristische_personen.xlsx) (Achtung, die Steuerbeträge sind in 1000 CHF angegeben):
https://www.ag.ch/de/dfr/statistik/statistische_daten/statistische_daten_details/dynamische_detailseite_10_96192.jsp ("Steuerstatistik 2017 – Juristische Personen: Publikation und eDossier", Tabellenblatt T1)
    - Hierbei handelt es sich um die einfache Kantonssteuer (100%). Nicht enthalten sind diverse Zuschläge (unter anderem für den Finanzausgleich) und die Gemeindesteuern)

- [Natürliche Personen](https://github.com/makwal/steuersenkungen/blob/master/Daten/kanton_ag_steuern_nat%C3%BCrliche_personen.xlsx):
https://www.ag.ch/de/dfr/statistik/statistische_daten/statistische_daten_details/dynamische_detailseite_10_96192.jsp ("Steuerstatistik 2017 – Natürliche Personen: Publikation und eDossier", Tabellenblätter T1 und T26a)
    - Auch hier handelt es sich um die einfache Kantonssteuer (100%)

- [Kantonserträge bis 2013](https://github.com/makwal/steuersenkungen/blob/master/Daten/kanton_ag_gemeinden_erfolgsrechnung_bis2013.csv) (Achtung, Beträge sind in 1000 CHF angegeben):
https://www.ag.ch/de/dfr/statistik/datenportal/filterabfrage/datenportal_filterabfrage.jsp?rewriteRemoteUrl=%2Fapp%2Fsajato-frontend%2Fdata%2FBN18TBN2TGN1TN2MN3

- [Kantonserträge ab 2014](https://github.com/makwal/steuersenkungen/blob/master/Daten/kanton_ag_gemeinden_erfolgsrechnung_ab2014.csv):https://www.ag.ch/de/dfr/statistik/datenportal/filterabfrage/datenportal_filterabfrage.jsp?rewriteRemoteUrl=%2Fapp%2Fsajato-frontend%2Fdata%2FBN18TBN2TGN1TN2MN5

**Vorgehen**

Die These soll anhand von folgenden **sieben Auswertungen** beleuchtet werden:
1. Steuerbelastung 2004-2016 ordentlich besteuerte Firmen vs. natürliche Personen (Aargau und CH-Durchschnitt) -> Daten ESTV_1
2. Steuerbelastung für einzelne Bevölkerungsgruppen (Ledig, verheiratet mit/ohne Kinder, Rentnerpaar) -> Daten ESTV_1
3. Steuerbelastung natürliche Personen 2016-2020 -> Daten ESTV_2
4. Steuerbelastung juristische Personen 2020 -> Daten ESTV_3
5. Entwicklung, wie viel der Kanton AG durch Gewinn- und Kapitalsteuern sowie Einkommens- und Vermögenssteuern einnimmt -> Daten Kanton AG
6. Anteil der Firmen- und Personensteuern am Fiskalertrag des Kantons Aargau -> Daten Kanton AG
7. Entwicklung Steuerertrag pro Kopf resp. Firma -> Daten Kanton AG

**Arbeitsprotokoll**

- 04.01. – 22.01.2021: Erstes Thema definiert, Idee nach Gesprächen mit zwei Briefing-Personen verworfen (3h)
- 23./24.01.2021: Suche nach neuem Thema, Einlesen in die Materie (Steuerentwicklung natürliche/juristische Personen) (5h)
- 25.01. - 08.02.2021: Suche nach geeigneten Daten bei Kanton AG und EFV/ESTV, mehrere Telefonate, erste Grobauswertungen mit Pandas (10h)
- 11.02.2021: Festlegen auf Datensets, Auswertungen der ESTV-Daten mit Pandas (9h)
- 12.02.2021: Auswertung der AG-Daten, Ergebnisse evaluieren (5h)
- 13.02.2021: Ergebnisse visualisieren (1,5h)
- 14.02.2021: Dokumentation der Datenquellen und des Codes (4h)
- 16.02.2021: Gespräche mit Experten, Bau des ESTV-Scrapers (7h)
- 17.02.2021: Gespräche mit Politikern, Artikel schreiben (6h)
- 21.02.2021: Letzte Dokumentation, Abgabe (2h)
