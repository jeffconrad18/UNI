kontinuierliche Mathematik heißt keine Löcher
diskrete Mathematik ist mit Löchern, also eig simpler

### Logik
- Zentrales Ziel der Mathematik ist Eindeutigkeit > Definitionen
- Zentrale Frage der Logik ist Erfüllbarkeit und (Allgemein-)Gültigkeit einer **Aussage** (Behauptung, Feststellung, Zusicherung)
	- Man kann einer Aussage entweder zustimmen oder ablehnen
	- Aussage ist **erfüllbar**, falls es eine Situation gibt, in der sie wahr ist
	- Aussage ist (allgemein-) **gültig** 
- Zur Prüfung sind Grundbegriffe wichtig:
	- **Junktoren**: und, oder, nicht, falls-dann (wenn-dann), genau-dann-wenn (falls-und-nur-falls), entweder-oder
	- **Quantoren**: *für alle*, *es existiert* (es gibt, für einige), *für kein* (es gibt kein)
	- Beispiel: *Wahrheitstabelle für Junktoren*

| **A** | **B** |   A und B   | A oder B   | Nicht A  | Falls A dann B    | A genau dann, wenn B  | Entweder A oder B |
| ----- | ----- | :---------: | ---------- | -------- | ----------------- | --------------------- | ----------------- |
| A     | B     | $A \land B$ | $A \lor B$ | $\neg A$ | $A \rightarrow B$ | $A \leftrightarrow B$ | $A \oplus B$      |
| f     | f     |      f      | f          | w        | w                 | w                     | f                 |
| f     | w     |      f      | w          | w        | w                 | f                     | w                 |
| w     | f     |      f      | w          | f        | f                 | f                     | w                 |
| w     | w     |      w      | w          | f        | w                 | w                     | f                 |

- *syn* kurz für *synonym* (gleichbedeutend)
	- "falls A, dann B" syn "(nicht A) oder B" syn "B oder nicht A"
	- "A gdw B" syn "(falls A, dann B) und (falls B, dann A)"
	- "entweder A oder B" syn "nicht (A gdw B)"
	- "weder A noch B" syn "nicht (A oder B)" syn "(nicht A) und (nicht B)"

![[Pasted image 20261015102415.png]]
nicht A | A und B | A oder B
![[Pasted image 20261015102448.png]]
Falls A, dann B | A gdw B | Entweder A oder B 

- [[Diskrete Strukturen.pdf#page=15|Entsprechend kann man Wahrheitstabellen und Venn-Diagramme auch f¨ur drei und mehr Aussagen(variablen) erstellen]]
- **Konditional**: *falls-dann (wenn-dann)* - Der Wahrheitswert von B ist nur relevant unter der Bedingung, dass A wahr ist 
- **Bikonditional**: *genau-dann-wenn (falls-und-nur-falls)*
- Kausalität oder zeitliche Abhängigkeiten spielen in der Aussagenlogik keine Rolle: ”Falls Schweine fliegen können, ist π irrational.“
### Hinreichend vs. notwendig, ”impliziert“ 
- Ist ”falls A, dann B“ (allgemein)**gültig**, dann sagt man auch 
	- ”A ist **hinreichend** für B” bzw. ”B ist **notwendig** für A“ 
	- häufig auch: ”A **impliziert** B“, ”B folgt (logisch) aus A“ 
- Ist ”A gdw B“ **allgemeingültig**, dann ist A **hinreichend** und **notwendig** für B. 
  (A gdw B syn falls A, dann B; und falls B, dann A.)

### [[Diskrete Strukturen.pdf#page=19|Beschränkte Quantoren]]
- Formal beschränkte Quantoren:
	- ”Alle x mit R(x) sind/haben/erfüllen auch P (x).“ 
	  ”Für alle x, für die R(x) wahr ist, ist auch P (x) wahr.“ 
	  ”Für jedes Objekt x gilt, falls R(x) wahr ist, dann ist auch P (x) wahr.“ 
	- ”Einige x mit R(x) sind/haben/erfüllen auch P (x).“ 
	  ”Es existiert ein x, für welches R(x) und zusätzlich auch P (x) wahr ist.“ 
	  ”Es gibt mind. ein Objekt x, das neben R(x) auch P (x) erfüllt.“
- Venn-Diagramme bzw. Euler-Diagramme
![[Pasted image 20261015105344.png]]

-  ”Einige $x$ mit $R(x)$ sind $P(x)$“ ist nur wahr, falls es ein konkretes Objekt $d$ gibt, für welches R(d) und P(d) wahr sind (d ist dann ein Beispiel oder Zeuge). 
	- Etwas formaler: ”Es existiert x, so dass R(x) und P(x)“ 
- ”Alle $x$ mit $R(x)$ sind $P(x)$“ ist nur falsch, falls es ein konkretes Objekt $d$ gibt, für das $R(d)$ und nicht $P(d)$ wahr ist (d ist dann ein Gegenbeispiel). 
	- Etwas formaler: ”F¨ur alle x, falls R(x), dann P(x)“

### [[Diskrete Strukturen.pdf#page=23|Beweise]]

> [!note] Behauptung
> „If all bandersnatches are borogoves, and all borogoves are slithy, then all bandersnatches are slithy.“ ist gültig.

Die zu beweisende Aussage hat für geeignete Prädikate $P$, $Q$, $R$ die Form:

$$
\frac{
\begin{array}{rll}
\text{If} & \text{A} & \text{for all } x\text{: if } P(x)\text{, then } Q(x)\text{,} \\
\text{and} & \text{B} & \text{for all } y\text{: if } Q(y)\text{, then } R(y)\text{,}
\end{array}
}{
\begin{array}{rll}
\text{then} & \text{C} & \text{for all } z\text{: if } P(z)\text{, then } R(z)\text{.}
\end{array}
}
$$

```mermaid
graph LR
    A["P(x)"] -->|Prämisse A| B["Q(x)"]
    B -->|Prämisse B| C["R(x)"]
    A -.->|Konklusion C| C
```
Wann immer 🅐 und 🅑 wahr sind, hat also jedes Objekt mit Eigenschaft $P$ auch die Eigenschaft $R$, d.h. 🅒 ist wahr unabhängig von der (subjektiven) Interpretation von $P, Q, R$ („bandersnatch“, „borogoves“, „slithy“).

![[Diskrete Strukturen.pdf#page=24&rect=17,14,342,206|Diskrete Strukturen, p.19]]
[[Diskrete Strukturen.pdf#page=31|richtig, falsch, richtig, gültig]]
### Übliche Beweisstrategien
* **[[Diskrete Strukturen.pdf#page=35|Direkter Beweis:]]** (z. B. für „Falls $A$, dann $B$“: Nimm $A$ an und zeige über logische Schlüsse, dass $B$ wahr ist).
* **[[Diskrete Strukturen.pdf#page=36|Kontraposition:]]**
	- „Falls $A$, dann $B$“ **gdw** „Falls nicht $B$, dann nicht $A$“.
	- „Alle $x$ mit $P(x)$ sind $Q(x)$“ **gdw** „Alle $x$ mit nicht $Q(x)$ sind nicht $P(x)$“.
* **Widerspruch:** Man zeigt $A$, indem man „falls nicht $A$, dann falsch“ zeigt. [[Diskrete Strukturen.pdf#page=37|BSP]]
* **Beweis für „$A$ genau dann, wenn $B$“:** Zeige „falls $A$, dann $B$“ und „falls $B$, dann $A$“ (oder nutze eine Kette von Äquivalenzen).
* **Induktion**
### Lemma von Euklid
Ist $p$ eine Primzahl und teilt $p$ ein Produkt zweier ganzer Zahlen $a \cdot b$, so teilt $p$ mindestens einen der Faktoren (also $p \mid a$ oder $p \mid b$).
**Beispiel für Beweis ($a^3$):**
Teilt die Primzahl $5$ die Zahl $a^3 = a \cdot a^2$, so folgt daraus direkt, dass $5$ auch die Zahl $a$ teilen muss ($5 \mid a$).

### [[Diskrete Strukturen.pdf#page=43|Notation für Junktoren und Quantoren]]

| | formale Logik (DS) | | Python (C++) | C, C++, Java |
| :--- | :--- | :--- | :--- | :--- |
| wahr | (triviale Tautologie) | wahr, $\top$ | `True` | `true` |
| falsch | (triviale Kontradiktion) | falsch, $\bot$ | `False` | `false` |
| nicht | Negation | $\neg A$ | `not A` | `!A` |
| oder | Disjunktion | $(A \lor B)$ | `A or B` | `A \|\| B` |
| und | Konjunktion | $(A \land B)$ | `A and B` | `A && B` |
| falls/wenn-dann | Konditional, Subjunktion | $(A \to B)$ | `not A or B` | `!A \|\| B` |
| genau-dann-wenn | Bikonditional | $(A \leftrightarrow B)$ | `A == B` | `A == B` |
| entweder-oder | exklusives Oder, (e)XOR | $(A \oplus B)$ | `A != B` | `A != B` |
| alle | Allquantor | $\forall x F$ | `all` | |
| einige | Existenzquantor | $\exists x F$ | `any` | |

$\triangleright$ Die korrekte Verwendung von $\land, \lor, \neg, \to, \exists, \forall$ benötigt die Definition einer formalen Sprache einschließlich deren Semantik.


## [[Diskrete Strukturen.pdf#page=45|Mengen]]
Die Reihenfolge der Objekte, mehrfache Nennung (Mehrfachheiten) von Objekten, etc. spielen keine Rolle
z.B. $\{0, 1\} = \{1, 0\} = \{0, 0, 1\}$

### [[Diskrete Strukturen.pdf#page=47|Basisdefinitionen]]
Gegeben ein Objekt $x$ und eine Menge $M$ kann nur einer von zwei komplementären Fällen eintreten:
* das Objekt $x$ ist in der Menge $M$ enthalten, kurz $x \in M$.
* das Objekt $x$ ist nicht in der Menge $M$ enthalten, kurz $x \notin M$.
* Man liest $x \in M$ ($x \notin M$) auch als „$x$ ist (kein) Element von $M$“.
Die leere Menge wird mit $\{\}$ oder $\emptyset$ bezeichnet:
Man definiert, dass für jedes Objekt $x$ stets $x \notin \emptyset$ gilt. (Mit anderen Worten: Es gibt kein Objekt $x$ mit $x \in \emptyset$.)

#### Von-Neumann-Modell für $\mathbb{N}_0$
John von Neumann definierte die natürlichen Zahlen $\mathbb{N}_0$ induktiv über Mengen:
* $0 := \emptyset$  $\rightarrow$ Zahl 0 wird als die leere Menge $\emptyset$ definiert
* $1 := \{0\} = \{\emptyset\}$ $\rightarrow$ Zahl 1 wird als die Menge definiert, die die Zahl 0 (also die leere Menge $\emptyset$) als einziges Element enthält.
* $2 := \{0, 1\} = \{\emptyset, \{\emptyset\}\}$
* $3 := \{0, 1, 2\} = \{\emptyset, \{\emptyset\}, \{\emptyset, \{\emptyset\}\}\}$
* $\dots$ In von Neumanns Modell entsteht der Nachfolger einer bereits konstruierten Zahl $n$ durch die Vereinigung der Zahl mit der Menge, die diese Zahl enthält
* $n := (n - 1) \cup \{n - 1\}$
$\rightarrow$ Ausgehend von den **natürlichen Zahlen $\mathbb{N}_{0}$** lassen sich die weiteren Zahlbereiche $\mathbb{Z}$, $\mathbb{Q}$, $\mathbb{R}$ und $\mathbb{C}$ Schritt für Schritt mathematisch präzise konstruieren.

### [[Diskrete Strukturen.pdf#page=49|Mengen: Definition durch Auflistung]]
$[n] := \{1, 2, \dots, n\}$ für jedes $n \in \mathbb{N}_0$ mit $[0] := \emptyset$  Natürliche Zahlen von 1 bis n
$\mathbb{Z}_n := \{0, 1, \dots, n - 1\}$ für jedes $n \in \mathbb{N}_0$ mit $\mathbb{Z}_0 := \emptyset$.

Wertemenge der Funktion f wenn die Defintionsmenge A ist


## Mengen: Definition durch Auflistung (Aufzählung)

* **Def:** $x \in \{x_1, \dots, x_k\}$ **:gdw** $x$ kommt in $x_1, \dots, x_k$ vor.
  ($x \notin \{x_1, \dots, x_k\}$ **gdw** $x$ kommt nicht in $x_1, \dots, x_k$ vor.)
* Die öffnende bzw. schließende Mengenklammer $\{\ ,\ \}$ signalisieren dabei den Beginn bzw. das Ende der Mengendefinition, „$,$“ dient als Trennzeichen.
* Im strikten Sinn muss die Liste vollständig ausgeschrieben werden, häufig wird aber eine angedeutete Auflistung zzgl. erklärendem Text akzeptiert:
  * $\{\mathbb{N}, \mathbb{N}_0\}$ und $\{\mathbb{N}, \mathbb{N}_0, \mathbb{Z}\}$ sind Mengen.
  * $\{\text{A}, \text{B}, \dots, \text{Z}, \text{a}, \text{b}, \dots, \text{z}\}$ Menge der Buchstaben des lateinischen Alphabets.
  * $\{!, '', \#, \dots, \sim\}$ Menge der darstellbaren ASCII-Zeichen.
* **Def:** $[n] := \{1, 2, \dots, n\}$ für jedes $n \in \mathbb{N}_0$ mit $[0] := \emptyset$.
  $\mathbb{Z}_n := \{0, 1, \dots, n - 1\}$ für jedes $n \in \mathbb{N}_0$ mit $\mathbb{Z}_0 := \emptyset$.
* ⚠️ „**:gdw**“ und „**:=**“ zur Betonung von Definitionen.
  (Der Text auf der linken Seite steht für Text auf der rechten Seite.)

---

## Mengen: Definition durch Auswahl (Aussonderung) und Ersetzung
* **Def:** $x \in \{y \in A \mid P(y)\}$ **:gdw** $x \in A$ und $P(x)$ sind wahr.
  ($x \notin \{y \in A \mid P(y)\}$ **gdw** $x \notin A$ oder $P(x)$ falsch.)
* **Def:** $x \in \{f(y) \mid y \in A\}$ **:gdw** $x = f(y)$ für ein $y \in A$.
  ($x \notin \{f(y) \mid y \in A\}$ **gdw** $x \neq f(y)$ für alle $y \in A$.)
  * Es ist wichtig, dass $A$ bereits wohldefiniert ist und für jedes Element $x \in A$ eindeutig bestimmt ist, ob es die Eigenschaft (Prädikat) $P$ besitzt oder nicht, bzw. dass die Konstruktion (Funktion) $f$ eindeutig definiert ist (siehe Russell).
  * Statt „$\mid$“ wird auch „$:$“ verwendet (z.B. $\{x \in \mathbb{R} : |x| < 1\}$).
  * Lies „$\{x \in A \mid P(x), Q(x)\}$“ als „$\{x \in A \mid P(x) \text{ und } Q(x)\}$“.
  * Statt „$\{x \in A \mid P(x)\}$“ auch „$\{x \mid x \in A, P(x)\}$“.
  * $x \in \{x \in A \mid P(x)\}$ **gdw** $x \in \{y \in A \mid P(y)\}$ (gebundene Umbenennung).
* **Bsp:** $A := \{0, 1, 2, 3, 4\}$
  $B := \{x \in A \mid x \leq 2\}$ oder auch $B := \{x \mid x \in A, x \leq 2\}$ ist $\{0, 1, 2\}$
  $C := \{y \in A : y \text{ gerade}\}$ oder auch $C := \{y : y \in A, y \text{ gerade}\}$
  $D := \{2x \mid x \in A\}$ {0,2,4,6,8}
  $E := \{\{x\} \mid x \in A, x \leq 2\}$ {{0}, {1}, {2}}

#### [[Diskrete Strukturen.pdf#page=51|Russellsche Antinomie]]
Da Mengen Objekte sind, können sie selbst Elemente von Mengen sein.