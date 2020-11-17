# Der Rentierschlitten des Weihnachtsmanns

## ~avatar avatar @unplugged
Bringe die Rentiere in Bewegung und lass sie den Schlitten des Weihnachtsmanns ziehen


## Schritt 1 Ein Rentier anzeigen lassen
Beginne in dem du die ``||variables: Variable||`` ``||variables: Rentier||`` erstellst. <br>
Schiebe nun den Block ``||variables: setze Variable auf ||`` in den Block  ``||basic: beim Start||``. <br>

Auf diese Variable soll nun das Bild den Rentiers gespeichert werden.
Suche dazu im fortgeschrittenen Bereich der Befehlsgruppen die Blöcke für ``||images: Bilder||``. <br>
Nutze hier den Block ``||images: ertelle Bild||``. Schiebe dieses in den Block ``||variables: setze Variable auf ||``.<br>
Jetzt kannst du in den Block ``||images: ertelle Bild||`` dein Rentier zeichnen. <br>
Um diesen testweise im Simulator anzeigen zu lassen kannst den Block ``||images: zeige Bild||`` ebenfalls in den Block   ``||basic: beim Start||`` schieben. <br>
Hier musst du nurnoch die voreingerstellte ``||variables: Variable||`` mit deiner Variable ``||variables: Rentier||`` ersetzen.

```blocks
let Rentier = images.createImage(`
    # . # . .
    . # . . .
    # # . # .
    . # # # .
    . # . # .
    `)
Rentier.showImage(0)
```

## Schritt 2 Das Rentier springen lassen.
Um die Bewegung des Rentiers zu Simulieren benötigen wir noch ein weiteres Bild um zwischen diesen beiden zu wechseln
Speichere dazu auf einer weiteren Variable noch ein Bild vom Rentier wie es springt. <br>

```blocks
let RentierSprung = images.createImage(`
    # . # . .
    . # . . .
    # # . # .
    . # # . .
    # . . # .
    `)
```
## Schritt 3 Das Rentier springen lassen.
Um das Rentier nun wirklich zu bewegen, müssen dur die beiden Bilder abwechselnd aufgerufen werden.

```blocks
basic.forever(function () {
    Rentier.showImage(0)
    RentierSprung.showImage(0)
})

let RentierSprung = images.createImage(`
    # . # . .
    . # . . .
    # # . # .
    . # # . .
    # . . # .
    `)
    let Rentier = images.createImage(`
    # . # . .
    . # . . .
    # # . # .
    . # # # .
    . # . # .
    `)
```

## Schritt 4 Das Rentier springen lassen.
Um das Rentier über den Bildschrirm laufen zu lassen kannst du nun die beiden Blöcke ``||images: zeige Bild||`` in eine ``||loops: Index-Schleife||`` schieben und dabei den Index von 0 bis 4 laufen lasen. <br> 
Diesen ``||variables: Index ||`` findest du jetzt auch unter ``||variables: Variablen||`` und kannst ihn jeweils in die Blöcke ``||images: zeige Bild||`` als Versatz verwenden. <br>
Jetzt läuft das Rentier von rechts nach links wenn du möchtest kannst du mit den Blöcken aus der ``||math: Mathematik||`` noch einen sogenannten offset erstellen, damit das Rentier über den ganzen Bilschritm läuft. <br>
Dann solltest du aber auch den Index deiner Schleife erhöhen.

```blocks
basic.forever(function () {
    for (let Index = 0; Index <= 6; Index++) {
        Rentier.showImage(Index - 4)
        RentierSprung.showImage(Index - 4)
    }
})
let RentierSprung = images.createImage(`
    # . # . .
    . # . . .
    # # . # .
    . # # . .
    # . . # .
    `)
    let Rentier = images.createImage(`
    # . # . .
    . # . . .
    # # . # .
    . # # # .
    . # . # .
    `)

```


## Schritt 5 Einen Schlitten ziehen lassen
Erstelle hierzu einfach ein Bild von einem Schlitten diesen kannst du entweder wieder auf eine Variable speichern oder direkt im Block ``||images: scrolle Bild||``. <br>
Den Block ``||images: scrolle Bild||`` kannst du einfach unter deine ``||loops: Index-Schleife||`` schieben. <br>
Ps. wenn du Im Block ``||images: scrolle Bild||`` die Zeit auf 300ms stellst haben Rentier und Schlitten ungefähr die gleiche Geschwindigkeit.


```blocks
basic.forever(function () {
    for (let Index = 0; Index <= 5; Index++) {
        Rentier.showImage(Index - 4)
        RentierSprung.showImage(Index - 4)
    }
    Schlitten.scrollImage(1, 300)
})

let RentierSprung = images.createImage(`
    # . # . .
    . # . . .
    # # . # .
    . # # . .
    # . . # .
    `)
    let Rentier = images.createImage(`
    # . # . .
    . # . . .
    # # . # .
    . # # # .
    . # . # .
    `)
let Schlitten = images.createImage(`
    . . . . .
    . . . . .
    . . # # #
    # . # . #
    # # # # #
    `)

```

## ~ @unplugged
Ich hoffe du hattest Spaß mit diesem Tutorial um es weiter zu schicken nutze gerne diesen Link: 


> Diese Seite bei [https://r00b1nh00d.github.io/rentier_zieht_schlitten/](https://r00b1nh00d.github.io/rentier_zieht_schlitten/) öffnen

## Als Erweiterung verwenden

Dieses Repository kann als **Erweiterung** in MakeCode hinzugefügt werden.

* öffne [https://makecode.calliope.cc/](https://makecode.calliope.cc/)
* klicke auf **Neues Projekt**
* klicke auf **Erweiterungen** unter dem Zahnrad-Menü
* nach **https://github.com/r00b1nh00d/rentier_zieht_schlitten** suchen und importieren

## Dieses Projekt bearbeiten ![Build Status Abzeichen](https://github.com/r00b1nh00d/rentier_zieht_schlitten/workflows/MakeCode/badge.svg)

Um dieses Repository in MakeCode zu bearbeiten.

* öffne [https://makecode.calliope.cc/](https://makecode.calliope.cc/)
* klicke auf **Importieren** und dann auf **Importiere URL**
* füge **https://github.com/r00b1nh00d/rentier_zieht_schlitten** ein und klicke auf Importieren

## Blockvorschau

Dieses Bild zeigt den Blockcode vom letzten Commit im Master an.
Die Aktualisierung dieses Bildes kann einige Minuten dauern.

![Eine gerenderte Ansicht der Blöcke](https://github.com/r00b1nh00d/rentier_zieht_schlitten/raw/master/.github/makecode/blocks.png)

#### Metadaten (verwendet für Suche, Rendering)

* for PXT/calliopemini
<script src="https://makecode.com/gh-pages-embed.js"></script><script>makeCodeRender("{{ site.makecode.home_url }}", "{{ site.github.owner_name }}/{{ site.github.repository_name }}");</script>
