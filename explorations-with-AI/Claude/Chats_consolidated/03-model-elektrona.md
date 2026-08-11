# Poglavlje 3: Model elektrona/fotona — soliton, Gausova raspodela, naelektrisanje

*Sastavljeno iz razgovora: "QED model naelektrisanja i singularitet" (22.01.2026), "Gausova raspodela i energija vrtologa" (23.05.2026), "Integral sa eksponencijalnom permitivnošću" (30.05.2026).*

---

## 3.1 Zašto ne QED

Standardni model tretira elektron kao tačkastu česticu, a naelektrisanje kao fundamentalno, nedeljivo svojstvo — bez unutrašnje strukture, sa singularitetom polja u samoj tački. FOUNDATIONS pristup polazi od suprotne pretpostavke, dosledne Poglavlju 1 i 2: ako je fundamentalna realnost konzistentan glatki kontinuum, ništa u njoj — pa ni elektron, pa ni njegovo naelektrisanje — ne sme biti tačkasto niti singularno. Svaka veličina mora imati glatku, konačnu prostornu raspodelu.

Elektron se, kao i foton, modeluje kao **energetski vrtlog (vortex)** — lokalizovana, glatka, sferno-simetrična raspodela energije, izvedena iz istih principa kao u Poglavlju 2: konzistentan glatki kontinuum, granica $F_{max}$, i zakon $E\cdot T=h$.

## 3.2 Gausova raspodela gustine energije

Radna pretpostavka za gustinu energije vrtloga, kao funkcija radijalnog rastojanja od centra:

$$u(r) = \frac{hc\,(2\pi)^{3/2}}{\lambda^4}\,e^{-\frac{2\pi^2 r^2}{\lambda^2}}$$

gde je $\lambda = hc/E$ Komptonova talasna dužina (za elektron, $E=m_ec^2\approx 8.187\times10^{-14}$ J, $\lambda\approx 2.426\times10^{-12}$ m). Ovo je Gausov profil sa standardnom devijacijom $\sigma=\lambda/2\pi=\bar\lambda=\hbar/(m_ec)$ — dakle, širina raspodele je, prirodno, redukovana Komptonova talasna dužina elektrona.

Uz gustinu energije ide i prostorno promenljiva permitivnost, motivisana istim principom konzistentnog kontinuuma i granicom maksimalne sile $F_{max}=c^4/G$:

$$\epsilon(r) = \epsilon_0\,\exp\!\left(\frac{E}{F_{max}}\cdot\frac{1}{\lambda/2+r}\right)$$

Numerička provera potvrđuje: kada je $\epsilon\approx\epsilon_0$ (van neposredne blizine centra), granični integral koji povezuje $u(r)$ i $\epsilon(r)$ postaje **tačno proporcionalan** $\lambda$ — što znači da je rezultujuća veličina univerzalna konstanta, ista za elektron, mion, ili bilo koju drugu masu, nezavisno od gravitacije.

## 3.3 Prirodna jedinica naboja

Integracijom $\epsilon(r)\sqrt[4]{\frac{u(r)}{\epsilon(r)}\cdot\frac{du}{d\epsilon}}\cdot4\pi r^2\,dr$ (veličina dimenzije $C\cdot m$ — električni dipolni moment) dobija se rezultat koji, podeljen sa $\lambda$, otkriva nešto neočekivano lepo: prefaktor cele konstrukcije **jeste** jedinica naboja

$$Q_0 = \sqrt{\epsilon_0 hc} = \sqrt{h/Z_0} = \frac{e}{\sqrt{2\alpha}} \approx 1.3262\times10^{-18}\ \text{C}$$

($Z_0=1/(\epsilon_0c)\approx 376.73\ \Omega$ — impedansa vakuuma). Ovo $Q_0$ izranja **prirodno**, direktno iz integrala nad Gausovim solitonom — nije uvedeno kao pretpostavka, već kao posledica geometrije i osnovnih konstanti $\epsilon_0$, $h$, $c$. Vredi primetiti da $Q_0$ i elementarno naelektrisanje $e$ stoje u odnosu $e=\sqrt{2\alpha}\cdot Q_0$, preko konstante fine strukture $\alpha$.

## 3.4 Koliko je $Q_0$ zaista dostižno — i gde nastaje problem

Postavlja se pitanje: koja granica integracije (koji "rub" solitona) daje efektivno naelektrisanje baš jednako $e$? Rezultati za nekoliko prirodnih izbora granice $R$ (izraženih u jedinicama $\sigma=\bar\lambda$):

| granica $R$ | $R/\sigma$ | $I_1/\lambda$ |
|---|---|---|
| $\bar\lambda$ (1$\sigma$, redukovana Comptonova) | 1.000 | $0.479\,e$ |
| granica koja daje tačno $e$ | 1.326 | $1.000\,e$ |
| $R=\sqrt2\,\sigma$ (gde $u(r)$ padne na $1/e$) | 1.414 | $1.173\,e$ |
| $R\to\infty$ (saturacija) | — | $5.899\,e$ |

Kada $R\to\infty$, integral saturira na $0.7127\,Q_0\approx5.899\,e$ — dakle geometrija **fizički zabranjuje** da rezultat ikad dostigne $Q_0$; staje na oko 71% te vrednosti.

Najprirodniji, samostalno-motivisani izbor granice — $R=\sqrt2\,\sigma$, tačka gde energija u sfernoj ljusci $r^2u(r)$ ima svoj maksimum (prirodni "rub" solitona po sadržaju energije) — daje $1.173\,e$: **odstupanje od oko 17% u odnosu na $e$.**

Granica koja bi dala tačno $e$ ($R^*=1.326\,\sigma$) leži između ta dva prirodna markera, ali se ne poklapa ni sa jednim od njih. To je, iskreno rečeno, za sada **biran unazad** da bi izašlo tačno $e$ — nema samostalno geometrijsko opravdanje. Ovo ostaje otvoreno pitanje modela, a ne prikriveni nedostatak: kvantizacija naboja se ovde javlja kao geometrijski uslov na veličinu solitona (i to čisto u elektromagnetnom/Komptonskom sektoru — gravitaciona konstanta $k$ ne učestvuje u ovom integralu), ali precizan iznos od 17% odstupanja pokazuje da Gausov profil, sam po sebi, nije poslednja reč.

## 3.5 Problem Kulonovog "repa" i pravac dalje istrage

Gausova raspodela ima jednu poznatu manu kad se koristi za model naboja: opada eksponencijalno brzo, mnogo brže nego što bi trebalo da opada polje koje na velikoj udaljenosti reprodukuje standardni Kulonov zakon ($\propto 1/r^2$). Ovo je aktivan pravac dalje istrage — razmatra se da li bi **kvadrirani Lorencov profil** (koji ima "deblji rep", sporije opadanje na velikim $r$) mogao bolje da reprodukuje ispravno asimptotsko ponašanje polja, bez gubljenja glatkoće i konačnosti u centru solitona.

## 3.6 Napomena o Lorenc-invarijantnosti

U standardnoj fizici naelektrisanje se smatra Lorenc-invarijantnom veličinom — konstantom koja se ne menja sa brzinom čestice. Ovaj model, budući da naelektrisanje izvodi iz geometrije energetskog solitona, otvara pitanje: da li bi, u principu, precizna merenja pri ekstremnim energijama mogla pokazati blagu zavisnost efektivnog naboja od brzine? Ovo pitanje je, za sada, ostavljeno otvorenim, kao pravac za dalju proveru, a ne kao tvrdnja.

---

*Sledeće poglavlje: **Spin i ugaoni moment** — kako se, iz krute rotacije energetskog vrtloga i korekcije za cilindrični krak poluge, izvodi da je ugaoni moment jednak $\hbar$.*
