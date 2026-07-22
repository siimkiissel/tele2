# Nokia NetAct / MantaRay NM – kiirmärkmed

## 1. NetAct ja MantaRay NM

- **NetAct** – Nokia võrguhaldussüsteem (Network Management System, NMS).
- **MantaRay NM** – NetActi uuem kasutajaliides ja haldusplatvorm.
- Funktsionaalsus on suuresti sama, kuid MantaRay on modernsem ja sisaldab uusi tööriistu.

---

## 2. Network Element (NE) integreerimine

### NE Integration Wizard

Tööriist uue tugijaama võrku lisamiseks.

Kasutatakse näiteks:

- uue saidi kasutuselevõtul;
- moderniseerimise (swap) lõppfaasis;
- pärast tarkvara või riistvara uuendust.

Selle käigus registreeritakse tugijaam võrgu haldussüsteemi.

**Asukoht:**

> **Administration → Network Element Integration**

---

## 3. Administration

### Network Element Integration

- uute tugijaamade lisamine võrku;
- võrgu elementide registreerimine.

### Working Set Manager

Võimaldab luua töökomplekte (Working Sets), et filtreerida võrgu elemente.

Näiteks:

- piirkonna järgi
- TAC järgi
- BSC järgi
- eNB ID järgi
- MRBTS järgi

#### TAC (Tracking Area Code)

LTE/5G võrgus kasutatav piirkonnakood.

Telefon registreerib ennast kindlasse **Tracking Area** piirkonda ning TAC võimaldab võrgul teada, kus telefon asub.

---

## 4. Configuration

### 4.1 CM Editor (Configuration Management)

Peamine tööriist võrgu seadistamiseks.

Siin tehakse:

- parameetrite muutmine
- uute kärgede loomine
- sageduste muutmine
- PCI muutmine
- TAC muutmine
- ANR seadistamine
- naaberkärgede muutmine

CM Editoris tehtud muudatused **ei rakendu kohe**.

Need tuleb hiljem aktiveerida.

---

### 4.2 CM Operations Manager

CM Editoris loodud plaanide aktiveerimine.

```text
CM Editor
    │
    ▼
Plan
    │
    ▼
CM Operations Manager
    │
    ▼
Activate
    │
    ▼
Muudatus läheb võrku
```

---

### 4.3 Software Manager

Kasutatakse tarkvarapakettide haldamiseks.

Näiteks:

- uue SW versiooni laadimine
- upgrade
- downgrade
- testclusteri uuendamine

Tavaliselt kasutatakse harva (nt 1–2 korda aastas).

---

## 5. Monitoring

### Monitor

Reaalajas võrgu jälgimine.

Sarnane **Remote NetAct Central** lahendusele.

Võimaldab jälgida:

- alarme
- kärgede olekut
- seadmete staatust
- ühendusi

---

## 6. Reporting

### Performance Manager+

Ajaloolise statistika vaatamine.

Näiteks:

- liiklus
- kasutajate arv
- PRB koormus
- throughput
- drop call
- handover edukus
- KPI-d

Ei näita reaalajas infot, vaid ajaloolist statistikat.

---

## 7. ANR (Automatic Neighbour Relation)

Automatic Neighbour Relation võimaldab tugijaamadel automaatselt:

- avastada uusi naaberkärgi;
- lisada need naabrite nimekirja;
- eemaldada mittevajalikud naabrid.

Peamine eesmärk:

- sujuvad handover'id;
- vähem käsitsi seadistamist.

---

## 8. Nokia objektide hierarhia

### 5G

```text
MRBTS
└── GNBTS
    └── NRCEL
```

- **MRBTS** – Master Base Station
- **GNBTS** – 5G baasjaam
- **NRCEL** – 5G kärg

### 4G

```text
MRBTS
└── LNBTS
    └── LNCEL
```

- **LNBTS** – LTE baasjaam
- **LNCEL** – LTE kärg

### 2G

```text
BSC
└── BTS
```

- **BTS** – 2G tugijaam.

---

## 9. Nokia LLD Form Estonia

**LLD = Low Level Design**

Sisaldab näiteks:

- sektori seadistused
- antennid
- kõrgused
- sagedused
- PCI
- TAC
- Azimuth
- Tilt
- võimsused

LLD järgi seadistatakse tugijaam.

---

## 10. Leviraadius (üldine hinnang)

### Madalad sagedused (700 / 800 / 900 MHz)

- kuni **30 km** või rohkem ideaaltingimustes
- parem levi
- parem siselevi

### Kõrgemad sagedused (1800 / 2100 / 2600 / 3500 MHz)

- umbes **10–15 km** (3500 MHz puhul sageli oluliselt vähem)
- suurem läbilaskevõime
- väiksem leviala

---

## 11. VSWR

**VSWR = Voltage Standing Wave Ratio**

Näitab, kui hästi antennisüsteem on sobitatud saatjaga.

**Ideaalne:** `1 : 1`

**Hea:** `≤ 1.5`

**Veel aktsepteeritav:** `kuni umbes 2.0`

Kõrge VSWR tähendab, et osa saatja võimsusest peegeldub tagasi, mis võib viidata vigasele antennile, feederile, jumperile või pistikule.

---

## 12. NEM RAN Baltics

Nokia RAN hooldus- ja haldusmeeskond Baltikumis.

Tüüpilised ülesanded:

- konfiguratsioonimuudatused
- integratsioon
- tarkvarauuendused
- probleemide lahendamine
- võrgu optimeerimise toetamine

---

## 13. Tools → BTS Config

Tööriist BTS-i konfiguratsiooni vaatamiseks või muutmiseks.

Sõltuvalt tarkvaraversioonist kasutatakse seda näiteks:

- BTS seadistuse kontrolliks
- TRX konfiguratsiooniks (2G)
- riistvara konfiguratsiooni vaatamiseks

---

## 14. Vanad ja uued tugijaama ID-d

Praktikas võib kohata erinevaid ID-vahemikke.

Näiteks:

- **14xxxx** – vanemad või ajaloolised saidi ID-d
- **16xxxx** – uuemad saidi ID-d

See ei ole Nokia tehniline standard, vaid operaatori sisemine nummerdamise loogika.

---

## Kiire meelespea

| Mõiste | Selgitus |
|--------|----------|
| **NetAct** | Nokia võrguhaldussüsteem |
| **MantaRay NM** | NetActi uuem kasutajaliides |
| **NE Integration Wizard** | Uue tugijaama integreerimine võrku |
| **Working Set** | Filtreeritud töövaade võrgu objektidest |
| **CM Editor** | Konfiguratsiooni muutmine |
| **CM Operations Manager** | Muudatuste aktiveerimine |
| **Software Manager** | Tarkvara haldus |
| **Monitor** | Reaalajas võrgu jälgimine |
| **Performance Manager+** | Ajaloolised KPI-d ja statistika |
| **ANR** | Automaatne naaberkärgede haldus |
| **MRBTS** | Füüsiline baasjaam |
| **LNBTS** | LTE baasjaam |
| **GNBTS** | 5G baasjaam |
| **LNCEL** | LTE kärg |
| **NRCEL** | 5G kärg |
| **VSWR** | Antennisüsteemi sobivuse näitaja |
