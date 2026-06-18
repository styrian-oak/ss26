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

# Tabellen
- Bsp. Tabellen-Methode: die ersten zwei Reihen anzeigen: `name_der_tabelle.show(2)`
- *neue* Tabelle erstellen, die nur aus der Spalte `KundenID` besteht: `meine_tabelle.select('KundenID')`
- neue Tabelle ohne die Spalte `Preis`: `produkt_tabelle.drop('Preis')`
- die originale `produkt_tabelle` wird dadurch nicht verändert
- s. 3.4 für weitere Tabellen-Methoden

Lesezeichen: 4
