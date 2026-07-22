# VersaNIS / Frontix Integrity – SRAN seadistamine (offline)

---

# 1. Töö algus

Holger saadab e-kirja järgmise nädala laienduste ja tööde kohta.

Kirjast on näha:

* millised tugijaamad (site'id) lähevad muutmisele;
* milliseid sagedusi lisatakse (nt **L18**, **L21** jne);
* vajadusel kommentaarid.

## Kontrolli

* kas kasutatakse õiget **ASIM** või **ASIB** süsteemimoodulit;
* lisa õige **Configuration Template (ConfiTemplate)**.

Näide:

* Kanaküla (**KAN386**)
* Lisatakse näiteks:

  * **L18**
  * **L21**
  * jne

---

# 2. Riistvara moodulid

## Madalsagedusmoodulid

Tavaliselt mudel:

**AHPMDG**

Toetavad sagedusi:

* 700 MHz
* 800 MHz
* 900 MHz

Tavaliselt 3 tk.

---

## Kõrgsagedusmoodulid

Tavaliselt mudel:

**AHEGG**

Toetavad kõrgemaid sagedusi (nt 1800/2100 MHz).

Samuti tavaliselt 3 tk.

---

# 3. VersaNIS avamine

**VersaNIS** = **Frontix Integrity**

Baltikumi ühine tööriist.

Ava:

```text
Locations
    ↓
372 Estonia
    ↓
RAN
```

Seal asuvad kõik SRAN-id.

---

# 4. Tugijaama leidmine

Näiteks **Kanaküla**.

* Tee aktiivseks **RAN** aken.
* Vajuta **Ctrl + F**.
* Otsi:

```text
KAN386
```

või

```text
62996
```

Avaneb vastav tugijaam.

---

# 5. Equipment puu

Mine:

```text
KAN386
    ↓
All Equipment
```

Seal on kaks põhiosa.

## Cabinet

Sisaldab:

* süsteemimoodulit;
* Baseband Unit (**BBU**).

## Mast

Sisaldab:

* raadiomooduleid (**Radio Modules**).

---

# 6. Vana konfiguratsiooni eemaldamine

Mine masti ossa.

Paremklõps:

```text
Remove conn. from equipment and child
```

See eemaldab:

* optikaühendused;
* süsteemimooduli ja raadiomooduli vahelised ühendused.

Pärast seda:

* kustuta mastiosa.

Vajadusel tee uuesti:

```text
Remove connections
```

või

```text
Delete
```

Kui valmis, siis on riistvara vanast konfiguratsioonist puhas.

**NB!** Tegemist on ainult **offline muudatusega**, mitte võrgu muudatusega.

---

# 7. Uue Equipment Template lisamine

Mine:

```text
Secondary Tree View
    ↓
Equipment Templates
    ↓
372 Estonia
    ↓
RAN
    ↓
Cabinet / Frame
    ↓
AS (AirScale)
```

Levinud template:

```text
3SectorAS N7 New Eq
```

See sisaldab tavaliselt:

* kõik LTE sagedused;
* GSM900;
* 5G N700.

Template peal klõpsates saab alumisest aknast vaadata:

* mooduleid;
* raadioid;
* süsteemimooduleid.

---

# 8. Template paigaldamine

Haara template hiirega.

Lohista:

```text
KAN386
```

peale.

Sellega luuakse uus riistvara.

---

# 9. BSSInfo kontroll

Leia:

```text
LNBTS-140386
```

See on **4G eNodeB ID**.

See number tuleb hiljem profiili lisada.

---

# 10. eNodeB ID määramine

Mine:

```text
All Equipment
    ↓
Cabinet
    ↓
Shelf
    ↓
Profile
```

Leia:

```text
ENodeBId
```

Paremklõps:

```text
Update Parameter
```

Sisesta:

```text
140386
```

Pärast seda on shelf näiteks:

```text
BBU04
```

---

# 11. Functional Network avamine

Mine:

```text
Shelf
    ↓
Profile
    ↓
Network Element
```

Paremklõps:

```text
Go to Functional Network
```

Avaneb näiteks:

```text
KAN386-BBU04-001
```

---

# 12. Cellide parandamine

Template loob vaikimisi:

```text
A
B
C
```

Aga võrgu järgi peab olema:

```text
A
B
D
```

Seega:

* asenda **C → D**.

Vajadusel:

```text
Update Interface
```

ja muuda viimased numbrid vastavaks.

---

# 13. Layered Network

Üleval:

```text
Layered Network
```

Seal on:

* 2G
* 4G
* 5G

Need määravad, millised tehnoloogiad kasutavad sama SRAN-i.

## 2G lisamine

Mine:

```text
2G
    ↓
Layered Network Elements
```

Leia:

```text
KAN386
```

(vajadusel **Refresh**)

Paremklõps:

```text
Relate LNE to Equipment
```

Vali:

**Type**

```text
Shelf
```

**Label**

```text
BBU04
```

Vajuta **OK**.

---

## 4G ja 5G lisamine

Mine:

```text
4G
```

ja

```text
5G
```

Paremklõps:

```text
Add Layered Network Element Ex
```

Täida:

**Location Name**

```text
KAN386
```

**Equipment**

```text
Shelf
```

Vajuta **OK**.

Kui küsib järgmisi layereid:

```text
No
```

---

# 14. CMDB Sync

Ava veebis:

```text
NEM RAN BALTICS
```

Mine:

```text
Tools
    ↓
Configuration Management Database Sync (CMDB Sync)
```

Vajuta:

```text
Trigger
```

See:

* küsib VersaNIS-ist andmed;
* uuendab CMDB-d vastavalt tehtud muudatustele.

---

# 15. Tabeli täitmine

Kui NIS-is on töö valmis, märgi tabelisse:

```text
Y
```

---

# Kiire töövoog

1. Vaata Holgeri e-kiri.
2. Kontrolli lisatavad sagedused.
3. Leia site VersaNIS-ist.
4. Kustuta vana riistvara.
5. Lohista õige AirScale template.
6. Lisa eNodeB ID.
7. Ava Functional Network.
8. Paranda cellid (**ABC → ABD**).
9. Seo 2G, 4G ja 5G Layered Networkiga.
10. Käivita CMDB Sync.
11. Märgi töö tabelis tehtuks (**Y**).
