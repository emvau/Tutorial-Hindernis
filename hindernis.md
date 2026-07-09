# Hindernisvermeidung @tutorial

## Schritt 1 @fullscreen

In diesem Tutorial programmieren wir den Maqueen Plus V2 so,
dass er automatisch vor Hindernissen stoppt! 🤖

Zuerst initialisieren wir den Roboter.

Füge den Block **I2C Init** aus der Kategorie **Maqueen Plus V2** ein.

```blocks
maqueenPlusV2.I2CInit()
```

## Schritt 2

Jetzt brauchen wir eine Variable für den Abstand.

Erstelle eine neue Variable und nenne sie **abstand**.

## Schritt 3

Füge eine **dauerhaft**-Schleife ein.

Darin messen wir den Abstand mit dem Ultraschallsensor:

```blocks
basic.forever(function () {
    abstand = maqueenPlusV2.readUltrasonic(DigitalPin.P13, DigitalPin.P14)
})
```

## Schritt 4

Jetzt prüfen wir ob ein Hindernis nah ist.

Füge eine **wenn/dann/sonst**-Bedingung ein:

- Wenn der Abstand **kleiner als 5** ist **und nicht 0** → **Stopp!**
- Sonst → **Vorwärts fahren** mit Geschwindigkeit **50**

```blocks
basic.forever(function () {
    abstand = maqueenPlusV2.readUltrasonic(DigitalPin.P13, DigitalPin.P14)
    if (abstand < 5 && abstand != 0) {
        maqueenPlusV2.controlMotorStop(maqueenPlusV2.MyEnumMotor.AllMotor)
    } else {
        maqueenPlusV2.controlMotor(maqueenPlusV2.MyEnumMotor.AllMotor, maqueenPlusV2.MyEnumDir.Forward, 50)
    }
})
```

## Schritt 5 @fullscreen

Fertig! 🎉

Lade das Programm auf deinen Maqueen und teste es!

💡 **Aufgaben zum Ausprobieren:**
- Ändere den Abstand von **5cm** auf **10cm** – was passiert?
- Ändere die Geschwindigkeit von **50** auf **100** – was passiert?
- Kannst du den Roboter statt stoppen **rückwärts fahren** lassen? 🤔
