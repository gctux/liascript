<!-- 
version:  0.0.1
language: de
narrator: Deutsch Female
persistent: true
author:  Lutz Herrmann

edit: true

tags: GK Informatik, Technische Informatik

comment: Aufgaben zum Thema Boolsche Algebra im GK Informatik.

link:     https://cdn.jsdelivr.net/chartist.js/latest/chartist.min.css

script:   https://cdn.jsdelivr.net/chartist.js/latest/chartist.min.js


-->


# 1.1.4 Boolsche Algebra - Aufgaben

Auf dieser Seite finden Sie Aufgaben zum Thema Boolsche Algebra für den Informatik GK Klasse 11 - Sachsen mit interaktiver Lösungseingabe bzw. Anzeigemöglichkeit der Lösung.



## Aufgabe 1

Entscheiden Sie, ob die folgenden sprachlichen Gebilde Aussagen sind. Entscheiden Sie bei den Aussagen, ob diese wahr oder oder falsch sind.

- a) Es gibt eine durch 2 teilbare Primzahl.

<details>
<summary>Antwort anzeigen</summary>
wahre Aussage
</details>


- b) Die Zahl n ist durch 11 teilbar. 

<details>
<summary>Antwort anzeigen</summary>
keine Aussage (Aussageform)
</details>

- c) Alle Vögel können fliegen. 

<details>
<summary>Antwort anzeigen</summary>
falsche Aussage
</details>

- d) Braune Schuhe sind wärmer als im Winter. 

<details>
<summary>Antwort anzeigen</summary>
keine Aussage 
</details>


- e) 3 + 3 = 33 

<details>
<summary>Antwort anzeigen</summary>
falsche Aussage
</details>

- f) Es gibt keine von Null verschiedenen ganze Zahlen $a$, $b$ und $c$ , die die Gleichung $$a^n + b^n = c^n \text{ mit } n \in \mathbb{N} \text{ und } n>2 $$ erfüllen. 

<details>
<summary>Antwort anzeigen</summary>
wahre Aussage (Satz des Fermat)
</details>

## Aufgabe 2

Gegeben sind die folgenden Aussagen $A$  und $B$:

$A$: Ich gehe zur Schule.
$B$: Die Sonne scheint.

Formulieren Sie die folgenden Verknüpfungen von Aussagefunktionen in Worten:
- a) $\overline{A} \vee B$ 

<details>
<summary>Antwort anzeigen</summary>
Ich gehe nicht zur Schule oder die Sonne scheint.
</details>

- b) $A \wedge \overline{B}$ 

<details>
<summary>Antwort anzeigen</summary>
Ich gehe zur Schule und die Sonne scheint nicht.
</details>

- c) $\overline{A \vee B} \wedge A$ 

<details>
<summary>Antwort anzeigen</summary>
Es stimmt nicht, dass ich zur Schule gehe oder  die Sonne scheint, und ich gehe zur Schule. 
</summary>

- d) $\overline{A \wedge B}$ 

<details>
<summary>Antwort anzeigen</summary>
Es stimmt nicht, dass ich zur Schule gehe und dass die Sonne scheint.
</details>


## Aufgabe 3

Erstellen Sie für die folgenden logischen Ausdrücke die Wahrheitstabelle!

- a) $(A \vee B) \wedge \overline{A \wedge B}$

[[!]]
<script>
  true;
</script>
****************************************

| $A$ | $B$ | $A \vee B$ | $\overline{A \wedge B}$ | $(A \vee B) \wedge \overline{A \vee B}$ |
| --- | --- | ---------- | ----------------------- | --------------------------------------- |
| 0   | 0   | 0          | 1                       | 0                                       |
| 0   | 1   | 1          | 1                       | 1                                       |
| 1   | 0   | 1          | 1                       | 1                                       |
| 1   | 1   | 1          | 0                       | 0                                       |

****************************************


- b) $(A \wedge B)\vee \overline C$

| $A$ | $B$ | $C$ | $A \wedge B$ | $\overline C$ | $(A \wedge B)\vee \overline C$ |
| --- | --- | --- | ------------ | ------------- | ------------------------------ |
| 0   | 0   | 0   | 0            | 1             | 1                              |
| 0   | 0   | 1   | 0            | 0             | 0                              |
| 0   | 1   | 0   | 0            | 1             | 1                              |
| 0   | 1   | 1   | 0            | 0             | 0                              |
| 1   | 0   | 0   | 0            | 1             | 1                              |
| 1   | 0   | 1   | 0            | 0             | 0                              |
| 1   | 1   | 0   | 1            | 1             | 1                              |
| 1   | 1   | 1   | 1            | 0             | 1                              |

- c) $(A \wedge B) \vee \overline{A \wedge B}$

| $A$ | $B$ | $A \wedge B$ | $\overline{A \wedge B}$ | $(A \wedge B) \vee \overline{A \wedge B}$ |
| --- | --- | ------------ | ----------------------- | ----------------------------------------- |
| 0   | 0   | 0            | 1                       | 1                                         |
| 0   | 1   | 0            | 1                       | 1                                         |
| 1   | 0   | 0            | 1                       | 1                                         |
| 1   | 1   | 1            | 0                       | 1                                         |
Die Verknüpfung c) ergibt für alle Kombinationen der Wahrheitswerte von A und B eine wahre Aussage. Man nennt sie deshalb auch **Tautologie**.

> Eine **Tautologie** ist eine Aussagenverbindung, die unabhängig von den Wahrheitswerten ihrer Teilaussagen immer wahr ist.

**Aufgabe 4**

Erstellen Sie aus den folgenden Wahrheitstabellen die disjunktive Normalform!

a) 

| $A$ | $B$ | $X$ |
| --- | --- | --- |
| 0   | 0   | 0   |
| 0   | 1   | 1   |
| 1   | 0   | 1   |
| 1   | 1   | 0   |
**Lösung:** $X = (\overline A \wedge B) \vee (A \wedge \overline B)$ 

> Diese Verknüpfung nennt man auch **Antivalenz (XOR)**. Sie wird mit $A \nsim B$ oder $A \nleftrightarrow B$ abgekürzt.

b) 

| $A$ | $B$ | $X$ |
| --- | --- | --- |
| 0   | 0   | 1   |
| 0   | 1   | 0   |
| 1   | 0   | 0   |
| 1   | 1   | 1   |
**Lösung:** $X= (\overline A \wedge \overline B) \vee (A \wedge B)$ 

> Diese Verknüpfung nennt man auch **Äquivalenz (XNOR)**. Sie wird mit $A \sim B$ oder $A \leftrightarrow B$ abgekürzt.


**Aufgabe 4**

Weisen Sie die folgenden Tautologien nach! Benutzen Sie dazu die Wahrheitstabelle der Äquivalenz

a)  $\overline{A \wedge B} \leftrightarrow \bar{A} \vee \bar{B}$

| $A$ | $B$ | $\bar{A}$ | $\bar{B}$ | $\overline{A \wedge B}$ | $\bar{A} \vee \bar{B}$ | $\overline{A \wedge B} \leftrightarrow \bar{A} \vee \bar{B}$ |
| --- | --- | --------- | --------- | ----------------------- | ---------------------- | ------------------------------------------------------------ |
| 0   | 0   | 1         | 1         | 1                       | 1                      | 1                                                            |
| 0   | 1   | 1         | 0         | 1                       | 1                      | 1                                                            |
| 1   | 0   | 0         | 1         | 1                       | 1                      | 1                                                            |
| 1   | 1   | 0         | 0         | 0                       | 0                      | 1                                                            |


b) $\overline{A \vee B} \leftrightarrow \bar{A} \wedge \bar{B}$


| $A$ | $B$ | $\bar{A}$ | $\bar{B}$ | $\overline{A \vee B}$ | $\bar{A} \wedge \bar{B}$ | $\overline{A \vee B} \leftrightarrow \bar{A} \wedge \bar{B}$ |
| --- | --- | --------- | --------- | --------------------- | ------------------------ | ------------------------------------------------------------ |
| 0   | 0   | 1         | 1         | 1                     | 1                        | 1                                                            |
| 0   | 1   | 1         | 0         | 0                     | 0                        | 1                                                            |
| 1   | 0   | 0         | 1         | 0                     | 0                        | 1                                                            |
| 1   | 1   | 0         | 0         | 0                     | 0                        | 1                                                            |


Die Tautologien in a) und b) nennt man auch de **Morgansche Regeln**.