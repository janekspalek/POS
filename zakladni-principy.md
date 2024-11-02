# 1. Základní principy přenosu dat
Dělí se podle směru přenosu
1. `Simplex` - **jednosměrný provoz**, kdy jde signál jen jedním směrem (TV)
2. `Half duplex` - **přenos obousměrný**, ale pouze jeden směr najednou (vysílačka)
3. `Full duplex` - **přenos obousměrný**, obě strany mohou komunikovat současně (Ethernet)

# 2. Paralelní a sériová komunikace
1. `Paralelní` - více bitů je přenášeno současně, je dražší a komplikovanější na synchronizaci
2. `Sériová` - v dnešní době standardem, kvůli nižším nákladům a jednodušší konstrukci kabelů

## Asynchronní a synchronní přenos

1. `Asynchronní` - přenáší znaky jeden po druhém s jednotlivými stop bity a možností kontroly parity (klávesnice)
2. `Synchronní` - data se přenáší ve formě **rámců s hlavičkou**, kontrolními součty a bez nutnosti synchronizace pro každý znak. **Vhodné pro vysokorychlostní přenos**, synchronizace probíhá na začátku bloku, takže ji není potřeba neustále obnovovat

# 3. Přenosová média a modulace signálu

1. `Fyzické vlastnosti signálu` - data se přenáší prostřednictvím **signálu** (napětí, intenzita světla...) který nese informace. Tyto signálu ale mohou být ovlivněny šumem a útlumem prostředí
2. `Typy médií` - optická vlákna, kroucená dvojlinka a koaxiální kabely
