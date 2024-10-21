## K čemu slouží router

- Router spojuje **různé sítě** a umožňuje přenos dat mezi nimi
- Řídí tok dat z jedné sítě do druhé pomocí **přesměrování**

## Konfigurace směrovacích portů

Nastavení názvu routeru
```
(config)# hostname <nazev_routeru>
```

### 1. Výběr rozhraní routeru
Tímto příkazem se vybere, které **rozhraní** (port) chci nakonfigurovat
```
(config)# interface <typ> <oznaceni>

(config)# interface FastEthernet 0/0
nebo
(config)# interface GigabitEthernet 0/0/1
```

### 2. Nastavení IP adresy a masky
Tento příkaz nastaví pro daný port adresu a masku podsítě
```
(config-if)# ip address <adresa> <maska>
(config-if)# ip address 10.0.0.1 255.255.255.252
```

### 3. Aktivace rozhraní
Standardně je rozhraní vypnuté, tímto příkazem jej zapneme
```
(config-if)# no shutdown
```

## Konfigurace přepínaných portů

