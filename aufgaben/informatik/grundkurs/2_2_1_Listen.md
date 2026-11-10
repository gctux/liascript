<!-- 
version:  0.0.1
language: de
narrator: Deutsch Female
persistent: true
author:  Lutz Herrmann

edit: true

tags: GK Informatik, Technische Informatik

comment: Aufgaben zum Thema Listen im GK Informatik.

link:     https://cdn.jsdelivr.net/chartist.js/latest/chartist.min.css

script:   https://cdn.jsdelivr.net/chartist.js/latest/chartist.min.js


-->

# 2.1.1 Aufgaben zu Listen in Python

Auf dieser Seite finden Sie Aufgaben zum Thema Listen in Python für den Informatik GK Klasse 11 - Sachsen mit interaktiver Lösungseingabe bzw. Anzeigemöglichkeit der Lösung.


## Aufgabe 1

Informieren Sie sich unter https://de.w3docs.com/learn-python/python-lists über weitere Python-Listenfunktionen. Notieren Sie einige!


## Aufgabe 2

Welche Ausgabe erfolgt jeweils bei den einzelnen **print**-Anweisungen? Überprüfe jeweils in einer Pythonshell!

```python
>>> liste = [2, 7, 15, 28, 45, 12, 17, 33]
>>> print(liste)
[2, 7, 15, 28, 45, 12, 17, 33]
>>> print(liste[5])

>>> print(liste[3:7])

>>> print(liste[:5])

>>> print(liste[3:])
```

## Aufgabe 3

Welche Ausgabe erfolgt jeweils bei den einzelnen **print**-Anweisungen? Überprüfe jeweils in einer Pythonshell!

```python
>>> liste=[[2,1,4,5],[3,2,1,8]]
>>> print(liste[1])
[3, 2, 1, 8]
>>> print(liste[0][3])

>>> print(liste[1][:2])
```

## Aufgabe 4

Welche Ausgabe erfolgt jeweils bei den einzelnen **print**-Anweisungen? Beachte, dass sich die Liste nach bestimmten Anweisungen ändert. Überprüfe jeweils in einer Pythonshell!

```python
>>> liste=[12,15,21,13,17,9,6,14]
>>> liste[4]=88
>>> print(liste)

>>> liste.append(16)
>>> print(liste)

>>> del(liste[3])
>>> print(liste)

>>> del(liste[5:])
>>> print(liste)
```

## Aufgabe 5

Schreiben Sie das folgende Pythonprogramm:

Importieren Sie das Paket random (import random). Erstellen anschließend ein Array mit 5 Adjektiven und ein zweites Array mit 5 Nomen. Erzeugen Sie  nun drei Zufallszahl. Die beiden ersten Zufallszahlen sollen mit random.randint(0,4) über den Index ein Adjektiv bzw. Nomen aus den beiden Arrays auswählen. Die dritte Zufallszahl wählt eine Zahle zwischen 1-100. Geben Sie das Erstellte zufällige Passwort als Kombination von Adjektiv, Nomen und Zahl aus.

Kleiden Sie den Algorithmus in eine Endlosschleife ein, der bei jedem Durchlauf fragt, ob ein weiteres Passwort erzeugt werden soll!

## Aufgabe 6

An seinem 75. Geburtstag entschied ein König, dass er einige seiner Gefangenen begnadigen wollte. Er hatte einen Kerker mit 1000 Zellen. In jeder Zelle saß genau ein Gefangener. Er gab seinem Diener die Anweisung, 1000mal durch den Kerker zu gehen. Beim ersten Durchgang sollte er den Schlüssel in jedem Schloss umdrehen, beim zweiten Durchgang in jedem zweiten Schloss, ..., beim n. Durchgang in jedem n. Schloss. Die Schlösser schließen immer abwechselnd auf und zu. Am Anfang waren alle Schlösser geschlossen. Nach dem 1000. Durchgang sollten sich die Wachen aus dem Kerker begeben, damit alle Gefangenen, deren Tür dann offen war, fliehen konnten.  
Bestimme mit Hilfe eines Programms und der Verwendung von Listen, wie viele Gefangene auf diese Weise die Freiheit zurück erlangen konnten!


Quelle: https://www.logisch-gedacht.de/matheraetsel/kerker/
