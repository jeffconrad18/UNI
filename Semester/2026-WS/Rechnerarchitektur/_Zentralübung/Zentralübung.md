![[zue_02_riscv_handout.pdf#page=3&rect=28,35,424,136|zue_02_riscv_handout, p.3]]
**Assembler**: Niedrigste Abstraktionsebene vor Maschinencode mit primitiven Befehlen

## RISC-V
- 32-Bit groß
- 32 Stück, von `x0` bis `x31`
- Konventionen für Verwendung, z.B. `x0` hat Constant value 0

**Befehle**
![[zue_02_riscv_handout.pdf#page=6&rect=204,31,429,214|zue_02_riscv_handout, p.6]]

### [[zue_02_riscv_handout.pdf#page=8|Zero- und Sign-Extension]]
![[zue_02_riscv_handout.pdf#page=8&rect=29,14,388,193|zue_02_riscv_handout, p.8]]

### [[zue_02_riscv_handout.pdf#page=16|Bitmasken]]
▶ and mit Maske: Bits an den 0-Stellen der Maske löschen (z.B. ersten vier Bits auf 0 setzen)
▶ or mit Maske: Bits an den 1-Stellen der Maske setzen
▶ xor mit Maske: Bits an den 1-Stellen der Maske invertieren
