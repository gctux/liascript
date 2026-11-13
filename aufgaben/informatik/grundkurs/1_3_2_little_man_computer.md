<!-- 
version:  0.0.1
language: de
narrator: Deutsch Female
persistent: true
author:  Lutz Herrmann

edit: true

tags: GK Informatik, Technische Informatik

comment: Aufgaben zum Thema Little Man Computer im GK Informatik.

link:     https://cdn.jsdelivr.net/chartist.js/latest/chartist.min.css

script:   https://cdn.jsdelivr.net/chartist.js/latest/chartist.min.js


-->


# 1.3.2 Little Man Computer - Aufgaben

Auf dieser Seite finden Sie Aufgaben zum Thema Little Man Computer für den Informatik GK Klasse 11 - Sachsen mit interaktiver Lösungseingabe bzw. Anzeigemöglichkeit der Lösung.



## Aufgabe 1

Lesen Sie die [Wikipediaseite](https://de.wikipedia.org/wiki/Little_Man_Computer) zum Little Man Computer durch! Notieren Sie kurz, was man unter Assemblersprache bzw. Mnemonikcode versteht.

[[!]]
<script>
  true;
</script>
****************************************
[Assemblersprache](https://de.wikipedia.org/wiki/Assemblersprache "Assemblersprache") ist eine Low-Level-Programmiersprache, die Mnemonikcodes und Beschriftungen anstelle numerischer Befehlscodes verwendet. Obwohl die LMC nur einen begrenzten Satz an Mnemonikcodes verwendet, wird die Bequemlichkeit der Verwendung eines [Mnemonikcodes](https://de.wikipedia.org/wiki/Assemblersprache "Assemblersprache") für jede Anweisung durch die unten gezeigte Assemblersprache desselben Programms deutlich – der Programmierer muss sich nicht länger einen Satz numerische Codes merken, sondern kann jetzt mit einer Reihe einprägsamerer mnemonischer Codes arbeiten. Wenn es sich bei der Mnemonik um eine Anweisung handelt, die eine Speicheradresse beinhaltet („entweder eine Verzweigungsanweisung oder das Laden/Speichern von Daten“), wird eine Bezeichnung zur Benennung der Speicheradresse verwendet.
****************************************

## Aufgabe 2

Testen Sie im [Simulator](https://oinf.ch/interactive/little-man-computer/) das Programmbeispiel 2:

```
00 902
01 407
03 600
04 
05 
06
07
08
```

Beschreiben Sie den Programmablauf!

[[!]]
<script>
  true;
</script>
****************************************
1. 902: Das Akkumulatorregister wird ausgegeben!
2. 407: Zum Akkumularoregister wird 7 addiert! 
3. 600: Springe zur Speicherzelle 0!
****************************************

## Aufgabe 3

Analysieren Sie das folgende Programm für den Little Man Computer und beschreiben Sie, was es macht!

```
00  901   
01  330   
02  901   
03  331   
04  530   
05  231   
06  809   
07  531   
08  610
09  530   
10  902   
11  0      

30  000   
31  000   
```

[[!]]
<script>
  true;
</script>
****************************************
Lösung:

```
00  901   //Erste Zahl in Akkumulator
01  330   //Zahl an Adresse 30 speichern
02  901   //Zweite Zahl in Akkumulator
03  331   //Zahl an Adresse 31 speichern
04  530   //Zahl aus Speicherzelle 30 in Akkumulator
05  231   //Zahl von Zelle 31 vom Akkumulator subtrahieren
06  809   //Springe zu Zelle 09, wenn Akkumulator größer gleich 0
07  531   //(wenn Zahl kleiner 0) Lade Zahl von Adresse 31 in Akkumulator
08  610   //Springe zur Adresse 10
09  530   //Lade Zahl von Adresse 31 in Akkumulator
10  902   //Gib den Akkumulator aus
11  0     //Halt

30  0     //Speicherzelle für erste Zahl
31  0     //Speicherzelle für zweite Zahl
```

Es werden zwei Zahlen eingelesen und die größere der beiden Zahlen wird ausgegeben, bei Gleichheit wird eine der Zahlen ausgegeben.
****************************************




## Aufgabe 4

Schreiben Sie ein Programm, welches zwei Zahlen, die in den Speicherzellen 20 und 21 stehen, multipliziert und das Ergebnis in der Speicherzelle 22 abspeichert.

[[!]]
<script>
  true;
</script>
****************************************
```
00  520   
01  223   
02  320   
03  522   
04  121   
05  322   
06  520   
07  223   
08  320
09  803   
10  000       

20 zahl1
21 zahl2
0
1
```
****************************************