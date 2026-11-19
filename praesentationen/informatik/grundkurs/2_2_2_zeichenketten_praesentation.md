<!-- 
version:  0.0.1
language: de
narrator: Deutsch Female
persistent: true
author:  Lutz Herrmann

edit: true

tags: GK Informatik, Programmieren in Python

comment: Aufgaben zum Thema Zeichenketten im GK Informatik.

link:     https://cdn.jsdelivr.net/chartist.js/latest/chartist.min.css

script:   https://cdn.jsdelivr.net/chartist.js/latest/chartist.min.js

import: https://raw.githubusercontent.com/LiaTemplates/Pyodide/master/README.md
-->

# 2.2.2 Zeichenketten

- Datentyp **Zeichenkette** bzw. **String** (str) -> strukturierter Datentyp, der aus einer Folge von Zeichen besteht. 
- Unterschied zur Liste: eine Zeichenkette darf nicht verändert werden

## Zugriff auf die einzelnen Zeichen

Genau wie bei Listen kann man auf die einzelnen Zeichen mit den entsprechenden Indizes eckigen Klammer zugreifen. Man kann wie bei Listen auch Slices benutzen. 

```python
zeichenkette = "Informatik"
print("Erster Buchstabe:",zeichenkette[0])
print("Wort im Wort:",zeichenkette[2:6]) 
```
@Pyodide.eval

## Operatoren

Wie schon aus Klasse 10 bekannt, können Zeichenkette mit dem Operator `+` verknüpft und mit dem Operator `*`mit einer natürlichen Zahl multipliziert werden. 

```python
wort1 = "Hallo"
wort2 = "Welt"
nachricht = wort1 + " " + wort2
print(nachricht)
```
@Pyodide.eval

```python
wort = "Hallo"
satz = 5 * wort
print(satz)
```
@Pyodide.eval

## Funktionen auf Zeichenketten

| Operation | Beschreibung                                                       | Beispiel                                                  |
| --------- | ------------------------------------------------------------------ | --------------------------------------------------------- |
| len()     | Gibt die Länge (Anzahl der Zeichen) eines Strings zurück           | `len("Hallo") # 5`                                        |
| lower()   | Konvertiert alle Buchstaben zu Kleinbuchstaben                     | `"Python".lower() # "python"`                             |
| upper()   | Konvertiert alle Buchstaben zu Großbuchstaben                      | `"Python".upper() # "PYTHON"`                             |
| strip()   | Entfernt führende und folgende Leerzeichen                         | `" text ".strip() # "text"`                               |
| split()   | Teilt den String anhand eines Trennzeichens in eine Liste auf      | `"a,b,c".split(",") # ["a", "b", "c"]`                    |
| replace() | Ersetzt Teile des Strings durch einen anderen String               | `"Hallo Welt".replace("Welt", "Python") # "Hallo Python"` |
| find()    | Findet die Position eines Teilstrings oder -1, wenn nicht gefunden | `"Hallo".find("ll") # 2`                                  |
| count()   | Zählt, wie oft ein Teilstring vorkommt                             | `"Banane".count("a") # 3`                                 |
| sorted()  | Gibt eine alphabetisch sortierte Liste der Zeichen zurück          | `sorted("python") # ['h', 'n', 'o', 'p', 't', 'y']`       |
