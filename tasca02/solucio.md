# Selecció d’un SAI per una empresa client

**Autora:** Isabel Bosch Millastre  
**Alumne:** Biel Batalla Rabassa  
**Data:** 30/09/2025  
**Curs:** SMX 2B  
**Unitat:** T02 (https://drive.google.com/drive/folders/1xEQrf-oKSBCoxjOjroSRnflnILGCvjE3?usp=sharing)

---

## Índex

1. [Descripció del cas](#descripció-del-cas)  
2. [Càlculs realitzats](#càlculs-realitzats)  
   - [Inventari d’equips](#inventari-dequips)  
   - [Models utilitzats](#models-utilitzats)  
   - [Càlcul de potència total](#càlcul-de-potència-total)  
   - [Determinació de l’autonomia del SAI](#determinació-de-lautonomia-del-sai)  
3. [Models analitzats](#models-analitzats)  
4. [Taula comparativa](#taula-comparativa)  
5. [Justificació de la selecció final](#justificació-de-la-selecció-final)

---

## Descripció del cas

L’empresa **TecnoGestió S.L.**, dedicada a la gestió documental i assessorament informàtic, té un petit despatx amb 4 ordinadors de sobretaula, una impressora-fotocopiadora multifunció (similar a les que té l’escola) i un router d’accés a Internet.  

Davant les constants incidències amb el subministrament elèctric a la zona, la direcció ha decidit adquirir un **SAI** per garantir la continuïtat del servei i protegir els equips.  

S’han posat en contacte amb l’empresa on esteu fent l’estada i el vostre responsable us ha encarregat que en feu l’estudi i tria del SAI.

---

## Càlculs realitzats

### Inventari d’equips

Al SAI es connectaran:

- 4 Ordinadors  
- 4 Monitors  
- 1 Router  
- *(La impressora-fotocopiadora **no** estarà connectada al SAI)*

---

### Models utilitzats

**PC:** [Intel Core i5-12400 / 16GB / 500GB SSD](https://www.pccomponentes.com/pccom-work-intel-core-i5-12400-16gb-500gb-ssd-windows-11-home)  
- Ordinador: 585 VA × 4  
- CPU: 65 VA × 4  
- **Total:** 2340 VA + 260 VA = **2600 VA / 2340 W**

**Monitor:** [MSI PRO MP251 24.5" IPS FullHD 100Hz](https://www.pccomponentes.com/monitor-msi-pro-mp251-245-ips-fullhd-100hz)  
- **Total:** 55 VA × 4 = **220 VA / 198 W**

**Router:**  
- **Total:** 39 VA / 35 W

---

### Càlcul de potència total

**Total de consum:**

| Tipus | Valor sense marge | +20% marge |
|:------|:----------------:|:-----------:|
| **VA** | 2859 VA | **3431 VA** |
| **W** | 2573 W | **3088 W** |

> Necessitem un SAI amb una capacitat **superior a 3500 VA i 3100 W.**

---

### Determinació de l’autonomia del SAI

Com que el SAI s’adquireix per garantir la continuïtat temporal per **guardar treballs i apagar correctament**, una **autonomia de 10 minuts** és adequada.  
Per tant, necessitarem un SAI amb un **runtime ≥ 10 minuts.**

---

## Models analitzats

### **SLC-4000-TWIN PRO3**
- **Potència:** 4000 VA / 4000 W  
- **Tipus:** On-line, doble conversió, torre  
- **Avantatges:** suficient per cobrir la càrrega amb el 20 % de reserva  
- **Inconvenients:** marge d’expansió limitat

---

### **SLC-4000-TWIN RT3**
- **Potència:** 4000 VA / 4000 W  
- **Tipus:** On-line, doble conversió, torre/rack  
- **Avantatges:** versàtil i compatible amb racks  
- **Inconvenients:** poc marge per expansions

---

### **SLC-7,5-CUBE4**
- **Potència:** 7500 VA / 7500 W  
- **Tipus:** On-line, doble conversió, professional  
- **Avantatges:** permet afegir més equips i té més autonomia  
- **Inconvenients:** cost i consum més elevats per un despatx petit

---

## Taula comparativa

| Model | Potència (VA/W) | Cobreix requisits | Autonomia estimada | Expansió futura | Observacions |
|:------|:----------------|:------------------|:--------------------|:----------------|:--------------|
| **SLC-4000-TWIN PRO3** | 4000 VA / 4000 W | Sí (reserva justa) | 10–12 min | Baixa | Torre bàsica |
| **SLC-4000-TWIN RT3** | 4000 VA / 4000 W | Sí (reserva justa) | 10–12 min | Baixa | Torre o rack, més flexible |
| **SLC-7,5-CUBE4** | 7500 VA / 7500 W | Sí (molt sobrat) | >20 min | Alta | Gran cost i dimensió |

---

## Justificació de la selecció final

Dels tres models proposats, la millor opció és el **SAI SLC-4000-TWIN RT3**.  
Aquest equip ofereix una potència que cobreix de sobres els valors necessaris i permet treballar amb un **marge de seguretat adequat**. El seu format **rack/torre** el fa més versàtil que el model PRO3.

Aquest SAI pot mantenir els equips en funcionament durant **10 minuts**, el temps necessari per **guardar el treball i apagar correctament** els ordinadors en cas d’interrupció del subministrament elèctric.

En comparació, el model **SLC-7,5-CUBE4**, tot i ser més potent, **supera les necessitats reals** i implica un cost i consum més elevats.

> **Conclusió:** el model **SLC-4000-TWIN RT3** és la solució més equilibrada en prestacions, flexibilitat i cost. Compleix els objectius de potència i autonomia, garantint seguretat en moments crítics.

