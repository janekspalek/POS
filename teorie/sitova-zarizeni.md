## Hlavní typy zařízení pro propojení LAN 💻
1. `Hub` - jednoduché zařízení, které pouzé přeposílá data **všem připojeným zařízením**. Neprovádní žádné filtrování a pracuje na fyzické vrstvě OSI
2. `Bridge` - pracuje na datové vrstvě (Layer 2) a spojuje dvě nebo více sítí tak, aby vytvořily jednu logickou síť. Filtruje provoz podle MAC adres, což snižuje kolize. Dnes jsem bridge nahrazené switchi
3. `Switch`- pokročilejší bridge, která také pracuje na datové vrstvě a přepíná data přímo na základě **MAC adres** v `tabulce přepínání` (switching table)

## Spanning Tree Protocol (STP) 🌳
- Protokol, využívaný ve switchi k prevenci smyček v síti
- Má za úkol vytvořit logické spojení mezi switchemi tak, aby mezi nimi existovala jediná cesta ke každému zařízení, což zabrání vzniku smyček
- Všechny redundantní cesty jsou automaticky zablokovány
- Vytváří stromovou strukturu (spanning tree) a blokuje redundantní cesty
- Pokud nastane výpadek, STP automaticky přepočítá topologii a zajistí, že síť zůstane funkční

## Routery (Směrovače)
- Směrovací zařízení, které propojuje sítě na síťové vrstvě (Layer 3)
- Umožňuje propojit různé sítě, používá IP adresy k předání dat na správné místo
- Routery mohou být nakonfigurovány ručně (`statické směrování`), nebo automaticky (`dynamické směrování`) například pomocí `OSPF`

**Jejich další funkce jsou:**
1. `NAT` (Network Address Translation)
2. `Firewall` a bezpečností funkce
3. `VPN` pro zabezpečené propojení na dálku

