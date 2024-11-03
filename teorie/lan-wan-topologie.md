## LAN (Local Area Network)
- **Místní síť**, často na **jednom** fyzickém místě (např. v jedné budově)
- Má vysoké přenosové rychlosti (Mbps až Gbps)
- Na médium se přenáší vždy **jen jeden paket najednou**

**Typické topologie:**
1. `Hvězda`
2. `Sběrnicová` (bus)
3. `Strom` (propojené hvězdy)

## WAN (Wide Area Network)
- **Širokopásmová síť**, která propojuje zařízení na větší vzdálenosti (např. mezi městy, zeměmi)
- **Nižší přenosové rychlosti** (běžně kbps, ale moderní WAN i Gbps)
- Na médium může být současně přenášeno více paketů

**Typické topologie:**
1. Síť (mesh)
2. Hvězda s centrálním uzlem

## Síťové topologie

### 1. Sběrnicová topologie (Bus)
- Všechna zařízení jsou připojena ke **společnému kabelu** (**sběrnici**)
- Nízké náklady, ale omezená bezpečnost a odolnost vůči selhání
- Vhodná pro malé sítě, ale obtížná na údržbu

<img src="https://github.com/user-attachments/assets/7c60e389-758e-4852-b410-a6664915d3e0" alt="Kroucená dvojlinka" style="max-width: 100%; width: 500px;">

### 2. Hvězdicová topologie (Star)
- Každé zařízení je připojeno k centrálnímu uzlu (např. `hub` nebo `switch`)
- Odolná vůči selhání jednotlivých zařízení, ale pokud selže centrální uzel, celá síť přestane fungovat
- **Je to nejčastější topologie v LAN sítích**

<img src="https://github.com/user-attachments/assets/93c0a06e-4762-47be-bdd2-3768eae1fd35" alt="Kroucená dvojlinka" style="max-width: 100%; width: 500px;">

### 3. Stromová topologie (Tree)
- Rozšířená hvězdicová topologie s hierarchickým uspořádáním (větve)
- Flexibilní a rozšiřitelná, často používaná v moderních LAN

<img src="https://github.com/user-attachments/assets/6bad1fe9-1b7e-412a-9719-f6b6d5958c12" alt="Kroucená dvojlinka" style="max-width: 100%; width: 500px;">

### 4. Kruhová topologie (Ring)
- Zařízení jsou propojena v kruhu a každé zařízení posíla data jen jednomu sousednímu zařízení
- Citlivá na výpadky

<img src="https://github.com/user-attachments/assets/a4d8c27d-73fc-4115-96ef-117fa57ed7fe" alt="Kroucená dvojlinka" style="max-width: 100%; width: 500px;">

### 5. Mesh (síťová topologie)
- Přímé propojení mezi zařízeními (**často mezi routery v WAN**)

<img src="https://github.com/user-attachments/assets/55eadc36-eeeb-43df-857c-9fed10a7ab08" alt="Kroucená dvojlinka" style="max-width: 100%; width: 500px;">

## 4. Příklad topologie internetu
- Internet kombinuje různé topologie LAN a WAN a propojuje je přes routery
- Každý menší síť v internetu může mít vlastní topologii
