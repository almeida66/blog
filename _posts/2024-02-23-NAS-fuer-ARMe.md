---
tags: ARM
---
Wie der Titel schon sagt: eine NAS (Network Attached Storage) und wieder mal mit ARM-Technologie. Zwei Schaechte genuegen um die Foto- und Musik-Sammlung auf HDD/SDD zu speichern. Hab wieder was recycelt, schon der Umwelt wegen. Eine Zyxel [NSA325v2](https://openwrt.org/toh/hwdata/zyxel/zyxel_nsa325) und eine QNAP TS-228.
Erstere kann OpenWrt vertragen (kirkwood), analog zum bereits beschriebenen pogoplug, die Zweite vertraegt aktuell nur QNAP-eigene Firmware, dafuer wird diese noch regelmaessig aktualisiert. Keine RAM-Monster, aber mit 1Gb geht schon was. Die LAN-Landschaft ist eh etwas inhomogen und stellenweise "nur" bis 100Mbit ausgelegt.

Egal, Thema ist die Installation mit OpenWrt. Leider sehr trikky, das neue uboot muss idealerweise mit einem FAT32 formatiertem USB-Stick geladen werden, welches natuerlich nicht erkannt wurde. Tatsaechlich duerfte die Win-Formatierung Schuld sein, da auch eine SSD nicht funktioniert hat.
Ach ja, eine serielle Anbindung muss gegeben sein, via USB-to-Serial-Adapter, also vorher das Gehaeuse wegbasteln.
Mit linux hat die FAT32 formatierte SSD dann geklappt und statt `usb reset`, wird ein `ide reset` notwendig.
