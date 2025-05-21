## Schritt 3 – Temperaturhöhe visualisieren @showhint

Jetzt baust du eine Entscheidung ein:  
Wenn die Temperatur unter 20 °C liegt, wird ein Smiley angezeigt, sonst ein trauriges Gesicht.

Benutze dafür ``||logic:if then else||`` aus der Kategorie ``||logic:||`` und ``||basic:show icon||`` aus ``||basic:||``.  
Achte darauf, diesen Block dauerhaft auszuführen!

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
