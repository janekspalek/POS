## Základní principy přenosu dat
Dělí se podle směru přenosu:
1. `Simplex` - data se přenášejí pouze **jedním směrem**, jeden kanál pro přenos (TV)
2. `Half duplex` - přenos **střídavě v obou směrech**, pouze jeden směr najednou. Pro přenos stačí jeden kanál (vysílačka)
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
- Pro `LAN`, `WAN`, `Ethernet`

#### Non Return to Zero (NRZ)
- Kvůli absenci neutrální hodnoty nelze toto kódování použít pro synchronní přenosy
- 0 -> nízká úroveň
- 1 -> vysoká úroveň

<img src="https://github.com/user-attachments/assets/e8305e70-3815-4bcc-823a-880aab853b59" alt="Kroucená dvojlinka" style="max-width: 100%; width: 500px;">

#### Non Return to Zero Inverted (NRZI)
- 0 -> úroveň signálu zůstává
- 1 -> inverze signálu

<img src="https://github.com/user-attachments/assets/695e000b-cc41-4891-b1db-707fb839fd7b" alt="Kroucená dvojlinka" style="max-width: 100%; width: 500px;">

#### Manchester
- Každý bit je reprezentován změnou uprostřed bitového intervalu
- 0 -> přechod z nízké na vysokou úroveň
- 1 -> přechod z vysoké na nízkou úroveň

<img src="https://github.com/user-attachments/assets/f992fdfc-4983-4012-8ba8-936410fc363c" alt="Kroucená dvojlinka" style="max-width: 100%; width: 500px;">

#### Diferenciální Manchester
- 0 -> změna
- 1 -> beze změny

<img src="https://github.com/user-attachments/assets/9ef3459d-d95c-46f7-b044-de40a30e5029" alt="Kroucená dvojlinka" style="max-width: 100%; width: 500px;">

#### Alternate Mark Inversion (AMI)
- 3 úrovně amplitudy signálu (-1, 0, +1)
- Problém při dlouhých posloupnostech nul
- 0 -> nulová hodnota
- 1 -> střídavě +1 a -1

<img src="https://github.com/user-attachments/assets/4c8b1a4a-8517-4694-8fe5-973bdb88a1eb" alt="Kroucená dvojlinka" style="max-width: 100%; width: 500px;">

#### 4B5B
- Každé 4 bity mají pevně danou kombinaci 5 bitů
- Datový tok se tím pádem zvýší o 25 %
- Každá kombinace 5 bitů má alespoň 2x 1 -> nenastanou dlouhé posloupnosti nul

### 2. Broadband
- Rozdělí šířku pásma na více kanálu
- Umožní tím **více komunikací současně**
- Využívá se například pro mobilní sítě (4G, 5G), Wi-Fi, optické sítě...
