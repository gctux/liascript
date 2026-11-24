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

import: https://raw.githubusercontent.com/LiaTemplates/Pyodide/master/README.md
-->
# 2.3.2 Iteration und Rekursion - Aufgaben

Hinweis: Bei den folgenden Aufgaben muss häufig in Obsidian Mathematikcode geschrieben werden. Sie können dazu den  [Latexeditor](https://convertorium.com/de/latex-tools/equation-editor) verwenden.

## Aufgabe 1

Finden Sie aus den Anfangsstücken der folgenden Zahlenfolgen jeweils die rekursive Bildungsvorschrift! (Anfangsglied und Rekursionsgleichung)

1. $(a_n) = (3, 10, 17, 24 ...)$ <details>
<summary>Antwort anzeigen</summary>
$a_1 = 3, a_{n+1} = a_n+7$
</details>

2. $(b_n) = (11, 8, 5, 2 ...)$ <details>
<summary>Antwort anzeigen</summary>
$a_1 = 11, a_{n+1} = a_n-3$
</details> 


3. $(c_n) = (4, 12, 36, 108 ...)$ <details>
<summary>Antwort anzeigen</summary>
$a_1 = 4, a_{n+1} = a_n \cdot 3$
</details>  
 

4. $(d_n)=\left(1,\dfrac{1}{2},\dfrac{1}{4},\dfrac{1}{8}, ...\right)$  <details>
<summary>Antwort anzeigen</summary>
$a_1 = 1, a_{n+1} = \dfrac{a_n}{2}$
</details>   


5. $(e_n) = (1, 2, 6, 24, 120, ...)$ <details>
<summary>Antwort anzeigen</summary>
$a_1 = 1, a_{n+1} = a_n\cdot(n+1)$
</details> 


6. $(f_n) = (1, 1, 2, 3, 5, 8, 13, ...)$  <details>
<summary>Antwort anzeigen</summary>
 $a_1 = 1, a_2 = 1, a_{n+2} = a_{n+1} + a_n$
</details> 

## Aufgabe 2

Schreiben Sie ein Pythonprogramm in dem Sie die Zahlenfolgen 1 bis 5 aus Aufgabe jeweils als iterative und rekursive Funktion umsetzen. Das Programm soll in einer Schleife laufen, in der nach Eingabe von für jede Funktion der Funktionswert ausgerechnet wird. Bei jeden Programmdurchlauf soll abgefragt werden, ob das Programm beendet werden soll.

**Zusatzaufgabe**

Ergänzen Sie die Folge 6 in Aufgabe 2! 

[[!]]
<script>
  true;
</script>
****************************************
```python
def a_iteration(n):
    result = 3
    for i in range(1,n):
        result = result + 7
    return result

def a_recursion(n):
    if n == 1:
        return 3
    else:
        return a_recursion(n-1) + 7

def b_iteration(n):
    result = 11
    for i in range(1,n):
        result = result - 3
    return result

def b_recursion(n):
    if n == 1:
        return 11
    else:
        return b_recursion(n-1) - 3
    
def c_iteration(n):
    result = 4
    for i in range(1,n):
        result = result * 3
    return result

def c_recursion(n):
    if n == 1:
        return 4
    else:
        return c_recursion(n-1) * 3
    
def d_iteration(n):
    result = 1
    for i in range(1,n):
        result = result / 2
    return result

def d_recursion(n):
    if n == 1:
        return 1
    else:
        return d_recursion(n-1) / 2

# Fakultät
def e_iteration(n):
    result = 1
    for i in range(1,n):
        result = result * (i+1)
    return result

def e_recursion(n):
    if n == 1:
        return 1
    else:
        return e_recursion(n-1) * n

# Fibonacci-Folge
def f_iteration(n):
    result1 = 0
    result2 = 1
    for i in range(n):
        temp = result1
        result1 = result2
        result2 = temp + result2
    return result1

def f_recursion(n):
    if n == 1:
        return 1
    elif n == 2:
        return 1
    else:
        return f_recursion(n-1) + f_recursion(n-2)
    
while True:
    print("Rekursion und Iteration")
    print()
    n = int(input("n (n>0) eingeben: "))
    print("Zahlenfolge a_n (iterativ):",a_iteration(n))
    print("Zahlenfolge a_n (rekursiv):",a_recursion(n))
    print("Zahlenfolge b_n (iterativ):",b_iteration(n))
    print("Zahlenfolge b_n (rekursiv):",b_recursion(n))
    print("Zahlenfolge c_n (iterativ):",c_iteration(n))
    print("Zahlenfolge c_n (rekursiv):",c_recursion(n))
    print("Zahlenfolge d_n (iterativ):",d_iteration(n))
    print("Zahlenfolge d_n (rekursiv):",d_recursion(n))
    print("Fakultät (iterativ):",e_iteration(n))
    print("Fakultät (rekursiv):",e_recursion(n))
    print("Fibonacci (iterativ):",f_iteration(n))
    print("Fibonacci (rekursiv):",f_recursion(n))
    w = input("Programm fortsetzen? (J|N)")
    if w.lower() == "n":
        break
```
@Pyodide.eval
****************************************
