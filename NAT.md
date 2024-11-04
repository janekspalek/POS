## K čemu slouží NAT (Network Address Translation)
- Toto nastavení na routeru umožňuje zařízením v **lokální síti** (`LAN`) komunikovat s **externími sítěmi**, jako je internet, pomocí **jedné nebo několika veřejných IP adres**
- `NAT` překládá `privátní` IP adresy vnitřní sítě na `veřejné` IP adresy
- Zvyšuje bezpečnost a šetří veřejný adresní prostor

## Konfigurace NAT na routeru

### Identifikace rozhraní
- **Vnitřní rozhraní** (`inside`) - rozhraní připojené k lokální síti
- **Vnější rozhraní** (`outside`) - rozhraní připojené k externí síti, například k internetu

```
(config)# interface GigabitEthernet0/0
(config-if)# ip nat inside
(config-if)# exit
(config)# interface GigabitEthernet0/1
(config-if)# ip nat outside
```
