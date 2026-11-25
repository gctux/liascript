<!-- 
version:  0.0.1
language: de
narrator: Deutsch Female
persistent: true
author:  Lutz Herrmann

edit: true

tags: GK Informatik, Programmieren in Python

comment: Aufgaben zum Thema Listen im GK Informatik.

link:     https://cdn.jsdelivr.net/chartist.js/latest/chartist.min.css

script:   https://cdn.jsdelivr.net/chartist.js/latest/chartist.min.js

import: https://raw.githubusercontent.com/LiaTemplates/Pyodide/master/README.md
-->

# 2.2.1 Listen

**Liste:** Behälter für mehrere Werte

**Beispiele:**

```python
[1,23,7,4]
["Hallo",4,34.2,[1,2,3]]
```

## Definition einer Liste

Eine Liste kann man einfach durch den Zuweisungsoperator `=` anlegen:

**Beispiele:**

```python
liste1 = [1,23,7,4]
liste2=["Glauchau","Meerane","Waldenburg", "Mülsen", "Thurm"]
liste3=[[1,2,3],[4,5,6],[7,8,9]]
liste4=[] #leere Liste
```

## Zugriff auf die Listenelemente

```python
liste1=[1,23,21,23,12]
print(liste1)
print(liste1[2])
```
@Pyodide.eval

### Teilbereiche

**Beispiele:**

```python
liste = [2, 5, 7, 3, 11, 15]
print(liste[1:4])
print(liste[:4])
print(liste[1:])
print(liste[:])
print(liste[3:3])
```
@Pyodide.eval

###  Zugriff auf die Listenelemente bei mehrdimensionalen Listen


**Beispiele:**

Definierte Liste:

```python
liste=[[1,2,3],[4,5,6],[7,8,9]]
print(liste[1])
print(liste[1][2])
print(liste[2][1:3])
```
@Pyodide.eval

## Weitere Listenfunktionen

Wir betrachten die Liste

```python
liste=[1,23,21,23,12]
liste[1]=555
print(liste)
```
@Pyodide.eval


```python
liste=[1,23,21,23,12]
liste.append(555)
print(liste)
```
@Pyodide.eval

```python
liste=[1,23,21,23,12]
del liste1[1:3]
print(liste1)
```
@Pyodide.eval


## Verwendung der for-Anweisung auf Listen



```python
for i in range(5):
```

```python
for i in [0, 1, 2, 3, 4]:
```


```python
for wert in ["Montag", "Dienstag", "Mittwoch", "Donnerstag", "Freitag", "Samstag", "Sonntag"]:
    print(wert)
```
@Pyodide.eval

