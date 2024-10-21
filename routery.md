## K čemu slouží router

- Router spojuje **různé sítě** a umožňuje přenos dat mezi nimi
- Řídí tok dat z jedné sítě do druhé pomocí **přesměrování**

## Konfigurace

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

(config-if)# ip address <adresa> <maska>
(config-if)# no shutdown
```

Nastavení rozhraní routeru

