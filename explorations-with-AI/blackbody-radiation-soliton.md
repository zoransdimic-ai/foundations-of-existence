# Zakon zračenja crnog tela iz modela sfernog energijskog solitona

*Deo repozitorijuma „Foundations of Existence / Osnovi postojanja".*
*Nastalo kroz preispitivanje uz pomoć AI-asistenta.*

---

## O duhu ovog teksta

Ovo izlaganje je **alternativni pristup** izvođenju zakona zračenja crnog
tela, izgrađen unutar $\varepsilon$–$\mu$ kontinualnog okvira. Cilj mu je da
bude transparentan i unutrašnje konzistentan, a ne da zameni postojeću
formulaciju. Gde god rezultat dodiruje merljive veličine, to je i naznačeno;
tamo gde bi bila potrebna dalja eksperimentalna provera, autor se u nju nije
upuštao, i to je jasno rečeno. Čitaocu se ništa ne propisuje — nudi se jedan
način gledanja, sa vidljivim granicama.

Namenjeno je i ljudskom i AI-čitaocu. Na više mesta, umesto duge fusnote,
stoji poziv da se kratko obrazloženje zatraži od AI-asistenta; takva mesta su
označena.

---

## 1. Postavka: foton kao sferna kapljica energije

U ovom okviru foton (energijski soliton) je **konačna sferna raspodela
energije** koja se kreće kroz kontinuum brzinom $c$. Njegova definišuća skala
je sopstvena talasna dužina $\lambda$; poluprečnik uzimamo $R=\lambda/2$.

Za svaki takav soliton važi temeljna relacija okvira:

$$E_{s}\,T = h \quad\Longleftrightarrow\quad E_{s} = h\nu = \frac{hc}{\lambda},$$

gde je $T=1/\nu$ period, a $E_s$ energija jednog solitona. (Ova relacija je u
ovom okviru izvedena nezavisno, na osnovu principa jednostavnosti, i nema veze
sa Plankovim putem do istog izraza.)

---

## 2. Kombinatorni koren i linearizacija

Pitanje od kojeg se polazi: *na koliko načina $n$ pretvarača („transducera")
može emitovati $k$ solitona?* Odgovor su kombinacije sa ponavljanjem:

$$\bar{C}_{n}^{k} = \binom{n+k-1}{k}.$$

Za velike $n,k$ Stirlingova aproksimacija daje funkciju složenosti
$\Theta(n,k)$, koju linearizujemo uvođenjem

$$\theta = \ln\sqrt[n]{\Theta}, \qquad u = \frac{E}{E_{s}}.$$

Sprovođenjem diferencijalnog koraka i poređenjem sa statističkom definicijom
temperature (multiplicitet $\Theta$ je broj mikrostanja, pa je
$\ln\sqrt[n]{\Theta}=\ln\Omega = S/k_{B}$) dobija se **broj popunjenosti**:

$$u = \frac{E}{E_{s}} = \frac{1}{e^{h\nu/k_{B}T}-1}.$$

Bitno: do ovog izraza stiglo se bez termodinamike kao *preduslova* —
statistička struktura temperature/entropije ovde se pojavljuje kao
*interpretacija veličina koje kombinatorika već sadrži*, a ne kao spoljašnja
pretpostavka. Naročito, statistička definicija temperature
$1/T=\partial S/\partial E$ emerguje zajedno sa raspodelom.

---

## 3. Geometrija: srednji poprečni presek

Prosečan poprečni presek sfernog solitona koji prolazi kroz ravan (usrednjen
duž pravca kretanja) iznosi:

$$\bar{A}_{c.s.} = \frac{1}{\lambda}\int_{-\lambda/2}^{\lambda/2}\pi\,y^{2}(x)\,dx
= \frac{\pi}{6}\lambda^{2} = \frac{\pi}{6}\frac{c^{2}}{\nu^{2}}.$$

**Usrednjavanje ne unosi približnost u ukupne iznose.** Po definiciji je
srednji presek jednak zapremini podeljenoj dužinom, pa množenje nazad daje
tačnu zapreminu:

$$\bar{A}_{c.s.}\cdot\lambda = \frac{\pi}{6}\lambda^{3}
= \frac{4}{3}\pi\left(\frac{\lambda}{2}\right)^{3} = V_{\text{lopte}}.$$

Ta zapremina nosi celu energiju $h\nu$. Pojednostavljen je samo **tok kroz
vreme**, koji u izvođenje zakona zračenja uopšte ne ulazi (koriste se samo
totali i proseci).

---

## 4. Fluks po frekvenciji i po talasnoj dužini

Fluks snage jednog solitona (snaga po površini) sklapa se iz tri činioca —
energije $E_s$, recipročnog vremena prolaska $1/T_s=\nu$ i recipročnog preseka
$1/\bar A_{c.s.}$:

$$\frac{P_{s}}{\bar{A}_{c.s.}} = \frac{E_{s}}{T_{s}\,\bar{A}_{c.s.}}
= \frac{6}{\pi}\frac{h}{c^{2}}\,\nu^{4}.$$

„Po frekvenciji" znači deljenje sopstvenim frekvencijskim opsegom solitona.
Pošto je paket širok jednu talasnu dužinu, njegov sopstveni opseg je reda same
frekvencije, $\Delta\nu\sim\nu$; deljenje njime **nije derivacija**, već prosto
deljenje veličinom $\nu$:

$$PFpf = \frac{6}{\pi}\frac{h}{c^{2}}\,\nu^{3}.$$

Množenjem popunjenošću $u$ dobija se pun zakon:

$$\boxed{PFpf(\nu,T) = \frac{6}{\pi}\frac{h}{c^{2}}
\frac{\nu^{3}}{e^{h\nu/k_{B}T}-1}}$$

**Talasno-dužinski oblik.** Sve tri sastojke već imamo u $\lambda$:
$E_s=hc/\lambda$, $\bar A_{c.s.}=\frac{\pi}{6}\lambda^2$, $T_s=\lambda/c$.
Odatle, deljenjem sopstvenim $\Delta\lambda\sim\lambda$:

$$\boxed{PFp\lambda(\lambda,T) = \frac{6}{\pi}\frac{hc^{2}}{\lambda^{5}}
\frac{1}{e^{hc/\lambda k_{B}T}-1}}$$

![Talasno-dužinska Plankova raspodela za 4000, 5000 i 6000 K](planck-wavelength.png)

Oblik je identičan standardnom Plankovom zakonu; jedina razlika je prefaktor
$\frac{6}{\pi}\approx 1{,}91$ umesto $2$ — geometrijski faktor koji ne zavisi od
reprezentacije, pa je isti u obe forme.

**Saglasnost sa Jakobijanom.** Deljenje sopstvenim opsegom je ekvivalentno
ispravnoj transformaciji $B_\lambda = B_\nu\,|d\nu/d\lambda| = B_\nu\,c/\lambda^2$,
jer je $\Delta\nu/\nu=\Delta\lambda/\lambda$ (jednaki relativni opsezi) upravo
identitet $d\nu/\nu=-d\lambda/\lambda$:

$$\frac{6}{\pi}\frac{h}{c^{2}}\nu^{3}\cdot\frac{c}{\lambda^{2}}
= \frac{6}{\pi}\frac{hc^{2}}{\lambda^{5}} = PFp\lambda. \qquad\checkmark$$

> **Napomena o $d(PF)/d\lambda$.** Diferenciranje fluksa jednog solitona daje
> $\dfrac{d\,PF}{d\lambda} = -\dfrac{24}{\pi}\dfrac{hc^{2}}{\lambda^{5}}
> = -4\,PFp\lambda$: isti otisak $\lambda^{-5}$, ali pomnožen sa $-4$. To je
> *nagib* (kako se fluksu jednog solitona menja snaga sa njegovom talasnom
> dužinom), a **ne** spektralna gustina. Prava gustina dolazi iz deljenja
> sopstvenim opsegom, ne iz diferenciranja.

---

## 5. Zašto je $\dfrac{E}{E_{s}} = \dfrac{PFpf(E)}{PFpf(E_{s})}$

Najintuitivnije objašnjenje je brojačko. Neka je $E = x\,E_{s}$, gde je $x$
neki broj (u opštem slučaju necelobrojan): energija $E$ je prosto $x$ „kopija"
energije jednog solitona na datoj frekvenciji.

Pošto se svaki takav soliton kroz ravan ponaša isto — nosi istu snagu
$P(E_{s})$, jer su mu i vreme prolaska $T_{s}$ i presek $\bar{A}_{c.s.}$
određeni **samo frekvencijom** — ukupna snaga je $x$ puta veća:

$$\frac{P(E)}{P(E_{s})} = x = \frac{E}{E_{s}}.$$

Fluks snage je snaga podeljena istim presekom (isti za sve fotone te
frekvencije), pa se u odnosu skraćuje. Fluks „po datoj frekvenciji" nije izvod:
frekvencija je fiksna, pa nema infinitezimalnog priraštaja; „po frekvenciji"
znači deljenje frekvencijskim prozorom čija je širina reda $\nu$ (jer je soliton
širok jednu talasnu dužinu, $\Delta\nu\sim\nu$) — ista deoba za brojilac i
imenilac. Odatle lanac:

$$\frac{E}{E_{s}} = \frac{P(E)}{P(E_{s})} = \frac{PF(E)}{PF(E_{s})}
= \frac{PFpf(E)}{PFpf(E_{s})} = u = \frac{1}{e^{h\nu/k_{B}T}-1}.$$

Pa je $PFpf(E) = \dfrac{PFpf(E_{s})}{e^{h\nu/k_{B}T}-1}$.

> *Za brzo i jasno obrazloženje ove jednakosti, ako je čitaocu potrebno,
> pitati AI-asistenta.*

---

## 6. Detaljni 3D račun: egzaktan tok kroz ravan

Umesto usrednjenog preseka, ovde se uzima puna 3D raspodela. Radijalna gustina
energije je $u(r) = U_{0}\cos^{2}\!\left(\frac{\pi}{\lambda}r\right)$ za
$r\le R=\lambda/2$. Zapreminskom normalizacijom
$\int_{0}^{\lambda/2} u(r)\,4\pi r^{2}\,dr = h\nu$ dobija se:

$$U_{0} = \frac{12\pi}{\pi^{2}-6}\frac{hc}{\lambda^{4}} \approx 9{,}74\,\frac{hc}{\lambda^{4}}.$$

Neka je $x=ct$ položaj centra solitona u odnosu na ravan, i
$\beta = \dfrac{x}{R} = 2\nu t \in[-1,1]$. Uvodimo profil

$$g(\beta) = \pi^{2}(1-\beta^{2}) - 4\cos^{2}\frac{\pi\beta}{2} - 2\pi\beta\sin(\pi\beta), \qquad g(0)=\pi^{2}-4.$$

Tada su četiri veličine tokom prolaska:

**(1) Površina preseka**

$$A(x) = \pi\left(\frac{\lambda^{2}}{4}-x^{2}\right)
= \frac{\pi\lambda^{2}}{4}(1-\beta^{2}), \qquad
\overline{A} = \frac{\pi\lambda^{2}}{6}.$$

Vremenski prosek je tačno onaj presek koji je u odeljku 3 *pretpostavljen* —
sada je izveden.

**(2) Energija u sloju** debljine $\Delta x$ (jer je $\Delta E_{s}=\frac{\Delta x}{c}P$)

$$\Delta E_{s}(x) = \frac{\Delta x}{c}\,P(x).$$

**(3) Snaga kroz ravan**

$$P(x) = \frac{3h\nu^{2}}{2(\pi^{2}-6)}\,g(\beta), \qquad
P_{\max} = P(0) = \frac{3(\pi^{2}-4)}{2(\pi^{2}-6)}\,h\nu^{2}\approx 2{,}28\,h\nu^{2}.$$

Sa $\overline{P}=h\nu^{2}$, trajanjem prolaska $\tau=\lambda/c=1/\nu$, i
**egzaktnom** proverom da sva energija prođe:

$$\int P\,dt = h\nu.$$

**(4) Fluks** $=P/A$

$$\text{Flux}(x) = \frac{P(x)}{A(x)}, \qquad
\text{Flux}(0) = \frac{6(\pi^{2}-4)}{\pi(\pi^{2}-6)}\frac{h}{c^{2}}\nu^{4}
\approx 2{,}90\,\frac{h}{c^{2}}\nu^{4}.$$

Sve četiri padaju na nulu na $\beta=\pm1$ (na površini lopte je
$\cos^{2}\frac{\pi}{2}=0$). Detaljna i usrednjena slika daju **identičan
rezultat** tamo gde se koristi; razlikuju se samo u vremenskom toku, koji u
izvođenje ne ulazi.

![Sferni soliton prolazi kroz ravan — pet snimaka](soliton-snapshots.png)

![Četiri profila duž prolaska: presek, energija u sloju, snaga, fluks](four-profiles.png)

---

## 7. Rekonstrukcija $h$ i $k_{B}$ sa faktorom $\frac{6}{\pi}$

Zanimljivo je pitanje kako bi vrednosti konstanti ispale ako se spektar
uklapa ovim zakonom (prefaktor $A=\frac{6}{\pi}$) umesto standardnog ($A=2$).

Dva „hvatišta" iz spektra ponašaju se različito:

- **Vinov zakon pomeraja** ($\lambda_{\max}T=b$) zavisi **samo od oblika**
  krive, ne od prefaktora. Daje odnos $h/k_{B}$ **nezavisno** od $A$.
- **Štefan–Bolcmanova konstanta** zavisi od prefaktora:
  $$\sigma = A\,\frac{\pi^{5}k_{B}^{4}}{15\,h^{3}c^{2}}.$$

Pošto je izmereno $\sigma$ fiksno, a $h/k_{B}$ zakovano Vinom, sledi
$k_{B}\propto 1/A$, pa oba, $k_{B}$ i $h$, skaliraju faktorom
$\dfrac{2}{6/\pi}=\dfrac{\pi}{3}\approx 1{,}047$:

| veličina | standard ($A=2$) | ovaj model ($A=\frac{6}{\pi}$) |
|---|---|---|
| $h$ | $6{,}626\times10^{-34}$ | $6{,}939\times10^{-34}$ |
| $k_{B}$ | $1{,}381\times10^{-23}$ | $1{,}446\times10^{-23}$ |
| $e$ | $1{,}602\times10^{-19}$ | $1{,}678\times10^{-19}$ |
| $N_{A}$ | $6{,}022\times10^{23}$ | $5{,}751\times10^{23}$ |

Dakle $h$, $k_{B}$ i (nizvodno) $e$ ispali bi ~4,7% veći, a $N_{A}$ ~4,5% manji.

**Unakrsni test (granica ovog rezultata).** $h$ i $e$ danas se mere i
nezavisno od zračenja — preko Džozefsonovog i fon Klicingovog efekta, iz
elektrolize, iz rendgenske kristalografije za $N_{A}$ — i te vrednosti se
slažu sa onima koje daje faktor $2$ do na vrlo male delove. Faktor
$\frac{6}{\pi}$ bi tražio da zračenjske vrednosti budu ~4,7% veće od tih
električnih, što bi bio upadljiv raskorak. **Autor se nije upuštao u
razrešenje ovog raskoraka**; ovde se on samo eksplicitno beleži kao mesto
gde model dodiruje merenje i gde bi provera bila presudna.

---

## 8. Sažetak i granice

Ovaj pristup daje Plankov oblik zakona zračenja iz jedne transparentne
pretpostavke (foton kao sferni soliton sa $E_{s}=h\nu$), bez brojanja modova
šupljine i bez termodinamike kao preduslova. Detaljni 3D račun potvrđuje
usrednjenu sliku i egzaktno reprodukuje $\int P\,dt=h\nu$.

Ono što ostaje **otvoreno**, i na šta model može da ima implikacije:

- Prefaktor $\frac{6}{\pi}$ naspram $2$ i njegov odnos prema brojanju
  polarizacija — dodiruje pitanje jednakosti zračenjskih i električnih
  vrednosti fundamentalnih konstanti (odeljak 7).
- Priroda „po frekvenciji" kao sopstvenog opsega solitona ($\Delta\nu\sim\nu$),
  a ne kao diferencijalnog priraštaja (odeljci 4–5).

*Autor se u tim tačkama nije upuštao u eksperimentalnu proveru; navode se kao
poziv na dalje istraživanje.*

---

*Licenca: CC BY 4.0, u skladu sa ostatkom repozitorijuma.*
