## Kódování

Soustřeď se raději na běžné formáty jako Manchester, Differential Manchester, AMI, HDB3 a NRZI, 
protože tyto se objevují v základech datových a telekomunikačních sítí častěji než méně rozšířené formáty.

### 1. Manchester a Differential Manchester
**Manchester**
- Každý bit je reprezentován změnouu úrovně uprostřed bitového intervalu
- 0 -> přechod z nízké na vysokou úroveň
- 1 -> přechod z vysoké na nízkou úroveň

**Manchester Differential**
- Změna signálu na začátku intervalu představuje 0, žádná změna představuje 1
- Přechod uprostřed bitu je vždy přítomen
- Použití Ethernet 10 Mbps

### 2. AMI (Alternate Mark Inversion)
- Tři úrovně signálu: 0, +1, -1
- 0 -> úroveň 0
- 1 -> střídání mezi +1 a -1
- Při dlouhých sekvencích 0 ztrácí synchronizaci

### 3. HDB3 (High Density Bipolar 3 Zeros)
- **Rozšíření AMI** - řeší problém synchronizace při sekvencích nul
- Po třech po sobě jdoucích nulách je vložena 1 s polaritou tak, aby porušila pravidlo střídaní polarity
- **Použití**: PCM linky (E1, E2, E3) pro digitální telekomunikační spojení.

### 4. NRZI (Non Return to Zero Inverted)
- Používá dvě úrovně
- 1 -> změna signálu
- 0 -> žádná změna signálu
- **Použití**: běžné v datových sítích, protože umožňuje lepší synchronizaci při dlouhých sekvencích 0 nebo 1.
