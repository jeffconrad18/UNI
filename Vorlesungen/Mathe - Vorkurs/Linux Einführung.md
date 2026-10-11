#### Essentielle Commands
`man` - Handbuch, z.B. ``man ls`` Anleitung für ``ls``
`~` - Home-Verzeichnis
`pwd` - Aktuelles Verzeichnis ausgeben
`cat` - Dateien anzeigen, erstellen oder kombinieren
`mkdir` - Ordner erstellen, mit `-p` ebenfalls Zwischenordner erstellen
`rm` - Ordner/Datei löschen (`rm -r foldername` - Ganzen Ordner löschen)
``mv path/to/file new/path/`` - Verschiebt ``file`` von ``path/to/`` nach ``new/path/``
``cp path/to/file other-path/to/copy`` - Kopiert ``file`` zu ``other-path/to/copy``
`tree` - Listet Ordner, Dateien und Unterordner auf
### Control Operators
`;` – Führt Befehle sequentiell nacheinander aus.
`&&` – **AND**: Führt den zweiten Befehl nur aus, wenn der vorherige erfolgreich war.
`||` – **OR**: Führt den zweiten Befehl nur aus, wenn der vorherige fehlschlägt.
 `&` – Führt den vorangestellten Befehl im Hintergrund aus.
`( ... )` – Führt die geklammerten Befehle in einer Subshell aus.
`|` – **Pipe**: Verbindet die Standardausgabe (`stdout`) des ersten Befehls mit der Standardeingabe (`stdin`) des zweiten.
### Redirection Operators (Ein-/Ausgabeumleitung)
 `>` – Leitet `stdout` in eine Datei um (überschreibt existierenden Inhalt).
 `>>` – Leitet `stdout` an eine Datei an (hängt den Inhalt an).
 `<` – Liest den Inhalt einer Datei als `stdin` für ein Programm ein.
 `<<` – **Here-Document**: Übergibt nachfolgenden Textblock bis zu einem Trennzeichen als `stdin`.