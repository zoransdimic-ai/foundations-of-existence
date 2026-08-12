# Poglavlje 5: Gravitacija — ε(r), μ(r) i četiri klasična testa

*Sastavljeno iz razgovora: "Hajde da razmotrimo kretanje s..." (22.07.2025), "Light Deflection in Gravitational Field" (22.07.2025), "Time perception in young children" (21.09.2025).*

---

## 5.1 Polazna slika: svetlost koja skreće bez zakrivljenog prostora

Ideja kreće od jedne domaće demonstracije: laserski zrak koji prolazi kroz akvarijum sa rastvorom šećera čija gustina kontinualno raste ka dnu, glatko skreće ka dnu. Razlog: donji deo zraka putuje kroz gušći (optički gušći) medijum i kreće se sporije od gornjeg dela — isto kao tenk čija sporija leva gusenica zakreće vozilo ulevo.

Foton nije kruto telo poput tenka — on je 3D "gomilica" energije, fluid koji održava integritet zahvaljujući unutrašnjem gradijentu $dE/ds$ (videti Poglavlje 2 i 3). Ali princip je isti: ako se jedna strana fotona kreće sporije od druge, foton skreće. U FOUNDATIONS modelu, ono što određuje lokalnu brzinu jeste $V_{ee}=1/\sqrt{\epsilon\mu}$ — pa gravitaciono skretanje svetlosti ne zahteva zakrivljen prostor-vreme, već samo **prostorno promenljive $\epsilon(r)$ i $\mu(r)$**.

## 5.2 Otkud ε(r) i μ(r): sudar dva gama fotona

Zašto bi $\epsilon$ i $\mu$ uopšte bili promenljivi u prostoru oko mase? Polazna tačka: kada se dva gama fotona sudare i promene pravac kretanja, ta promena mora biti posledica toga što se $\epsilon$ i $\mu$ menjaju baš u tom delu prostora — a jedini "novi" fizički događaj koji se tu dešava (a koji se nije dešavao pre sudara) jeste **konfrontacioni fluks energija**.

Najinteresantnija moguća posledica takvog sudara: formiranje energijskog vrtloga. Polazeći od najjednostavnijeg kružnog kretanja $v(r)=\omega r$ i normalizacije brzine $V_{ee}(r)/V_{max}=1/\sqrt{(\epsilon(r)/\epsilon_0)(\mu(r)/\mu_0)}$, prvi, najprostiji pokušaj — $\epsilon(r)/\epsilon_0=R/r$ — odmah se pokazuje neispravnim: kada $r\to\infty$, izraz teži nuli, a treba da teži 1 (daleko od mase, $\epsilon\to\epsilon_0$). Najjednostavnija ispravka: $\epsilon(r)/\epsilon_0 = 1+R/r$, oblik koji dalje evoluira (u kasnijem radu, videti Poglavlje 3) ka eksponencijalnoj formi $\epsilon(r)=\epsilon_0\exp\!\left(\frac{E}{F_{max}}\cdot\frac{1}{r}\right)$ (i njenim varijantama).

## 5.3 Gravitaciona konstanta nije proizvoljna

Iz sile na foton u polju promenljivog $\epsilon$: $dE/dr = -a(r)\,E(r)/c^2$ — gde efektivna masa $m_{eff}(r)=E(r)/c^2$ **nije ovde preuzeta iz teorije relativnosti**, nego je nezavisno izvedena unutar samog modela, direktno iz brzinskog profila $v(r)$ (puna izvedba, sa svim koracima koji su probani i odbačeni, u Dodatku B) — i efektivnu masu klastera $\mathbf{M}=\mathbf{E}/c^2$ (izvedenu na isti način), sledi:

$$a(r) = \frac{c^2}{F_{max}}\cdot\frac{E}{r^2} = \frac{c^4}{F_{max}}\cdot\frac{\mathbf{M}}{r^2}$$

Poređenjem sa Newtonovim zakonom $a=GM/r^2$, prepoznaje se:

$$\boxed{G = \frac{c^4}{F_{max}}}$$

Gravitaciona konstanta se ovde ne postulira — ona je posledica dva fundamentalna ograničenja prirode koja su već uvedena u Poglavlju 1 i 2: maksimalne brzine $c$ i maksimalne sile $F_{max}$. Dimenziona provera: $[c^4/F_{max}] = (\text{m}^4/\text{s}^4)/(\text{kg}\cdot\text{m}/\text{s}^2) = \text{m}^3/(\text{kg}\cdot\text{s}^2) = [G]$. ✓

## 5.4 Šapirovo kašnjenje — direktna provera

Sa $\epsilon(r)/\epsilon_0\approx e^{2GM/(c^2r)}$ (odnosno $V_{ee}(r)\approx c\,e^{-2GM/(c^2r)}$ za slabo polje), vreme potrebno svetlosti da pređe put od Zemlje do tačke najbližeg prilaska Suncu $S$, pa do Marsa, i nazad, produženo je za:

$$\Delta t \approx \frac{4GM}{c^3}\ln\!\left(4\frac{L_1 L_2}{R_S^2}\right)$$

Numerički proračun (VBA), sa $M_\odot=1.989\times10^{30}$ kg, $R_\odot=6.95\times10^8$ m, i tipičnim rastojanjima Zemlja–Sunce i Mars–Sunce, daje:

$$\Delta t \approx 2.474\times10^{-4}\ \text{s} = 247.4\ \mu\text{s}$$

— vrednost koja se poklapa sa Shapirovim izmerenim kašnjenjem.

## 5.5 Ostala tri klasična testa

Isti oblik $c(r)=c\,e^{-GM/(c^2r)}$ (uz $\epsilon(r)=\epsilon_0 e^{E/(F_{max}r)}$, $\mu(r)=\mu_0 e^{E/(F_{max}r)}$) reprodukuje, u slabom polju, sva četiri klasična testa opšte relativnosti:

**Gravitacioni crveni pomak (Pound–Rebka):** iz $\nu_R\lambda_R=c(R)$ i konstantnog talasnog broja, $\dfrac{\nu_\infty}{\nu_R}=e^{GM/(c^2R)}$, odnosno za slabo polje $\dfrac{\nu_\infty-\nu_R}{\nu_R}\approx\dfrac{GM}{c^2R}$ — isti izraz kao u opštoj relativnosti.

**Skretanje svetlosti:** iz Fermatovog principa $\delta\int \frac{ds}{c(r)}=0$ u polarnim koordinatama, za malo skretanje: $\theta = \dfrac{4GM}{c^2d}$ — tačno Ajnštajnova vrednost.

**Precesija Merkurove orbite:** efektivni potencijal $V_{eff}(r)=-\dfrac{GM}{r}+\dfrac{L^2}{2r^2}-\dfrac{GML^2}{c^2r^3}$ (poslednji član iz promenljivog $c(r)$) daje ugao precesije po orbiti $\Delta\phi=\dfrac{6\pi GM}{c^2a(1-e^2)}$, što za Merkur ($a=5.79\times10^{10}$ m, $e=0.2056$) iznosi **≈ 43″ po veku** — poklapa se sa opaženom anomalnom precesijom.

Punu Lagranžijansku formulaciju precesije (i numeriku koja vodi do 43″/vek) videti u dodatku ovog poglavlja, preuzetom direktno iz izvedenog dokumenta o precesiji Merkura.

---

## Dodatak: Precesija Merkurove orbite — puna Lagranžijanska izvedba

**Klasičan slučaj (bez precesije).** Iz Lagranžijana u polarnim koordinatama $L_{/m}=\tfrac12(\dot r^2+r^2\dot\phi^2)+\dfrac{GM}{r}$, Ojler-Lagranžova jednačina za $\phi$ (bez eksplicitne $\phi$-zavisnosti) daje očuvanje ugaonog momenta: $r^2\dot\phi = l_{/m} = \text{const}$, pa $\dot\phi_{n.p.}=l_{/m}/r^2$.

**Modifikovan prostor-vreme.** Prostorna metrika: $ds=\sqrt{dr^2+r^2d\phi^2}\cdot e^{-2GM/(c^2r)}$; dilatacija vremena: $d\tau = dt\cdot e^{-GM/(c^2r)}$. Odatle $\dfrac{d\phi}{d\tau}=\dfrac{l_{/m}}{r^2}e^{4GM/(c^2r)}$, pa nakon uvrštavanja $d\tau$:

$$d\phi = d\phi_{n.p.}\cdot e^{3GM/(c^2r)} \approx d\phi_{n.p.}\left(1+3\frac{GM}{c^2r}\right)$$

Dodatni ugao po orbiti: $\Delta\phi=\oint 3\dfrac{GM}{c^2r}\,d\phi_{n.p.} = \dfrac{6\pi GM}{c^2 a(1-e^2)}$.

**Za Merkur** ($a=5.79\times10^{10}$ m, $e=0.2056$, $M_\odot=1.989\times10^{30}$ kg): $\Delta\phi\approx 43$ lučnih sekundi po veku — potvrđuje opaženu anomalnu precesiju.

---

## Dodatak B: Rađanje dinamike — F=ma i efektivna masa iz brzinskog profila

*Ovo je nezavisna izvedba $F=ma$ i $m_{eff}=E/c^2$, koja ne pretpostavlja teoriju relativnosti niti bilo šta iz nje pozajmljuje — oba rezultata se dobijaju direktno iz brzinskog profila $v(r)$ već uvedenog u §5.2 i Poglavlju 8. Put je istraživački, sa granama koje su probane i odbačene; to je namerno zadržano, jer upravo ta eliminacija pokazuje zašto je preživela grana jedina koja daje predviđanja u skladu sa stvarnošću.*

**Polazna tačka.** Već imamo (§5.2): $v(r)=v_0\,e^{-\frac{1}{K_F}\frac{\mathbf E}{r}}$, gde je $\mathbf E$ energija (masa) klastera, $K_F=F_{max}$. Direktnim izvodom:

$$\frac{dv(r)}{dr} = \frac{v(r)}{K_F}\frac{\mathbf E}{r^2} \tag{1}$$

**Pitanje koje se mora postaviti.** $v(r)=ds(r)/dt(r)$ — ali koji od dva elementa, $ds(r)$ ili $dt(r)$, zapravo nosi eksponencijalni faktor? Moguće je da ga nosi samo jedan, ili da ga nose oba (u nekoj kombinaciji koja se, sabrana, svede na poznati $v(r)$). Pišemo to opšte, sa dva slobodna parametra:

$$ds(r) = dr\,e^{-k_1\frac{1}{K_F}\frac{\mathbf E}{r}}, \qquad dt(r) = dt\,e^{-k_2\frac{1}{K_F}\frac{\mathbf E}{r}}, \qquad k_1-k_2=1$$

(uslov $k_1-k_2=1$ osigurava da količnik $ds(r)/dt(r)$ ponovo daje poznati $v(r)$). Ovo ne fiksira $k_1$ i $k_2$ pojedinačno — samo njihovu razliku. Tri prirodna kandidata:

**(a) $dt(r)=dt$ (nepromenjeno; $k_2=0,\,k_1=1$).** Vreme $T(r)$ potrebno fotonu da prođe kroz fiksnu tačku na rastojanju $r$ ne bi zavisilo od $r$. Iz $E(r)T(r)=h$, sa $T(r)=T=\text{const}$, sledi $E(r)=E=\text{const}$ — fotonova energija se ne bi menjala sa rastojanjem od klastera. **Ovo je u suprotnosti sa postojanjem gravitacionog crvenog pomaka — odbačeno.**

**(b) $ds(r)=dr$ (nepromenjeno; $k_1=0,\,k_2=-1$).** Tada $T(r)=T\,e^{+\frac{1}{K_F}\frac{\mathbf E}{r}}$ — eksponent suprotnog znaka od onog u $v(r)$. Iz $E(r)T(r)=h$ sledi da $E(r)$ **raste** sa rastojanjem od klastera (fažuje udaljavajući se). **Ovo je suprotno od onoga što Pound–Rebka meri (foton koji se penje iz gravitacionog polja gubi energiju) — odbačeno.**

**(c) $dt(r)$ nosi isti eksponencijalni faktor kao i sam $v(r)$ ($k_2=1,\,k_1=2$).** Ovo je jedina od tri isprobane mogućnosti čije predviđanje — foton je energičniji blizu klastera, gubi energiju udaljavajući se — odgovara poznatom postojanju i smeru gravitacionog crvenog pomaka. Zadržava se.

*Napomena o statusu ovog koraka: ovo je eliminacija među tri isprobane, fizički motivisane mogućnosti, potvrđena poređenjem sa poznatom (izmerenom) činjenicom o gravitacionom crvenom pomaku — nije tvrdnja da je (c) jedina matematički zamisliva raspodela $k_1,k_2$ uz $k_1-k_2=1$. Selekcija se oslanja na spoljašnji, empirijski podatak, ne na čistu unutrašnju nužnost.*

**Sledi:** $T(r) = T\,e^{-\frac{1}{K_F}\frac{\mathbf E}{r}}$, i iz $E(r)T(r)=h$:

$$E(r) = \frac{h}{T(r)} = E\,e^{\frac{1}{K_F}\frac{\mathbf E}{r}}$$

Direktnim izvodom:

$$\frac{dE(r)}{dr} = -\frac{1}{K_F}\frac{\mathbf E}{r^2}\,E(r) \tag{2}$$

**Ubrzanje.** Iz definicije $a\equiv dv/dt$, odnosno, $a(r)\equiv dv(r)/dt(r)$:

$$a(r) = \frac{v_0^2}{K_F}\frac{\mathbf E}{r^2} \tag{3}$$

*(Dimenziona provera: $[\mathbf E/(K_Fr^2)]=1/\text{m}$; da bi $a(r)$ imalo jedinicu ubrzanja, m/s², množilac mora biti $v_0^2$, ne $v_0$ — proveriti pažljivo pri prepisivanju, lako se ispusti eksponent.)*

**Rođenje dinamike.** Iz (2) i (3), pošto obe imaju isti faktor $\frac{1}{K_F}\frac{\mathbf E}{r^2}$:

$$\frac{dE(r)}{dr} = -a(r)\,\frac{E(r)}{v_0^2}$$

Leva strana je, po definiciji uvedenoj u Poglavlju 2 (stabilnost solitona), sila: $F\equiv dE/dr$. Desna strana je prepoznatljiva kao Njutnov oblik $F=am$, sa efektivnom (inercijalnom) masom:

$$\boxed{m_{eff}(r) = \frac{E(r)}{v_0^2}}$$

Ovo nije pretpostavka niti pozajmica iz relativnosti — izvedeno je iz istog brzinskog profila $v(r)$ koji je već uveden radi opisa gravitacije (§5.2), uz jedini spoljašnji unos: poznat smer gravitacionog crvenog pomaka, korišćen da se od tri geometrijski moguće raspodele eksponencijalnih faktora izabere jedina koja mu ne protivreči.

**Numerička provera — Pound–Rebka.** Za malo $\delta r$, gde je $a(r)$ praktično konstantno ($a$):

$$\frac{\delta E}{E} \approx -\frac{a}{v_0^2}\,\delta r$$

Sa $a=9.81\ \text{m/s}^2$ (gravitaciono ubrzanje na Zemljinoj površini), $v_0=c=299792458\ \text{m/s}$, $\delta r=22.5\ \text{m}$ (visina Jefferson-ovog tornja, originalni eksperiment):

$$\frac{\delta E}{E} \approx 2.4559\times10^{-15}$$

— potvrđeno numerički, poklapa se sa izmerenim/predviđenim rezultatom Pound–Rebka eksperimenta (~2.5×10⁻¹⁵).

---

*Sledeće poglavlje: **Zračenje crnog tela** — kombinatorno izvođenje Plankovog zakona iz sfernog solitonskog modela, i otvoreno pitanje prefaktora $6/\pi$ naspram standardnog $2$.*
