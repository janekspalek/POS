## Hlavní typy zařízení pro propojení LAN 💻
1. `Hub` - jednoduché zařízení, které pouzé přeposílá data **všem připojeným zařízením**. Neprovádní žádné filtrování a pracuje na fyzické vrstvě OSI
2. `Bridge` - pracuje na datové vrstvě (Layer 2) a spojuje dvě nebo více sítí tak, aby vytvořily jednu logickou síť. Filtruje provoz podle MAC adres, což snižuje kolize. Dnes jsem bridge nahrazené switchi
3. `Switch`- pokročilejší bridge, která také pracuje na datové vrstvě (Layer 2) a přepíná data přímo na základě **MAC adres** v `tabulce přepínání` (switching table)

## Spanning Tree Protocol (STP) 🌳
- Protokol, využívaný ve switchi k prevenci smyček v síti
- Má za úkol vytvořit logické spojení mezi switchemi tak, aby mezi nimi existovala jediná cesta ke každému zařízení, což zabrání vzniku smyček
- Všechny redundantní cesty jsou automaticky zablokovány
- Vytváří stromovou strukturu (spanning tree) a blokuje redundantní cesty
- Pokud nastane výpadek, STP automaticky přepočítá topologii a zajistí, že síť zůstane funkční

## Routery (Směrovače) 
- Směrovací zařízení, které propojuje sítě na **síťové vrstvě** (Layer 3)
- Umožňuje propojit různé sítě, používá IP adresy k předání dat na správné místo
- Routery mohou být nakonfigurovány ručně (`statické směrování`), nebo automaticky (`dynamické směrování`) například pomocí `OSPF`

**Jejich další funkce jsou:**
1. `NAT` (Network Address Translation)
2. `Firewall` a bezpečností funkce
3. `VPN` pro zabezpečené propojení na dálku

## Switch (Přepínače) 
- Fungují na **linkové vrstvě** (Layer 2)
- Hlavní výhodou je schopnost **přepínat data mezi segmenty bez kolizí**
- Switche využívají `CAM tabulku` (Content Addressable Memory), která uchovává `MAC adresu` a přiřadí si ji k portu
- Díky této tabulce mají také lepší **bezpečnost** - data jdou pouze tam, kam mají (po naučení CAM tabulky)
- Každý port může fungovat v jiném módu (`half duplex`, `full duplex`)

### Metody přepínání
1. `Store-and-forward` - rámec je **nejprve uložen**, zkontrolován pomocí `CRC` (kontrola, zda nejsou data poškozena během přenosu) a pak přeposlán díle
2. `Cut-through` - rámec je přeposlán **hned** po přečtení cílové `MAC adresy`
3. `Fragment Free` - kombinuje výhody obou metod, přeposílání začíná, až když je jisté, že nedojde ke kolizi

