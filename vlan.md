## K čemu slouží VLAN

- Dovoluje nám rozdělit **jeden fyzický switch** na **více menších switchů**
- Každý VLAN je **číslo** přiřazené ke každému **portu** na switchi
- Všechny porty, které nemají přiřazené VLAN číslo jsou v **defaultním VLANu (číslo 1)**

## Trunk a Access porty

- **Access port** = může být pouze v jedné VLAN, je do něj většinou připojený PC
- **Trunk port** = řídí provoz mezi více VLAN

## Konfigurace

### 1. Vytvoření VLAN na každém switchi

Vytvoření VLAN s číslem
```
Switch(config)# vlan 10
```

Pojmenování VLAN (nepovinné)
```
Switch(config-vlan)# name V10
```


