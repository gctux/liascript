<!-- 
version:  0.0.1
language: de
narrator: Deutsch Female
persistent: true
author:  Lutz Herrmann

edit: true

tags: GK Informatik, Programmieren in Python

comment: Aufgaben zum Thema Einstieg Objektorientierung im GK Informatik.

link:     https://cdn.jsdelivr.net/chartist.js/latest/chartist.min.css

script:   https://cdn.jsdelivr.net/chartist.js/latest/chartist.min.js

import: https://raw.githubusercontent.com/LiaTemplates/Pyodide/master/README.md
-->

# 2.4.1 Einstieg in die Objektorientierung

## Idee der objektorientierten Modellierung

> [!NOTE] Idee
> - Unsere Umwelt besteht aus **Objekten**, welche Eigenschaften (**Attribute**) haben.
> - Mit **Methoden** lassen sich die **Attribute** von **Objekten** ändern. Außerdem können **Objekte** selbst **Methoden** ausführen.
> - **Objekte** mit gleichen **Attributen** und **Methoden** kann man zu **Klassen** zusammenfassen. Ein **Objekt** bezeichnet man in der Programmierung auch als **Instanz** einer **Klasse**.

## Ein Beispiel

<div style="
    width: 100%;
    padding: 15px;
    border: 2px solid var(--text-normal);
    border-radius: 8px;
    box-sizing: border-box;"
>


    <div style="
        padding: 20px;
        margin-bottom: 15px;
        border: 2px solid var(--text-muted);
        border-radius: 6px;
        text-align: center;
        background-color: var(--background-secondary);
    ">

        <h2 style="margin: 0;">Klasse Fahrzeug</h2>

    </div>

    <!-- Zwei nebeneinanderliegende Boxen -->
    <div style="
        display: flex;
        gap: 15px;
    ">

        <!-- Linke Box -->
        <div style="
            flex: 1;
            min-width: 0;
            min-height: 200px;
            padding: 15px;
            border: 2px solid var(--text-muted);
            border-radius: 6px;
            background-color: var(--background-secondary);
            box-sizing: border-box;
        ">

            <h3>Objekt: Bumblebee (Chevrolet Camaro)</h3>

            <img src="https://www.conceptcarz.com/images/Chevrolet/Chevy-Camaro-Bumblebee-Coupe-Image-001-1280.jpg">

	            <ul>
		            <li>Gewicht: 1,7 Tonnen</li>
			        <li>Leisung: 430 PS</li>
			         <li>Farbe: gelb-schwarz</li>
			         <li>Geschwindigkeit: 318 km/h</li>
	            </ul>
            

        </div>

        <!-- Rechte Box -->
        <div style="
            flex: 1;
            min-width: 0;
            min-height: 200px;
            padding: 15px;
            border: 2px solid var(--text-muted);
            border-radius: 6px;
            background-color: var(--background-secondary-alt);
            box-sizing: border-box;
        ">

            <h3>Objekt: Optimus Prime (Peterbilt 379 Semi Truck)</h3>

            <img src="https://i.pinimg.com/originals/f0/bb/16/f0bb16e4b794c2f21ae05613b454d305.jpg">

	            <ul>
		            <li>Gewicht: 9,1 Tonnen</li>
			        <li>Leisung: 565 PS</li>
			         <li>Farbe: orange-blau</li>
			         <li>Geschwindigkeit: 85 km/h</li>
	            </ul>

            

        </div>

    </div>

</div>



## Darstellung von Objekten und Klassen - UML


![](./images/uml.svg)

## Weitere Fachbegriffe

- Objekte besitzen einen Namen bzw. eine Bezeichnung.
- Methoden können **Parameter** haben, mit denen zusätzliche Informationen übergeben werden.
- Manche Methoden können Informationen über ein Objekt durch einen **Rückgabewert** (**Ergebnis**) zurückliefern.
- Parameter und Rückgabewert haben einen bestimmten **Datentyp**. Der Typ bestimmt die Art der Werte die angenommen werden können. (z.B. Kommazahl, ganze Zahl, Text, Wahrheitswert)
- Objekte (Instanzen einer Klasse) haben einen **Zustand**, der durch die Werte der Attribute (**Attributwerte**) bestimmt wird.
- Objekte können miteinander kommunizieren, indem sie gegenseitig ihre Methoden aufrufen.
