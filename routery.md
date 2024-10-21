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

## Konfigurace přepínaných portů (pro PC)
### 1. Výběr rozhraní routeru
Tímto příkazem se vybere konkrétní port, který bude připojený k síti a přiřadíme ho do určité VLAN
Místo X se dá číslo portu
```
(config)# interface gi0/1/X
```

### 2. Nastavení režimu portu
Tento příkaz nastaví port do režimu _access_
```
(config-if)# switchport mode access
```

### 3. Vytvoření VLAN
```
(config-if)# vlan 10
```

### 3. Přiřazení portu k VLAN
```
(config-if)# switchport access vlan 10
```

### 4. Aktivace rozhraní
Standardně je rozhraní vypnuté, tímto příkazem jej zapneme
```
(config-if)# no shutdown
```

## Konfigurace virtuálního rozhraní pro VLAN (SVI - Switched Virtual Interface)
### 1. Výběr virtuálního rozhraní VLAN
Vybrání virtuální rozhraní pro určitou VLAN
```
(config)# interface vlan 10
```

### 2. Nastavení IP adresy a masky pro VLAN
```
(config-if)# ip address <adresa> <maska>
```

### 3. Aktivace virtuálního rozhraní
```
(config-if)# no shutdown
```

## Statické směrování

- **Síť** = adresa sítě, do které se chceme dostat
- **Maska** = maska sítě, do které se chceme dostat
- **Nexthop** = adresa routeru, přes který má cesta do sítě jít
```
(config)# ip route <sit> <maska> <nexthop>

(config)# ip route 10.0.4.0 255.255.255.0 10.0.0.2
```

