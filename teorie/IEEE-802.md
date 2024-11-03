IEEE 802 a ISO 8802 Standardy

IEEE 802 je projekt organizace IEEE, který začal v roce 1982 s cílem standardizovat různé technologie v LAN sítích (Local Area Networks). Tento projekt vedl k vytvoření standardů, které byly následně přijaty organizací ISO jako ISO 8802. Hlavní oblastí zaměření je fyzická a linková vrstva OSI modelu, což jsou vrstvy zajišťující fyzický přenos dat a správu přístupu k médiu.

Hlavní části IEEE 802

	1.	IEEE 802.1: Zahrnuje strukturu a organizaci sítě, protokoly pro mosty (bridging), spanning tree, VLAN, a QoS.
	2.	IEEE 802.2: Definuje Logical Link Control (LLC), což je subvrstva, která sjednocuje přístup pro různé LAN technologie.
	3.	IEEE 802.3: Definuje Ethernet a metodu CSMA/CD (Carrier Sense Multiple Access with Collision Detection).
	4.	IEEE 802.5: Specifikuje Token Ring.
	5.	IEEE 802.11: Standard pro bezdrátové sítě LAN (např. WiFi).

Struktura Linkové Vrstvy v IEEE 802

Linková vrstva je rozdělena na dvě subvrstvy:

	•	LLC (Logical Link Control): Poskytuje univerzální služby pro vyšší vrstvy a sjednocuje rozdíly mezi jednotlivými LAN technologiemi.
	•	MAC (Media Access Control): Specifická pro jednotlivé síťové technologie, definuje přístupové metody, formáty rámců, adresování, a detekci chyb.

Sublayer MAC

MAC (Media Access Control) subvrstva se stará o:

	•	Přístupové metody: Definuje, jak stanice přistupují ke sdílenému médiu (např. CSMA/CD pro Ethernet).
	•	Formát rámců: Struktura rámce, včetně adresních polí a kontrolních součtů.
	•	Adresování: Každé zařízení má unikátní MAC adresu (48 bitů) pro identifikaci v rámci sítě.

Sublayer LLC

LLC (Logical Link Control) subvrstva:

	•	Poskytuje jednotný přístup pro různé LAN technologie.
	•	Definuje SAP (Service Access Points), které zajišťují komunikaci mezi vrstvami.
	•	Umožňuje různé služby:
	•	Connectionless unacknowledged service (bez potvrzování, nejčastější).
	•	Connection-oriented service (logické spojení s kontrolou chyb a řízením toku).
	•	Connectionless acknowledged service (bez spojení, ale s potvrzováním, zřídka používané).

LLC Hlavička

	•	Obsahuje pole DSAP (Destination Service Access Point) a SSAP (Source Service Access Point) pro identifikaci cílových a zdrojových procesů.
	•	Řídící pole umožňují předávat základní příkazy a informace o toku dat.

Shrnutí

IEEE 802 a ISO 8802 standardy se zaměřují na sjednocení technologií v LAN sítích a zajištění jejich kompatibility. Projekt IEEE 802 rozdělil linkovou vrstvu na dvě části – MAC a LLC – aby umožnil větší flexibilitu a jednotné připojení pro různé síťové technologie. Tyto standardy jsou základním stavebním kamenem pro většinu současných LAN sítí, včetně Ethernetu a WiFi.
