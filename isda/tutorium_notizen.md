# Relationale Algebra
- Relationale Algebra (RA): Relationen auf dem Papier verändern
- `DQL` basiert auf RA
- RA arbeitet mit Mengen, `DQL` mit Multimengen

- wieso 5 + 1 Operatoren?
    - 5 Grundoperatoren (aus denen man andere ableiten kann)
    - + Umbenennung

unär:
- Selektion `σ` -> (bezieht sich auf) Tupel
- Projektion `π` -> Attribute
    - Selektion & Projektion sind kommutativ
- Umbenennung `ρ` -> Attribute

binär:
- Differenz `-` -> Instanzen (läuft auf Tupel hinaus)
- Vereinigung `∪` -> Instanzen (läuft auf Tupel hinaus)
- Kreuzprodukt/kartesisches Produkt `⨯` -> Instanzen (Felder)
    - Intuition: Skat-Karten

abgeleitete Operatoren:
- können durch Grundoperatoren dargestellt werden
- Natural Join `><`
    - zwei Relationen haben ein oder mehrere Attribute mit demselben Namen
    - Ergebnis: neue Relation, die nur die Tupel enthält, die beim gemeinsamen Attribute denselben Wert haben
- Theta-Join `><a_1=a_2`
    - braucht keine Attribute gleichen Namens
    - stattdessen werden die Attribute, bei denen Werte übereinstimmen, explizit angegeben
- Division `/` = für-alle-Operator
    - alle X, die für alle Y eine bestimmte Beziehung erfüllen
    - zB "die Segler, die alle Boote reserviert haben" (eine Tabelle Segler, eine Boote und eine reserviert)
- Sortierung `τ` muss als letztes angewendet werden, weil ihr Ergebnis keine Menge ist
