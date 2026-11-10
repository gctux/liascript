<!-- 
version:  0.0.1
language: de
narrator: Deutsch Female
persistent: true
author:  Lutz Herrmann

edit: true

tags: GK Informatik, Technische Informatik

comment: Aufgaben zum Thema Zeichenkatten im GK Informatik.

link:     https://cdn.jsdelivr.net/chartist.js/latest/chartist.min.css

script:   https://cdn.jsdelivr.net/chartist.js/latest/chartist.min.js


-->

# 2.1.1 Aufgaben zu Zeichenketten in Python

Auf dieser Seite finden Sie Aufgaben zum Thema Zeichenketten in Python für den Informatik GK Klasse 11 - Sachsen mit interaktiver Lösungseingabe bzw. Anzeigemöglichkeit der Lösung.


## Aufgabe 1

Erstellen Sie ein Pythonprogramm mit Thonny!
Implementieren Sie darin die Lösung der folgenden Teilaufgaben.

- ​a) Eine Zeichenkette soll mit `input()` eingegeben werden.

- b) Die Zeichenkette soll in Großbuchstaben ausgegeben werden.

- c) Geben Sie die die Anzahl der Zeichen in der Zeichenkette aus.

- d) Geben Sie den Ersten und den letzten Buchstaben der Zeichenkette aus.

- e) Geben Sie die Zeichenkette mit vertauschten ersten und letzten Buchstaben aus.

[[!]]
<script>
  true;
</script>
****************************************
```python
zeichenkette = input("a) Zeichenkette: ")
print("b) Zeichenkette in Großbuchstaben:",zeichenkette.upper())
print("c) Anzahl der Zeichen:", len(zeichenkette))
print("d) Erstes Zeichen:",zeichenkette[0],", Letztes Zeichen:",zeichenkette[len(zeichenkette)-1])
print("e) Zeichenkette mit vertauschten ersten und letzten Buchstaben:",zeichenkette[len(zeichenkette)-1]+zeichenkette[1:len(zeichenkette)-1]+zeichenkette[0])
```
****************************************


## Aufgabe 2

Schreiben Sie ein Pythonprogramm, welches testet, ob ein eingegebenes Wort ein Pallindrom ist. Ein Pallindrom ist ein Wort, welches von hinten nach vorn gelesen dasselbe Wort ergibt. (z.B. Otto, Rentner)

[[!]]
<script>
  true;
</script>
****************************************
```python
wort = input("Geben Sie ein Wort ein: ")
wort = wort.upper()
rueckwaerts = ""
for i in range(len(wort)-1,-1,-1):
    rueckwaerts += wort[i]
if wort == rueckwaerts:
    print("Das Wort ist ein Pallindrom.")
else:
    print("Das Wort ist ein kein Pallindrom.")
```
****************************************

## Aufgabe 3

Anagramme sind Zeichenketten, die dieselben Buchstaben in gleicher Anzahl, aber beliebiger Reihenfolge enthalten.

- a) Schreiben Sie ein Pythonprogramm, welches überprüft, ob zwei eingeben Wörter Anagramme sind z.B. Lampe und Palme.

- b) Erweitern Sie das Programm, sodass es erkennt ob zwei beliebige Zeichenketten Anagramme sind. Leerezeichen werden dabei ignoriert. (Beispiel: "Tom Marvolo Riddle" und "I am Lord Voldemort")

[[!]]
<script>
  true;
</script>
****************************************
```python
print("Test, ob zwei Zeichenketten Anagramme sind")
zeichenkette1 = input("Geben Sie das erste Wort ein: ")
zeichenkette2 = input("Geben Sie das zweite Wort ein: ")

z1 = ""
for i in range(len(sorted(zeichenkette1.upper()))):
    if sorted(zeichenkette1.upper())[i] != ' ':
        z1 += sorted(zeichenkette1.upper())[i]
        
z2 = ""
for i in range(len(sorted(zeichenkette2.upper()))):
    if sorted(zeichenkette2.upper())[i] != ' ':
        z2 += sorted(zeichenkette2.upper())[i]
    
if z1==z2:
    print("Die Zeichenketten sind Anagramme.")
else:
    print("Die Zeichenketten sind keine Anagramme.")

```
****************************************

