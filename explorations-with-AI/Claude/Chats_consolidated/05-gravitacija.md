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

Iz sile na foton u polju promenljivog $\epsilon$: $dE/dr = -a(r)\,E(r)/c^2$, uz efektivnu masu fotona $m_{eff}=E/c^2$ (poznato iz relativnosti) i efektivnu masu klastera $\mathbf{M}=\mathbf{E}/c^2$, sledi:

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

*Sledeće poglavlje: **Zračenje crnog tela** — kombinatorno izvođenje Plankovog zakona iz sfernog solitonskog modela, i otvoreno pitanje prefaktora $6/\pi$ naspram standardnog $2$.*
