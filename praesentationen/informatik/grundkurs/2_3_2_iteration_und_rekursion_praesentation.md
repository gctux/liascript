<!-- 
version:  0.0.1
language: de
narrator: Deutsch Female
persistent: true
author:  Lutz Herrmann

edit: true

tags: GK Informatik, Programmieren in Python

comment: Aufgaben zum Thema Iteration und Rekursion im GK Informatik.

link:     https://cdn.jsdelivr.net/chartist.js/latest/chartist.min.css

script:   https://cdn.jsdelivr.net/chartist.js/latest/chartist.min.js

import: https://raw.githubusercontent.com/LiaTemplates/Pyodide/master/README.md
-->
# 2.3.2 Iteration und Rekursion

In der Informatik gibt es für eine bestimmte Problemklasse zwei grundlegende Techniken zur Lösung von Problemen: Iteration und Rekursion.

## Iteration

**Iteration** ist ein wiederholter Prozess, bei dem eine Aufgabe in Schritten wiederholt wird, bis eine bestimmte Bedingung erfüllt ist. Dies geschieht in der Regel mithilfe von Schleifen, wie zum Beispiel einer `for`-Schleife oder einer `while`-Schleife.

Hier ist ein Beispiel in Python, wie man die Summe von 0 bis n mit Iteration berechnet:

```python
def sum_iteration(n):
    result = 0
    for i in range(n + 1):
        result += i
    return result

n = 5
print("Summe von 0 bis", n, "mit Iteration:", sum_iteration(n))
```
@Pyodide.eval

## Rekursion

**Rekursion** ist ein Ansatz, bei dem eine Funktion sich selbst aufruft, um ein Problem in kleinere Teilprobleme aufzuteilen und diese zu lösen. Jeder rekursive Aufruf verringert die Größe des Problems, bis eine Abbruchbedingung erreicht ist.

Die Rekursion besteht also aus zwei Hauptteilen: Dem Basisfall und dem rekursiven Fall. Der Basisfall liefert die endgültige Lösung, der rekursive Fall ermittelt die Lösung durch einen weiteren Aufruf der Funktion.

Hier ist ein Beispiel in Python, wie man die Summe von 0 bis n mit Rekursion berechnet:

```python
def sum_recursion(n):
#Abbruchbedingung:
    if n == 0:
        return 0
#Rekursionsschritt
    else:
        return n + sum_recursion(n - 1)

n = 5
print("Summe von 0 bis", n, "mit Rekursion:", sum_recursion(n))
```
@Pyodide.eval

[Beispie Rekursion](./images/2_3_2_beispiel_rekursion.pdf)


**Aufgabe:**

Testen Sie die beiden Programme mit weiteren Werten für n!

## Mathematischer Exkurs - Zahlenfolgen

Da sich rekursiv definierte Zahlenfolgen sehr gut mit Rekursion bzw. Iteration berechnen lassen, erfolgt an dieser Stelle ein kleiner mathematischer Exkurs zu Zahlenfolgen.



> [!NOTE] Zahlenfolge (Folge):
> - Funktion mit dem Definitionsbereich $D_f = \{n \in \mathbb{N} \text{ | } n > 0\}$
> - Bezeichnung $\left( a_n \right)$
> - Funktionswerte: $a_n \rightarrow$ Glieder der Zahlenfolge
> - Argumente: $n$ Nummer des Folgenglieds

**Beispiel:** Folge der ungeraden Zahlen

Angabe der Folge durch Aufzählung: 
$\left( a_n \right) = \left( 1, 3, 5, 7, ... \right)$

Explizite Bildungsvorschrift: 
Funktionsterm: $\left( a_n \right) = 2n-1 \qquad n \in \mathbb{N}, n>0$

Rekursive Bildungsvorschrift:
Anfangsglied: $a_1 = 1$
Rekursionsgleichung: $a_{n+1} = a_n + 2$


## Berechnung von rekursiven Zahlenfogen durch Iteration und Rekursion

### Beispiel: Folge der ungeraden Zahlen

```python
def ungerade_iteration(n):
    result = 1
    for i in range(1,n):
        result = result + 2
    return result

def ungerade_recursion(n):
    if n == 1:
        return 1
    else:
        return ungerade_recursion(n-1) + 2

print(ungerade_iteration(3))
print(ungerade_recursion(3))
```
@Pyodide.eval

### Verallgemeinerung

Gegeben ist eine Zahlenfolge in rekursiver Bildungsvorschrift: $\left(a_n\right): a_1, a_{n+1} = f(a_n)$
durch ihr Anfangsglied und ihre Rekursionsgleichung.

**Berechnung eines Folgengliedes durch Iteration:**

```python
def zahlenfolge_iteration(n):
    result = a1 # erstes Folgenglied
    for i in range(1,n):
        result = f(result) # Reursionsgleichung
    return result
```

**Berechnung eines Folgengliedes durch Rekursion:**

```python
def zahlenfolge_recursion(n):
    if n == 1:
        return a1 # Rückgabe des ersten Folgenglieds
    else:
        return f(ungerade_recursion(n-1)) # Rückgabe des Aufrufs des vorherigen Folgengliedes in der Rekursionsgleichung
```

## Vor und Nachteile

### Iteration - Vorteile

- Meist **speichersparender** als Rekursion
- Kein Stack Overflow durch viele Wiederholungen
- Häufig schneller, da weniger Funktionsaufrufe entstehen
- Gut geeignet für:
    - Zählen
    - Durchlaufen von Listen
    - Wiederholungen mit fester Anzahl
    - Verarbeitung großer Datenmengen
- Abbruchbedingungen sind oft leichter zu kontrollieren

### Iteration - Nachteile

- Bei verschachtelten Strukturen kann der Code unübersichtlich werden
- Manche Probleme lassen sich rekursiv deutlich einfacher formulieren
- Verschachtelte Schleifen können schwer verständlich und fehleranfällig sein
- Verwaltung von Zuständen und Zwischenwerten kann zusätzlichen Code erfordern

### Rekursion - Vorteile

- Oft **übersichtlicher und leichter verständlich** bei Problemen mit verschachtelten Strukturen
- Geeignet für:
    - Baumstrukturen
    - Graphen
    - Teile-und-herrsche-Algorithmen
    - Backtracking
- Kann mathematische Definitionen direkt abbilden
- Häufig kürzerer und eleganterer Quellcode

### Rekursion - Nachteile

- Verbraucht zusätzlichen **Speicher auf dem Aufrufstapel**
- Gefahr eines **Stack Overflow**, wenn die Rekursion zu tief wird
- Kann langsamer sein, da viele Funktionsaufrufe entstehen
- Eine fehlerhafte oder fehlende Abbruchbedingung führt zu einer **Endlosrekursion**