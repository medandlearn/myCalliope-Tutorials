## Schritt 1 – Ziel verstehen @showhint
In diesem Tutorial programmierst du den Calliope mini v3 so, dass er:
- die Temperatur misst,
- bei unter 20 °C ein Smiley zeigt,
- bei 20 °C oder mehr ein trauriges Gesicht.

Du nutzt außerdem eine kurze Pause, um die Anzeige zu steuern.

## Schritt 2 – Temperaturanzeige vorbereiten @showhint
Du misst die Temperatur mit dem Block ||input:temperature||  
und entscheidest mit ||logic:if then else||, welches Icon angezeigt wird.  
Alle Anweisungen kommen in einen einzigen ||basic:forever||-Block.

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

## Schritt 3 – Geschafft! 🎉 @showhint
Dein Programm zeigt jetzt je nach Temperatur ein Gesicht auf dem Display.

Probiere es aus: Lege den Calliope an einen warmen oder kühlen Ort  
und beobachte die Anzeige!

Gut gemacht! 🚀
