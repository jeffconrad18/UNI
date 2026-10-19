### Zahlensysteme
- Dezimalsystem: Mensch
- Binär: Rechner
- Hexadezimal: Darstellung Computer für Menschen, Vorteil 1 Hex-Symbol = 4 Binär-Symbole
![[Pasted image 20261013165124.png|702]]

- Konventionen sind wichtig um zu wissen, was gemeint ist z.B. **Darstellung negativer Zahlen mit Invertierung + 1**
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
![[era02-asm.pdf#page=21&rect=8,97,943,537&color=yellow|era02-asm, p.21]]
- [[era02-asm.pdf#page=18|ISAs = Instruction Set Architectures]]: legt als Vertrag fest, was ein Prozessor überhaupt kann
- Drei Hauptklassen von Befehlen: 
	- Arithmetische und logische Operationen 
	- Datentransfer 
	- Steuerung des Programmablaufs = Sprünge und Unterprogrammaufrufe