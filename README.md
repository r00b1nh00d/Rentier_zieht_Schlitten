# Der Rentierschlitten des Weihnachtsmannes

## ~avatar avatar @unplugged
Bringe dein Rentier in Bewegung und lass es den Schlitten des Weihnachtsmannes ziehen
![Rentierschlitten](https://github.com/r00b1nh00d/Rentier_zieht_Schlitten/blob/master/RentierGif.gif?raw=true)




## Schritt 1 Ein Rentier anzeigen lassen

Beginne, indem du die ``||variables: Variable||`` ``||variables: Rentier||`` erstellst. <br>
Schiebe nun den Block ``||variables: setze Variable auf ||`` in den Block  ``||basic: beim Start||``. <br>

Auf diese Variable soll nun das Bild des Rentiers gespeichert werden.
Suche dazu im fortgeschrittenen Bereich der Befehlsgruppen die Blöcke für ``||images: Bilder||``. <br>
Nutze hier den Block ``||images: erstelle Bild||`` und schiebe diesen in den Block ``||variables: setze Variable auf ||``.<br>
Jetzt kannst du in den Block ``||images: erstelle Bild||`` dein Rentier zeichnen. <br>
Um es testweise im Simulator anzeigen zu lassen, kannst du den Block ``||images: zeige Bild||`` ebenfalls in den Block   ``||basic: beim Start||`` schieben. <br>
Hier musst du nur noch die voreingestellte ``||variables: Variable||`` mit deiner Variable ``||variables: Rentier||`` ersetzen.

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
Um die Bewegung des Rentiers zu simulieren, benötigen wir noch ein weiteres Bild, um zwischen diesen beiden zu wechseln.
Speichere dazu auf einer weiteren Variable noch ein Bild vom Rentier, wie es springt. <br>

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
Um das Rentier nun wirklich zu bewegen, müssen nur die beiden Bilder abwechselnd aufgerufen werden.

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
Um das Rentier über den Bildschirm laufen zu lassen, kannst du nun die beiden Blöcke ``||images: zeige Bild||`` in eine ``||loops: Index-Schleife||`` schieben und dabei den Index von 0 bis 4 laufen lassen. <br> 
Diesen ``||variables: Index ||`` findest du jetzt auch unter ``||variables: Variablen||`` und kannst ihn jeweils in die Blöcke ``||images: zeige Bild||`` als Versatz verwenden. <br>
Jetzt läuft das Rentier von rechts nach links. Wenn du möchtest, kannst du mit den Blöcken aus der ``||math: Mathematik||`` noch einen sogenannten offset (Versatz) erstellen, damit das Rentier über den ganzen Bildschirm läuft. <br>
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
Erstelle jetzt noch ein Bild von einem Schlitten. Diesen kannst du entweder wieder auf eine Variable speichern oder direkt in den Block ``||images: scrolle Bild||`` schieben. <br>
Den Block ``||images: scrolle Bild||`` kannst du einfach unter deine ``||loops: Index-Schleife||`` schieben. <br>
Ps. Wenn du im Block ``||images: scrolle Bild||`` die Zeit auf 300ms stellst, haben Rentier und Schlitten ungefähr die gleiche Geschwindigkeit.


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
Ich hoffe, du hattest Spaß mit diesem Tutorial. Um es weiter zu schicken, nutze gerne diesen Link: [https://makecode.calliope.cc/#tutorial:https://github.com/r00b1nh00d/rentier_zieht_schlitten] 




#### Metadaten (verwendet für Suche, Rendering)

* for PXT/calliopemini
<script src="https://makecode.com/gh-pages-embed.js"></script><script>makeCodeRender("{{ site.makecode.home_url }}", "{{ site.github.owner_name }}/{{ site.github.repository_name }}");</script>
