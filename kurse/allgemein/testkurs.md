<!-- 
version:  0.0.1
language: de
narrator: Deutsch Female
persistent: true
author:  Lutz Herrmann

edit: true

tags: Erste Schritte

comment: Dies ist ein erster Test-Kurs.

link:     https://cdn.jsdelivr.net/chartist.js/latest/chartist.min.css

script:   https://cdn.jsdelivr.net/chartist.js/latest/chartist.min.js
-->

# Testkurs

> Dies ist ein erster Testkurs, um die möglichkeiten von Liascript zu dokumentieren.

## Textformatierung

**Fett**, *kursiv*, ***fett+kursiv***

~Durchgestrichen~, ~~unterstrichen~~, ^hochgestellt^

`Inline-Code`

## Überschriften

```markdown
# H1 - Kurstitel
## H2 - Abschnitt (neue Folie)
### H3 - Unterabschnitt
#### H4 - Unter-Unterabschnitt
```

## Listen

**Ungeordnet**

- Punkt 1
- Punkt 2
  - Verschachtelter Punkt
  - Noch ein verschachtelter

**Geordnet**

1. Erster Schritt
2. Zweiter Schritt
   1. Unterschritt A
   2. Unterschritt B

**Aufgaben**

- [ ] Todo
- [x] Erledigt

## Links

[Linktext](https://liascript.github.io)

[Abschnittslink](#textformatierung)

## Blockzitate

> Einfaches Blockzitat
>
> > Verschachtelte Blockzitate
> > sind auch möglich...

> Zitat mit Quellenangabe
>
> -- Autor Name

## Mathematik

Inline: $a^2 + b^2 = c^2$

Anzeige:

$$
\int_0^1 x^2 \, dx = \frac{1}{3}
$$

Mehrzeilig:

$$
\begin{aligned}
f(x) &= x^2 + 2x + 1 \\
     &= (x + 1)^2
\end{aligned}
$$

Matrix:

$$
\begin{pmatrix}
1 & 0 \\
0 & 1
\end{pmatrix}
$$

Chemie: $\ce{H2O}$ oder $\ce{CO2 + C -> 2 CO}$

## Tabellen

| Links | Zentriert | Rechts |
| :---- | :-------: | -----: |
| A     |     B     |      C |
| D     |     E     |      F |
| H     |     I     |      J |

## Multimedia

**Bilder**

![Alt-Text](https://picsum.photos/300/200)

**Audio**

?[Audio](https://bigsoundbank.com/UPLOAD/mp3/1068.mp3)

**Video**

!?[YouTube-Video](https://www.youtube.com/watch?v=rbqm6MN0We4)

### Galerien

![Bild 1](https://picsum.photos/200/150?1) ![Bild 2](https://picsum.photos/200/150?2) ![Bild 3](https://picsum.photos/200/150?3)

### QR-Code

[qr-code](https://liascript.github.io "Scanne mich")

### oEmbed

??[SketchFab 3D-Modell](https://sketchfab.com/3d-models/phoenix-bird-844ba0cf144a413ea92c779f18912042)

## Animationen & Text-zu-Sprache

     {{0}}
Schritt 0: Erscheint zuerst

     {{1}}
Schritt 1: Erscheint als zweites

     {{2-3}}
Schritte 2-3: Sichtbar ab Schritt 2, verschwindet bei Schritt 4

     {{4}}
Schritt 4: Erscheint zuletzt

### Mit Sprachausgabe

     --{{0}}--
Dieser Text wird gesprochen, wenn Schritt 0 erscheint.

     {{0}}
Erster Inhalt

     --{{1 UK English Female}}--
This uses a different voice for step 1.

     {{1}}
Zweiter Inhalt

     --{{2 French Female}}--
Ceci est parlé en français.

     {{2}}
!?[Ein Dokument mehrere Darstellungen](https://www.youtube.com/watch?v=saxAFw7XpjI)

**Inline-Animationen:**

Immer sichtbar, aber {1}{dies erscheint in Schritt 1}, und {2}{dies in Schritt 2}.

## Styling

<!-- style="color: red; font-weight: bold;" -->
Gestaltet den gesamten Block.

Gestaltet nur Ein<!-- style="color: blue;" --> Element

## Diagramme

### ASCII 1

                                  Diagrammtitel
    1.5 |                                  PUNKTE
        |                 ***
      y |               *     *
      - |         r r r*r r r r*r r r
      a |             *         *
      x |            *           *
      i |     B B B * B B B B B B * B B B
      s |         *                 *
        | *  * *                       * *  *
   -1.0 +------------------------------------
        0            x-Achse               1


### ASCII 2

```ascii
 .---------------.
(      Start      )
 '-------+-------'
         |
         v
    +----+----+      .----------.
    | Eingabe |----->| Prozess  |
    +---------+      '-----+----'
                          /
                         /
                        /
        +--------------+---+
        |                  |
        v                  v
   +----+----+       +-----+-----+
   | Erfolg  |       |   Fehler  |
   +---------+       +-----------+
```

### Datenvisualisierung

__Liniendiagramme__

| Jahr | Verkäufe | Gewinn |
| :--: | :------: | :----: |
| 2018 |   1000   |  500   |
| 2019 |   1500   |  700   |
| 2020 |   1200   |  400   |
| 2022 |   1800   |  890   |
| 2023 |   2000   |  999   |

__Balkendiagramme__

| Tier            | Gewicht (kg) | Lebensspanne (Jahre) | Mitogen |
| --------------- | ------------:| --------------------:| -------:|
| Maus            |        0.028 |                    2 |      95 |
| Flughörnchen    |        0.085 |                   15 |      50 |
| Braune Flederm. |        0.020 |                   30 |      10 |
| Schaf           |           90 |                   12 |      95 |
| Mensch          |           68 |                   70 |      10 |

__Kreisdiagramme__

| Musikstil 1994  | Klassik | Country | Reggae | Hip-Hop | Hard Rock | Samba |
|:--------------- | -------:| -------:| ------:| -------:| ---------:| -----:|
| Studentenbewert.|      50 |      50 |    100 |     200 |       350 |   250 |

__Netzdiagramme__

| Tier            | Gewicht (kg) | Lebensspanne (Jahre) | Mitogen |
| --------------- | ------------:| --------------------:| -------:|
| Maus            |        0.028 |                    2 |      95 |
| Flughörnchen    |        0.085 |                   15 |      50 |
| Braune Flederm. |        0.020 |                   30 |      10 |

## Quiz

### Texteingabe

Was ist 2 + 2?

    [[4]]

### Multiple Choice

    [[X]] Richtig
    [[ ]] Falsch
    [[X]] Auch richtig

### Single Choice

    [(X)] Richtig
    [( )] Falsch
    [( )] Auch falsch

### Auswahl

    [[ Option A | (Option B) | Option C ]]

### Mit Hinweisen

    [[42]]
    [[?]] Erster Hinweis
    [[?]] Zweiter Hinweis

### Mit Lösung

    [[Antwort]]
****************************************

Hier steht die Erklärung der Lösung.

****************************************

### Lückentext

Fülle die [[ leeren ]] Wörter in diesem [[ Satz ]] aus.

Du kannst auch Auswahl verwenden: [[(eins)|zwei|drei]] und [[(eine andere)|Wahl]].

## Ausführbarer Code

```javascript
// Dein Code hier
let x = 5;
let y = 10;
console.log("Summe:", x + y);

x + y  // Rückgabewert
```
<script>@input</script>

### Mehrere Dateien

``` js     -script.js
let result = data.value * 2;
"Ergebnis: " + result
```
``` json    +data.json
{
  "value": 21
}
```
<script>
  let data = @input(1);
  eval(`@input(0)`);
</script>

### Diagramme mit Chartist

```javascript
new Chartist.Line('#chart1', {
  labels: [1, 2, 3, 4, 5],
  series: [[12, 9, 7, 8, 5]]
});
```
<script>@input</script>

<div class="ct-chart ct-golden-section" id="chart1"></div>

### JavaScript

Die $\sqrt{2} = $ <script>Math.pow(2, 0.5)</script>

#### Wetter-API Beispiel

Längengrad: <script default="13.33125" input="range" output="longitude">@input</script>

Breitengrad: <script default="50.92558" input="range" output="latitude">@input</script>

<script run-once="true" style="display: block">
  fetch("https://api.open-meteo.com/v1/forecast?latitude=@input(`latitude`)&longitude=@input(`longitude`)&hourly=temperature_2m")
    .then(response => response.json())
    .then(data => {
      let table = "<!-- data-show data-type='line' data-title='Open-Meteo Wetter-API' -->\n"

      table += "| Zeit | Temperatur |\n"
      table += "| ---- | ---------- |\n"

      for (let i=0; i < data.hourly.time.length; i++) {
        table += "| " + data.hourly.time[i] + " | " + data.hourly.temperature_2m[i] + " |\n"
      }
      send.lia("LIASCRIPT: "+table) }
    )
    .catch(e => {
      send.lia("ups, etwas ist schief gelaufen")
    })
  "Warte auf das Wetter"
</script>

## Umfragen

Bewerte diesen Kurs:

    [(1)] ⭐
    [(2)] ⭐⭐
    [(3)] ⭐⭐⭐
    [(4)] ⭐⭐⭐⭐
    [(5)] ⭐⭐⭐⭐⭐

Feedback:

    [[___]]

## Fußnoten

Text mit Fußnote[^1]

[^1]: Fußnoteninhalt

## Veröffentlichung

1. Auf GitHub hochladen
2. Raw-URL holen: `https://raw.githubusercontent.com/user/repo/main/README.md`
3. Teilen: `https://liascript.github.io/course/?DEINE_RAW_URL`


**Erstelle deinen Kurs von hier aus! 🚀**

