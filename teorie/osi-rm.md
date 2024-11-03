## OSI Model

- Definuje, jak různé systémy komunikují v síťovém prostředí
- Model rozděluje tuto komunikaci do **sedmi vrstev**, z nichž každá má specifické funkce a význam
- Dělí se na:
  - `Connection-Oriented Communication` - spojení je navázáno přes přenosem dat a ukončeno po skončení přenosu, data jsou ve správném pořadí a je spolehlivý (např. `TCP`)
  - `Connectionless Communication` - data se odesílají bez předchozího navázájí spojení, každý paket je nezávislý a může dorazit ve špatném pořadí (např. `UDP`)

### 1. Fyzická vrstva (Physical Layer)
- Zajišťuje přenos jednotlivých bitů mezi zařízeními
- Definuje **fyzické aspekty**, jako jsou **kabely, konektory, signály a rychlosti**
- Příklady: `Ethernet`, `USB`

### 2. Linková vrstva (Data Link Layer)
- Poskytuje logické spojení mezi sousedními uzly
- Zajišťuje formátování `rámců` (frames), adresování pomocí `MAC adres`, detekci chyb a řízení toku
- Příklady: Ethernet (`LLC` a `MAC` subvrstvy), `PPP`
