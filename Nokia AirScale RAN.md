

# Nokia AirScale RAN objektide hierarhia

```text
MRBTS (Physical Base Station / Site)
│
├── EQM (Equipment Management)
│   ├── APEQM (Baseband Unit)
│   ├── RMOD (Radio Module)
│   ├── ANTL (Antenna Line)
│   ├── FTM (Transmission Module)
│   └── muud riistvaraobjektid
│
├── IPNO / IP Interface
│
├── SYNC (Synchronization)
│
├── LNBTS (LTE BTS)
│   ├── LNCEL (LTE Cell)
│   │   ├── LNHOIF
│   │   ├── LNADJL
│   │   ├── LNREL
│   │   ├── PRACH
│   │   ├── PUCCH
│   │   ├── PDSCH
│   │   └── SIB Configuration
│   │
│   └── Carrier Configuration
│
├── NRBTS (5G BTS)
│   ├── NRCEL (5G Cell)
│   │   ├── NRHOIF
│   │   ├── NRADJL
│   │   ├── PRACH
│   │   ├── SSB
│   │   └── Beam Configuration
│   │
│   └── Carrier Configuration
│
└── WNBTS (3G, kui kasutatakse)
```

\---

# Kõige tähtsamad objektid

|Objekt|Tähendus|Lihtsalt öeldes|
|-|-|-|
|**MRBTS**|Multi Radio BTS|Kogu füüsiline baasjaam|
|**EQM**|Equipment Management|Riistvara haldus|
|**APEQM**|Application Equipment|Baseband (BBU)|
|**RMOD**|Radio Module|Raadioseade (RRH)|
|**ANTL**|Antenna Line|Antenniühendus|
|**LNBTS**|LTE Base Station|LTE osa|
|**LNCEL**|LTE Cell|LTE sektor/kärg|
|**NRBTS**|NR Base Station|5G osa|
|**NRCEL**|NR Cell|5G sektor/kärg|
|**WNBTS**|WCDMA BTS|3G osa|

\---

# Naabersuhete objektid

Need on väga olulised optimeerimisel ja ANR-i puhul.

|Objekt|Tähendus|
|-|-|
|**LNADJL**|LTE Adjacent LTE Cell|
|**LNREL**|LTE Relation|
|**LNHOIF**|LTE Handover Information|
|**NRADJL**|5G Adjacent Cell|
|**NRREL**|5G Relation|

Mäletamiseks:

```
ADJL = Kes on minu naaber?
REL = Kas handover on lubatud?
HOIF = Millist infot handoveriks kasutatakse?
```

\---

# Raadioseaded

LTE:

* EARFCN
* PCI
* TAC
* PRACH
* PUCCH
* PUSCH
* PDSCH
* SIB1
* SIB2

5G:

* NRARFCN
* PCI
* SSB
* Beam
* PRACH
* BWP

\---

# Riistvara

```
MRBTS
│
├── Baseband (APEQM)
│
├── Radio Module (RMOD)
│
├── Antenn
│
├── Jumper
│
└── Feeder/Fiber
```

\---

# Näide päris elust

```
MRBTS-2101
│
├── LNBTS-1
│   ├── LNCEL-1 (B20)
│   ├── LNCEL-2 (B3)
│   ├── LNCEL-3 (B1)
│   └── LNCEL-4 (B7)
│
└── NRBTS-1
    ├── NRCEL-1 (n28)
    └── NRCEL-2 (n78)
```

See tähendab:

* üks füüsiline mast (**MRBTS**);
* neli LTE kärge eri sagedusaladel;
* kaks 5G kärge.

\---

# Levinumad objektid, millega disaini- ja optimeerimistiim kokku puutub

|Objekt|Kui tihti|
|-|-|
|MRBTS|⭐⭐⭐⭐⭐|
|LNBTS|⭐⭐⭐⭐⭐|
|LNCEL|⭐⭐⭐⭐⭐|
|NRCEL|⭐⭐⭐⭐⭐|
|LNADJL|⭐⭐⭐⭐|
|LNREL|⭐⭐⭐⭐|
|NRADJL|⭐⭐⭐|
|PRACH|⭐⭐⭐|
|RMOD|⭐⭐⭐|
|APEQM|⭐⭐|
|ANTL|⭐⭐|
|SIB|⭐⭐|

\---

## Hea meelespea

Mõtle objektidest nagu puust:

```text
MRBTS          ← kogu puu
│
├── LNBTS      ← LTE oks
│   └── LNCEL  ← üks LTE leht
│
├── NRBTS      ← 5G oks
│   └── NRCEL  ← üks 5G leht
│
└── EQM        ← puu tüvi (riistvara)
```

Kuna oled praegu Nokia RAN-i ja VersaNIS-iga töötamas, võiks järgmise sammuna teha ka **"Nokia objektid, mida disainiinsener igapäevaselt muudab"** spikri. Seal oleks lahti seletatud näiteks **MRBTS, LNBTS, LNCEL, LNADJL, LNREL, ANR, EARFCN, PCI, TAC, PRACH, RACH Root Sequence, X2, NG, S1 ja EN-DC** ning nende omavahelised seosed praktiliste näidetega.

