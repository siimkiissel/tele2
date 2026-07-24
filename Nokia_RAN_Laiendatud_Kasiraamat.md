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

## Sagedusribad

Siin on tabel ainult nende sagedustega, mida **Tele2 Eesti reaalselt kasutab** oma 2G, 4G ja 5G võrgus. Lisasin ka **FDD/TDD** veeru. Andmed vastavad Tele2 tehnilise võrguinfo lehele. ([Tele2][1])

| Lühend / mõiste | Täisnimi | Duplex  | Kirjeldus                                                                             |
| --------------- | -------- | ------- | ------------------------------------------------------------------------------------- |
| **GSM900**      | GSM 900  | **FDD** | 2G võrk 900 MHz sagedusel. Kasutatakse peamiselt kõnedeks ja IoT/M2M seadmetele.      |
| **B1**          | LTE2100  | **FDD** | 4G LTE 2100 MHz. Hea kompromiss leviala ja mahutavuse vahel.                          |
| **B3**          | LTE1800  | **FDD** | 4G LTE 1800 MHz. Tele2 peamine LTE mahutavussagedus.                                  |
| **B8**          | LTE900   | **FDD** | 4G LTE 900 MHz. Hea leviala ja siselevi.                                              |
| **B20**         | LTE800   | **FDD** | 4G LTE 800 MHz. Väga hea maapiirkondade ja hoonete sisene leviala.                    |
| **n1**          | NR2100   | **FDD** | 5G NR 2100 MHz. Kasutatakse DSS-i või eraldiseisva NR kandjana.                       |
| **n28**         | NR700    | **FDD** | 5G NR 700 MHz. Väga suur leviala ja hea siselevi.                                     |
| **n40**         | NR2300   | **TDD** | 5G NR 2300 MHz. Lisamahutavus suurema liiklusega piirkondades.                        |
| **n78**         | NR3500   | **TDD** | 5G NR 3500 MHz. Tele2 peamine suure kiiruse ja mahutavusega 5G sagedus.               |
| **n258**        | NR26GHz  | **TDD** | 5G mmWave 26 GHz. Väga suur kiirus, kuid väga väike leviala; kasutatakse erijuhtudel. |

### FDD vs TDD

| Duplex                              | Selgitus                                                                                                                                                                                         |
| ----------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **FDD (Frequency Division Duplex)** | Üleslink (UL) ja allalink (DL) kasutavad **kahte erinevat sagedust**. Sobib hästi suure levialaga võrkudele ning on kasutusel enamikul 2G ja 4G sagedustest ning ka 5G n1 ja n28 puhul.          |
| **TDD (Time Division Duplex)**      | Üleslink ja allalink kasutavad **sama sagedust**, kuid erinevatel ajahetkedel. Võimaldab paindlikult jagada DL/UL mahtu ning sobib hästi suure läbilaskevõimega 5G sagedustele (n40, n78, n258). |.

