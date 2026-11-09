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

# 2.3.1 Wiederholung Funktionen - Aufgaben

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

- a) Das Programm zum Tauschen von zwei Zahlenwerten liefert beim Ausführen eine Fehlermeldung. Warum?<details>
<summary>Antwort anzeigen</summary>
Die Variablen zahl1 und zahl2 sind lokale Variablen.
</details>


- b) Verändern Sie das Programm so, dass es korrekt arbeitet.
[[!]]
<script>
  true;
</script>
****************************************
```python
def zahlen_eingeben():
    zahl1 = int(input("Zahl 1: "))
    zahl2 = int(input("Zahl 2: "))
    return zahl1, zahl2

def zahlen_tauschen(zahl1,zahl2):
    hilf = zahl1
    zahl1 = zahl2
    zahl2 = hilf
    return zahl1, zahl2

def zahlen_ausgeben(zahl1,zahl2):
    print("Zahl 1: ", zahl1)
    print("Zahl 2: ", zahl2)

# Hauptprogramm: Funktionsaufrufe
zahl1, zahl2 = zahlen_eingeben()
zahl1, zahl2 = zahlen_tauschen(zahl1,zahl2)
zahlen_ausgeben(zahl1,zahl2)
```
****************************************

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

[[!]]
<script>
  true;
</script>
****************************************
```python
def meineFunktion(a,b):
    a = a * b
    erg = a + b
    return erg

print(meineFunktion(3,4))
```
****************************************


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

[[!]]
<script>
  true;
</script>
****************************************
```python
def meineFunktion(n):
    b = "Hallo "
    print(b + n)

n = "Robert"
meineFunktion(n)
```
****************************************



c) 

```python
def meineFunktion(x):
  erg = x.count("e")  #count ist ein Befehl der Listen und zählt die Anzahl
  return erg


anz = meineFunktion(66)
print(anz)
```

[[!]]
<script>
  true;
</script>
****************************************
```python
def meineFunktion(x):
  erg = x.count("e")  #count ist ein Befehl der Listen und zählt die Anzahl
  return erg


anz = meineFunktion([66])
print(anz)
```
****************************************

d) 

```python
def meine Funktion(n)
    n = n + 34
    return n

erg = meine Funktion(45)
print(erg)
```

[[!]]
<script>
  true;
</script>
****************************************
```python
def meineFunktion(n):
    n = n + 34
    return n

erg = meineFunktion(45)
print(erg)
```
****************************************

e)

```python
def meineFunktion(x,y):
    if (x % y == 0):
        return True
    else:
        return False

if meineFunktion(8,4):
    print("super")
else:
    print("schade")
```

[[!]]
<script>
  true;
</script>
****************************************
```python
def meineFunktion(x,y):
    if (x % y == 0):
        return True
    else:
        return False

if meineFunktion(8,4):
    print("super")
else:
    print("schade")
```
****************************************




f)

```python
def meineFunktion(x):
    y = x * 10

meineFunktion(2)
print(y)
```

[[!]]
<script>
  true;
</script>
****************************************
```python
def meineFunktion(x):
    global y
    y = x * 10

meineFunktion(2)
print(y)
```
****************************************




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

[[!]]
<script>
  true;
</script>
****************************************
```python
import random

def isPrim(n):
        # Implementation uses the Miller-Rabin Primality Test
    # The optimal number of rounds for this test is 40
    # See http://stackoverflow.com/questions/6325576/how-many-iterations-of-rabin-miller-should-i-use-for-cryptographic-safe-primes
    # for justification

    # If number is even, it's a composite number

    if n < 0:
        return False

    if n == 1:
        return False

    if n == 2 or n == 3:
        return True

    if n % 2 == 0:
        return False

    r, s = 0, n - 1
    while s % 2 == 0:
        r += 1
        s //= 2
    for _ in range(3):
        a = random.randrange(2, n - 1)
        x = pow(a, s, n)
        if x == 1 or x == n - 1:
            continue
        for _ in range(r - 1):
            x = pow(x, 2, n)
            if x == n - 1:
                break
        else:
            return False
    return True

def ziffer_in_zahl(n,z):
    return str(n).count(str(z))

def eine_ziffer_je_zahl(n):
    anz = 0
    for i in range(10):
        if ziffer_in_zahl(n,i) == 1:
            anz += 1
    if anz == 6:
        return True
    else:
        return False

zahlenliste = []
primzahlenliste = []

for i in range(100000,1000000):
    if eine_ziffer_je_zahl(i):
        zahlenliste.append(i)
        if isPrim(i):
            primzahlenliste.append(i)
        
        
print("Länge der Zahlenliste:",len(zahlenliste))
print("Länge der Primzahlenliste:",len(primzahlenliste))    
```
****************************************


## Aufgabe 5 - Tresor knacken

Ein reicher Mann hat leider den Code für seinen Tresor vergessen. Er weiß lediglich noch, dass alle Ziffern von 1 bis 9 genau einmal vorkommen. Der Code hat also die Form ABCDEFGHI. Außerdem hat er noch einen kleinen Zettel mit folgenden Notizen gefunden:  

E - I = F  

I + E = B  

G * I = A  

H - C = D / I  

Können Sie den Tresor knacken?

[[!]]
<script>
  true;
</script>
****************************************
```python
for a in range(1,10):
   for b in range(1,10):
       for c in range(1,10):
           for d in range(1,10):
               for e in range(1,10):
                   for f in range(1,10):
                       for g in range(1,10):
                           for h in range(1,10):
                               for i in range(1,10):
                                   if (e-i==f) and (i+e==b) and (g*i==a) and (float(h-c)==d/i):
                                       liste = [a]+[b]+[c]+[d]+[e]+[f]+[g]+[h]+[i]
                                       if len(liste) == len(set(liste)):
                                           print(liste)
```
****************************************

## Aufgabe 6

Spielen Sie Lotto! Vereinfacht! Solange, bis alle 6 Zahlen richtig sind.

Vorgehen:  
- Eingabe deiner 6 Zahlen  
- Funktion zum Ziehen von 6 Zahlen aus 49. Dabei ist zu beachten, dass jede Zahl nur einmal gezogen werden kann.  
- Vergleich der jeweils 6 Zahlen.  
- Solange wiederholen, bis du gewonnen hast.


[[!]]
<script>
  true;
</script>
****************************************
```python
import random

def ziehen():
    global liste2
    liste2 = []
    for i in range(6):
        zahl = random.randint(1,49)
        while zahl in liste2:
            zahl = random.randint(1,49)
        liste2.append(zahl)
    liste2.sort()
    
    
print("Lotto spielen")
print("#############")
print()
print("Gib deine Zahlen ein!")

liste1=[]
liste2=[]
ziehungen = 0

for i in range(6):
    zahl = int(input("Zahl "+str(i+1)+": "))
    while zahl in liste1:
        print("Zahl wurde bereits eingegeben!")
        zahl = int(input("Zahl "+str(i+1)+": "))
    while zahl < 1 or zahl > 49:
        print("Keine Lottozahl!")
        zahl = int(input("Zahl "+str(i+1)+":"))
    liste1.append(zahl)

liste1.sort()

while liste2 != liste1:
    ziehen()
    ziehungen += 1

print(liste1, liste2)
print("Anzahl Ziehungen:", ziehungen)
```
****************************************


