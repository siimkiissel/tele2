# Nokia RAN / NetAct – Laiendatud mõistete käsiraamat

See dokument koondab olulisemad Nokia RAN, LTE, 5G ja NetActi terminid ühte kohta.

## Võrguhaldus

| Lühend / mõiste | Täisnimi | Kirjeldus |
|---|---|---|
| **NetAct** | Nokia Network Management System | Nokia keskne võrguhaldussüsteem alarmide, konfiguratsioonide, KPI-de ja monitooringu jaoks. |
| **MantaRay NM** | MantaRay Network Manager | NetActi uuem veebipõhine haldusliides. |
| **NMS** | Network Management System | Üldnimetus võrguhaldussüsteemile. |
| **NEM** | Network Element Manager | Haldab konkreetseid võrguelemente. |
| **VersaNIS** | Versatile Network Integration System | Offline konfiguratsioonide loomise ja muutmise tööriist. |
| **CM Editor** | Configuration Management Editor | VersaNIS-i konfiguratsiooniredaktor. |
| **Frontix Integrity** | — | Kontrollib konfiguratsioonide loogikat enne võrku laadimist. |
| **NAC** | NetAct Configurator | Laeb kontrollitud konfiguratsioonid võrku. |
| **Traffica** | — | Nokia jõudlus- ja liiklusanalüüsi tööriist. |
| **BTS Site Manager** | — | Üksiku tugijaama haldustööriist. |

## RAN objektid

| Lühend / mõiste | Täisnimi | Kirjeldus |
|---|---|---|
| **MRBTS** | Master Radio Base Station | Nokia tugijaama põhiobjekt. |
| **BCF** | Base Control Function | 2G baasjaama juhtplokk. |
| **BTS** | Base Transceiver Station | 2G tugijaam. |
| **TRX** | Transceiver | 2G raadiosaatja-vastuvõtja. |
| **LNBTS** | LTE NodeB | 4G tugijaama objekt. |
| **gNB** | Next Generation NodeB | 5G tugijaam. |
| **CELL** | Cell | Raadiokärg. |
| **Sector** | — | Antenni leviala üks osa, tavaliselt 3 sektorit saidi kohta. |
| **BBU** | Baseband Unit | Digitaalne baasriba protsessor. |
| **RRU** | Remote Radio Unit | Raadioseade antenni juures. |
| **ASIB** | Antenna System Interface Board | Vanem antenniliidese moodul. |
| **ASIM** | Antenna System Interface Module | Uuem antenniliidese moodul. |

## Raadiomõõdikud

| Lühend / mõiste | Täisnimi | Kirjeldus |
|---|---|---|
| **RSSI** | Received Signal Strength Indicator | Signaali üldine tugevus. |
| **RSRP** | Reference Signal Received Power | LTE/5G referentssignaali tugevus. |
| **RSRQ** | Reference Signal Received Quality | LTE/5G signaali kvaliteet. |
| **SINR** | Signal to Interference plus Noise Ratio | Signaali ja häirete suhe. |
| **CQI** | Channel Quality Indicator | UE hinnang kanali kvaliteedile. |
| **MCS** | Modulation and Coding Scheme | Määrab modulatsiooni ja kodeeringu. |
| **BLER** | Block Error Rate | Vigaste plokkide osakaal. |
| **VSWR** | Voltage Standing Wave Ratio | Antenni ja kaabli sobivuse näitaja. |
| **Throughput** | — | Andmeedastuskiirus. |
| **Latency** | — | Võrgu viivitus. |
| **Packet Loss** | — | Kadunud andmepaketid. |

## LTE ja 5G

| Lühend / mõiste | Täisnimi | Kirjeldus |
|---|---|---|
| **EARFCN** | E-UTRA Absolute RF Channel Number | LTE sageduskanali number. |
| **NRARFCN** | NR Absolute RF Channel Number | 5G sageduskanali number. |
| **PCI** | Physical Cell Identity | LTE/5G füüsiline kärje ID. |
| **CGI** | Cell Global Identity | Kärje globaalne identifikaator. |
| **ECGI** | E-UTRAN Cell Global Identity | LTE kärje identifikaator. |
| **NCGI** | NR Cell Global Identity | 5G kärje identifikaator. |
| **ANR** | Automatic Neighbour Relation | Automaatne naaberkärgede õppimine. |
| **ADJL** | Adjacent Cell List | Käsitsi seadistatud naaberkärgede nimekiri. |
| **Handover** | — | Kasutaja üleviimine teise kärge. |
| **CA** | Carrier Aggregation | Mitme kandja ühendamine. |
| **PCC** | Primary Component Carrier | Peamine kandja. |
| **SCC** | Secondary Component Carrier | Lisakandja. |
| **NSA** | Non-Standalone | 5G töötab LTE tuumvõrgu abil. |
| **SA** | Standalone | Täielik 5G arhitektuur. |
| **EN-DC** | E-UTRA NR Dual Connectivity | LTE+5G samaaegne kasutamine. |
| **Beamforming** | — | Kiire suunamine kasutaja poole. |
| **Massive MIMO** | — | Suur antennimassiiv paralleelsete voogude jaoks. |
| **SSB** | Synchronization Signal Block | 5G sünkroniseerimisplokk. |
| **PRACH** | Physical Random Access Channel | Võrku sisenemise kanal. |
| **BWP** | Bandwidth Part | 5G aktiivne ribalaiuse osa. |

## Core Network

| Lühend / mõiste | Täisnimi | Kirjeldus |
|---|---|---|
| **MME** | Mobility Management Entity | LTE mobiilsuse juhtimine. |
| **AMF** | Access and Mobility Management Function | 5G mobiilsuse juhtimine. |
| **SMF** | Session Management Function | 5G sessioonide haldus. |
| **UPF** | User Plane Function | 5G kasutajaliikluse edastus. |
| **SGW** | Serving Gateway | LTE kasutajatasandi sõlm. |
| **PGW** | Packet Gateway | LTE ühendus välisvõrkudega. |
| **SGSN** | Serving GPRS Support Node | 2G/3G pakettside sõlm. |
| **GGSN** | Gateway GPRS Support Node | 2G/3G andmelüüs. |

## Transport

| Lühend / mõiste | Täisnimi | Kirjeldus |
|---|---|---|
| **OAM** | Operations Administration and Maintenance | Haldus ja hooldus. |
| **VLAN** | Virtual Local Area Network | Virtuaalne kohtvõrk. |
| **MPLS** | Multiprotocol Label Switching | Operaatorivõrgu transporditehnoloogia. |
| **Fronthaul** | — | Ühendus BBU ja RRU vahel. |
| **Midhaul** | — | Ühendus hajutatud üksuste vahel. |
| **Backhaul** | — | Ühendus tugijaama ja tuumvõrgu vahel. |
| **S1** | — | LTE eNodeB ↔ MME liides. |
| **X2** | — | LTE tugijaamade vaheline liides. |
| **Xn** | — | 5G tugijaamade vaheline liides. |

## KPI-d

| Lühend / mõiste | Täisnimi | Kirjeldus |
|---|---|---|
| **Accessibility** | — | Ühenduse loomise edukus. |
| **Retainability** | — | Ühenduse püsimise edukus. |
| **Availability** | — | Võrgu töövalmidus. |
| **Drop Call Rate** | — | Katkenud kõnede osakaal. |
| **Handover Success Rate** | — | Õnnestunud handover'ite osakaal. |

# Sagedusribad

Siin on tabel ainult nende sagedustega, mida **Tele2 Eesti reaalselt kasutab** oma 2G, 4G ja 5G võrgus. Lisasin ka **FDD/TDD** veeru. Andmed vastavad Tele2 tehnilise võrguinfo lehele.

## 2G GSM

| Band       | Täisnimi | Tele2 sagedus | Duplex | Tele2 kasutatav sagedusplokk                     | Kirjeldus                                          |
| ---------- | -------- | ------------- | ------ | ------------------------------------------------ | -------------------------------------------------- |
| **GSM900** | GSM 900  | **900 MHz**   | FDD    | **DL 936.7–948.1 MHz**<br>**UL 891.7–903.1 MHz** | 2G võrk kõnede, SMS-ide ja IoT/M2M seadmete jaoks. |

---

## 4G LTE (E-UTRA)

| Band    | Täisnimi | Tele2 sagedus | Duplex | Tele2 kasutatav sagedusplokk                         | Kirjeldus                                                        |
| ------- | -------- | ------------- | ------ | ---------------------------------------------------- | ---------------------------------------------------------------- |
| **B20** | LTE800   | **800 MHz**   | FDD    | **DL 811–821 MHz**<br>**UL 852–862 MHz**             | Väga hea maapiirkondade katvus ja siselevi.                      |
| **B8**  | LTE900   | **900 MHz**   | FDD    | **DL 936.7–948.1 MHz**<br>**UL 891.7–903.1 MHz**     | Hea leviala ja siselevi. Kasutab sama sagedusplokki nagu GSM900. |
| **B3**  | LTE1800  | **1800 MHz**  | FDD    | **DL 1830.1–1854.9 MHz**<br>**UL 1735.1–1759.9 MHz** | Tele2 peamine LTE mahutavussagedus.                              |
| **B1**  | LTE2100  | **2100 MHz**  | FDD    | **DL 2110–2140 MHz**<br>**UL 1920–1950 MHz**         | Lisamahutavus ning Carrier Aggregation.                          |

> **Märkus:** Tele2-l puudub Eestis LTE Band 7 (2600 MHz FDD).

---

## 5G NR (New Radio)

| Band     | Täisnimi | Tele2 sagedus | Duplex | Tele2 kasutatav sagedusplokk                                            | Kirjeldus                                               |
| -------- | -------- | ------------- | ------ | ----------------------------------------------------------------------- | ------------------------------------------------------- |
| **n28**  | NR700    | **700 MHz**   | FDD    | **DL 758–768 MHz**<br>**UL 703–713 MHz**                                | Üleriigiline 5G leviala ja hea siselevi.                |
| **n1**   | NR2100   | **2100 MHz**  | FDD    | **DL 2110–2140 MHz**<br>**UL 1920–1950 MHz**                            | 5G DSS või eraldiseisev NR kandja.                      |
| **n40**  | NR2300   | **2300 MHz**  | TDD    | **2300–2360 MHz**                                                       | Suurem mahutavus suure liiklusega piirkondades.         |
| **n78**  | NR3500   | **3500 MHz**  | TDD    | **3540–3600 MHz** ja **3730–3800 MHz** *(pärast refarmi 3670–3800 MHz)* | Tele2 peamine suure kiiruse ja mahutavusega 5G sagedus. |
| **n258** | NR26GHz  | **26 GHz**    | TDD    | **24.7–25.5 GHz**                                                       | mmWave. Väga suur kiirus, kuid väga väike leviala.      |

---

### Tele2 kasutab lisaks ka järgmisi litsentse

| Band          | Sagedus      | Duplex | Kasutus             |                                                                                                |
| ------------- | ------------ | ------ | ------------------- | ---------------------------------------------------------------------------------------------- |
| **B39 / n39** | **1900 MHz** | TDD    | **1910.2–1920 MHz** | Eestis kasutatakse väga piiratud ulatuses. Tavapärastes Tele2 makrojaamades üldiselt ei kohta. |
| **B38**       | **2600 MHz** | TDD    | -                   | Tele2-l Eestis aktiivset kasutust praktiliselt ei ole.                                         |
| **B7**        | **2600 MHz** | FDD    | -                   | Tele2-l Eestis puudub kasutus.                                                                 |

See tabel vastab Tele2 Eesti tegelikele sagedusplokkidele ning on sobiv kasutada Nokia SRAN, NetActi ja MantaRay konfiguratsioonide juures. Samuti on sellest lihtne aru saada, millised bandid kasutavad sama sagedusressurssi (näiteks **GSM900 ↔ LTE B8** ja **LTE B1 ↔ NR n1** DSS-i korral).

### FDD vs TDD

| Duplex                              | Selgitus                                                                                                                                                                                         |
| ----------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **FDD (Frequency Division Duplex)** | Üleslink (UL) ja allalink (DL) kasutavad **kahte erinevat sagedust**. Sobib hästi suure levialaga võrkudele ning on kasutusel enamikul 2G ja 4G sagedustest ning ka 5G n1 ja n28 puhul.          |
| **TDD (Time Division Duplex)**      | Üleslink ja allalink kasutavad **sama sagedust**, kuid erinevatel ajahetkedel. Võimaldab paindlikult jagada DL/UL mahtu ning sobib hästi suure läbilaskevõimega 5G sagedustele (n40, n78, n258). |.

