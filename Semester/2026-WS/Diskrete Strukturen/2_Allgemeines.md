### [[Diskrete Strukturen.pdf#page=42|Definitionen Begriffe]]
* **Thm** (kurz für **Theorem / Satz**): wichtiges, häufig verwendetes und/oder nicht offensichtliches Resultat
* **Lem** (kurz für **Lemma**): weniger wichtig oder Hilfsresultat für ein Theorem
* **Kor** (kurz für **Korollar**): einfach zu beweisende Konsequenz eines Theorems/Lemmas
* **Fkt** (kurz für **Fakt**): offensichtliches Ergebnis (proof by intimidation ...)
* **Def** (kurz für **Definition**): eindeutige Begriffsabgrenzung/-erklärung (ggf. Eindeutigkeit/Wohldefiniertheit zu beweisen)


### [Notation für Junktoren und Quantoren](Diskrete%20Strukturen.pdf#page=43)

|  | formale Logik (DS) |  | Python (C++) | C, C++, Java |
| --- | --- | --- | --- | --- |
| wahr | (triviale Tautologie) | wahr, \top | `True` | `true` |
| falsch | (triviale Kontradiktion) | falsch, \bot | `False` | `false` |
| nicht | Negation | \neg A | `not A` | `!A` |
| oder | Disjunktion | (A \lor B) | `A or B` | `A \\|\\| B` |
| und | Konjunktion | (A \land B) | `A and B` | `A && B` |
| falls/wenn-dann | Konditional, Subjunktion | (A \to B) | `not A or B` | `!A \\|\\| B` |
| genau-dann-wenn | Bikonditional | (A \leftrightarrow B) | `A == B` | `A == B` |
| entweder-oder | exklusives Oder, (e)XOR | (A \oplus B) | `A != B` | `A != B` |
| alle | Allquantor | \forall x F | `all` |  |
| einige | Existenzquantor | \exists x F | `any` |  |

\triangleright Die korrekte Verwendung von \land, \lor, \neg, \to, \exists, \forall benötigt die Definition einer formalen Sprache einschließlich deren Semantik.