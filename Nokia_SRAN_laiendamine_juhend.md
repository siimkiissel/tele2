# Nokia SRAN laiendamine – praktiline tööjuhend

## 1. FDD ja TDD

### FDD (Frequency Division Duplex)

- Üleslaadimine (UL) ja allalaadimine (DL) toimuvad **erinevatel sagedustel**.
- Saatmine ja vastuvõtt toimuvad samaaegselt.
- Kasutusel enamiku 4G LTE sageduste ning osade 5G sageduste puhul.

**Näide**

| Uplink | Downlink |
|--------|----------|
| 1710–1785 MHz | 1805–1880 MHz |

### TDD (Time Division Duplex)

- UL ja DL kasutavad **sama sagedust**.
- Erinevus on ainult ajas.

```text
DL DL DL UL DL UL
```

Kõrgetel 5G sagedustel (nt n78 / 3500 MHz) kasutatakse enamasti TDD-d, sest see võimaldab paindlikumat üles- ja allalaadimise suhte määramist.

---

## 2. Data Center MCF

MCF (**Master Configuration File**) asub Data Centeris.

Sisaldab kogu tugijaama põhikonfiguratsiooni ning seda kasutatakse:
- backupide tegemiseks
- restore'iks
- reprocessimiseks
- konfiguratsioonifailide genereerimiseks

---

## 3. ABIO ja ABIA

### ABIO
- Kasutatakse 4G (LTE) ja 5G (NR) jaoks.

### ABIA
- Kasutatakse 2G (GSM) jaoks.

---

## 4. Laienduskaardid

Uue sageduse või raadiomooduli lisamisel võib olla vaja lisada laienduskaart (nt **AHEGG**).

---

## 5. BSSInfo

BSSInfo abil saab vaadata:
- Cellide infot
- sagedusi
- antenniporte
- olemasolevat konfiguratsiooni

---

## 6. Uue AHEGG mooduli lisamine

Mine **Shelf** vaatesse.

1. Lohista **AHEGG** seadme **MAST Root** alla.
2. Salvesta muudatus.

---

## 7. Vendor Radio Module

Mine:

```
Profile
```

Vali:

```
Vendor Radio Modules
```

Paremklõps:

```
Update Parameter
```

Vali vaba ID (näiteks **8**).

---

## 8. Optical Interface

Mine:

```
AHEGG
└── Sub Interface
    └── Optical Interface 1
```

Seal on:

- RX
- TX

Ühendused:

- TX → RX
- RX → TX

---

## 9. Functional Elements

Mine:

```
Network Element
└── Functional Elements
```

Siin lisatakse uued Cellid.

---

## 10. Cell ID (HEX)

Cell ID kuvatakse sageli HEX-kujul.

Näide:

```
4A71
```

---

## 11. Uue Celli lisamine

Paremklõps:

```
Add Interface
```

Näide:

```
Cell G4A71
```

Kui kõik õnnestub:

```
Interface successfully added
```

---

## 12. Celli nimetused

| Algus | Tehnoloogia |
|--------|-------------|
| puudub täht | 4G LTE |
| G | 2G GSM |
| N | 5G NR |

Näited:

```
5841
```

```
G4A71
```

```
N2158
```

---

## 13. Antenniportide määramine

Pärast Celli loomist tuleb määrata antenniport.

Lihtsaim viis:
- vaata olemasolevat sama sektori Celli
- kopeeri sama port

Näiteks:

```
ANT1
```

Lohista see uuele Cellile.

---

## 14. 4G

Näide:

```
N21 (2100 MHz)
58
```

Märkus: "N21" võib olla ettevõttesisene nimetus. 2100 MHz LTE vastab 3GPP järgi Band 1 (B1) ning 5G puhul n1.

---

## 15. 5G

5G Cellile määratakse tavaliselt kaks RF-porti.

Näiteks:

```
Port 1
Port 2
```

---

## 16. Vendor Antenna Line Usage

Mine:

```
Profile
└── vendor-antennaLine-usage
```

Paremklõps:

```
Update Parameter
```

---

## 17. NEM

Mine:

```
NEM
└── Devices
```

Otsi näiteks soovitud site.

Seejärel vali:

```
Reprocess Backup
```

või

```
Reprocess
```

---

## 18. Planned Cells

Planned Cellid saadakse tavaliselt:

- LLD
- ClickOnSite

---

## 19. BTS Config

Mine:

```
Tools
└── BTS Config
```

Kui kõik on korras, genereeritakse XML konfiguratsioonifail.

---

## 20. Konfiguratsiooni laadimine

1. Logi tugijaama IP-aadressiga sisse.
2. Laadi XML fail üles.

4G ja 5G sektorid lisatakse XML konfiguratsiooniga.

---

## 21. 2G lisamine

2G lisatakse eraldi **CM Editoris**.

CM Editor asub:

```
NetAct / MantaRay NM
```

---

# Töövoog

```text
LLD / ClickOnSite
        │
        ▼
Lisa AHEGG
        │
        ▼
Vendor Radio Module
        │
        ▼
Optical Interface
        │
        ▼
Loo Cell
        │
        ▼
Määra antenniport(id)
        │
        ▼
Vendor Antenna Line Usage
        │
        ▼
Reprocess
        │
        ▼
BTS Config
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
