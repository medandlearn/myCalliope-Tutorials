## Schritt 2 – Temperatur anzeigen @showhint
Zieh in den Block "Beim Start" den Anzeigeblock für Zahlen: Dann nutze den Block ``||basic:show number||`` (zeige Zahl), um eine Zahl im 5×5 LED-Displayanzeigen zu können.
Click on the ``||input:||`` Eingabe-Kategorie und ziehe den  ``||input:temperature||`` Temperatur-Block in das Anzeigefeld (oval).
. Damit die Anzeige eine Zeit sichtbar bleibt, kannst du eine Pause einfügen. 
``||basic: pause||`` - und trage die Pausenzeit in Millisekunden ein. 

```blocks
basic.forever(function () {
    basic.showNumber(input.temperature())
    basic.pause(1000)
})
```

