---
tags: libreboot
---
## ChromeOS, die 2te
Es hat so ein Spass gemacht, dass ein **hp pavilion Chromebook 14** folgte, der butterfly, mit lahmeren celeron 847 mit 1.1GHz, aber voll aufruestbar. D.h. massives RAM und ganz normale SSD.

Beides hatte ich rumliegen, also wieder die bekannte Seite von <http://mrchromebox.tech> aufgesucht, Geraet in *developermode* gebracht, aufgeschraubt - diesmal ist es ein richtiger Schalter - entsperrt und auf 8GB RAM und 120GB SSD aufgeruestet.

Diesmal hat das Skript auf Anhieb das BIOS geplaettet und mit SeaBIOS ueberschrieben. Danach das Betriebssystem der Wahl einspielen.
Diesmal hab ich Win10 ausprobiert und siehe da - es funktioniert. Die intenso SSD ist nicht die schnellste und der celeron 847 auch nicht; da sind andere Betriebssysteme besser geeignet.

Die andere Seite sind die **ARM-Chromebooks**, wie der samsung **chromebook XE303C12**, alias [snow](https://github.com/hexdump0815/linux-mainline-on-arm-chromebooks). Diese Systeme haben kein richtiges BIOS, sondern werden via *uboot* bedient. Das Entsperren ist identisch zu ihren intel Pendanten, nur wird wie beim *recovery* ein adaptiertes Startmedium mit dem Betriebssytem der Wahl reingeschrieben. Dafuer muss in der *chronos-shell* ein `su` ausgefuerht werden und `crossystem dev_boot_usb=1 dev_boot_signed_only=0` eingegeben werden. Damit startet das System von USB oder SD.

Und zu guter letzt ein **Acer C720**, alias peppy, mit einem celeron 2995U mit 1.4GHz. Schade dass die 2te M.2 keine SSD aufnimmt bzw. nicht intern kontaktiert ist.