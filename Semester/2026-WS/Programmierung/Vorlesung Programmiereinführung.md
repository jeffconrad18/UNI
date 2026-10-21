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

## Syntax
- **Arithmetic expressions (`expr`)** → liefern einen Zahlenwert (`int`).
- **Boolean expressions / Conditions (`cond`)** → liefern Wahrheitswerte (`true` oder `false`, z. B. Vergleiche wie `x > 0` oder Verknüpfungen mit `&&`, `||`, `!`).

### Mengen: Definition durch Auflistung (Aufzählung)

**[Def]** $x \in \{x_1, \dots, x_k\}$ **:gdw** $x$ kommt in $x_1, \dots, x_k$ vor.
($x \notin \{x_1, \dots, x_k\}$ **gdw** $x$ kommt nicht in $x_1, \dots, x_k$ vor.)

* Die öffnende bzw. schließende Mengenklammer $\{$, $\}$ signalisieren dabei den Beginn bzw. das Ende der Mengendefinition, „,“ dient als Trennzeichen.
* Im strikten Sinn muss die Liste vollständig ausgeschrieben werden, häufig wird aber eine angedeutete Auflistung zzgl. erklärendem Text akzeptiert:
  * $\{\mathbb{N}, \mathbb{N}_0\}$ und $\{\mathbb{N}, \mathbb{N}_0, \mathbb{Z}\}$ sind Mengen.
  * $\{\text{A}, \text{B}, \dots, \text{Z}, \text{a}, \text{b}, \dots, \text{z}\}$ Menge der Buchstaben des lateinischen Alphabets.
  * $\{!, ”, \#, \dots, \sim\}$ Menge der darstellbaren ASCII-Zeichen.

**[Def]** $[n] := \{1, 2, \dots, n\}$ für jedes $n \in \mathbb{N}_0$ mit $[0] := \emptyset$.
$\mathbb{Z}_n := \{0, 1, \dots, n-1\}$ für jedes $n \in \mathbb{N}_0$ mit $\mathbb{Z}_0 := \emptyset$.

⚠️ „**:gdw**“ und „$:=$“ zur Betonung von Definitionen.
(Der Text auf der linken Seite steht für Text auf der rechten Seite.)