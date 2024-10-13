## K čemu slouží VLAN

- Dovoluje nám rozdělit **jeden fyzický switch** na **více menších switchů**
- Každý VLAN je **číslo** přiřazené ke každému **portu** na switchi
- Všechny porty, které nemají přiřazené VLAN číslo jsou v **defaultním VLANu (číslo 1)**

## Trunk a Access porty

- **Access port** = může být pouze v jedné VLAN, je do něj většinou připojený PC
- **Trunk port** = řídí provoz mezi více VLAN

## Konfigurace

### 1. Vytvoření VLAN na každém switchi

Vytvoření VLAN s _číslem_ a jeho _pojmenování_ (nepovinné)
```
Switch(config)# vlan 10
Switch(config-vlan)# name V10
```

### 2. Konfigurace access portů

Každému portu zvlášť nastavíme _mode = access_ a číslo VLAN
```
Switch(config)# interface Ethernet 0/0
Switch(config-if)# switchport mode access
Switch(config-if)# switchport access vlan 10
```

### 3. Konfigurace trunk portů

Každému portu nastavíme _mode = trunk_
```
Switch(config)# interface Ethernet1/1
Switch(config-if)# switchport mode trunk
```

### 4. Povolení určitých VLAN na trunk portech

Defaultně mají trunk porty povoleny všechny VLAN z databáze
```
Switch(config)# interface Ethernet 2/1
Switch(config-if)# switchport trunk allowed vlan 10,20
```

## Další příkazy

### Seznam access portů a VLANů

```
Switch# show vlan brief

VLAN Name                             Status    Ports
---- -------------------------------- --------- -------------------------------
1    default                          active    Et0/2, Et0/3, Et1/0, Et1/2
                                                Et1/3, Et2/0, Et2/3, Et3/0
                                                Et3/1, Et3/2, Et3/3
10   RED                              active    Et0/0
20   ORANGE                           active
30   BLUE                             active    Et0/1
```

### Seznam trunk portů

```
Switch# show interfaces trunk

Port        Mode             Encapsulation  Status        Native vlan
Et1/1       on               802.1q         trunking      2
Et2/1       on               802.1q         trunking      3
Et2/2       on               802.1q         trunking      3

Port        Vlans allowed on trunk
Et1/1       1-4094
Et2/1       10,20
Et2/2       20,30

Port        Vlans allowed and active in management domain
Et1/1       1,10,20,30
Et2/1       10,20
Et2/2       20,30

Port        Vlans in spanning tree forwarding state and not pruned
Et1/1       1,10,20,30
Et2/1       10,20
Et2/2       20,30
```



