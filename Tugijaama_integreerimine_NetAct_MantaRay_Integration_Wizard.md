# Tugijaama integreerimine NetActi (MantaRay Integration Wizard)

## Eesmärk
<img width="936" height="877" alt="image (1)" src="https://github.com/user-attachments/assets/c2592e13-ba36-4e2f-ab0a-79c9d535150f" />

Integreerimise eesmärk on lisada uus Nokia SRAN tugijaam NetActi võrguhaldusesse, et seda oleks võimalik hallata, monitoorida ja seadistada.

---

# 1. MantaRay Integration Wizard

Integreerimine toimub **MantaRay Integration Wizardi** abil.

Wizard loob NetActi vajalikud objektid ning lisab uue tugijaama võrguhaldusesse.

---

# 2. Olulisemad väljad

## MO Class

Näitab, millist tüüpi võrguelement lisatakse.

Näide:

`MO Class: MRBTS`

**MRBTS** = Multi Radio Base Transceiver Station

See on Nokia SRAN tugijaama põhielement.

---

## MO Release

Näitab tarkvara versiooni.

Näide:

`SBTS25R3`

See tähendab, et tugijaam kasutab Nokia SBTS tarkvara versiooni 25R3.

---

## Maintenance Region (MR)

Määrab, millisesse hoolduspiirkonda tugijaam kuulub.

Näited:

- MRC-C1
- MR-EE_SRAN

See aitab NetActis seadmeid organiseerida.

---

## Distinguished Name (DN)

Näide:

`PLMN-PLMN/MRBTS-160719`

DN on objekti täielik identifikaator NetActis.

Selle järgi tunneb NetAct tugijaama ära.

---

## NE Presentation Name

Näide:

`EE-719-Painurme`

See on kasutajale nähtav nimi NetActis.

Koosneb tavaliselt:
- riik
- site number
- objekti nimi

---

## MRBTS IP aadress

Näide:

`10.55.34.43`

See on juhtimisliidese (management interface) IP-aadress, mille kaudu NetAct suhtleb tugijaamaga.

---

## NE3SWS Agent Security Mode

Näide:

`Non_TLS`

Määrab, kas ühendus toimub TLS krüpteeringuga või ilma.

Vanemates lahendustes kasutatakse sageli **Non_TLS** režiimi.

---

# 3. Kui integreerimine õnnestub

NetActis muutub võrguobjekti olek roheliseks.

See tähendab, et:
- ühendus töötab;
- NetAct näeb tugijaama;
- haldus on edukalt loodud.

---

# 4. SRAN ja IP-aadressid

## Vanemad Nokia süsteemid

Vanematel BTS-idel oli peaaegu igal moodulil oma IP-aadress.

## Nokia SRAN

SRAN-is kasutatakse ühtset arhitektuuri.

Tavaliselt on üks management IP kogu tugijaamale.

Mõnikord räägitakse siiski "2G IP-st", sest:
- 2G BSC peab suutma tugijaamaga ühendust võtta;
- osa 2G juhtimisest kasutab endiselt BSC ühendust;
- ajalooliselt nimetatakse seda lihtsalt 2G IP-ks.

---

# 5. NWE

**NWE = Network Element**

See tähendab võrguobjekti (tugijaama), mida NetAct haldab.

---

# 6. BSC

**BSC = Base Station Controller**

BSC juhib GSM (2G) tugijaamu.

Tema ülesanded:
- kanalite haldus;
- handover;
- TRX juhtimine;
- BTS juhtimine;
- konfiguratsioon;
- alarmide haldus.

SRAN-is on 2G endiselt loogiliselt seotud BSC-ga.

---

# 7. PuTTY

PuTTY kasutatakse võrgu seadmetesse sisse logimiseks.

Näiteks:
- BSC
- MGW
- serverid
- Linux hostid

Ühendus toimub tavaliselt SSH kaudu.

---

# 8. MML käsud

**MML = Man Machine Language**

See on Nokia käsurea halduskeel.

Paljud käsud algavad tähega **Z**.

Näiteks:

`ZEEI`

---

# 9. Käsk ZEEI

Näiteks:

`ZEEI:BSC=1905;`

Annab infot BCF-ide kohta.

---

# 10. BCF

**BCF = Base Control Function**

2G BTS juhtobjekt.

Näide:

`BCF=1905`

BCF all paiknevad:
- sektorid;
- TRX-id;
- GSM konfiguratsioon.

BCF kaudu saab:
- sektoreid avada ja sulgeda;
- kontrollida konfiguratsiooni;
- vaadata tööolekut.

---

# Kiire meelespea

| Mõiste | Tähendus |
|---------|----------|
| MantaRay Integration Wizard | SRAN tugijaama lisamine NetActi |
| MRBTS | Nokia SRAN tugijaam |
| SBTS25R3 | Tarkvaraversioon |
| Maintenance Region | Hoolduspiirkond |
| Distinguished Name | Võrguobjekti täielik nimi |
| NE Presentation Name | NetActis kuvatav nimi |
| MRBTS IP | Tugijaama juhtimis-IP |
| Non_TLS | Krüpteerimata ühendus |
| NWE | Network Element |
| BSC | Base Station Controller |
| MML | Man Machine Language |
| ZEEI | BCF info kuvamise käsk |
| BCF | Base Control Function |
