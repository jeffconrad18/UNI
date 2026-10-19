Ähm counter: aaaaa aaaaa aaaaa aaaaa aaaaa aaaaa aaaaa aaaaa aaaaa aaaaa aaaaa aaaaa aaaaa aaaaa aaaaa aaaaa aaaaa aaaaa aaaaa aaaaa a
15 / 100 = 

### [[01-problems-and-minijava.pdf#page=10|Euklidischer Algorithmus]]
Berechnung des größten gemeinsamen Teiler:
1. If a = b, stop and return a: gcd(a, b) = a. Otherwise, continue with step 2. 
2. If a > b, replace a by a − b and return to step 1. Otherwise, continue with step 3. 
3. Now a < b. Replace b by b − a and return to step 1.

Algorithmus ist terministisch, weil
- Beide Nummern bleiben pos
- Integer $a+b$ wird kleiner
- Kann nicht für immer kleiner werden

### Eigenschaften Algorithmus
- **Endliche Definition**: Beschreibung hat endliche Länge
- **Dynamische Endlichkeit**: Bei jedem Schritt ist die gespeicherte Information endlich
- **Termination**: Ergebnis nach endlicher Ausführung
- **Determination**: Gleiche Inputs = Gleiche Ausgabe
- **Determinismus**: Nächster Schritt ist eindeutig festgelegt