# Nokia MantaRay NM -- RET (Remote Electrical Tilt) seadistamine

## Eesmärk

RET (Remote Electrical Tilt) võimaldab muuta antenni elektrilist
kaldenurka kaugjuhtimise teel ilma masti ronimata.

Enne RET väärtuste seadistamist tuleb MantaRay NM-is siduda õiged RET-id
(ALD-d) õigete antenniportide ja raadiomoodulitega.

------------------------------------------------------------------------

# 1. Ava RET Commissioning

MantaRay NM-is:

``` text
Commissioning Wizard
    ↓
Antenna Line Devices
    ↓
Antenna Line Devices RET
```

Vajadusel ava RET-id "+" märgiga lahti.

------------------------------------------------------------------------

# 2. Mõista RMOD paigutust

Tüüpilises 6 raadiomooduliga sektoris:

  Moodul   Sagedus
  -------- ---------------
  RMOD-1   Madal sagedus
  RMOD-2   Madal sagedus
  RMOD-3   Madal sagedus
  RMOD-4   Kõrge sagedus
  RMOD-5   Kõrge sagedus
  RMOD-6   Kõrge sagedus

Näiteks:

-   RMOD-3 → madala sageduse raadio
-   RMOD-6 → sama sektori kõrge sageduse raadio

Need töötavad tavaliselt sama antenni küljes.

------------------------------------------------------------------------

# 3. Ühise antenni loogika

Kui üks antenn teenindab nii madalaid kui kõrgeid sagedusi, siis on
mõlemal oma RET.

``` text
              Antenn

          ANT1
          ANT2
          ANT3
          ANT4

             ▲
       RET (madal)

             ▲
       RET (kõrge)

             ▲
     RMOD-3      RMOD-6
```

Seetõttu tuleb RET-id siduda mõlema vastava raadiomooduliga.

------------------------------------------------------------------------

# 4. Millised moodulid kuuluvad kokku?

  Madal sagedus   Kõrge sagedus
  --------------- ---------------
  RMOD-1          RMOD-4
  RMOD-2          RMOD-5
  RMOD-3          RMOD-6

Need moodustavad üldjuhul sama sektori.

------------------------------------------------------------------------

# 5. RET tähiste lugemine

RET-id tunneb ära nende seerianumbri lõpu järgi.

  RET   Antenniport   Kasutus
  ----- ------------- ---------------
  R1    ANT1--ANT2    Madal sagedus
  R2    ANT3--ANT4    Madal sagedus
  Y1    ANT1--ANT2    Kõrge sagedus
  Y2    ANT3--ANT4    Kõrge sagedus

### Madala sageduse ALD-d

-   AHPMDB
-   AHPMDG
-   AHPMDJ

### Kõrge sageduse ALD-d

-   AHEGA
-   AHEGB
-   AHEGG
-   AHEGI

------------------------------------------------------------------------

# 6. Võimalikud erandid

Kui kasutatakse tähiseid nagu **Y3**, **Y4**, **Y5** või **P1**,
kontrolli alati antenni tootja dokumentatsiooni.

------------------------------------------------------------------------

# 7. RET sidumine

RETU-1 alt vali iga RET jaoks õiged antenniportid.

Näide:

-   RMOD-3 kasutab RET-i **Y2**
-   Y2 juhib **ANT3--ANT4**
-   Sama sektori kõrge sageduse moodul **RMOD-6** kasutab samuti seda
    RET-i.

Lõpeta töö:

``` text
Done
↓
Validate
↓
Activate Plan
```

------------------------------------------------------------------------

# 8. Kust leida õige info?

## Antenni spetsifikatsioon

Sealt leiad:

-   RET tähised
-   Antenniportide jaotuse
-   RET-de arvu

## Rollout Excel

Vaata:

-   **Ant Info**
-   **Comment**

Seal on kirjas antenni mudel ning vajalikud RET Tilt väärtused.

------------------------------------------------------------------------

# 9. RET väärtuste määramine

Pärast RET-ide sidumist määra Electrical Tilt väärtused Rollout Exceli
järgi.

------------------------------------------------------------------------

# RET ja LTE / 5G seos

Üks antenn võib teenindada samaaegselt:

-   GSM900
-   LTE800
-   LTE900
-   LTE1800
-   LTE2100
-   NR1800
-   NR2100
-   NR3500

RET (Remote Electrical Tilt) muudab antenni elektrilist kaldenurka, ilma et antenni füüsilist asendit muudetaks. Antenni korpus jääb samasse asendisse, kuid antenni kiirgusdiagrammi suunatakse elektrooniliselt üles- või allapoole. See mõjutab kõiki sagedusi ja tehnoloogiaid, mis kasutavad seda antenni (nt 2G, 4G ja 5G), kui need on ühendatud sama antenni külge.

------------------------------------------------------------------------

# Kiirspikker

``` text
Commissioning Wizard
        ↓
Antenna Line Devices
        ↓
Antenna Line Devices RET
        ↓
Leia õige ALD
        ↓
Määra õiged ANT1–ANT4 portid
        ↓
Done
        ↓
Validate
        ↓
Activate Plan
        ↓
Määra RET Tilt väärtused Rollout Exceli järgi
```
