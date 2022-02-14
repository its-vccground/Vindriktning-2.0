# Vindriktning-2.0
User Friendly Firmware for Converting Ikea Vindriktning Partical Sensor into a Multi Sensor to be used as Standalone or integrate with Home Assistant.
This Tasmota binary file is the upgraded version of the earlier Vindriktning firmware customised & shared by me a month ago, which was customized especially to be used with an Ikea Vindriktning Air Particle Sensor. You can flash a Wemos D1 mini or a similar esp8266 board and connect it to Vindriktning Sensor to transform it into a connected smart multi sensor unit. For deep details & connections diagram, watch my earlier video numbers 34 & 35 on "vccground" Youtube channel.

What's new in this updated VINDRIKTNING-2.0 binary file ?

Apart from basic Tasmota, The following functions are enabled in this bin file...

    Pre configured bin file for Vindriktning & other Sensors.
    Support for VINDRIKTNING PARTICLE SENSOR PM1, PM2.5 & PM10 readings.
    Support for BMP085/BMP180/BMP280/BME280/BME680 and similar I2C sensors.
    Support for AHT10/15 I2C humidity and temperature sensor
    Support for Expressions and IF statements in Tasmota Rules.
    All features are fully User customisable without any coding knowledge.
   
How to use ?

    Download Zip file by clicking the green code button above.
    Follow the connections diagram to connect the wemos board to Vindriktning sensor (watch video 34 for details).
    Flash Wemos D1 mini with the provided Vindriktning-2.0 bin file.
    Configure the module as explained in the video number 34 and you are good to go.
    
User Configuration Settings:
    
    The default LED indication for PM2.5 Air Quality is the same as set by Ikea.
    GREEN: 0-35 : Good
    AMBER: 36-85: OK
    RED: 86 and above : Not Good
    PULSING: Start-up mode.
    
    VINDRIKTNING-2.0 firmware is preconfigured to use the same values by default, but all these setttings are 100% user customisable via Tasmota Console.
    To make the configuration easy, I have used seven memory variables (MEM1....MEM7) and five "event" commands (watch video 37 for details). 
    
    Memory Variables:
    MEM1 : Stores PM2.5 lower threshold value. Default is 35. e.g.Command Syntex: MEM1 45
    MEM2 : Stores PM2.5 upper threshold value. Default is 85. e.g.Command Syntex: MEM2 120
    MEM3 : Stores PM2.5 variation differential value. Default is 5. e.g.Command Syntex: MEM3 10
    MEM4 : Stores LUX lower threshold value. Default is 5. e.g.Command Syntex: MEM4 6
    MEM5 : Stores LUX upper threshold value. Default is 10. e.g.Command Syntex: MEM5 15
    MEM6 : Stores PM2.5 offset value for Home Assistant. Default is 0. e.g.Command Syntex: MEM6 45 or MEM6 -20
    MEM7 : Stores AutoMode control value for controlling LED panel. Default is 1. e.g.Command Syntex: MEM7 0 or MEM7 1 
    
    Event ShowCurrent : Show currently configured memory variable values
    Event BackupMySettings : Backup currently configured memory variable values
    Event ShowBackup : Show variable values currently stored in backup
    Event RestoreMySettings : Restore memory variable values from backup
    Event RestoreDefaults : Restore all values to default
    
Full details on why and how to use these settings, are explained in video number 37 on "vccground" YouTube Channel.

Join "vccground" telegram channel to ask any query thereafter.
