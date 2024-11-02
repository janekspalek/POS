## Hlavní typy zařízení pro propojení LAN
1. `Hub` - jednoduché zařízení, které pouzé přeposílá data všem připojeným zařízením. Neprovádní žádné filtrování a pracuje na fyzické vrstvě OSI
2. `Bridge` - pracuje na datové vrstvě (Layer 2) a spojuje dvě nebo více sítí tak, aby vytvořily jednu logickou síť. Filtruje provoz podle MAC adres, což snižuje kolize. Dnes jsem bridge nahrazené switchi
3. `Switch`- pokročilejší bridge, která také pracuje na datové vrstvě a přepíná data přímo na základě **MAC adres** v `tabulce přepínání` (switching table)
