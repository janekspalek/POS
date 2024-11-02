## Multiple Access Protocols

- Umožňují více zařízením sdílet jeden komunikační kanál (např. kabel, bezdrátová frekvence jako Wi-Fi), aniž by docházelo k neustálým kolizím
- Tyto protokoly rozhodují, **které zařízení může vysílat data a kdy**

**Dělí se na dvě hlavní kategorie:**
1. **Pravděpodobnostní protokoly** (Contention-based) - používají náhodné algortimy pro přístup ke kanálu, což může způsobit kolize, ale jsou jednodušší na implementaci
2. **Deterministické protokoly** (Contention-free) - stanice se střídají podle předem daného algoritmu, **což zabrání kolizím**


## Pravděpodobnostní protokoly (Contention-based)

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
