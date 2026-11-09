<!-- 
version:  0.0.1
language: de
narrator: Deutsch Female
persistent: true
author:  Lutz Herrmann

edit: true

tags: GK Informatik, Technische Informatik

comment: Aufgaben zum Thema Wiederholung Funktionen im GK Informatik.

link:     https://cdn.jsdelivr.net/chartist.js/latest/chartist.min.css

script:   https://cdn.jsdelivr.net/chartist.js/latest/chartist.min.js


-->

# 2.3.1 Wiederholung - Aufgaben

Auf dieser Seite finden Sie Aufgaben zum Thema Wiederholung Funktionen für den Informatik GK Klasse 11 - Sachsen mit interaktiver Lösungseingabe bzw. Anzeigemöglichkeit der Lösung.

## Aufgabe 1

- a) Erstellen Sie eine Funktion `drucke_zufallszahl()`, die eine zufällige Zahl zwischen 1 und 100 generiert und ausgibt. Die Prozedur gibt keinen Wert zurück. (Hinweis: Du brauchst dafür das Modul/die Bibliothek "random" und daraus die Funktion "randint")

[[!]]
<script>
  true;
</script>
****
```python
import random

def drucke_zufallszahl():
    print(random.randint(1,100))
    
drucke_zufallszahl()
```
****************************************


- b) Erstellen Sie eine Funktion namens `zufallsliste()`, die eine Liste mit 100 zufälligen Zahlen zwischen 1 und 6 erstellt.

[[!]]
<script>
  true;
</script>
****************************************
```python
import random

def zufallsliste():
    liste = []
    for i in range(100):
        liste.append(random.randint(1,6))
    return liste
    
print(zufallsliste())
```
****************************************

- c) Erstellen Sie eine Funktion namens `gerade(zahl)`, die überprüft ob eine übergebene Zahl gerade oder ungerade ist und dies mit True oder False zurück gibt.

[[!]]
<script>
  true;
</script>
****************************************
```python
def gerade(zahl):
    return(zahl%2 == 0)
    
print(gerade(3))
print(gerade(4))
```
****************************************

- d) Erstellen Sie eine Funktion namens `pasch()`, die zwei Würfelzahlen zufällig erzeugt und prüft ob sich um einen Pasch handelt oder nicht. Zurück gegeben wird ob ein Pasch gewürfelt wurde (True) oder nicht (False).

[[!]]
<script>
  true;
</script>
****************************************
```python
import random

def pasch():
    zahl1 = random.randint(1,6)
    zahl2 = random.randint(1,6)
    return zahl1 == zahl2
    
print(pasch())
```
****************************************

<br><br><br>

## Aufgabe 2

Gegeben ist das folgende Pythonprogramm (`lokale_globale_Variablen.py`):

```python
# Unterprogramme
def zahlen_eingeben():
    zahl1 = int(input("Zahl 1: "))
    zahl2 = int(input("Zahl 2: "))

def zahlen_tauschen(zahl1,zahl2):
    hilf = zahl1
    zahl1 = zahl2
    zahl2 = hilf

def zahlen_ausgeben(zahl1,zahl2):
    print("Zahl 1: ", zahl1)
    print("Zahl 2: ", zahl2)

# Hauptprogramm: Funktionsaufrufe
zahlen_eingeben()
zahlen_tauschen(zahl1,zahl2)
zahlen_ausgeben(zahl1,zahl2)
```

- a) Das Programm zum Tauschen von zwei Zahlenwerten liefert beim Ausführen eine Fehlermeldung. Warum?
- b) Verändern Sie das Programm so, dass es korrekt arbeitet.

## Aufgabe 3

In den jeweiligen Programmen sind Fehler enthalten. Kopieren Sie den Quellcode in die Entwicklungsumgebung. Überarbeiten Sie die Programme so, dass sie wieder funktionieren und die Funktionen ihren Zweck erfüllen.

a)

```python
def meineFunktion(a,b):
a = a * b
erg = a + b
return erg

print(meineFunktion())
```

b)

```python
def meineFunktion():
    b = "Hallo "
    n = "Udo"
    print(b + n)

n = "Robert"
meinFunktion()

#Es soll eigentlich "Hallo Robert" ausgegeben werden.
```

c) 

```python
def meineFunktion(x):
  erg = x.count("e")  #count ist ein Befehl der Listen und zählt die Anzahl
  return erg


anz = meineFunktion(66)
print(anz)
```

d) 

```python
def meine Funktion(n)
    n = n + 34
    return n

erg = meine Funktion(45)
print(erg)
```

e)

```python
meineFunktion(x,y):
    if (x % y == 0):
        return True
    else:
        return False

if meineFunktion("Hallo","Welt"):
    print("super")
else:
    print("schade")
```

f)

```python
def meineFunktion(x):
    y = x * 10

meineFunktion(2)
print(y)
```


## Aufgabe 4 - Zahlenrätsel

Es soll eine Liste mit ganz speziellen Zahlen erstellt werden.  
Alle Zahlen sind 6-stellig, jede Ziffer in der Zahl kommt nur einmal vor.  
Schreiben Sie ein Programm, dass eine Liste mit diesen Zahlen erstellt.  
Zur Kontrolle: Es gibt 136080 solche Zahlen.  

Ergänzung:  
Gib nur die Zahlen in der Liste aus, die auch eine Primzahl sind. Zur Kontrolle: 10239 Zahlen

Vorgehen:  
Schreiben Sie  eine Funktion `ziffer_in_zahl`. Sie soll prüfen ob die Ziffer in der Zahl vorkommt. Als Rückgabewert wird die Anzahl der Vorkommen angegeben.  
Schreiben Sie eine Funktion `eine_ziffer_je_zahl`. Sie soll prüfen, ob in der Zahl jede Ziffer von 0 bis 9 höchstens einmal vorkommt. Wenn das so ist gib "True" zurück, ansonsten "False".  
Erstellen Sie nun das Hauptprogramm und testen Sie alle 6-stelligen Zahlen. Erfüllt eine Zahl das Kriterium, so kommt sie in die Liste.  
Vermeiden Sie es, die ganze Zahlen auszugeben. Das dauert zu lange. Besser ist die Anzahl der Zahlen zu zählen bzw. die Länge der Liste auszugeben.

Tipp: Um auf die einzelnen Ziffern einer Zahl zuzugreifen, kann man die Zahl in ein String umwandeln (str(zahl)). Ein String kann wie ein Array benutzt werden. Beachte aber, dass die Ziffern dann auch vom Typ String sind.


## Aufgabe 5 - Tresor knacken

Ein reicher Mann hat leider den Code für seinen Tresor vergessen. Er weiß lediglich noch, dass alle Ziffern von 1 bis 9 genau einmal vorkommen. Der Code hat also die Form ABCDEFGHI. Außerdem hat er noch einen kleinen Zettel mit folgenden Notizen gefunden:  

E - I = F  

I + E = B  

G * I = A  

H - C = D / I  

Können Sie den Tresor knacken?

## Aufgabe 6

Spielen Sie Lotto! Vereinfacht! Solange, bis alle 6 Zahlen richtig sind.

Vorgehen:  
- Eingabe deiner 6 Zahlen  
- Funktion zum Ziehen von 6 Zahlen aus 49. Dabei ist zu beachten, dass jede Zahl nur einmal gezogen werden kann.  
- Vergleich der jeweils 6 Zahlen.  
- Solange wiederholen, bis du gewonnen hast.





