## OSI Model

- Definuje, jak různé systémy komunikují v síťovém prostředí
- Model rozděluje tuto komunikaci do **sedmi vrstev**, z nichž každá má specifické funkce a význam
- Dělí se na:
  - `Connection-Oriented Communication` - spojení je navázáno přes přenosem dat a ukončeno po skončení přenosu, data jsou ve správném pořadí a je spolehlivý (např. `TCP`)
  - `Connectionless Communication` - data se odesílají bez předchozího navázájí spojení, každý paket je nezávislý a může dorazit ve špatném pořadí (např. `UDP`)
 
### Enkapsulace a dekapsulace
- Data procházejí jednotlivými **vrstvami** OSI modelu
- Každý vrstva přidá své vlastní informace k těmto datům (hlavičky, patičky apod.)
- Tyto informace pomáhají při přenosu dat na cílové zařízení
- Na opačné straně nastává dekapsulace, kdy každá vrstva přijme data, odstraní svoji hlavičku a předá data vrstvě výše

### 1. Fyzická vrstva (Physical Layer)
- Zajišťuje přenos jednotlivých bitů mezi zařízeními
- Definuje **fyzické aspekty**, jako jsou **kabely, konektory, signály a rychlosti**
- **Příklady**: `Ethernet`, `USB`

### 2. Linková vrstva (Data Link Layer)
- Poskytuje logické spojení mezi sousedními uzly
- Zajišťuje formátování `rámců` (frames), adresování pomocí `MAC adres`, detekci chyb a řízení toku
- **Příklady**: Ethernet (`LLC` a `MAC` subvrstvy), `PPP`

### 3. Síťová vrstva (Network Layer)
- Umožňuje směrování paketů mezi nesousedními uzly a zajišťuje **adresování zařízení** v rámci celé sítě
- Zajišťuje přenos mezi různými sítěmi
- **Příklady**: `IP`, `IPX`

### 4. Transportní vrstva (Transport Layer)
- Zajišťuje spolehlivý nebo nespolehlivý přenos dat mezi zařízeními, spravuje více spojení současně
- Segmentuje a skládá data zpět, zajišťuje řízení toku a korekci chyb
- **Příklady**: `TCP` (spolehlivý), `UDP` (nespolehlivý)

### 5. Relační vrstva (Session Layer)
- Řídí a synchronizuje dialog mezi aplikacemi na různých systémech
- Umožňuje simplexní, duplexní nebo poloduplexní přenosy a kontroluje přenosy důležitých dat
- **Příklady**: Remote Procedure Call (`RPC`)

### 6. Prezentační vrstva (Presentation Layer)
- Starost o překódování dat do správného formátu, jako je převod znaků nebo komprese a šifrování
- **Příklady**: `ASCII`, `JPEG`, `TLS` (šifrování)

### 7. Aplikační vrstva (Application Layer)
- Poskytuje přístup k síťovým službám pro aplikace a uživatele
- Zajišťuje komunikaci mezi aplikacemi (např. e-mail, web, souborový přenos)
- **Příklady**: `HTTP`, `FTP`, `SMTP`



