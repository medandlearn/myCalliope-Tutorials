## Schritt 1 – Was ist das Ziel? @showhint
In diesem Tutorial programmierst du den Calliope mini v3 so, dass er:
- die Temperatur misst,
- bei unter 20 °C einen Smiley anzeigt und alle 3 LEDs grün leuchten lässt,
- bei unter 25 °C ein neutrales Gesicht und orange LEDs zeigt,
- bei 25 °C oder mehr ein trauriges Gesicht und rote LEDs anzeigt.

## Schritt 2 – Temperatur anzeigen @showhint
Öffne die Kategorie ||input:|| und hole dir den Block ||input:temperature||.  
Ziehe ihn in den Block ||basic:show number||, um die aktuelle Temperatur anzuzeigen.

```blocks
basic.forever(function () {
    basic.showNumber(input.temperature())
    basic.pause(1000)
})
```

## Schritt 3 – Gesicht anzeigen @showhint
Zeige je nach Temperatur ein Smiley oder trauriges Gesicht.  
Nutze dazu den Block ||logic:if then else|| aus ||logic:|| und ||basic:show icon||.

```blocks
basic.forever(function () {
    if (input.temperature() < 20) {
        basic.showIcon(IconNames.Happy)
    } else {
        basic.showIcon(IconNames.Sad)
    }
    basic.pause(1000)
})
```

## Schritt 4 – RGB-LEDs steuern @showhint
Jetzt steuerst du zusätzlich die Farbe der RGB-LEDs.  
Nutze ||neopixel:create strip|| und ||neopixel:show color||.

```blocks
let strip = neopixel.create(DigitalPin.P1, 3, NeoPixelMode.RGB)

basic.forever(function () {
    let temp = input.temperature()
    if (temp < 20) {
        basic.showIcon(IconNames.Happy)
        strip.showColor(neopixel.colors(NeoPixelColors.Green))
    } else if (temp < 25) {
        basic.showIcon(IconNames.Asleep)
        strip.showColor(neopixel.colors(NeoPixelColors.Orange))
    } else {
        basic.showIcon(IconNames.Sad)
        strip.showColor(neopixel.colors(NeoPixelColors.Red))
    }
    basic.pause(1000)
})
```

## Schritt 5 – Geschafft! 🎉 @showhint
Du hast dein erstes Temperatur-Ampel-Programm erfolgreich gebaut!  
Teste es mit einem kühlen Ort (z. B. Fensterbank) oder deiner Hand.  
Beobachte, wie sich die Anzeige und LED-Farbe je nach Temperatur ändern.

Super gemacht! 🚀
