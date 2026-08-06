# Merenje dielektrične konstante piezo-elementima

*2026-05-04*


---


**Zoran:**

Zdravo : )
Teorijski, ova jednačina bi mogla da se koristi za određivenja/merenje $\epsilon$:
$$\varepsilon = \frac{2Fd^2}{SU^2}$$
npr. pomoću piezo-elemenata, ili pomoću osetljive, precizne vage.
Zanima me ... red veličina koje bi trebalo da imaju elementi koji su na desnoj strani, da bi merenje bilo ... realno, ostvarljivo. I dovoljno precizno.



**Claude:**

Zdravo! Lepo pitanje — hajde da to razrešimo konkretno.

## Kontekst jednačine

Ovo je elektrostatička sila između ploča kondenzatora izražena kroz ε:

$$\varepsilon = \frac{2F d^2}{S U^2}$$

gde je:
- $F$ — sila privlačenja između ploča
- $d$ — rastojanje između ploča
- $S$ — površina ploča
- $U$ — napon

---

## Propagacija greške (ključno pre nego što biramo veličine)

$$\frac{\delta\varepsilon}{\varepsilon} = \sqrt{\left(\frac{\delta F}{F}\right)^2 + \left(\frac{2\,\delta d}{d}\right)^2 + \left(\frac{\delta S}{S}\right)^2 + \left(\frac{2\,\delta U}{U}\right)^2}$$

Odmah se vidi: **$d$ ulazi sa kvadratom**, što znači da je merenje rastojanja između ploča **najkritičniji faktor**. Relativna greška u $d$ udvostručuje se u konačnom rezultatu.

---

## Realni opsezi veličina

Za $\varepsilon_0 \approx 8{,}854 \times 10^{-12}$ F/m, $F = \varepsilon_0 S U^2 / (2d^2)$, pa možemo da iteriramo:

| Parametar | Skromna varijanta | Laboratorijska varijanta |
|---|---|---|
| $U$ | 500 V | 1000 V |
| $d$ | 1 mm | 1 mm |
| $S$ | 100 cm² (10×10 cm) | 100 cm² |
| **$F$ (izračunato)** | **≈ 11 mN ≈ 1,1 g** | **≈ 44 mN ≈ 4,5 g** |

Sila je **red mili-Njutna** — dakle, ne pikonjutni svet, ali ni gde se oseća rukom.

---

## Merljivost sile

| Metoda | Rezolucija | Komentar |
|---|---|---|
| Analitička vaga | ~0,01 mg ≈ 0,1 μN | Odlično — relativna greška <0,01% za F≈4,5g |
| Piezo senzor sile | ~0,1–1 mN | Brže, ali kalibracijski zahtevnije |
| Torzione vage | sub-μN | Složenost raste |

Analitička vaga je verovatno **najpraktičniji izbor** za kućnu/laboratorijsku realizaciju.

---

## Merljivost ostalih veličina

**Napon $U$:** Stabilan HV izvor + precizni voltmetar → 10–100 ppm realno. Greška: ~0,01%.

**Rastojanje $d$:** Ovo je **Ahilova peta** čitavog merenja.
- Mikrometarskim vijkom: ~1 μm rezolucija → $\delta d / d \approx 0,1\%$ → doprinos greški u $\varepsilon$: **0,2%**
- Optički interferometar (LaserHead ili slično): sub-nm → merenje više nije ograničavajuće
- Praktičan kompromis: **mehanički džig sa kalibriranim razmakom** (npr. staklene perlice poznatog promera kao spejseri)

**Površina $S$:** Klijer/CMM → merljivo na 0,01% bez problema. Nije ograničavajuće.

---

## Sistematske greške — ne smeju se zanemariti

1. **Ivični efekti (fringe fields)** — ploče konačne veličine, polje "curi" oko ivica. Klasično rešenje: **Kelvin-ova zaštitna prstenasta elektroda** (guard ring). Bez nje, greška može biti ~1% i više.

2. **Paralelnost ploča** — nagib od samo 10 μrad na 10 cm ploči unosi grešku u efektivnom $d$.

3. **Kontaktni napon** — na niskim naponima može biti značajan; na 500–1000 V je zanemarljiv.

---

## Sumarni budžet grešaka (realna laboratorijska varijanta)

| Izvor | Rel. greška |
|---|---|
| $F$ (analitička vaga) | ~0,02% |
| $d$ (mikrometar) | ~**0,2%** (dominantna) |
| $S$ (klijer) | ~0,01% |
| $U$ (precizni voltmetar) | ~0,02% |
| **Ukupno** | **~0,3–0,5%** |

Uz guard ring i interferometarsko merenje $d$: može ući u region **0,01–0,05%** — što je respektabilno za apsolutno merenje $\varepsilon_0$.

---

**Zaključak:** Merenje je apsolutno realno sa relativno skromnom opremom. Najvažnija ulaganja su u precizno definisanje rastojanja $d$ i geometriju guard ring elektrode. Piezo opcija je zanimljiva za dinamička merenja, ali analitička vaga daje bolji signal/šum za statička merenja ove veličine sile.

Jesi li razmatrao konkretnu geometriju ploča, ili je ovo još uvek na nivou procene izvodljivosti?



**Zoran:**

Nisam, ovo je još uvek na nivou procene izvodljivosti, ali što se tiče geometrije, ... ne znam, tu bih išao na kružne ploče (krug, najlakše i najpreciznije se može "iseći" takva ploča o bakra (pretpostavljam))



**Claude:**

Dobar instinkt! Kružne ploče imaju nekoliko konkretnih prednosti ovde:

## Zašto kružne ploče — dobri razlozi

**Mehanički:** Laserskim ili vodenim rezanjem, kružni disk od bakarne ploče (npr. PCB bakar ili čist Cu) može se iseci na prečnik tačan na ~10–50 μm bez posebne opreme. Pravougaona ploča je nominalno jednostavnija, ali ivice su podložnije greškama u pravosti.

**Geometrijski:** Površina $S = \pi r^2$ — jedna mera ($r$) određuje sve, nema ortogonalnosti. Greška površine:
$$\frac{\delta S}{S} = \frac{2\,\delta r}{r}$$
Za $r = 5$ cm i $\delta r = 50\,\mu$m → $\delta S / S \approx 0{,}1\%$ — sasvim pristojno.

**Simetrija polja:** Kružna geometrija → aksijalna simetrija → ivični efekti su uniformno raspoređeni po obimu, što olakšava korekciju (ili guard ring dizajn).

---

## Guard ring — ovde postaje zanimljivije

Za kružne ploče, guard ring je **koncentrični prsten** iste debljine, odvojen uskim prorezom od centralne elektrode:

```
┌─────────────────────────────┐
│  guard ring (uzemljen/isto U)│
│   ┌─────────────────┐       │
│   │  aktivna ploča  │       │
│   │    (meri F)     │       │
│   └─────────────────┘       │
│                             │
└─────────────────────────────┘
```

Prez između prstena i centralne elektrode treba da bude **mali u odnosu na $d$** (pravilo palca: $\leq d/5$). Ovo se lako postiže na bakarnoj ploči graviranom ili rezanom.

Ključna tačka: **silu meriš samo na centralnoj elektrodi** — guard ring "preuzima" ivične efekte na sebe.

---

## Praktični predlog geometrije

| Element | Vrednost | Napomena |
|---|---|---|
| Prečnik aktivne elektrode | 80 mm | $S \approx 50\,\text{cm}^2$ |
| Širina preza | 0,5 mm | Laserski rez |
| Spoljni prečnik guard ringa | 120 mm | Dovoljno da "apsorbuje" fringe |
| Debljina bakarne ploče | 2–3 mm | Rigidnost, ravnost |
| Rastojanje $d$ | 1 mm | Spejseri od kalibriranog stakla/safira |

Sa ovim, $F \approx 20\,\text{mN}$ pri $U = 1000\,\text{V}$ — lepo merljivo vagom rezolucije 1 mg.

---

## Jedna praktična napomena o bakru

Bakar je dobar izbor, ali **površinska oksidacija** može uneti kontaktni napon (do ~0.5 V). Na 1000 V radnog napona to je zanemarljivo (~0,05%), ali ako ikad želiš da radiš na nižim naponima — zlato ili nikl prevlaka (ili jednostavno brušenje pre merenja). Za sada, goli bakar + visok napon = nema problema.

---

Dakle, kružna geometrija + concentrični guard ring + stakleni spejseri za $d$ — to je klasičan, provereni dizajn (sličan Thomson-Lampard principu, koji ti ionako dobro poznaješ 😄). Izvodljivo i bez fabričke opreme.

