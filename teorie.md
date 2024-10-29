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
