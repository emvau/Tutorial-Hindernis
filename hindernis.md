# Hindernisvermeidung @tutorial

## Schritt 1 @fullscreen

In diesem Tutorial programmieren wir den Maqueen Plus V2 so,
dass er automatisch vor Hindernissen stoppt! 🤖

Zuerst initialisieren wir den Roboter.

Füge den Block ``||MaqueenPlusV2:initialisieren Maqueen Plus V2||`` ein.

## Schritt 2

Jetzt brauchen wir eine Variable für den Abstand.

Gehe zu ``||variables:Variablen||`` und erstelle eine neue Variable.
Nenne sie **abstand**.

## Schritt 3

Füge eine ``||basic:dauerhaft||`` Schleife ein.

Darin messen wir den Abstand mit dem Ultraschallsensor.
Nutze den Block ``||MaqueenPlusV2:Ultraschall lesen P13 P14||``
und speichere den Wert in ``||variables:abstand||``.

## Schritt 4

Jetzt prüfen wir ob ein Hindernis nah ist.

Füge eine ``||logic:wenn/dann/sonst||`` Bedingung ein:

- Wenn ``||variables:abstand||`` **kleiner als 5** ist ``||logic:und||`` ``||variables:abstand||`` **nicht 0** ist → füge ``||MaqueenPlusV2:alle Motoren stoppen||`` ein
- Sonst → füge ``||MaqueenPlusV2:alle Motoren vorwärts Geschwindigkeit 50||`` ein

## Schritt 5 @fullscreen

Fertig! 🎉

Lade das Programm auf deinen Maqueen und teste es!

💡 **Aufgaben zum Ausprobieren:**
- Ändere den Abstand von **5cm** auf **10cm** – was passiert?
- Ändere die Geschwindigkeit von **50** auf **100** – was passiert?
- Kannst du den Roboter statt stoppen **rückwärts fahren** lassen? 🤔
