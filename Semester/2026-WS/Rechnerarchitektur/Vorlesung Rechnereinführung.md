## Einführung Assembler
### Zahlensysteme
- Dezimalsystem: Mensch
- Binär: Rechner
- Hexadezimal: Darstellung Computer für Menschen, Vorteil 1 Hex-Symbol = 4 Binär-Symbole
- [[Mathe - Vorkurs|Formeln im Vorkurs]] 
![[Pasted image 20261013165124.png|702]]

- Konventionen sind wichtig um zu wissen, was gemeint ist z.B. **Darstellung negativer Zahlen mit Invertierung + 1**
- **[[era01-intro.pdf#page=32|Möglichkeiten Darstellung für negative Zahlen]]**
	- Vorzeichenbit: Erstes Bit gibt +/- an ABER Doppelnull, Rechnen schwieriger
	- Einerkomplement: Invertierung ABER Rechnen schwieriger
	- **Zweierkomplement**: Invertierung + 1 PERFEKT Grundrechenarten funktionieren gleich mit neg/pos Zahlen
- Darstellung Reale Zahlen: [[era01-intro.pdf#page=34|Gleitkommazahlen]]
- Textzeichen durch Konvention: [[era01-intro.pdf#page=38|ASCII Tabelle]] | Unicode UTF-16
### [[era01-intro.pdf#page=40|Abstraktionsebenen]]
![[era01-intro.pdf#page=41&rect=280,4,880,456|era01-intro, p.41]]

- Assemblersprachen sind plattformspezifisch, z.B. [[era02-asm.pdf#page=13|Intel/AMD, ARM]] oder offener Standard [[era02-asm.pdf#page=14|RISC-V]]
#### [[era02-asm.pdf#page=20|Befehlsformat]]
- Ein Befehl besteht grundsätzlich immer aus 
	- der Spezifikation der Operation (Opcode) 
	- der Spezifikation der Operanden 
- Zwei mögliche Varianten: 
	- Einheitliches Befehlsformat 
		- Alle Befehle haben eine feste Länge 
		- Klassische Lösung für RISC 
	- Variables Befehlsformat 
		- Befehle können verschieden viele und verschieden-formatige Adressen enthalten
	- In RISC-V sind (normalerweise) alle Befehle 32bit
![[era02-asm.pdf#page=28&rect=8,109,936,535|era02-asm, p.28]]
*unwichtig | Operand (a5) | Operand (a4) | Sagt, dass Funktion | Ziel (a5) | Genaue Funktion*
01111=15, weil a5 auf x15 $\rightarrow$ analog für a4
![[era02-asm.pdf#page=27&rect=479,52,917,466|era02-asm, p.27]]

## Assemblerbefehle und Operanden (am Beispiel RISC-V)
- [[era02-asm.pdf#page=18|ISAs = Instruction Set Architectures]]: legt als Vertrag fest, was ein Prozessor überhaupt kann
- Drei Hauptklassen von Befehlen: 
	- Arithmetische und logische Operationen 
	- Datentransfer 
	- Steuerung des Programmablaufs = Sprünge und Unterprogrammaufrufe

*signed*: Mit Vorzeichen
*unsigned*: Ohne Vorzeichen
#### [[era02-asm.pdf#page=30|Erzeugung von 12-BIT Konstanten]]
#### [[era02-asm.pdf#page=31|Erzeugung von 32-BIT Konstanten]]
#### [[era02-asm.pdf#page=32|Multiplikation]]
- Angeben, ob Vorzeichen dabei sind oder nicht
- Wichtig auch zu wissen, wie groß Ergebnis wird
#### [[era02-asm.pdf#page=33|Division]]
- Mit und ohne Rest ausgeben
#### [[era02-asm.pdf#page=34|Logische Operationen]]
#### [[era02-asm.pdf#page=36|Schiebebefehle]]
- **Logische Schieben nach rechts**: Schiebt alle Bits nach rechts. Von links werden immer Nullen (0) nachgezogen.
- **Arithmetisches Schieben nach rechts**: Schiebt alle Bits nach rechts. Das höchstwertige Bit (Vorzeichenbit) bleibt erhalten und wird von links dupliziert.

## Datentransferbefehle (Haupt) Speicher
### [[era02-asm.pdf#page=39|Datenspeicherung]]
Operanden nur aus Registern und Konstanten 
- Register sind schnell, aber auch sehr begrenzt 
- Nur als Zwischenspeicher gedacht 

Zusätzlich: Hauptspeicher 
- Große Speicherkapazität 
- Ablage aller zu berarbeitenden Daten 
- Nicht zum Verwechseln mit „Hintergrundspeicher“ 
	- Hauptspeicher meist flüchtig 
	- Daten müssen in den Hauptspeicher geladen werden 
- Meist als “Random Access Memory“ oder RAM 
	- Man kann auf jedes gespeicherte Element zugreifen 
	- Kein „vorspulen“ / „zurückspulen“ 
	
Konsequenz 
- Daten müssen übertragen werden 
- „Load“ und „Store“ Befehle → RISC-V ist eine „Load and Store Architecture“ 
- Andere ISAs erlauben Operanden direkt aus dem Hauptspeicher
### [[era02-asm.pdf#page=42|Speichergrößen]]

| Dezimal: Wert | Dezimal: Abk. | Dezimal: Metrik | Binär: Wert | Binär: Abk. | Binär: Metrik |
| :------------ | :------------ | :-------------- | :---------- | :---------- | :------------ |
| 1             | B             | byte            | 1           | B           | byte          |
| 1000 = 10³    | KB            | kilobyte        | 1024 = 2¹⁰  | KiB         | kibibyte      |
| 1000²         | MB            | megabyte        | 1024²       | MiB         | mebibyte      |
| 1000³         | GB            | gigabyte        | 1024³       | GiB         | gibibyte      |
| 1000⁴         | TB            | terabyte        | 1024⁴       | TiB         | tebibyte      |
| 1000⁵         | PB            | petabyte        | 1024⁵       | PiB         | pebibyte      |
| 1000⁶         | EB            | exabyte         | 1024⁶       | EiB         | exbibyte      |
| 1000⁷         | ZB            | zettabyte       | 1024⁷       | ZiB         | zebibyte      |
Ein Adressraum mit folgender Adresslänge hat folgende Größe:
- 16 bit: 2¹⁶ = 64 KiB
- 32 bit: 2³² = 4 GiB
- 64 bit: 2⁶⁴ = 16 EiB
Speicherzellen auf ISA Ebene sind üblicherweise mehrere Byte breit

## [[era02-asm.pdf#page=51|Sprünge]]
- Sprünge sind wie $if...else$ 
- **Unbedingter Sprung:** Programm wird an anderer Stelle fortgesetzt
- **Bedingter Sprung**: Sprung nur, wenn eine Bedingung erfüllt ist, z.B. equal, not equal, less than, greater than or equal 
- [[era02-asm.pdf#page=55|Damit lassen sich auch *While* Schleifen implementieren]]
- [[era02-asm.pdf#page=56|Alternative (z.B. x86) mit Statusregister]]: Extra Register in der ISA um Bedingungen zu speichern, basierend auf letzter arithmetischen Operation