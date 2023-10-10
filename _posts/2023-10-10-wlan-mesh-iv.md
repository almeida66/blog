---
tags: OpenWrt
---
## OpenWrt und mesh iv
Ich habe jetzt die Variante mit 5G+2G nachgebildet und zwar mit günstige alte tp-link [Archer c50](https://openwrt.org/toh/tp-link/archer-c50); das Aufspielen von OpenWrt war zwar etwas umständlich via einem extra boot.bin und danach erst die Aktualisierung, aber es ging gut...

Sinn ist das schnelle 5G für die interne mesh-Kommunikation zu verwenden und 2G für die stellenweise betagten Endgeräte zu nutzen. Die Zentraleinheit hat(te) ja bereits 5G, somit bleibt die Konfiguration der anderen *wireless AccessPoints*, alias **Dumb AP**. D.h. hier werden weder firewall, dns, oder dhcp benötigt, somit wird der eh knappe Speicherplatz des Archers C50 gespart. Diese Firmware kann man via dem [online](https://firmware-selector.openwrt.org/) Konfigurator zusammenstellen bzw. abwählen.

Je nach Modell kommt dann sowas zustande:
'''base-files busybox ca-bundle dropbear fstools kmod-gpio-button-hotplug kmod-leds-gpio kmod-mt7603 kmod-mt76x2 kmod-nft-offload libc libgcc libustream-wolfssl logd mtd netifd opkg procd procd-seccomp procd-ujail swconfig uci uclient-fetch urandom-seed urngd wpad-mesh-wolfssl mesh11sd uhttpd luci-mod-admin-full luci-base libiwinfo-lua luci-theme-bootstrap luci-mod-network'''
dns, ohcp, ppp, firewall, iptables kommen weg, dafür die mesh-Variante des wpad und die minimale LuCi Installation mit zusätl. Netzwerk-mod (der besseren Übersicht halber)
