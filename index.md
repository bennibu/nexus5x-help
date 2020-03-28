# Neue Updates für dein Nexus 5x

Mit dem Ende von LineageOS für Android Oreo (15.1 bzw 8.1) gibt es keine offiziellen Builds mehr für das Nexus 5X. 

Razorlove stellt aber weiter builds zur Verfügung. Siehe [Post auf XDA](https://forum.xda-developers.com/showpost.php?p=81981557&postcount=1687). Um nicht alle Daten beim Wechsel auf die 
inoffiziellen Builds zu verlieren, gibt es eine Migration von Razorlove, welche vor dem Einspielen 
der builds **einmalig** via adb auf das Gerät gespielt werden muss.

**Es wird außerdem empfohlen vorher ein Backup zu machen!**

## Neustes Update einspielen

1. Neustes [lineage build](https://androidfilehost.com/?w=files&flid=306263) und [Migration](https://androidfilehost.com/?fid=962187416754465877) runterladen
1. In Recovery Mode wechseln: `adb reboot recovery`
1. Auf “Advanced” -> “ADB Sideload” gehen und “Swipe to Start Sideload” wischen
1. Migration einspielen: `adb sideload lineage-migration-official-to-unofficial.zip`
1. Mit “Back” zurück gehen und erneut ADB Sideload starten
1. Neustes Lineage einspielen: `adb sideload lineage-15.1-20200310-UNOFFICIAL-bullhead.zip`
1. Telefon neu starten: `adb reboot system`


## Backup

1. `adb reboot recovery`
1. `adb backup -f nexus5x.backup --twrp system cache data boot`

### Backup wiederherstellen:

1. `adb reboot recovery`
1. `adb restore nexus5x.backup`


