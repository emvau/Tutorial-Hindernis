# Hindernisvermeidung @tutorial
##   @fullscreen
In diesem Tutorial programmieren wir den Maqueen Plus V2 so,
dass er automatisch vor Hindernissen stoppt! 🤖 
Denk daran, zuerst die Erweiterung zu installieren!
## 
Zuerst initialisieren wir den Roboter.
Füge den Block ``||MaqueenPlusV2:initialisieren Maqueen Plus V2||`` ein.
##  
Jetzt brauchen wir eine Variable für den Abstand.
Gehe zu ``||variables:Variablen||`` und erstelle eine neue Variable.
Nenne sie **abstand**.
##  
Füge eine ``||basic:dauerhaft||`` Schleife ein.
Darin messen wir den Abstand mit dem Ultraschallsensor.
Setze die Variable ``||variables:abstand||`` auf  ``||MaqueenPlusV2:abstand in cm (Pins TRIG P13/ECHO P14)``
##  
Jetzt prüfen wir ob ein Hindernis nah ist.
Füge eine ``||logic:wenn/dann/sonst||`` Bedingung ein:
- Wenn ``||variables:abstand||`` **kleiner als 5** ist ``||logic:und||`` ``||variables:abstand||`` **nicht 0** ist → füge ``||MaqueenPlusV2:stop beide Räder||`` ein
- Sonst → füge ``||MaqueenPlusV2:steuere beide Räder vorwärts Geschwindigkeit 50||`` ein

##   @fullscreen
Fertig! 🎉
Lade das Programm auf deinen Maqueen und teste es!

💡 **Aufgaben zum Ausprobieren:**
- Ändere den Abstand von **5cm** auf **10cm** – was passiert?
- Kannst du den Roboter statt stoppen **rückwärts fahren** lassen?
- Kannst du den Roboter zusätzlich eine Kurve fahren lassen? 🤔
