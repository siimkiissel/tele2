# Nokia SRAN laiendamine – praktiline tööjuhend

See juhend kirjeldab tüüpilist töövoogu uue raadiomooduli ja cellide lisamisel Nokia NetAct / MantaRay NM keskkonnas.

---

# 1. MCF ja Data Center

## MCF (Master Configuration File)

MCF sisaldab tugijaama põhikonfiguratsiooni ning seda kasutatakse:
- konfiguratsiooni varundamiseks (backup)
- reprocessimiseks
- XML konfiguratsioonide genereerimiseks

---

# 2. Riistvara

## ABIO
- Kasutatakse 4G (LTE) ja 5G (NR) jaoks.

## ABIA
- Kasutatakse 2G (GSM) jaoks.

## AHEGG

Kõrgema sageduse raadiosaatja (Radio Module), mida kasutatakse uue sageduskihi lisamisel.

Lisamine:

1. Ava **Shelf**.
2. Lohista **AHEGG** seadme **MAST Root** alla.

---

# 3. Vendor Radio Module

Mine:

`Profile`

Vali:

`Vendor Radio Modules`

Paremklõps:

`Update Parameter`

Vali vaba ID (nt **8**).

---

# 4. Optical Interface

Ava:

`AHEGG → Sub Interface → Optical Interface 1`

Seal määratakse:

- RX
- TX

Ühendus:

- TX → RX
- RX → TX

---

# 5. Uue Celli loomine

Mine:

`Network Element → Functional Elements`

Paremklõps:

`Add Interface`

Näiteks:

`Cell G4A71`

Kui kõik õnnestub:

`Interface successfully added`

---

# 6. Cellide tähistus

| Tähis | Tehnoloogia |
|-------|-------------|
| puudub täht | 4G LTE |
| G | 2G GSM |
| N | 5G NR |

Näited:

- 5841 → 4G
- G4A71 → 2G
- N2158 → 5G

Cell ID kuvatakse sageli HEX-kujul.

---

# 7. Antenniportide määramine

Pärast Celli loomist tuleb määrata antenniport.

Lihtsaim viis:

- vaata olemasoleva sama sektori Celli porte
- kasuta samu porte uuel Cellil

Näiteks:

- ANT1
- ANT2

5G puhul kasutatakse tavaliselt kahte RF-porti.

---

# 8. Vendor Antenna Line Usage

Mine:

`Profile → vendor-antennaLine-usage`

Paremklõps:

`Update Parameter`

Määra uuele Cellile õige antenniliin.

---

# 9. Planned Cells

Planned Cellid saadakse tavaliselt:

- LLD
- ClickOnSite

Need määravad, millised Cellid tuleb lisada.

---

# 10. NEM

Mine:

`NEM → Devices`

Otsi soovitud site.

Seejärel vali:

- Reprocess Backup
- või Reprocess

---

# 11. BTS Config

Mine:

`Tools → BTS Config`

Kui konfiguratsioon on korrektne, genereeritakse XML konfiguratsioonifail.

---

# 12. XML laadimine tugijaama

1. Logi tugijaama IP-aadressiga sisse.
2. Laadi genereeritud XML üles.

4G ja 5G sektorid lisatakse XML konfiguratsioonifaili kaudu.

---

# 13. 2G lisamine

2G seadistamine tehakse eraldi.

Kasutatakse:

`CM Editor`

CM Editor avaneb:

`NetAct / MantaRay NM`

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
