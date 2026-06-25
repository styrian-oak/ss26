- `computational thinking` = computergestütztes, computerorientiertes, rechnerisches Denken
- `inferential thinking` = schlussfolgerndes Denken

- Data Science (DS) = Schlussfolgerungen aus Daten ziehen
- Bestandteile:
    - `exploration` durch Visualisierung & Deskriptive Statistik
    - `prediction` durch Machine Learning & Optimierung
    - `inference` durch statistische Tests & Modelle

- Statistik (Teil von DS): Schlussfolgerungen aus unvollständigen Infos ziehen
- `randomness`: eine Methode, um mit unvollständigen Daten umzugehen
- DS ist eine Erweiterung von Statistik, ermöglicht durch Computer & Visualisierung

# Kausalität
- schreckt die Todesstrafe ab? ist Schokolade gut für die Gesundheit? was verursacht Brustkrebs?
- diese 3 Fragen versuchen einem Effekt eine Ursache zuzuweisen
- Beobachtungsstudie: man zieht Schlussfolgerungen aus Daten, die man beobachtet, aber nicht selbst erzeugt hat
    - man beobachtet einen Vorgang, der sowieso schon passiert
- oft stellt man erst in einer Beobachtungsstudie eine `association` (Korrelation) fest
- ...und versucht dann in einer genaueren Analyse Kausalität nachzuweisen
- John Snow nutzte Beobachtung & Visualisierung, um eine `association` zwischen einer Wasserpumpe und einem Cholera-Ausbruch herzustellen (Karte)
- `comparison`: Vergleich zwischen `treatment`- und Kontroll-Gruppe
    - sind die Ergebnisse unterschiedlich, deutet dies auf eine `association` hin
    - beweist aber noch keine Kausalität

- Wie Snow Kausalität gezeigt hat:
    - die Gruppen dürfen sich nur in Hinsicht auf das `treatment` unterscheiden
    - (Kontroll-Gruppe: Firma mit sauberem Wasser, `treatment`-Gruppe: Firma mit dreckigem Wasser)
    - nur dann, kann man Kausalität zwischen `treatment` & `outcome` zuweisen
> In an observational study, if the treatment and control groups differ in ways other than the treatment, it is difficult to make conclusions about causality.
- so einen Unterschied nennt man `confounding factor`
- Bsp. Kaffee & Lungenkrebs: `confounding factor`: Rauchen
    - nur `association` zwischen Kaffee und Krebs, keine Kausalität
- `confounding` = verwirrend
- `randomized controlled trial` (RCT): Teilnehmer für die Gruppen werden zufällig ausgewählt (um `confounding` zu vermeiden)
- dabei muss die `randomization` vorsichtig & unter Beachtung der Gesetze der Wahrscheinlichkeit durchgeführt werden
- dies ermöglicht präzise mathematische Aussagen über die Unterschiede zwischen den Gruppen
- Zusammenfassung: wenn man Kausalität etablieren will, sollte man ein RCT durchführen; mit Beobachtungsstudien kann man `association`, aber nur schwer Kausalität nachweisen (`confounding`)

- `g` = Wachstumsrate (`growth rate`)
- kann man so berechnen:
```python
g = (endwert / startwert) - 1
```
- Variable `t` wird oft als # Jahre benutzt

- in `jupyter notebook` gibt es Tab-Vervollständigung
    - zB zeigt `math.` + `Tab` alle Funktionen des `math`-Moduls
- mit `?` kannst du Hilfe über eine Funktion ausgeben, zB: `math.log?`
    - im Output bedeutet `[x]`, dass Argument `x` optional ist

# Tabellen-Grdl.
- Bsp. Tabellen-Methode: die ersten zwei Reihen anzeigen: `name_der_tabelle.show(2)`
- *neue* Tabelle erstellen, die nur aus der Spalte `KundenID` besteht: `meine_tabelle.select('KundenID')`
- neue Tabelle ohne die Spalte `Preis`: `produkt_tabelle.drop('Preis')`
- die originale `produkt_tabelle` wird dadurch nicht verändert
- s. 3.4 für weitere Tabellen-Methoden

# 4 Datentypen
- in Python gibt es nur 2 Zahlen-Typen: `int` & `float`
- bei `float`-Zahlen werden nur die ersten 15 Ziffern beachtet, der Rest wird von Python ignoriert
- Mit `float`s rechnen ist nicht exakt. Rundungsfehler sind oft verwirrend, wenn man ihnen zum ersten Mal begegnet.
- ein String kann ein Wort, ein Satz, ein ganzes Buch sein
- die String-Methode `replace` ersetzt jedes Vorkommen eines Sub-Strings, Bsp.: `'hitchhiker'.replace('hi', 'ma')` -> `'matchmaker'`

# 5 Sequences
- = eine Sammlung/Gruppe von `values`
- diese `collection` können wir dann zB an eine Funktion übergeben

## Arrays
- Array = Reihe, Anordnung
- Arrays können nicht verschiedene Datentypen enthalten
- man kann Arrays mit Zahlen addieren/multiplizieren
    - bei der Multiplikation wird zB jeder Eintrag des Arrays mit der Zahl multipliziert
- `numpy` hat einen Haufen nützlicher Array-Funktionen (nicht Methoden)
    - s. 5.1 für eine Übersicht der wichtigsten **<- bei Übungsaufgaben referenzieren**

## Ranges
- `range` = `array` von Zahlen in ab-/aufsteigender Reihenfolge; die Zahlen sind alle durch das gleiche Intervall voneinander getrennt
- `np.arange` kann bis zu 3 Argumente nehmen: `start`, `end` & `step`
    - wird nur 1 Argument gegeben, wird dies der `end`-Wert (es wird angenommen: `start=0`, `step=1`)
    - bei 2 Argumenten: `start` & `end` (`step=1` angenommen)
    - mit dem 3. Argument kann man `step` explizit einstellen
    - `start` ist in der Range drin, `end` nicht (Python-Konvention)
    - die Argumente können auch negativ sein
- mit `.item(Index)` kannst du auf ein Array-Element zugreifen
- wenn 2 Ranges/Arrays gleich groß sind, kannst du zB `array1 - array2` berechnen:
    - dabei wird elementweise subtrahiert
    - das Ergebnis ist wieder ein Array

# 6 Tabellen
- eine Tabelle kann man aus 2 Perspektiven betrachten...
- **jede Spalte einer** `table` **ist ein Array**

## Funktionen/Methoden des datascience-Moduls
- auf die Zelle in der 5. Spalte und 1. Zeile einer Tabelle zugreifen: `meine_tabelle.column(4).item(0)`
- die Funktion `Table()` erstellt eine neue leere Tabelle
- `Table().with_columns('meine Spalte', make_array(8, 34, 5))` erstellt eine Tabelle mit einer Spalte
- die `with_columns`-Methode erstellt immer eine neue Tabelle, die ursprüngliche bleibt unverändert
- *Kapitel 6 stellt noch mehr nützliche Methoden/Funktionen vor*

---

- die `help`-Funktion gibt Hilfe zu einer Funktion/Methode, zB: `help(meine_tabelle.sort)`
- so etwas wie `descending=True` wird als benanntes Argument bezeichnet
- im Gegensatz dazu ist das `True` bei `sort('SALARY', True)` ein sog. `positional argument`

- mit `.take()` kannst du auf Zeilen anhand einer Range zugreifen, zB: `meine_tabelle.take(np.arange(3, 6))`
- mit `.where()` kannst du nur die Zeilen anzeigen, die eine bestimmte Bedingung erfüllen
- grds. Anwendung der `where`-Methode: `original_table_name.where(column_label_string, are.condition)`
- s. 6.2.5 für eine Übersicht der `are`-Prädikate für `where()`
