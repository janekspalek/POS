## Multiple Access Protocols

- Umožňují více zařízením sdílet jeden komunikační kanál (např. kabel, bezdrátová frekvence jako Wi-Fi), aniž by docházelo k neustálým kolizím
- Tyto protokoly rozhodují, **které zařízení může vysílat data a kdy**

**Dělí se na dvě hlavní kategorie:**
1. `Nedeterministické protokoly` (kolizní)
   - Používají náhodné algortimy pro přístup ke kanálu
   - O přístup na kanál se může pokusit více stanic současně -> **kolize**
   - Jsou jednodušší na implementaci
3. `Deterministické protokoly` (bezkolizní)
   - Stanice se střídají podle předem daného algoritmu, **což zabrání kolizím**
   - Na kanál nikdy nebude přistupovat více stanic současně


## Nedeterministické protokoly (kolizní)
### 1. Aloha
- Základní protokol, kde stanice vysílá bez kontroly, zda je kanál volný
- Po kolizi stanice počká náhodný čas a zkusí to znovu
- `Pure Aloha` - kolizní čas může být až dvojnásobkem časového úseku rámce
- `Slotted Aloha` - vysílání začíná pouze v předem daných časových slotech, což snižuje pravděpodobnost kolize a zvyšuje efektivitu

### 2. CSMA (Carrier Sense Multiple Access)
- Stanice "naslouchá" (sleduje kanál), jestli je volný, než začne vysílat
- `1-persistent CSMA` - stanice čeká, dokud kanál není volný, a pak hned vysílá
- `Non-persistent CSMA` - pokud je kanál obsazený, stanice počká náhodný čas a zkusí znovu
- `p-persistent CSMA` - když je kanál volný, stanice vysílá s pravděpodobností p, jinak čeká na další časový slot

### 3. CSMA/CD (CSMA with Collision Detection)
- Po kolizi stanice detekuje srážku a zastaví vysílání, aby šetřila kapacitu kanálu
- `Ethernet` **je příkladem technologie, která tento protokol využívá**

## Deterministické protokoly (bezkolizní)
### 1. Token passing
- Ve stavu klidu, když žádný uzel nevyžaduje právo na vysílání, cyklicky putuje mezi uzly rámec `Token` (vysílací právo)
- Počítač může začít vysílat pouze tehdy, když získá tento `Token`
- ** Dělí se na 2 metody:**
     1. `Token ring`
     2. `Token bus`
### 1. Centralized Control
- Jeden hlavní uzel (např. master stanice) řídí přístup ke kanálu pro ostatní uzly
- `Polling` - hlavní uzel dotazuje stanice, zda chtějí vysílat
- `Request Arbitration` - stanice žádají o přístup na odděleném kanálu a hlavní uzel rozhoduje o přidělení

### 2. Distributed Control
- Každá stanice má možnost přístupu bez centrální kontroly, ale podle určitého algoritmu
- `Bit-Map Protocol` - hlavní stanice generuje rezervační rámec, který určiuje, která stanice může vysílat
- `Binary Countdown` - stanice vysílají adresy bit po bitu. Stanice s nejvyšší prioritou získává právo vysílat
- `Token passing` - právo na vysílání je reprezentováno tokenem, který si stanice předávají
