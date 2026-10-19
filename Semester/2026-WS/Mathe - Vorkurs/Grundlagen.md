# Mathematische Grundlagen zum Lösen von Gleichungen

## 1. Äquivalenzumformungen
Operationen, die die Lösungsmenge einer Gleichung nicht verändern:
- **Addition / Subtraktion:** Auf beiden Seiten denselben Term addieren oder subtrahieren.
  $$A = B \iff A \pm c = B \pm c$$
- **Multiplikation / Division:** Beide Seiten mit einer Zahl $c \neq 0$ multiplizieren oder durch sie teilen.
  $$A = B \iff A \cdot c = B \cdot c \quad (c \neq 0)$$
- **Achtung (keine zwingende Äquivalenz):**
  - **Quadrieren:** Kann Scheinlösungen erzeugen $\rightarrow$ Probe zwingend erforderlich ($x = 2 \implies x^2 = 4 \implies x = \pm 2$).
  - **Multiplikation mit Termen, die $x$ enthalten:** Kann Definitionslücken verletzen oder Nullteiler erzeugen.

---

## 2. Grundlegende algebraische Identitäten

### Binomische Formeln
1. Plus-Formel: $(a + b)^2 = a^2 + 2ab + b^2$
2. Minus-Formel: $(a - b)^2 = a^2 - 2ab + b^2$
3. Plus-Minus-Formel: $(a + b)(a - b) = a^2 - b^2$

### Rechengesetze
- **Distributivgesetz (Ausmultiplizieren / Ausklammern):**
  $$a \cdot (b + c) = ab + ac$$
- **Kommutativgesetz:** $a + b = b + a \quad \text{und} \quad a \cdot b = b \cdot a$
- **Assoziativgesetz:** $(a + b) + c = a + (b + c) \quad \text{und} \quad (a \cdot b) \cdot c = a \cdot (b \cdot c)$

---

## 3. Potenz- und Wurzelgesetze

### Potenzen
- $a^m \cdot a^n = a^{m+n}$
- $\frac{a^m}{a^n} = a^{m-n}$
- $(a^m)^n = a^{m \cdot n}$
- $(a \cdot b)^n = a^n \cdot b^n$
- $a^{-n} = \frac{1}{a^n} \quad (a \neq 0)$
- $a^0 = 1 \quad (a \neq 0)$

### Wurzeln & gebrochene Exponenten
- $\sqrt[n]{a} = a^{\frac{1}{n}} \quad (a \ge 0)$
- $a^{\frac{m}{n}} = \sqrt[n]{a^m} = (\sqrt[n]{a})^m$
- $\sqrt{a \cdot b} = \sqrt{a} \cdot \sqrt{b} \quad (a, b \ge 0)$
- $\sqrt{\frac{a}{b}} = \frac{\sqrt{a}}{\sqrt{b}} \quad (a \ge 0, b > 0)$
- **Wichtig:** $\sqrt{a^2} = |a|$ (nicht einfach $a$)

---

## 4. Lineare Gleichungen ($ax + b = 0$)
- Form: $ax + b = 0 \iff ax = -b \iff x = -\frac{b}{a} \quad (a \neq 0)$

---

## 5. Quadratische Gleichungen

### Satz vom Nullprodukt
Ein Produkt ist genau dann $0$, wenn mindestens ein Faktor $0$ ist:
$$A \cdot B = 0 \iff A = 0 \lor B = 0$$
*Tipp:* Immer erst prüfen, ob sich $x$ ausklammern lässt (z. B. $x^2 - 5x = 0 \iff x(x - 5) = 0$).

### Reinquadratische Gleichungen ($ax^2 + c = 0$)
$$x^2 = d \implies x_{1,2} = \pm \sqrt{d} \quad (\text{für } d \ge 0)$$

### Allgemeine Form: Mitternachtsformel (Große Lösungsformel)
Für $ax^2 + bx + c = 0$ mit $a \neq 0$:
$$x_{1,2} = \frac{-b \pm \sqrt{b^2 - 4ac}}{2a}$$
- **Diskriminante $D = b^2 - 4ac$:**
  - $D > 0$: Zwei reelle Lösungen
  - $D = 0$: Genau eine reelle Lösung (doppelte Nullstelle)
  - $D < 0$: Keine reelle Lösung

### Normalform: pq-Formel (Kleine Lösungsformel)
Für $x^2 + px + q = 0$:
$$x_{1,2} = -\frac{p}{2} \pm \sqrt{\left(\frac{p}{2}\right)^2 - q}$$

### Satz von Vieta
Für normierte quadratische Gleichungen $x^2 + px + q = 0$ mit den Nullstellen $x_1, x_2$:
- $x_1 + x_2 = -p$
- $x_1 \cdot x_2 = q$
- Faktorisierte Form: $(x - x_1)(x - x_2) = 0$

---

## 6. Fortgeschrittene Lösungsstrategien

### Substitution (Ersetzung)
- Anwendbar bei Gleichungen höherer Ordnung mit geraden Potenzen (z. B. biquadratisch: $a x^4 + b x^2 + c = 0$).
- **Vorgehen:**
  1. Setze $u = x^2$ (führt zu $a u^2 + b u + c = 0$).
  2. Quadratische Gleichung für $u$ lösen.
  3. **Rücksubstitution:** $x = \pm \sqrt{u}$ (nur für $u \ge 0$).

### Polynomdivision / Horner-Schema
- Bei Polynomen vom Grad $\ge 3$ (z. B. $x^3 + ax^2 + bx + c = 0$):
  1. Eine ganzzahlige Lösung $x_0$ durch Ausprobieren finden (Teiler des Absolutglieds $c$).
  2. Polynom durch $(x - x_0)$ teilen $\rightarrow$ Restpolynom ist quadratisch.
  3. Restliche Nullstellen mit Mitternachts-/pq-Formel berechnen.

---

## 7. Spezielle Gleichungstypen

### Bruchgleichungen
- Definitionsbereich bestimmen (Nenner $\neq 0$).
- Mit dem **Hauptnenner** multiplizieren, um Brüche aufzulösen.
- Gefundene Lösungen mit dem Definitionsbereich abgleichen.

### Wurzelgleichungen
- Wurzel isolieren: $\sqrt{f(x)} = g(x)$
- Beide Seiten quadrieren: $f(x) = (g(x))^2$
- **Probe ist Pflicht**, da Quadrieren keine Äquivalenzumformung ist.

### Betragsgleichungen ($|f(x)| = g(x)$)
- **Fallunterscheidung:**
  - Fall 1: $f(x) \ge 0 \implies f(x) = g(x)$
  - Fall 2: $f(x) < 0 \implies -f(x) = g(x)$
- Alternativ bei $|f(x)| = |g(x)|$: $f(x) = g(x) \lor f(x) = -g(x)$.

### Exponential- und Logarithmengleichungen
- **Umkehrfunktion nutzen:** $a^x = b \iff x = \log_a(b) = \frac{\ln(b)}{\ln(a)} \quad (a > 0, a \neq 1, b > 0)$
- **Logarithmengesetze:**
  - $\log(u \cdot v) = \log(u) + \log(v)$
  - $\log\left(\frac{u}{v}\right) = \log(u) - \log(v)$
  - $\log(u^k) = k \cdot \log(u)$
  - $\log(\sqrt[n]{u}) = \frac{1}{n} \cdot \log(u)$
  - $\log\left(\frac{1}{v}\right) = -\log(v)$
- **Exponentialfunktion**: 
  - Schreibweise: $\exp(x) = e^x \iff x = \ln(y) \quad \text{für } y = e^x$
- **Natürlicher Logarithmus:** 
  - Schreibweise:   $\ln(x) := \log_e(x) := \log(x)$
  - - $e^{\ln(x)} = x \quad (x > 0)$
  - $\ln(e^x) = x \quad (x \in \mathbb{R})$
  - $\ln(1) = 0, \quad \ln(e) = 1, \quad e^0 = 1, \quad e^1 = e$

```_graph
f(x) = \sin(x)
```

```_graph
f(x) = \cos(x)
```

```_graph
f(x) = \tan(x)
```

```_graph
f(x) = \ln(x)
```
```_graph
f(x) = \e^x
```


