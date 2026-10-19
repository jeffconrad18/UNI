Eine **Funktion** ordnet **jedem Element** der Definitionsmenge **genau ein Element** aus der Wertemenge zu.

Definitionen für eine Funktion $f: A \to B$:

- **Injektiv** (höchstens ein Treffer): Verschiedene Elemente aus der Definitionsmenge $A$ werden immer auf verschiedene Elemente in der Zielmenge $B$ abgebildet. Kein Wert im Zielbereich wird mehrfach getroffen.
    
    - _Formal:_ Wenn $f(x_1) = f(x_2)$, dann muss stets $x_1 = x_2$ gelten (äquivalent: $x_1 \neq x_2 \implies f(x_1) \neq f(x_2)$).
        
- **Surjektiv** (mindestens ein Treffer): Jedes Element der Zielmenge $B$ wird von mindestens einem Element aus der Definitionsmenge $A$ erreicht. Es bleibt also kein Element im Zielbereich ungetroffen übrig.
    
    - _Formal:_ Für jedes $y \in B$ existiert mindestens ein $x \in A$ mit $f(x) = y$.
        

Erfüllt eine Funktion beide Eigenschaften gleichzeitig, nennt man sie **bijektiv** – jedes Element im Zielbereich wird genau einmal getroffen.

Bijektive Funktionen kann man transformieren, also umkehren $f: B \to A$:

$$ \text{if} f  \text{ is not bijective: } f^{-1}: B \to 2^A   \text{ with } f^{-1}(b) = \{a \in A \mid f(a) = b\}$$

Eine Art „Umkehrung“ für eine Funktion definiert, selbst wenn sie nicht bijektiv ist, d.h.:
- **Nicht injektiv:** Mehrere Elemente aus $A$ landen beim selben $b \in B$.
- AND
- **Nicht surjektiv:** Ein Element $b \in B$ wird von gar keinem Element aus $A$ getroffen.

Weil eine echte Funktion jedem Eingangswert aber _genau ein_ eindeutiges Ergebnis zuordnen muss, kann das Ergebnis kein einzelnes Element aus $A$ sein. Stattdessen gibt man eine **Menge** von Elementen zurück! 📦

Deshalb steht dort die Potenzmenge $2^A$ (oft auch $\mathcal{P}(A)$ geschrieben):

$$f^{-1}: B \to 2^A$$

Das bedeutet: Für jedes $b \in B$ ist die Antwort eine **Teilmenge von $A$** (das sogenannte **Urbild** 🎯):

$$f^{-1}(b) = \{a \in A \mid f(a) = b\}$$

### Zahlenmengen

- **$\mathbb{N}$ (Natürliche Zahlen):** Die klassischen Zählzahlen ohne Null.
    
    _Beispiele:_ $1, 2, 3, 42$
    
- **$\mathbb{N}_0$ (Natürliche Zahlen mit Null):** Alle natürlichen Zahlen einschließlich der Null.
    
    _Beispiele:_ $0, 1, 2, 100$
    
- **$\mathbb{Q}$ (Rationale Zahlen):** Alle Zahlen, die sich als Bruch zweier ganzer Zahlen $\frac{a}{b}$ (mit $b \neq 0$) darstellen lassen. Dazu gehören endliche und periodische Dezimalzahlen.
    
    _Beispiele:_ $\frac{1}{2}, -\frac{3}{4}, 5 = \frac{5}{1}, 0{,}75, 0{,}\bar{3}$
    
- **Irrationale Zahlen:** Zahlen, die sich **nicht** als Bruch darstellen lassen. Ihre Dezimaldarstellung hat unendlich viele Nachkommastellen ohne periodisches Muster.
    
    _Beispiele:_ $\sqrt{2}, \pi, e, \sqrt{5}$
    
- **$\mathbb{R}$ (Reelle Zahlen):** Die Zusammenfassung aller rationalen und irrationalen Zahlen. Sie bilden den lückenlosen Zahlenstrahl.
    
    _Beispiele:_ $-17, 0, \frac{2}{3}, \sqrt{3}, \pi$

### Körperaxiome (Field Axioms) für $(\mathbb{R}, +, \cdot)$

Für alle $x, y, z \in \mathbb{R}$ gilt:

- **Kommutativität:** $x + y = y + x \quad$ und $\quad x \cdot y = y \cdot x$
    
- **Assoziativität:** $(x + y) + z = x + (y + z) \quad$ und $\quad (x \cdot y) \cdot z = x \cdot (y \cdot z)$
    
- **Neutrale Elemente:** Es existieren $0, 1 \in \mathbb{R}$ ($0 \neq 1$) mit:
    
    $x + 0 = x \quad$ und $\quad x \cdot 1 = x$
    
- **Inverse Elemente:**
    - Zu jedem $x$ existiert $-x$ mit: $x + (-x) = 0$
        
    - Zu jedem $x \neq 0$ existiert $x^{-1}$ (bzw. $\frac{1}{x}$) mit: $x \cdot x^{-1} = 1$
        
- **Distributivität:** $x \cdot (y + z) = x \cdot y + x \cdot z$
    
- **Körper:** $\mathbb{Q}$ und $\mathbb{R}$ erfüllen alle Axiome (sind Körper). $\mathbb{Z}$ und $\mathbb{N}_0$ sind keine Körper (keine multiplikativen Inversen).
    
- **Konventionen:** $xy := x \cdot y, \quad x - y := x + (-y), \quad \frac{x}{y} := x \cdot y^{-1}$ ($y \neq 0$)


### Anordnungsaxiome (Order Axioms) für $(\mathbb{R}, \le)$

Für alle $x, y, z \in \mathbb{R}$ gilt:

- **Trichotomie (Vergleichbarkeit):** Genau eine der drei Aussagen trifft zu:
    $$x < y \quad \text{oder} \quad x = y \quad \text{oder} \quad y < x$$
    
- **Monotonie der Addition:** Das Addieren einer Zahl ändert die Ungleichung nicht:
    $$x < y \iff x + z < y + z$$
    
- **Monotonie der Multiplikation:** Das Multiplizieren mit einer positiven Zahl ($z > 0$) erhält die Richtung:
    $$x < y \iff z \cdot x < z \cdot y$$
    

**Vollständigkeit / Supremums-Eigenschaft (Unterschied von $\mathbb{R}$ zu $\mathbb{Q}$: $\mathbb{R}$ hat keine Löcher, $\mathbb{Q}$ schon.)**

- Jede nicht-leere, nach oben beschränkte Teilmenge $X \subseteq \mathbb{R}$ besitzt ein **Supremum** ($\sup X \in \mathbb{R}$), also eine **kleinste obere Schranke**:
      
    - $\sup X$ ist eine obere Schranke: Für alle $x \in X$ gilt $x \le \sup X$.
        
    - $\sup X$ ist die kleinste: Ist $b$ irgendeine obere Schranke von $X$, so gilt $\sup X \le b$.
        
- **Geordneter Körper:** $\mathbb{Q}$ und $\mathbb{R}$ sind geordnete Körper (die komplexen Zahlen $\mathbb{C}$ lassen sich nicht anordnen).
    
- **Der Clou:** Erst die Supremums-Eigenschaft macht $\mathbb{R}$ lückenlos (vollständig) – in $\mathbb{Q}$ existiert das Supremum für Mengen wie $\{q \in \mathbb{Q} \mid q^2 < 2\}$ nicht.

Die **Vollständigkeit** (oder **Supremums-Eigenschaft**) ist genau der Unterschied, der die reellen Zahlen $\mathbb{R}$ von den rationalen Zahlen $\mathbb{Q}$ trennt: **$\mathbb{R}$ hat keine Löcher, $\mathbb{Q}$ schon.**


> [!NOTE]- Erklärung mit Beispiel  
> Die **Vollständigkeit** (oder **Supremums-Eigenschaft**) ist genau der Unterschied, der die reellen Zahlen $\mathbb{R}$ von den rationalen Zahlen $\mathbb{Q}$ trennt: **$\mathbb{R}$ hat keine Löcher, $\mathbb{Q}$ schon.**
> 
> **Was bedeutet „obere Schranke“ und „Supremum“?**
> 
> Stell dir eine Teilmenge $X$ von Zahlen vor, zum Beispiel $X = {x \in \mathbb{R} \mid x < 2}$.
> 
> - **Obere Schranke:** Jede Zahl, die größer oder gleich allen Elementen aus $X$ ist. Für $X$ wären zum Beispiel $5$, $3$ und $2$ obere Schranken, denn kein Element aus $X$ ist größer als diese Zahlen.
>     
> - **Supremum $\sup X$:** Die **kleinste** aller oberen Schranken. In unserem Fall ist $\sup X = 2$. Es ist also die optimale Grenzmarke nach oben.
>     
> 
> **Warum ist das in $\mathbb{Q}$ ein Problem? (Das „Loch“)**
> 
> Betrachte die Menge aller rationalen Zahlen, deren Quadrat kleiner als $2$ ist: $X = {q \in \mathbb{Q} \mid q^2 < 2}$.
> 
> Diese Menge enthält Brüche wie $1{,}4 = \frac{14}{10}$ oder $1{,}414 = \frac{1414}{1000}$.
> 
> Sie ist nach oben beschränkt. Zum Beispiel ist $2$ eine obere Schranke, denn $2^2 = 4 > 2$.
> 
> Die optimale Grenze, also die **kleinste obere Schranke**, müsste genau $\sqrt{2}$ sein: $\sup X = \sqrt{2}$.
> 
> **Das Problem:** $\sqrt{2}$ ist **keine rationale Zahl**: $\sqrt{2} \notin \mathbb{Q}$.
> 
> In der Welt der rationalen Zahlen existiert diese kleinste obere Schranke deshalb nicht. An der Stelle von $\sqrt{2}$ klafft ein **Loch im Zahlenstrahl**.
> 
> **Was garantiert die Vollständigkeit in $\mathbb{R}$?**
> 
> Das Vollständigkeitsaxiom besagt:
> 
> > **Jede** nicht-leere Menge von reellen Zahlen, die nach oben beschränkt ist, besitzt eine kleinste obere Schranke, die selbst wieder eine reelle Zahl ist.
> 
> Formal kann man das so schreiben: $X \subseteq \mathbb{R}$, $X \neq \varnothing$ und $X$ ist nach oben beschränkt $\Rightarrow \sup X \in \mathbb{R}$.
> 
> In $\mathbb{R}$ existiert $\sqrt{2}$. Die Menge besitzt daher ihre kleinste obere Schranke in $\mathbb{R}$.
> 
> Anschaulich gesprochen **„stopft“ die Supremums-Eigenschaft alle Lücken** – zum Beispiel bei $\sqrt{2}$, $\sqrt{3}$, $\pi$ oder $e$ – und macht den Zahlenstrahl zu einer durchgehenden, lückenlosen Linie.

# Betrag & Metrik in ℝ

### Definitionen
- **Signum $\operatorname{sgn}(x)$:** Vorzeichenfunktion ($+1$ für $x > 0$, $0$ für $x = 0$, $-1$ für $x < 0$)
- **Betrag $|x|$:** $|x| := \operatorname{sgn}(x) \cdot x$
  - Geometrisch: Distanz von $x$ zum Ursprung $0$
  - Immer nicht-negativ: $|x| \ge 0$
- **Metrik (Abstand):** $|x - y| = |y - x|$
  - Geometrisch: Distanz zwischen den Punkten $x$ und $y$ auf der Zahlengeraden
  - Symmetrisch: Reihenfolge irrelevant

### Min / Max & Abstand
- **Mittelpunkt:** $M = \frac{x+y}{2}$ (Mitte der Strecke zwischen $x$ und $y$)
- **Halber Abstand:** $D = \frac{|x-y|}{2}$ (Distanz von der Mitte zu jedem Randpunkt)
- **Maximum:** $\max(x,y) = \frac{x+y}{2} + \frac{|x-y|}{2}$
  - Vom Mittelpunkt nach rechts laufen $\rightarrow$ größerer Wert
- **Minimum:** $\min(x,y) = \frac{x+y}{2} - \frac{|x-y|}{2}$
  - Vom Mittelpunkt nach links laufen $\rightarrow$ kleinerer Wert
- **Gesamtabstand:** $|x - y| = \max(x,y) - \min(x,y)$
  - Größerer minus kleinerer Wert ergibt immer den positiven Abstand

### Rechenregeln
- **Multiplikativität:** $|xy| = |x| \cdot |y|$
  - Betrag eines Produkts = Produkt der Einzelbeträge
- **Quadrat:** $|x^2| = |x|^2 = x^2$
  - Quadrate sind ohnehin stets $\ge 0$, Betragsstriche redundant
- **Nullstellen:** $|xy| = 0 \iff x = 0 \lor y = 0$
  - Ein Produkt ist genau dann $0$, wenn mindestens ein Faktor $0$ ist

### Dreiecksungleichungen
$$||x| - |y|| \le |x \pm y| \le |x| + |y|$$

- **Rechte Seite (Standard-Dreiecksungleichung):** $|x + y| \le |x| + |y|$
  - Betrag der Summe ist maximal so groß wie die Summe der Einzelabstände
  - Maximalwert $|x| + |y|$ nur bei gleichem Vorzeichen (beide Zahlen ziehen in dieselbe Richtung)
  - Bei Gegenzeichen heben sich Teilbeträge auf
- **Linke Seite (Umgekehrte Dreiecksungleichung):** $||x| - |y|| \le |x - y|$
  - Der Abstand zwischen zwei Zahlen schrumpft nie unter die Differenz ihrer Abstände zum Ursprung
  - Minimalwert $||x| - |y||$ wird bei entgegengesetztem Vorzeichen bzw. Auslöschung erreicht


# Reelle Zahlen: Wichtige Teilmengen

**Def** Endliche Intervalle für $a \le b$ in $\mathbb{R}$:
- $(a, b) := {]a, b[} := \{x \in \mathbb{R} \mid a < x < b\}$ (offenes Intervall)
- $(a, b] := {]a, b]} := \{x \in \mathbb{R} \mid a < x \le b\}$ (linksoffenes Intervall)
- $[a, b) := {[a, b[} := \{x \in \mathbb{R} \mid a \le x < b\}$ (rechtsoffenes Intervall)
- $[a, b] := \{x \in \mathbb{R} \mid a \le x \le b\}$ (abgeschlossenes Intervall)

### Unendliche Intervalle:
- $\mathbb{R}^+ := \mathbb{R}_{>0} := (0, \infty) := {]0, \infty[} := \{x \in \mathbb{R} \mid 0 < x\}$ (positiv)
- $\mathbb{R}_0^+ := \mathbb{R}_{\ge 0} := [0, \infty) := {[0, \infty[} := \{x \in \mathbb{R} \mid 0 \le x\}$ (nicht-negativ)
- $\mathbb{R}^- := \mathbb{R}_{<0} := (-\infty, 0) := {]-\infty, 0[} := \{x \in \mathbb{R} \mid x < 0\}$ (negativ)
- $\mathbb{R}_0^- := \mathbb{R}_{\le 0} := (-\infty, 0] := {]-\infty, 0]} := \{x \in \mathbb{R} \mid x \le 0\}$ (nicht-positiv)
- Analog: $[a, \infty)$, $(a, \infty)$, $(-\infty, b]$, $(-\infty, b)$

---

⚠️ **(Erinnerung)** Aus der Konstruktion/Definition von $\mathbb{R}$: „$\mathbb{Q}$ liegt dicht in $\mathbb{R}$.“

Für jedes $x \in \mathbb{R}$ und jedes $\varepsilon > 0$ gibt es ein $r \in \mathbb{Q}$ mit $|x - r| < \varepsilon$.

> [!NOTE]- Erklärung mit Beispiel  
>Ganz gleich, welche reelle Zahl du dir aussuchst – und ganz gleich, wie winzig du den erlaubten Fehler $\varepsilon$ machst: **Du findest immer einen gewöhnlichen Bruch $r$, der so nah an $x$ herankommt, dass die Abweichung kleiner als $\varepsilon$ ist.**

# Stellenwertsysteme & Basen

---

## 1. Ganze Zahlen in Basis $b \in \mathbb{N}$

### Darstellung
Eine Zahl wird als Ziffernfolge notiert:
$$(d_l d_{l-1} \dots d_1 d_0)_b \quad \text{mit } d_i \in \{0, \dots, b-1\}$$

- $d_0$: Niederwertigste Ziffer mit Gewicht $b^0 = 1$
- $d_l$: Höchstwertigste Ziffer mit Gewicht $b^l$

---

### Umrechnung: Basis $b \to$ Zehnersystem (Basis 10)
Auswertung der Stellenwertsumme über Potenzen der Basis $b$:
$$n = \sum_{i=0}^l d_i \cdot b^i = d_l \cdot b^l + d_{l-1} \cdot b^{l-1} + \dots + d_1 \cdot b^1 + d_0 \cdot b^0$$

**Beispiel:** $(210)_3$ ins Zehnersystem:
$$(210)_3 = 2 \cdot 3^2 + 1 \cdot 3^1 + 0 \cdot 3^0 = 2 \cdot 9 + 1 \cdot 3 + 0 \cdot 1 = 18 + 3 + 0 = (21)_{10}$$

---

### Umrechnung: Zehnersystem $\to$ Basis $b$
Fortgesetzte Division mit Rest durch die Basis $b$:

1. Rest bestimmen: $d := n \bmod b$ (liefert die nächste Ziffer von rechts nach links)
2. Zahl verkleinern: $n' := \lfloor \frac{n}{b} \rfloor$
3. Wiederholen: Mit $n'$ fortfahren, bis $n = 0$ erreicht ist

**Beispiel:** $17_{10}$ in Basis $b=2$:
- $17 = 2 \cdot 8 + 1 \implies d_0 = 1$
- $8 = 2 \cdot 4 + 0 \implies d_1 = 0$
- $4 = 2 \cdot 2 + 0 \implies d_2 = 0$
- $2 = 2 \cdot 1 + 0 \implies d_3 = 0$
- $1 = 2 \cdot 0 + 1 \implies d_4 = 1$
$$\implies 17_{10} = (10001)_2$$

---

## 2. Gebrochene Anteile (Nachkommastellen) in Basis $b$

### Darstellung & Umrechnung in Basis 10
Nachkommastellen entsprechen negativen Potenzen der Basis:
$$(0.d_1 d_2 \dots d_l)_b := \sum_{i=1}^l d_i \cdot b^{-i} = d_1 \cdot b^{-1} + d_2 \cdot b^{-2} + \dots + d_l \cdot b^{-l}$$

- Jede Stelle nach rechts teilt durch eine weitere Potenz von $b$ ($\frac{1}{b}, \frac{1}{b^2}, \dots$)
- Schranke: $0 \le (0.d_1 d_2 \dots d_l)_b \le 1 - b^{-l} < 1$

**Beispiel:** $(0.12)_3$ ins Zehnersystem:
$$(0.12)_3 = 1 \cdot 3^{-1} + 2 \cdot 3^{-2} = \frac{1}{3} + \frac{2}{9} = \frac{3}{9} + \frac{2}{9} = \frac{5}{9} \approx 0{,}555\dots_{10}$$

---

### Wichtige Eigenschaften
- Endliche Darstellung: Jede endliche Ziffernfolge liefert stets eine rationale Zahl ($\in \mathbb{Q}$).
- Irrationale Zahlen: Besitzen in jeder Basis zwingend eine unendliche Ziffernfolge.
- Basisabhängigkeit: Ein Bruch kann in einer Basis endlich sein, in einer anderen periodisch unendlich (z. B. $\frac{1}{3} = (0.1)_3$, aber $(0.333\dots)_{10}$).

## Stetige Funktion
Eine Funktion heißt stetig, wenn sie verträglich mit Approximationen und Grenzwertbildungen ist.
### Definition von Stetigkeit

Eine Funktion $f\colon D \to \mathbb{R}$ ist an einer Stelle $x^* \in D$ stetig, wenn eine der beiden äquivalenten Bedingungen erfüllt ist:

* **Folgendefinition (Heine):** Für jede Folge $(x_n)$, die gegen $x^*$ konvergiert, konvergiert auch die Folge der Funktionswerte gegen $f(x^*)$:
$$\lim_{n \to \infty} f(x_n) = f\left(\lim_{n \to \infty} x_n\right) = f(x^*)$$
Grenzwertbildung und Funktionsauswertung dürfen vertauscht werden.

* **$\varepsilon$-$\delta$-Definition (Cauchy):** Zu jedem noch so kleinen Fehlertoleranz-Bereich $\varepsilon > 0$ existiert ein Schrankenwert $\delta > 0$, sodass für alle Argumente mit $\vert{}x - x^*\vert{} < \delta$ folgt:
$$\vert{}f(x) - f(x^*)\vert{} < \varepsilon$$
Eine hinreichend genaue Näherung des Inputs garantiert eine beliebig gute Näherung des Outputs.
Eine Funktion heißt auf einem Intervall oder Bereich stetig, wenn sie in jedem Punkt dieses Bereichs stetig ist.

---
### Zentrale Eigenschaften stetiger Funktionen

* **Abschluss unter Rechenoperationen:** Sind $f$ und $g$ an der Stelle $x^*$ stetig, dann sind auch $f + g$, $f - g$, $f \cdot g$ sowie $f / g$ (für $g(x^*) \neq 0$) stetig.
* **Verkettung:** Die Komposition $g \circ f$ stetiger Funktionen ist wieder stetig.
* **Stetigkeit von Umkehrfunktionen:** Ist eine stetige Funktion auf einem Intervall streng monoton (und damit bijektiv), so ist auch ihre Umkehrfunktion $f^{-1}$ stetig.
* **Zwischenwertsatz:** Eine stetige Funktion macht keine Sprünge. Nimmt sie an zwei Punkten $a$ und $b$ die Werte $f(a)$ und $f(b)$ an, so nimmt sie auf dem Intervall dazwischen jeden Zwischenwert mindestens einmal an.
* **Nullstellensatz:** Gilt für eine stetige Funktion $f(a) < 0$ und $f(b) > 0$, besitzt sie im Intervall $(a, b)$ mindestens eine reelle Nullstelle (Grundlage z. B. des Bisektionsverfahrens).
* **Approximierbarkeit:** Stetige Funktionen auf kompakten (abgeschlossenen, beschränkten) Intervallen sind gleichmäßig stetig und lassen sich beliebig genau abtasten (Sampling) sowie durch Polynome (Weierstraß-Approximationssatz) oder neuronale Netze approximieren.
* **Klassen elementarer Funktionen:** Alle Polynome, rationalen Funktionen (im Definitionsbereich), Exponentialfunktionen, trigonometrischen Funktionen ($\sin, \cos$), Betragsfunktionen sowie deren Wurzeln/Logarithmen sind in ihren Definitionsbereichen stetig.

Hier ist die Zusammenfassung der Herleitung aus der Vorlesung sowie die Übersicht der vorgestellten Ableitungsregeln.

  

### 1. Kompakte Herleitung der Ableitung

1. **Zielsetzung:** Gesucht ist diejenige lineare Funktion (Gerade), die eine Kurve an einer Stelle $x^*$ lokal am besten annähert.
    
2. **Geradengleichung:** Jede Gerade durch den Punkt $(x^*, f(x^*))$ lässt sich mit einer Steigung $m$ und dem Abstand $h$ darstellen als:$$g(x^* + h) = f(x^*) + m \cdot h$$
    
3. **Bedingung für die „beste“ Näherung:** Der verbleibende Fehler zwischen Kurve und Gerade ist:
    $$\text{Fehler}(h) = f(x^* + h) - \big(f(x^*) + m \cdot h\big)$$
    
    Damit die Näherung optimal ist, muss dieser Fehler schneller gegen $0$ fallen als der Abstand $h$ selbst:
    $$\lim_{h \to 0} \frac{\text{Fehler}(h)}{h} = 0 \text{[cite: 1]}$$
    
4. **Auflösen nach der Steigung $m$:**
    $$\lim_{h \to 0} \left( \frac{f(x^* + h) - f(x^*)}{h} - m \right) = 0 \implies m = \lim_{h \to 0} \frac{f(x^* + h) - f(x^*)}{h} \text{[cite: 1]}$$
    
5. **Ergebnis:** Existiert dieser Grenzwert des Differenzenquotienten, nennen wir ihn die Ableitung $f'(x^*)$. Die Ableitung ist also genau die Steigung der optimalen linearen Näherung.

### Ableitungsregeln
- **Potenzregel**: $f'(x) = n \cdot x^{n-1}$
- **Linearkombination:** $(c \cdot f + d \cdot g)' = c \cdot f' + d \cdot g'$ für Konstanten $c, d$.
- **Produktregel:** $(f \cdot g)' = f' \cdot g + f \cdot g'$.
- **Kettenregel:** $(f(g(x)))' = f'(g(x)) \cdot g'(x)$ (äußere Ableitung mal innere Ableitung).
- **Quotientenregel:** $\left(\frac{f}{g}\right)' = \frac{f' \cdot g - f \cdot g'}{g^2}$ (ergibt sich aus Produkt- und Kettenregel).
- **Umkehrfunktion:** $(f^{-1})'(y) = \frac{1}{f'(f^{-1}(y))}$ (folgt aus der Spiegelung an der Winkelhalbierenden).
#### Wichtige Grundableitungen:
- **Konstante:** $(c)' = 0$  
- **Potenzregel:** $(x^n)' = n \cdot x^{n-1}$ (gilt für ganzzahlige und rationale Exponenten)    
- **Natürliche Exponentialfunktion:** $(e^x)' = e^x$ (ist invariant unter Ableitung)
- **Allgemeine Exponentialfunktion:** $(b^x)' = \ln(b) \cdot b^x$
- **Natürlicher Logarithmus:** $(\ln(x))' = \frac{1}{x}$
- **Trigonometrie:** $(\sin(x))' = \cos(x)$ und $(\cos(x))' = -\sin(x)$
