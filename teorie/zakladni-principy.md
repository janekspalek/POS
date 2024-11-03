## Základní principy přenosu dat
Dělí se podle směru přenosu
1. `Simplex` - data se přenášejí pouze **jedním směrem**, jeden kanál pro přenos (TV)
2. `Half duplex` - přenos **střídavě v obou směrech**, pouze jeden směr najednou. pro přenos stačí jeden kanál (vysílačka)
3. `Full duplex` - obě strany mohou komunikovat **současně**, musí být dva nezávislé kanály (Ethernet)

## Paralelní a sériová komunikace
1. `Paralelní` - více bitů je přenášeno současně, je dražší a komplikovanější na synchronizaci
2. `Sériová` - v dnešní době standardem, kvůli nižším nákladům a jednodušší konstrukci kabelů

### Sériová asynchronní a synchronní přenos
1. `Asynchronní` - přenáší znaky jeden po druhém s jednotlivými stop bity a možností kontroly parity (klávesnice)
2. `Synchronní` - data se přenáší ve formě **rámců s hlavičkou**, kontrolními součty a bez nutnosti synchronizace pro každý znak. **Vhodné pro vysokorychlostní přenos**, synchronizace probíhá na začátku bloku, takže ji není potřeba neustále obnovovat

## Přenosová média a modulace signálu
1. `Fyzické vlastnosti signálu` - data se přenáší prostřednictvím **signálu** (napětí, intenzita světla...) který nese informace. Tyto signálu ale mohou být ovlivněny šumem a útlumem prostředí
2. `Typy médií` - optická vlákna, kroucená dvojlinka a koaxiální kabely

### Modulace
1. `AM (Amplitude Modulation)` - změna **amplitudy** nosného signálu podle dat
2. `FM (Frequency Modulation)` - změna **frekvence** nosného signálu podle dat
3. `PM (Phase modulation)` - změna **fáze** signálu, aby nesl informace

## Základní přenosové metody Baseband a Broadband
### 1. Baseband
- Přenáší data v původní frekvenční oblasti **bez modulace**
- Data mohou využívat celé frekvenční pásmo pro sebe, nevyužívají různé kanály - nedělí médium pro více uživatelů
- Pro `LAN`, `WAN`

#### Non Return to Zero (NRZ)
- 0 -> nízká úroveň
- 1 -> vysoká úroveň

1. `Baseband` - přenáší data v původní frekvenční oblasti bez modulace. Data mohou využívat celé frekvenční pásmo pro sebe a nevyužívají různé kanály, nedělí tedy médium pro více uživatelů. Používá se v LAN, Ethernetu
2. `Broadband` - rozdělí šířku pásma na více kanálů, což umožní **více komunikací současně**. Je typický pro kabelovou televizi, mobilní sítě (3G, 4G, 5G), Wi-Fi sítě, satelitní internet a televize, optické sítě

## Kódování signálu pro přenos dat
### 1. Manchester a Differential Manchester
**Manchester**
- Každý bit je reprezentován změnou úrovně uprostřed bitového intervalu
- 0 -> přechod z nízké na vysokou úroveň
- 1 -> přechod z vysoké na nízkou úroveň

**Manchester Differential**
- Změna signálu na začátku intervalu představuje 0, žádná změna představuje 1
- Přechod uprostřed bitu je vždy přítomen
- Použití Ethernet 10 Mbps

![image](https://github.com/user-attachments/assets/0640e6f2-25fa-473e-ab05-ca89b6dffeef)

### 2. AMI (Alternate Mark Inversion)
- **Tři úrovně signálu**: 0, +1, -1
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
