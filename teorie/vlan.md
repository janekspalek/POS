## VLAN (Virtual LAN)

- `VLAN` umožňují **logické oddělení zařízení** v rámci jedné sítě
- Lepší bezpečnost, rozdělení například podle oddělení
- Není potřeba fyzicky upravovat kabeláž, stačí nastavit VLAN
- Zařízení v jedné VLAn nevidí broadcasty z jiné VLAn
- `Trunk porty` - řenášejí provoz více VLAN najednou pomocí `IEEE 802.1q` (přidává rámcům hlavičku s identifikátorem `VLAN`)
- `Access porty` - přenášejí data pouze jedné VLAN bez označení, patří jen do **jedné** VLAN