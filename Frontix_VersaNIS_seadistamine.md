Jah. Panin need loogilisse järjekorda nii, et need oleksid kasutatavad tööjuhendina.



\---



\# VersaNIS / Frontix Integrity – SRAN seadistamine (offline)



\## 1. Töö algus



\* Holger saadab e-kirja järgmise nädala laienduste ja tööde kohta.

\* Kirjast on näha:



&#x20; \* millised tugijaamad (site'id) lähevad muutmisele;

&#x20; \* milliseid sagedusi lisatakse (nt \*\*L18, L21\*\* jne);

&#x20; \* vajadusel kommentaarid.



\### Kontrolli



\* Kas kasutatakse õiget \*\*ASIM\*\* või \*\*ASIB\*\* süsteemimoodulit.

\* Lisa õige \*\*Configuration Template (ConfiTemplate)\*\*.



Näide:



\* Kanaküla (KAN386)

\* Lisatakse näiteks:



&#x20; \* L18

&#x20; \* L21

&#x20; \* jne.



\---



\# 2. Riistvara moodulid



\## Madalsagedusmoodulid



Tavaliselt mudel:



\*\*AHPMDG\*\*



Toetavad sagedusi:



\* 700 MHz

\* 800 MHz

\* 900 MHz



Tavaliselt 3 tk.



\---



\## Kõrgsagedusmoodulid



Tavaliselt mudel:



\*\*AHEGG\*\*



Samuti tavaliselt 3 tk.



\---



\# 3. VersaNIS avamine



VersaNIS = Frontix Integrity.



Baltikumi ühine tööriist.



Ava:



```

Locations

&#x20;   ↓

372 Estonia

&#x20;   ↓

RAN

```



Seal asuvad kõik SRAN-id.



\---



\# 4. Tugijaama leidmine



Näiteks Kanaküla.



\* Tee aktiivseks RAN aken.

\* Vajuta \*\*Ctrl + F\*\*.

\* Otsi:



```

KAN386

```



või



```

62996

```



Avaneb vastav tugijaam.



\---



\# 5. Equipment puu



Mine:



```

KAN386

&#x20;   ↓

All Equipment

```



Seal on kaks põhiosa.



\## Cabinet



Sisaldab:



\* süsteemimoodulit

\* Baseband Unit (BBU)



\---



\## Mast



Sisaldab:



\* raadiomooduleid (Radio Modules)



\---



\# 6. Vana konfiguratsiooni eemaldamine



Mine masti ossa.



Paremklõps:



```

Remove conn. from equipment and child

```



See eemaldab:



\* optikaühendused

\* süsteemimooduli ja raadiomooduli vahel.



Pärast seda:



\* kustuta mastiosa.



Vajadusel tee uuesti:



```

Remove connections

```



või



```

Delete

```



Kui valmis, siis:



\*\*Kanaküla riistvara on vanast konfiguratsioonist puhas.\*\*



See on ainult \*\*offline muudatus\*\*, mitte võrgu muudatus.



\---



\# 7. Uue Equipment Template lisamine



Mine:



```

Secondary Tree View

&#x20;   ↓

Equipment Templates

&#x20;   ↓

372 Estonia

&#x20;   ↓

RAN

&#x20;   ↓

Cabinet / Frame

&#x20;   ↓

AS (AirScale)

```



Levinud template:



```

3SectorAS N7 New Eq

```



See sisaldab tavaliselt:



\* kõik LTE sagedused

\* GSM900

\* 5G N700



Template peal klõpsates saab alumisest aknast vaadata:



\* moodulid

\* raadiod

\* süsteemimoodulid



\---



\# 8. Template paigaldamine



Haara template hiirega.



Lohista:



```

KAN386

```



peale.



Sellega luuakse uus riistvara.



\---



\# 9. BSSInfo kontroll



Leia:



```

LNBTS-140386

```



See on:



4G eNodeB ID.



See number tuleb hiljem profiili lisada.



\---



\# 10. eNodeB ID määramine



Mine:



```

All Equipment

&#x20;   ↓

Cabinet

&#x20;   ↓

Shelf

&#x20;   ↓

Profile

```



Leia:



```

ENodeBId

```



Paremklõps



```

Update Parameter

```



Sisesta:



```

140386

```



Pärast seda on shelf näiteks:



```

BBU04

```



\---



\# 11. Functional Network avamine



Mine:



```

Shelf

&#x20;   ↓

Profile

&#x20;   ↓

Network Element

```



Paremklõps:



```

Go to Functional Network

```



Avaneb näiteks:



```

KAN386-BBU04-001

```



\---



\# 12. Cellide parandamine



Template loob vaikimisi:



```

A

B

C

```



Aga võrgu järgi peab olema:



```

A

B

D

```



Seega:



\* asenda C → D



Vajadusel:



```

Update Interface

```



ja muuda viimased numbrid vastavaks.



\---



\# 13. Layered Network



Üleval:



```

Layered Network

```



Seal on:



\* 2G

\* 4G

\* 5G



Need määravad, millised tehnoloogiad kasutavad sama SRAN-i.



\---



\## 2G lisamine



Mine:



```

2G

&#x20;   ↓

Layered Network Elements

```



Leia:



```

KAN386

```



(vajadusel Refresh)



Paremklõps:



```

Relate LNE to Equipment

```



Vali:



Type:



```

Shelf

```



Label:



```

BBU04

```



OK.



\---



\## 4G ja 5G lisamine



Mine:



```

4G

```



ja



```

5G

```



Paremklõps:



```

Add Layered Network Element Ex

```



Location Name:



```

KAN386

```



Equipment:



```

Shelf

```



OK.



Kui küsib järgmisi layer'eid:



```

No

```



\---



\# 14. CMDB Sync



Ava veebis:



```

NEM RAN BALTICS

```



Mine:



```

Tools

&#x20;   ↓

Configuration Management Database Sync (CMDB Sync)

```



Vajuta:



```

Trigger

```



See:



\* küsib VersaNIS-ist andmed;

\* uuendab CMDB vastavalt tehtud muudatustele.



\---



\# 15. Tabeli täitmine



Kui NIS-is on töö valmis:



märgi tabelisse:



```

Y

```



\---



\# Kiire töövoog



1\. Vaata Holgeri e-kiri.

2\. Kontrolli lisatavad sagedused.

3\. Leia site VersaNIS-ist.

4\. Kustuta vana riistvara.

5\. Lohista õige AirScale template.

6\. Lisa eNodeB ID.

7\. Ava Functional Network.

8\. Paranda cellid (ABC → ABD).

9\. Seo 2G, 4G ja 5G Layered Networkiga.

10\. Käivita CMDB Sync.

11\. Märgi töö tabelis tehtuks (`Y`).



Sellisel kujul on märkmed juba üsna lähedal samm-sammulisele tööjuhendile, mida saad uue SRAN-i seadistamisel lihtsalt järjekorras läbi teha.



