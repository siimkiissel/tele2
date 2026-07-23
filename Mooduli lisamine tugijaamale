Jah. Panin sinu märkmed samasse stiili nagu eelnevad käsiraamatud – selgitustega juurde, et sellest oleks hiljem päriselt kasu.

---

# Nokia SRAN laiendamine – praktiline tööjuhend

## 1. FDD ja TDD

### FDD (Frequency Division Duplex)

* Üles- (UL) ja allalaadimine (DL) toimuvad **erinevatel sagedustel**.
* Saatmine ja vastuvõtt toimuvad korraga.
* Eestis kasutatakse FDD-d enamiku:

  * LTE (4G)
  * osa 5G sageduste puhul.

Näide:

| Uplink        | Downlink      |
| ------------- | ------------- |
| 1710–1785 MHz | 1805–1880 MHz |

---

### TDD (Time Division Duplex)

* Uplink ja Downlink kasutavad **sama sagedust**.
* Erinevus on ainult ajas.

Näide

```
DL DL DL UL DL UL
```

Sama kanal vaheldumisi saadab ja võtab vastu.

---

### Miks 5G-ga tuli TDD rohkem kasutusele?

Kõrged sagedused (nt n78 – 3500 MHz) vajavad:

* suuremat läbilaskevõimet
* paindlikku UL/DL jaotust
* Massive MIMO antenne

Seetõttu kasutatakse seal enamasti TDD-d.

---

## 2. Data Center MCF

MCF (**Master Configuration File**) asub Data Centeris.

See sisaldab kogu tugijaama konfiguratsiooni.

Sellest tehakse:

* backup
* restore
* reprocess
* konfiguratsioonide genereerimine

MCF on sisuliselt tugijaama "põhikonfiguratsioon".

---

# 3. ABIO ja ABIA

## ABIO

Moodul 4G ja 5G jaoks.

Kasutatakse:

* LTE
* NR

---

## ABIA

Moodul 2G jaoks.

Kasutatakse GSM raadios.

---

# 4. Laienduskaardid

Kui lisatakse uus sagedus või uus raadiomoodul, tuleb vajadusel lisada laienduskaart.

Näiteks:

* AHEGG
* muud RF moodulid

Need võimaldavad lisada uusi raadiosagedusi.

---

# 5. BSSInfo

BSSInfo abil saab kontrollida:

* olemasolevaid sektoreid
* sagedusi
* Cell ID-sid
* antenniporte
* konfiguratsiooni

Tihti kasutatakse enne muudatuste tegemist.

---

# 6. Uue raadiomooduli lisamine

Näiteks lisatakse

**AHEGG**

See on kõrgema sageduse raadiosaatja.

---

## Lisamine Shelf vaates

Mine

```
Shelf
```

Lisa

```
AHEGG
```

Lohista see

```
MAST Root
```

alla.

---

# 7. Vendor Radio Module määramine

Mine

```
Profile
```

otsi

```
Vendor Radio Modules
```

vali

```
Update Parameter
```

Leia vaba number.

Näiteks

```
8
```

See tähendab, et uus moodul registreeritakse ID-ga 8.

---

# 8. Optical Interface

Mine

```
AHEGG

↓

Sub Interface

↓

Optical Interface 1
```

Seal on

* RX
* TX

Need tähendavad:

RX = Receive

TX = Transmit

Oluline:

```
TX → RX

RX → TX
```

Ühe seadme TX ühendatakse alati teise seadme RX-ga.

---

# 9. Functional Elements

Mine

```
Network Element

↓

Functional Elements
```

Siin lisatakse uued Cell-id.

---

# 10. Cell ID (HEX)

Cell ID kuvatakse sageli kuueteistkümnendsüsteemis (HEX).

Näiteks

```
4A71
```

See on lihtsalt Cell ID hex-kujul.

---

# 11. Uue Celli lisamine

Parem klõps

```
Add Interface
```

Näiteks

```
Cell G4A71
```

Kui kõik õnnestub:

```
Interface successfully added
```

---

# 12. Celli nimetamine

Näiteks

```
G4A71
```

kus

G tähendab:

```
2G
```

---

# Cellide tähistus

| Algus       | Tehnoloogia |
| ----------- | ----------- |
| puudub täht | LTE (4G)    |
| G           | GSM (2G)    |
| N           | NR (5G)     |

Näited

```
5841
```

→ LTE

```
G4A71
```

→ GSM

```
N2158
```

→ NR

---

# 13. Antenniportide määramine

Pärast Celli loomist tuleb sellele määrata antenniport.

Lihtsaim viis:

Vaata olemasolevat samas sektoris olevat Celli.

Näiteks

```
ANT1
```

Lohista

```
ANT1
```

uuele Cellile.

---

# 14. 4G antenniport

Näiteks

```
N21(2100)

58
```

* N21 tähendab 2100 MHz sageduskihti (märkus: siin kasutatav "N21" on teie ettevõtte sisemine nimetus; 3GPP järgi on LTE band **B1** 2100 MHz ja 5G band **n1** 2100 MHz).
* 58 on sektori või Celli number.

---

# 15. 5G antenniport

5G puhul kasutatakse tavaliselt kahte RF-porti.

Näiteks

```
Port 1

Port 2
```

Mõlemad tuleb Celliga siduda.

---

# 16. Vendor Antenna Line Usage

Mine

```
Profile

↓

vendor-antennaLine-usage
```

Parem klõps

```
Update Parameter
```

Määra uus antenniliin.

---

# 17. NEM

Mine

```
NEM

↓

Devices
```

Otsi näiteks

```
t-kliinikum
```

Seejärel

```
Reprocess Backup

või

Reprocess
```

See uuendab konfiguratsiooni.

---

# 18. Planned Cells

Planned Cellid saadakse tavaliselt:

* LLD-st (Low Level Design)
* ClickOnSite'ist

Need määravad, millised Cellid tuleb lisada.

---

# 19. BTS Config

Mine

```
Tools

↓

BTS Config
```

Kui kõik seadistused on õiged, genereeritakse

```
XML Configuration File
```

See fail sisaldab kogu uue konfiguratsiooni.

---

# 20. Konfiguratsiooni laadimine tugijaama

Pärast XML faili loomist:

1. Logi tugijaama sisse selle IP-aadressiga.
2. Laadi genereeritud konfiguratsioon üles.

Sellega lisatakse:

* 4G sektorid
* 5G sektorid

Need tulevad XML konfiguratsioonifaili kaudu.

---

# 21. 2G lisamine

2G konfiguratsioon tehakse eraldi.

Selleks kasutatakse:

```
CM Editor
```

CM Editor avaneb

```
NetAct / MantaRay NM
```

keskkonnas.

Seal lisatakse vajalikud 2G objektid (nt BTS, TRX, Cellid ja nende parameetrid).

---

# Kokkuvõte – tüüpiline töövoog

```text
LLD / ClickOnSite
        │
        ▼
Lisa uus raadiosagedus
        │
        ▼
Lisa AHEGG Shelfi
        │
        ▼
Määra Vendor Radio Module
        │
        ▼
Lisa Optical Interface (RX/TX)
        │
        ▼
Loo uus Cell
        │
        ▼
Määra antenniport(id)
        │
        ▼
Uuenda vendor-antennaLine-usage
        │
        ▼
Reprocess NEM-is
        │
        ▼
Tools → BTS Config
        │
        ▼
Genereeri XML
        │
        ▼
Laadi XML tugijaama
        │
        ▼
Lisa vajadusel 2G CM Editoris
```

See juhend sobib hästi sinu kasvavasse Nokia SRAN käsiraamatusse ning täiendab varasemaid peatükke laiendusmoodulite, antenniportide ja konfiguratsiooni genereerimise praktilise töövooga. Mõne termini (nt **AHEGG**, **ABIO**, **ABIA** või ettevõttesisese nimetuse **N21**) täpne tähendus võib Nokia tarkvaraversioonist või ettevõtte sisemisest nimetusest sõltuda, seega tasub need vajadusel üle kontrollida teie dokumentatsioonist.
