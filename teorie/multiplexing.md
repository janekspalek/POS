## Multiplexing
- Metoda, která umožňuje přenos **více komunikačních kanálů přes jedno sdílené médium**
- Když má médium dostatečně široké **pásmo** (kapacitu), můžeme jej rozdělit na **několik kanálů najednou**
- Využívá se v **telefonních sítích televiziním vysílání** apod.

### 1. Frequency Division Multiplexing (FMD)
- Rozdělení kanálů podle **specifických frekvencí**
- Je vhodné pro **fixní počet uživatelů**, mezi jednotlivými kanály je potřeba ponechat **frekvenční mezery** kvůli rušení

<img src="https://github.com/user-attachments/assets/9d760807-6c72-4a3e-a6f4-05048e4c6e89" alt="Kroucená dvojlinka" style="max-width: 100%; width: 500px;">

### 2. Wave Division Multiplexing (WDM)
- Speciální případ `FDM`
- Využívá se pro `optické sítě`
- Každý kanál má **různou vlnovou délku** (barvu světla), toto umožní více signálů přes jedno optické vlákno

<img src="https://github.com/user-attachments/assets/c0b39934-6c2e-461a-bebf-371954c77533" alt="Kroucená dvojlinka" style="max-width: 100%; width: 500px;">

### 3. Time Division Multiplexing (TDM)
- Každý kanál dostane přidělený `časový úsek`, kdy může vysílat
- Může to být neefektivní, pokud nejsou všechny kanály využívány stále

### 4. Statistical Multiplexing
- Data se přenáší v **proměnlivých intervalech** (bursty)
- Přidělení pásma závisí na aktuální potřebě jednotlivých kanálů, každý dostane jiný prostor a čas
- Data jsou rozdělena do `paketů` nebo buněk s hlavičkami, které obsahují informace o **zdroji a cíli**
- Je to ideální v případě, kdy není provoz stabilní a zařízení často posílají data nepravidelně (bursty)
- Například při prohlížení internetu - **chvíli ano** (stahování stránky) a **chvíli ne** (čtení stránky)
- Vhodné pro `Wi-Fi`
