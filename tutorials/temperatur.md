# Schritt-für-Schritt-Anleitung - Temperatur messen und reagieren

  

## Schritt 1 - Was ist das Ziel?

  

Dieses Tutorial hilft dir dabei, ein erstes kleines Demo-Programm für den Calliope v3 zu erstellen. 
Ist dein Programm fertig, so zeigt es dir einen Smiley an, wenn die Temperatur maximal 20° ist 
und ein trauriges Gesicht, falls die Temperatur höher ist. Die Anzeige wird im 5x5 LED-Feld dargestellt.

  

## Schritt 2 - Zeige die Temperatur @showhint

Click on the ``||basic:Basis||`` category in the Toolbox.  

Hol dir einen ``||input:temperature||``-Block und baue ihn in das W
ertefeld von ``||basic:show number||``.

  

```blocks

forever(function() {
    basic.showNumber(input.temperature())
    basic.pause(1000)
})
```

