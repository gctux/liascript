<!-- 
version:  0.0.1
language: de
narrator: Deutsch Female
persistent: true
author:  Lutz Herrmann

edit: true

tags: GK Informatik, Technische Informatik

comment: Aufgaben zum Thema Zeichencodierung im GK Informatik.

link:     https://cdn.jsdelivr.net/chartist.js/latest/chartist.min.css

script:   https://cdn.jsdelivr.net/chartist.js/latest/chartist.min.js


-->


# 1.1.3 Zeichencodierung - Aufgaben

Auf dieser Seite finden Sie Aufgaben zum Thema Zeichencodierung für den Informatik GK Klasse 11 - Sachsen mit interaktiver Lösungseingabe bzw. Anzeigemöglichkeit der Lösung.



## Aufgabe 1

Verschlüsseln Sie ein Wort selbst in ASCII-Codierung. Gehen Sie davon aus, dass das "A" die 65 ist und das "a" die 97. Berechne im Kopf die Dezimalzahlen für die Buchstaben deines Wortes. Rechne danach die Zahlen in Binärzahlen um.

<details>
<summary>Antwort anzeigen</summary>
Lösung:  z.B. Apfel -> 65 112 102 101 108
</details>

## Aufgabe 2

"Marsianer" benutzen ein Hexadezimalsystem und empfangen die folgende Nachricht:  
52 65 74 74 75 6e 67 20 69 6e 20 53 69 63 68 74 3a 29  
Wandeln Sie die Nachricht in das Dezimalsystem um und entschlüsseln Sie  den Text mit Hilfe einer ASCII- Tabelle.

<details>
<summary>Antwort anzeigen</summary>
Lösung "Rettung in Sicht:)"
</details>

## Aufgabe 3

Wenn man die Nummer eines UTF-8-Zeichens kennt, kann man es mit der Funktion `chr()` in Python anzeigen.

```
>>> chr(128512)
'😀'
```

Umgekehrt erhält man durch die Funktion `ord()` die Nummer des Unicode-Zeichens als Dezimalzahl.

```
>>> ord('😀')
128512
```

Schreiben Sie ein Programm welches nach Eingabe einer Zahl die nachfolgenden 20 Unicodezeichen ausgibt.


[[!]]
<script>
  true;
</script>
****************************************
```python
while True:
    z = int(input("Geben Sie eine Zahl ein! "))
    for i in range (z,z+20):
        print(chr(i))
    e = input("Eine weitere Zahl eingeben (J|N)? ")
    if e == 'N':
        break
```
****************************************