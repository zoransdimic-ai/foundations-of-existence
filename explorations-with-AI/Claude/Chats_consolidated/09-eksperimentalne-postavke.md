# Poglavlje 9: Eksperimentalne postavke — merenje ε₀, μ₀, G

*Sastavljeno iz razgovora: "Kevendiš i merenje gravitacione konstante" (05.04.2026), "Thompson-Lampardov kondenzator" (16.04.2026), "Određivanje vrednosti μ" (23.04.2026), "Merenje dielektrične konstante piezo-elementima" (04.05.2026), "Komentarisanje prethodnog teksta" (08.05.2026).*

*Napomena: ovo poglavlje ima drugačiji karakter od prethodnih — manje je o izvođenju jednačina, a više o tome kako se osnovne konstante FOUNDATIONS modela mogu izmeriti sa skromnim, "primitivnim" sredstvima. To je namerno: teorija koja se ne može proveriti nije vredna mnogo.*

---

## 9.1 Merenje ε₀ silom između ploča kondenzatora

Polazna jednačina, elektrostatička sila privlačenja između ploča ravnog kondenzatora:

$$\epsilon_0 = \frac{2Fd^2}{SU^2}$$

Ideja: izmeriti silu $F$ (precizno osetljivom vagom, ili piezo-elementom) za poznatu površinu ploča $S$, razmak $d$ i napon $U$, i iz toga izračunati $\epsilon_0$. Za realno izvodljive vrednosti — $S=0.5\,\text{m}^2$, $d=1\,\text{mm}$, $U=10\,\text{V}$ — dobijena sila je reda $10^{-8}$ N, na granici merljivosti čak i preciznim analitičkim vagama, što motiviše pitanje smanjenja razmaka $d$ (uz napon do ~50 V) radi povećanja sile, i pitanje da li je merenje izvodljivo sa "primitivnim" sredstvima — na primer, standardnim olovnim akumulatorima (Pb, H₂SO₄) — kakvi bi bili dostupni i u vreme kada je prvi put izmerena "podužna kapacitivnost" prostora.

### Zaštitni prsten (guard ring) — Kelvinovo rešenje

Kod realnih (konačnih) ploča kondenzatora, linije polja se na ivicama izvijaju prema spolja ("fringe field"), pa formula $F=\epsilon_0SU^2/(2d^2)$, tačna za beskonačne ploče, unosi grešku reda $0.5$–$1\%$ za ploče $20\times20$ cm sa $d=1$ mm — baš u redu veličine tražene preciznosti.

Rešenje je Lord Kelvinov **zaštitni prsten** (guard ring), iz njegovog apsolutnog elektrometra (1860): provodna ivica oko merne ploče, u istoj ravni i na istom potencijalu. Između dva provodnika na istom potencijalu nema razlike potencijala, dakle nema polja, dakle nema silnica koje prelaze taj procep. Merna ploča je time, iz svoje perspektive, kao da se nalazi u unutrašnjosti mnogo veće ploče — sve ivične nepravilnosti "presele" su se na spoljašnju ivicu prstena, gde ne utiču na merenje.

Ovo nije trivijalan trik: Kelvin je shvatio da problem nije u *merenju* nego u *definisanju šta se meri* — i umesto da se greška naknadno ispravlja računski, eksperiment se redizajnira tako da greška uopšte ne nastane tamo gde se meri. Isti princip metrologije vraća se i u Thompson-Lampardovoj konstrukciji niže.

## 9.2 Thompson-Lampardov kondenzator — merenje bez poznavanja oblika ploča

Genijalnost Thompson-Lampardove konstrukcije (1956): cilindrični kondenzator čija kapacitivnost zavisi **samo od dužine** $L$, a ne od prečnika ili oblika poprečnog preseka elektroda — dakle merljiv obično lenjirom, bez potrebe za mehanički savršeno preciznim pločama.

Duboka analogija koja stoji iza ovoga: za cilindričan provodnik sa uniformnom raspodelom struje, magnetno polje **van** provodnika egzaktno je jednako polju linijskog provodnika na osi — bez ikakvog aproksimiranja, direktna posledica Amperovog zakona u integralnom obliku. Ovo je matematički **isti mehanizam** kao Njutnova teorema o ljusci (shell theorem) za gravitaciju: gravitaciono polje Sunca izvan njega ne "vidi" da je Sunce sfera, a ne tačka. Oba su posledica $1/r^2$ zakona i prostorne simetrije. Zato je sila po jedinici dužine između dve paralelne žice egzaktno $F/L=\mu_0I_1I_2/(2\pi d)$, za bilo koji poluprečnik žice (dokle god se žice ne dodiruju) — isti geometrijski "trik" koji Thompson-Lampardova konstrukcija koristi na električnoj strani.

## 9.3 Analogija ε₀ ↔ μ₀: kondenzator naspram kalema

Priroda ε i μ (Poglavlje 1) sugeriše prirodnu analogiju u načinu na koji se mere:

| Veličina | Električna strana | Magnetna strana |
|---|---|---|
| Osobina vakuuma | $\epsilon_0$ | $\mu_0$ |
| Pasivni element | kondenzator $C$ | kalem $L$ |
| Geometrijska veza | $C=\epsilon_0\cdot A/d$ | $L=\mu_0\cdot N^2A/l$ |
| "Kalkulabilni" standard | Thompson-Lampardov kondenzator | (otvoreno — analogna magnetna konstrukcija) |

Ova tabela, postavljena kao polazna tačka, otvara pitanje: postoji li magnetni analogon Thompson-Lampardove konstrukcije — geometrija u kojoj se induktivnost može odrediti čisto iz dužine, nezavisno od preciznog oblika provodnika? Pitanje ostaje otvoreno kao pravac dalje razrade.

## 9.4 Cavendishov eksperiment — i predložena piezo-nadogradnja

Henry Cavendish (1798) prvobitno nije merio $G$ — hteo je da izmeri gustinu Zemlje, a $G$ je naknadno izvučen iz rezultata, uz aparaturu koju je dizajnirao John Michell. Torziona vaga: horizontalna šipka (~1.8 m) obešena o tanku nit, sa dve male olovne kugle na krajevima; spolja se postavljaju dve velike olovne kugle. Gravitaciona sila između njih rotira šipku; nit pruža povratnu silu proporcionalnu uglu zaokreta.

Predložena nadogradnja koristi princip poluge sa piezo-elementom: blizu centra horizontalne šipke, mali izolovani "pipak" (zavaren za šipku) dodiruje piezo-element fiksiran za pod. Kada se postave velike kugle, šipka se blago rotira i pipak pritiska piezo. Poluga pretvara silu na kraju šipke ($L/2\approx900$ mm od centra) u silu na pipku udaljenom $d_{pipak}\approx1$ mm od centra:

$$F\cdot\frac{L}{2} = F_{piezo}\cdot d_{pipak} \quad\Rightarrow\quad F_{piezo} = F\cdot\frac{L/2}{d_{pipak}} = 42\,\mu\text{N}\cdot\frac{1000\,\text{mm}}{1\,\text{mm}} = 42\,\text{mN}$$

— pojačanje poluge reda **×1000**, koje prevodi silu na granici merljivosti (mikronjutni) u opseg lako dostupan preciznim piezo-vagama (milinjutni). Uz modernu rezoluciju piezo-elemenata (~1 μN), signal-šum odnos bi trebalo da bude povoljan; sistematske greške (pozicioniranje kugli, temperatura, simetrija aparature) ostaju dominantan izazov — kao i kod svih modernih $G$ eksperimenata.

## 9.5 Duh ovog poglavlja

Zajednička nit kroz sva četiri primera — guard ring, Thompson-Lampard, Cavendish/piezo — jeste ista metrološka filozofija: kad god je moguće, **eksperiment se redizajnira tako da greška ne nastane tamo gde se meri**, umesto da se greška naknadno računski ispravlja. To je isti duh koji vodi čitav FOUNDATIONS projekat na teorijskom nivou (Poglavlje 1–8): manje slepog poverenja u formalizam, više insistiranja da se svaki korak može proveriti — ovde, doslovno, lenjirom, vagom i piezo-elementom.

---

*Sledeće poglavlje: **Sprega (coupling)** — logičko-matematičko modelovanje veze između logičkog I, preseka skupova i množenja, kao manifestacija jedne te iste strukture.*
