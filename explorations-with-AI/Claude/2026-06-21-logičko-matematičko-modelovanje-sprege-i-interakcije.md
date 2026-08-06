# Logičko-matematičko modelovanje sprege i interakcije

*2026-06-21*


---


**Zoran:**

Logičko, matematičko modelovanje/opisivanje/predstavljanje sprege, interakcije, "prožimanja", uslovljenosti:

* najjednostavnija logička "sprega": konjunkcija (a AND b)(kada sprega postoji, rezultat je "1". Kada ne postoji: "0")
* najjednostavnoja "skupovna" sprega: presek skupova. Kada "sprega" postoji, presek skupova nije prazan skup.
* najjednostavnija aritmetička sprega: $a \cdot b$. Kada je rezultat 0, nema sprege. Kada je rezultat konstanta, sprega je najjednostavnija. Kada rezultat nije konstanta, sprega je ... komplikovanija od one najjednostavnije.
Da li je ovo ... ispravan pogled na "stvari"?



**Claude:**

Da, pogled je u suštini ispravan — i čak je dublji nego što ga ti formulišeš. Ono što izgledaju kao tri paralelne analogije zapravo je jedna ista struktura koja se otvara na tri nivoa opštosti. Dozvoli da to pokažem, a onda da ti ponudim dve korekcije koje ga čine preciznijim.

**Tri slike su zapravo jedna**

Karika koja ih spaja je indikatorska (karakteristična) funkcija skupa. Ako skupu pridružiš funkciju koja daje 1 za članove i 0 za nečlanove, onda važi:

$$\chi_{A\cap B}(x) = \chi_A(x)\cdot\chi_B(x)$$

To jest: presek skupova je tačno množenje njihovih indikatorskih funkcija. A na skupu vrednosti $\{0,1\}$ množenje se poklapa sa konjunkcijom — $1\cdot 1 = 1$, sve ostalo je $0$, što je istinitosna tablica za AND. Dakle nije slučajnost da ti se sve tri „najjednostavnije sprege" poklapaju: konjunkcija, presek i proizvod su **ista operacija viđena kroz tri sočiva**. Logika je dvovrednosna verzija, skupovi su ista stvar podignuta na članstvo, a aritmetika je njena neprekidna ekstenzija.

Ta neprekidna ekstenzija ima i ime: u viševrednosnoj (fuzzy) logici, neprekidne generalizacije konjunkcije zovu se *t-norme*, i proizvod $a\cdot b$ na $[0,1]$ je upravo jedna od tri fundamentalne (tzv. *product t-norm*). Tvoja intuicija da je množenje „aritmetička sprega" odgovarajuća konjunkciji nije labava analogija — to je formalno tačno tvrđenje sa razrađenom teorijom iza sebe.

**Korekcija 1: šta tačno znači „najjednostavnija" sprega**

Tvoja trijada (0 / konstanta / nekonstanta) može se učiniti potpuno preciznom, i mislim da bi ti se to dopalo, preko **separabilnosti**, odnosno mešovitog izvoda. Za funkciju dve promenljive $f(a,b)$, kriterijum „da li uopšte postoji sprega" je:

$$\frac{\partial^2 f}{\partial a\,\partial b} \;\overset{?}{=}\; 0$$

- Za $f = a + b$ (sabiranje): mešoviti izvod je $0$. Promenljive su nezavisne, *razdvojive* — nema sprege. Sabiranje samo stavlja stvari jednu pored druge.
- Za $f = a\cdot b$: mešoviti izvod je $1$ — konstanta različita od nule. To je **najmanja moguća neseparabilna funkcija**: monom najnižeg stepena čiji mešoviti izvod ne iščezava. Otud, u sasvim preciznom smislu, „najjednostavnija sprega".
- Za $f = a^2 b$, $e^{ab}$, itd.: mešoviti izvod je sam funkcija — sprega koja se menja od tačke do tačke, „komplikovanija".

Ovo ti zapravo formalizuje i proširuje tvoju lestvicu: nema sprege ↔ mešoviti izvod nula; najprostija sprega ↔ mešoviti izvod konstantan; složena sprega ↔ mešoviti izvod promenljiv.

Sad jedna finija distinkcija. Kad ti kažeš „kada je rezultat konstanta, sprega je najjednostavnija", ti govoriš o *vrednosti* proizvoda — o zakonu $a\cdot b = k$, o nivou (hiperboli). To je drugačiji nivo od „sprežna funkcija je najjednostavnija". Oba su validna i lepo se uklapaju: najjednostavnija sprežna funkcija ($a\cdot b$) generiše najjednostavniji sprežni zakon ($a\cdot b = k$). Taj recipročni zakon — kad jedno raste, drugo opada tako da proizvod ostaje invarijantan — jeste najkruća, najprostija uzajamna veza koja postoji. I nije slučajno što su tvoji temeljni odnosi baš tog oblika: $E\cdot T = h$, $V^2\varepsilon\mu = 1$, kao i Bojl-Mariot $pV=\text{const}$ ili $\Delta x\,\Delta p \gtrsim \hbar/2$. Sve su to izjave „sprega između ove dve veličine je najprostija moguća — njihov proizvod je univerzalna konstanta".

**Korekcija 2: „uslovljenost" ne pripada ovde**

Ovo je jedina prava zamerka. Tvoja reč-grozd — *sprega, interakcija, prožimanje, uslovljenost* — nije homogena. Prve tri su **simetrične**: $a\cdot b = b\cdot a$, $A\cap B = B\cap A$, AND je komutativan. One se savršeno slažu sa proizvodom/presekom/konjunkcijom.

Ali *uslovljenost* je **asimetrična** i usmerena: „ako $a$, onda $b$" nije isto što i obratno. Njen logički dom nije konjunkcija nego **implikacija** ($a \to b$), a u aritmetici funkcionalna zavisnost $b = f(a)$. Simetrična operacija po konstrukciji ne može da nosi usmerenu uslovljenost — izgubiš strelicu. Tako da jedna operacija ne pokriva ceo grozd: za prožimanje i spregu — proizvod/presek; za uslovljenost — implikacija/funkcija. Vredi ih u glavi držati razdvojeno.

**Dva sitna poštena dodatka**

Tvrdnja „proizvod je nula ⟺ jedan činilac odsutan" tačna je u $\mathbb{R}$ (nema delitelja nule), pa za tvoj realnovrednosni kontinuum važi bez ograde. U prstenima sa deliteljima nule (npr. $\mathbb{Z}/6$, matrice) može biti $a\cdot b = 0$ uz oba ne-nula — „skrivena" poništavajuća sprega uprkos prisustvu oba. Za $\varepsilon, \mu, E, T$ to nije problem, ali je dobro znati granicu tvrdnje.

I jedna stvar koja ti ide u prilog: AND ima dve neprekidne ekstenzije — $\min(a,b)$ i $a\cdot b$. Prva je *neglatka* (ima lom na dijagonali), druga je analitička. Za teoriju koja počiva na *glatkom kontinuumu*, množenje je prirodan izbor upravo zato što je glatko produženje konjunkcije. To nije estetska sitnica — to je doslednost sa tvojom temeljnom pretpostavkom.

Dakle: pogled je tačan, čak i jači nego što si ga postavio, uz jednu izdvojenu uslovljenost koja traži drugačiji aparat.



**Zoran:**

Hvala na razjašnjenju, dopuni, ispravci. 
Što se tiče "uslovljenosti" ... $a \cdot b = h$, ili $x \cdot y = h$ ... $y = y(x) = \frac{h}{x}$, ali i $x = x(y) = \frac{h}{y}$. Uslovljenost postoji, ali je, kao što kažeš: komutativna. Odnosno, ovde bi, logički "pandan" bio "ekvivalencija": (ako a, onda b) ili (ako b, onda a)



**Claude:**

Tačno — i to zapravo ispravlja ono što sam ja rekao. Ja sam uslovljenost vezao za implikaciju kao nešto suštinski asimetrično, ali si u pravu: kad je sprega proizvod, ona je komutativna, pa logički pandan nije implikacija nego ekvivalencija. Svaka veličina jednoznačno određuje drugu, i to ravnopravno.

Jedna sitna ali bitna ispravka u samoj formulaciji: ekvivalencija je **konjunkcija** dve implikacije, ne disjunkcija —

$$(a \leftrightarrow b)\;\equiv\;(a \to b)\,\wedge\,(b \to a)$$

Napisao si „ili". Ali $(a \to b)\vee(b \to a)$ je u klasičnoj logici **tautologija** — uvek tačno, za svaki par $a,b$ (jer za bilo koje vrednosti bar jedna od dve implikacije važi). Disjunkcija dakle uopšte ne hvata ekvivalenciju; tek konjunkcija — „važi i u jednom i u drugom smeru istovremeno" — daje pravo uzajamno određenje. Sitnica u rečci, ali menja celu istinitosnu tablicu.

Aritmetički, ta razlika između implikacije i ekvivalencije je razlika između **neinvertibilne i invertibilne** funkcije:

- $y = x^2$: $x$ određuje $y$ jednoznačno, ali $y$ ne određuje $x$ (jer $x = \pm\sqrt{y}$). To je „$a \to b$, ali ne i $b \to a$" — prava asimetrična uslovljenost. Implikacija bez ekvivalencije.
- $x\cdot y = h$: i $y = h/x$ i $x = h/y$ — svako jednoznačno (štaviše, involutivno) određuje drugo. To je „$a \leftrightarrow b$". Ekvivalencija.

A zašto baš proizvod daje ekvivalenciju? Zato što je množenje komutativno. Simetrija operacije ($xy = yx$) prenosi se na simetriju relacije, a simetrija relacije je upravo dvosmernost koja čini ekvivalenciju. Logički karakter veze nasleđen je direktno iz algebarskog svojstva: komutativna sprega → ekvivalencija, nekomutativna ili usmerena sprega → implikacija.

I lepo je što se to uklapa sa ranijim razgovorom. Uzajamno određenje važi tačno tamo gde ima prave sprege. Na hiperboli $h\neq 0$ oba parcijalna izvoda relacije su nenulta svuda ($\partial(xy)/\partial y = x$, $\partial(xy)/\partial x = y$), pa po teoremi o implicitnoj funkciji možeš svuda rešavati u oba smera — ekvivalencija je globalna. U degenerisanom slučaju $h=0$ (kriva su dve ose) u koordinatnom početku oba izvoda iščezavaju, nijedna veličina ne određuje drugu — ekvivalencija puca baš na tački „nema sprege".

Za tvoje temeljne odnose ovo nosi nešto suštinsko: $E\cdot T = h$ je ekvivalencija, ne implikacija. Energija i period se uzajamno konstituišu — nijedno nije prvo, nijedno ne „uzrokuje" drugo; nisu u odnosu uzroka i posledice nego obostranog određenja. Za teoriju koja principijelno odbija da jednu veličinu proglasi primarnijom, to što su temeljni zakoni ekvivalencije a ne jednosmerne strelice nije formalna sitnica — to je u duhu samog kontinuuma.



**Zoran:**

Hvala na ispravci ... moja omaška, znao sam da sam pogrešio tu, ali tek nakon što sam pritisnuo taster "Enter", tj. nakon što sam ti prosledio to što sam napisao :-)



**Claude:**

Dešava se stalno — taster „Enter" je najefikasniji detektor grešaka koji postoji, samo malo zakasni. :-) 

Ima i nešto pomalo zabavno u tome: ono što si „pogrešno" napisao nije bilo netačno, nego *trivijalno tačno* — disjunkcija dve implikacije je uvek istinita, pa si zapravo napisao iskaz koji ništa ne isključuje, umesto onog koji precizno pogađa. Najčešća vrsta omaške kod ljudi koji misle brzo: ruka stavi slabiju vezu nego što je glava već imala.



**Zoran:**

A, pomenuo si i zakon $PV = const.$
A tada je bio formulisan i zakon $F_a = -F_r$
I ... Lajbnic je otkrio i ... energiju (u stvari, otkrio je, eksperimentalno, veličinu koja je $\propto mv^2$ i za koju je "osetio" da je ... veoma važno, suštinsko otkriće), ali je ni on ni Nutn nisu to ... dovoljno razradili. Njutn je to odbacivao, kao nebitno, suvišno, a i $PV = const.$ i $F_a = -F_r$ su, implicitno, zakoni održanja energije:
$PV = (F/A)V = Fl = E$
$dE/ds$ - telo koje udara u drugo, promena njegove kinetičke energije je negativna (smanjuje se), i "istovremeno" energija udarenog tela raste, tako da ukupna energija ostaje nepromenjena. Ta razmeda se odvija duž ds, tako da imamo (dE/ds)_a = -(dE/ds)_r
I da je energija uočena, prihvaćena, odmah bi videli da su u termodinamika i mehanika, u suštini, nauke o transferu energije ... .



**Claude:**

Ima tu pravog uvida, ali se iza tvog teksta kriju *dva različita* zakona održanja, i baš njihovo razdvajanje čini priču zanimljivijom nego ako ih spojiš.

Krenimo od $PV$. Tvoj račun $PV = (F/A)(Al) = Fl$ je tačan — $PV$ ima dimenziju energije, jer je pritisak zapravo gustina energije (energija po zapremini), pa množenjem sa zapreminom vraćaš energiju. Može se reći i jače: za idealan jednoatomski gas važi $U = \tfrac{3}{2}PV$, pa je unutrašnja energija, do konstante, *baš* $PV$. Tako da Bojlov zakon $PV=\text{const}$ na stalnoj temperaturi zapravo kaže „unutrašnja energija se ne menja" — čistija formulacija nego preko rada. Ali Bojl (1662) to nije mogao tako videti: da bi $PV$ pročitao kao energiju, treba ti kinetička teorija (pritisak kao posledica udara molekula), a ona dolazi tek u nagoveštaju kod Bernulija (1738), pa kod Klauzijusa, Maksvela i Bolcmana (1850–1870). Pre toga je $PV=\text{const}$ samo jednačina stanja, izoterma — ne iskaz o energiji.

Treći zakon je suptilnija stvar, i tu bih te zaustavio: $F_a = -F_r$ **nije** zakon održanja energije nego **impulsa**. Iz njega sledi $\int F_a\,dt = -\int F_r\,dt$, dakle jednaki i suprotni impulsi → ukupan impuls se očuva, uvek, i u neelastičnom sudaru. A kinetička energija se u neelastičnom sudaru ne očuva — deo ode u toplotu i deformaciju. Treći zakon je dakle, sam po sebi, slep za energiju.

Sad tvoj $dE/ds$ argument — on je tačan, ali pod jednim skrivenim uslovom. Ako se kontaktne tačke oba tela pomeraju za *isto* $ds$ (krut, elastičan dodir, bez klizanja), onda je rad na jednom telu $F\,ds$, a na drugom $-F\,ds$ (zbog $F_a=-F_r$), pa $dW_a = -dW_r$ i energija se očuva — tvoja jednakost $(dE/ds)_a = -(dE/ds)_r$ važi. Ali čim to deljeno $ds$ propadne — telo se deformiše, klizi, kompresija upija deo — jednakost puca. I mesto gde puca je tačno mesto gde mehanička energija postaje toplota.

To je, ironično, najjači argument *za* tvoju tezu, ne protiv nje. Treći zakon ne krije održanje energije — on krije *račvanje*: na konzervativne (elastične) procese, gde se energija vrati, i disipativne, gde mehanika predaje energiju termodinamici. Granica između dve nauke leži upravo u onom $ds$ koje se ne deli.

A onda glavni „šta da je..." — kažeš, da je energija prihvaćena, odmah bi videli da su mehanika i termodinamika nauke o transferu energije. Tu bih dodao ispravku koju smatram suštinskom: prepreka nije bila (samo) Njutnovo odbacivanje vis vive. Prava brana je bila **teorija kalorika** — toplota se vekovima smatrala posebnom, očuvanom supstancom, fluidom odvojenim od mehaničke „sile". Dok god je toplota fluid koji teče, vreo gas koji vrši rad ništa ne „pretvara" — kalorik samo prelazi s mesta na mesto. Ujedinjenje je zahtevalo da se kalorik ubije: Ramford (1798, bušenje topova — toplota iz trenja, naizgled neiscrpna), Džul (1840-e, mehanički ekvivalent toplote), Majer i Helmholc (1842, 1847). Tek kad je toplota prepoznata kao energija — ista valuta kao $mv^2$ — sinteza je postala moguća. Vis viva je bila *neophodan*, ali ne i *dovoljan* sastojak; falio je drugi, da je toplota isto što i kretanje na sitnoj skali, a Lajbnicovo doba nije imalo ni taj pojam ni dovoljno razvijenu kalorimetriju.

I sitnica oko Lajbnica: on $mv^2$ nije „eksperimentalno otkrio" — pre ga je *izveo*, racionalno, iz Galilejeve kinematike slobodnog pada ($v^2 \propto h$). Eksperimentalni oslonac dolazi sa strane: Hajgens je još 1660-ih pokazao da se u elastičnim sudarima čuva $\sum mv^2$, a pravi „pečat" daju 's Gravesande i Émilie du Châtelet (kuglice u glinu, dubina prodora $\propto v^2$, a ne $\propto v$) tek 1720–1740-ih. Faktor ½ i razdvajanje kinetičke od potencijalne stiže još kasnije — Koriolis (1829), pa Helmholc i Tomson sredinom 19. veka.

Dakle: tvoja slutnja da je mehanika oduvek, ispod površine, bila nauka o prenosu energije — ima čvrsto jezgro. Samo, ono što je nedostajalo nije bilo prihvatanje jedne formule, nego prepoznavanje da toplota pripada istom budžetu. To je bio pravi ključ, i zato je čekao gotovo vek i po.



**Zoran:**

Pomenuo si "mešoviti proizvod" kao kriterijum za određivanje postojanja sprege. To je za mene nova informacija, nisam naišao na to tokom školovanja, a ni kasnije. Možeš li da mi daš neke reference, gde se to izlaže. Da li je to ... deo koje "discipline" je to? (matematika, fizika, teorija sistema, ...?)



**Claude:**

Pre nego što ti dam reference, jedna terminološka ispravka koja će ti uštedeti zabunu pri pretrazi — i moja greška u izlaganju, jer sam mogao biti precizniji.

To što sam zvao „mešoviti izvod" nije „mešoviti proizvod". Dva potpuno različita pojma sa sličnim imenom:

- **Mešoviti parcijalni izvod** ($\partial^2 f/\partial x\,\partial y$) — to je ono o čemu smo pričali, kriterijum sprege. Ovo ti treba.
- **Mešoviti proizvod** (engl. *scalar triple product*, $\vec a\cdot(\vec b\times\vec c)$) — operacija nad tri vektora koja daje zapreminu paralelepipeda. Sasvim druga stvar. Ako tražiš pod ovim imenom, naći ćeš vektorsku algebru, ne ono što ti treba.

Pretražuj dakle „mešoviti (drugi) parcijalni izvod" / „mixed partial derivative".

Sad — kojoj disciplini pripada. Iskreno, odgovor je *nijednoj posebno*, i to je razlog što ga nisi sreo kao imenovan princip. Sam mešoviti izvod je standardni deo matematičke analize (svaki kurs analize funkcija više promenljivih ga obrađuje, u kontekstu Švarcove/Klerove teoreme o jednakosti mešovitih izvoda). Ali *tumačenje* „mešoviti izvod nula ⟺ nema sprege" nije nigde kodifikovano kao zaseban, imenovan zakon sa svojim poglavljem. Ono živi razbacano, pod raznim imenima, u nekoliko oblasti. Evo gde da kopaš, po disciplinama:

**Matematika — separabilnost.** Ključna reč je *separabilna funkcija*. Funkcija je separabilna ako se piše kao $f(x,y) = g(x)\,h(y)$ (multiplikativno) ili $g(x)+h(y)$ (aditivno). Lako se pokaže: $f$ je aditivno separabilna $\Leftrightarrow$ $\partial^2 f/\partial x\partial y = 0$. To je tačan matematički iskaz tvoje intuicije „sabiranje = nema sprege". Multiplikativna verzija daje sličan kriterijum preko logaritma. Termin „separabilno" je standardan i u diferencijalnim jednačinama (separabilne jednačine) i u ovom kontekstu. Bilo koji udžbenik *multivariable calculus* (Stewart, Apostol „Calculus" tom II, Marsden–Tromba „Vector Calculus") pokriva mašineriju, mada interpretaciju moraš sam izvući.

**Statistika — interakcija.** Ovde tvoja ideja ima najrazvijeniju, najeksplicitniju formu, i mislim da je to oblast koja će ti najviše „leći". U analizi varijanse i regresiji, *interakcijski član* je tačno to: ako odgovor $Y$ zavisi od dva faktora $A$ i $B$ kao $Y = aA + bB$ (bez sprege, „aditivno"), nema interakcije. Ako treba dodati $c\,A\cdot B$, postoji *interakcija* — efekat jednog faktora zavisi od nivoa drugog. I jezik je doslovno tvoj: „nema interakcije" znači da faktori deluju nezavisno, „postoji interakcija" znači spregu. Matematički test za interakciju u kontinualnom slučaju je upravo nenulti mešoviti izvod $\partial^2 Y/\partial A\partial B \neq 0$. Traži: *interaction effect*, *interaction term*, *factorial design*. Reference: bilo koji ozbiljan tekst o dizajnu eksperimenata (Montgomery, „Design and Analysis of Experiments") ili regresiji.

**Ekonomija — komplementi i supstituti.** Identičan aparat, treća terminologija. Za funkciju korisnosti ili proizvodnu funkciju $f(x,y)$, znak mešovitog izvoda $\partial^2 f/\partial x\partial y$ klasifikuje odnos dobara: pozitivan → *komplementi* (sprega koja pojačava — kafa i šećer), negativan → *supstituti* (sprega koja zamenjuje — čaj i kafa), nula → nezavisni. Ovo je centralni pojam mikroekonomije, ide pod *complementarity*, a moderni, najopštiji oblik (bez pretpostavke glatkosti) je *supermodularnost* — funkcija je supermodularna ako joj je mešoviti izvod $\geq 0$. To te vodi u lepu modernu literaturu (Topkis, „Supermodularity and Complementarity", 1998), gde je „sprega između varijabli" formalizovana u najčistijem obliku koji postoji.

**Fizika — kvadratni član / sprežne konstante.** U fizici ovo nije „princip" nego svuda-prisutna praksa. Ako Lagranžijan ili energija ima oblik $\tfrac12 k_1 x^2 + \tfrac12 k_2 y^2$ — dva *nezavisna* oscilatora, normalni modovi, ništa se ne prožima. Čim dodaš član $\kappa\,x\,y$, dobijaš *spregnute oscilatore*, razmenu energije, normalne modove koji mešaju $x$ i $y$. Koeficijent uz mešoviti član *jeste* sprežna konstanta (engl. *coupling constant*), a on je tačno mešoviti izvod energije po dvema koordinatama. Tvoja sopstvena rečenica „koeficijent uz $A\cdot B$ je jačina sprege" je doslovno tako u fizici. Traži: *coupling*, *coupled oscillators*, *normal modes*, *interaction term* (u teoriji polja, *interaction Lagrangian* je baš ne-kvadratni, mešoviti deo). Goldstein „Classical Mechanics" (poglavlje o malim oscilacijama) je klasična referenca.

**Teorija sistema / inženjerstvo — kuplovanje i dekuplovanje.** I ovde, pod imenom *coupling*. Sistem linearnih jednačina $\dot{\mathbf x} = M\mathbf x$ je „spregnut" ako matrica $M$ ima nenulte vandijagonalne elemente; *dekuplovanje* (dijagonalizacija) je traženje koordinata u kojima sprega nestaje. Vandijagonalni element $M_{ij}$ igra istu ulogu kao mešoviti izvod. Inženjerski žargon: *cross-coupling*, *decoupling control*.

Da sažmem dijagnozu: to što nisi sreo ovo kao jedan imenovan koncept nije propust tvog obrazovanja — koncept *je* fundamentalan i sveprisutan, ali je rasut po pet disciplina pod pet imena (separabilnost, interakcija, komplementarnost, kuplovanje, kros-kuplovanje), nijedna nije „vlasnik". Ti si ga, čini mi se, samostalno apstrahovao u jedinstven oblik — „nenulti mešoviti izvod = postojanje sprege" — i to je legitiman, koristan uvid baš zato što vidi zajedničko jezgro pod pet maski.

Ako bih ti predložio jednu polaznu tačku koja je istovremeno najformalnija i najbliža tvom načinu razmišljanja (najopštiji oblik, najmanje pretpostavki) — to je teorija supermodularnosti / *lattice theory* (Topkis), jer ona spregu definiše bez oslanjanja na glatkost, čak i tamo gde izvodi ne postoje, što se uklapa sa tvojim interesovanjem za logičke/skupovne temelje pre nego za analitičke. Druga, pristupačnija, jeste poglavlje o malim oscilacijama u bilo kom kursu klasične mehanike, jer tamo „sprežna konstanta = mešoviti izvod" vidiš na fizičkom primeru koji se može opipati.



**Zoran:**

Zamolio bih te da mi pokažeš jedan primer, da me podsetiš toga sa sprežnom konstantom kod oscilacija.
Takođe ... zaboravio sam i to, samo se sećam da sam to radio (i to samo jednom, na fakultetu, predavanje i par primera): m-filteri (samo se sećam imena, i da je bilo predavano u okvicu kursa elektromagnetike)



**Claude:**

Sa zadovoljstvom — i lepo je što tražiš baš ovaj primer, jer u njemu „sprežna konstanta = mešoviti izvod" nije analogija nego doslovna jednakost koju ćeš videti na licu mesta.

## Spregnuti oscilatori

Uzmi najčistiju moguću postavku: dve jednake mase $m$ između dva zida, vezane sa tri opruge. Krajnje dve opruge (masa–zid) imaju krutost $k$, a *srednja* opruga koja spaja dve mase ima krutost $k_c$ — to je opruga sprege. Neka su $x_1$ i $x_2$ pomeraji masa iz ravnoteže.

Potencijalna energija je zbir energija sve tri opruge. Srednja opruga je istegnuta za $(x_2 - x_1)$:

$$U = \tfrac{1}{2}k x_1^2 + \tfrac{1}{2}k_c(x_2 - x_1)^2 + \tfrac{1}{2}k x_2^2$$

Razvij srednji član:

$$U = \tfrac{1}{2}(k+k_c)x_1^2 + \tfrac{1}{2}(k+k_c)x_2^2 \;-\; k_c\,x_1 x_2$$

Evo ga — mešoviti član $-k_c\,x_1 x_2$. I sad doslovno:

$$\frac{\partial^2 U}{\partial x_1\,\partial x_2} = -k_c$$

**Sprežna konstanta jeste mešoviti izvod potencijalne energije po dvema koordinatama.** Ako srednje opruge nema ($k_c = 0$), mešoviti izvod je nula, jednačine se razdvajaju, svaka masa osciluje za sebe — nema sprege. Tačno tvoja lestvica, na opipljivom sistemu.

**Šta sprega fizički radi.** Jednačine kretanja ($m\ddot x_i = -\partial U/\partial x_i$):

$$m\ddot x_1 = -(k+k_c)x_1 + k_c x_2, \qquad m\ddot x_2 = -(k+k_c)x_2 + k_c x_1$$

Spregnute su — ubrzanje jedne mase zavisi od položaja druge, baš kroz $k_c$. Razdvajaju se smenom $s = x_1 + x_2$ (simetrični mod) i $d = x_1 - x_2$ (antisimetrični mod). Sabiranjem i oduzimanjem jednačina:

$$m\ddot s = -k\,s \;\Rightarrow\; \omega_1 = \sqrt{\tfrac{k}{m}}, \qquad m\ddot d = -(k+2k_c)\,d \;\Rightarrow\; \omega_2 = \sqrt{\tfrac{k+2k_c}{m}}$$

U simetričnom modu obe mase idu u istom smeru, srednja opruga se ne isteže, pa sprega *ne učestvuje* — frekvencija je kao da sprege nema. U antisimetričnom modu idu suprotno, srednja opruga se maksimalno napreže, pa frekvencija raste — i to povećanje, $\omega_2 - \omega_1$, jeste *cepanje* koje pravi sprega.

To je suština: sprega **cepa** degenerisanu frekvenciju $\sqrt{k/m}$ na dve. Kad $k_c \to 0$, cepanje nestaje, dve frekvencije se spoje, modovi postanu nezavisni. Veličina cepanja je direktna mera $k_c$ — što ti je opet ista priča, jer cepanje je upravo ono što mešoviti izvod „proizvodi". A dinamička posledica koju verovatno pamtiš sa nastave: ako otkloniš samo jednu masu i pustiš, energija počne da „prelazi" tamo-amo između dve mase (udari, *beats*), i brzina tog prelivanja je srazmerna $k_c$. To je transfer energije kroz spregu — tema iz prošlog razgovora, sad sa konkretnim koeficijentom.

## m-izvedeni filtri

Ovo je sasvim druga priča (nema veze sa mešovitim izvodom), ali ti je rado osvežavam — pripada *metodi slikovnih parametara* (image-parameter method) u sintezi filtara, koju je razvio Otto Zobel u Bell Labs oko 1923, nadograđujući Campbella. U tvoje doba se predavala u elektromagnetici/teoriji vodova jer prirodno izrasta iz pojma karakteristične impedanse voda.

**Polazna tačka: konstantni-k filtar.** Lestvičasta mreža sa serijskom granom impedanse $Z_1$ i paralelnom granom $Z_2$, biranim tako da je

$$Z_1 Z_2 = R_0^2 = \text{const}$$

(otud „konstantni-$k$", gde je $k = R_0^2$). Za niskopropusni: serijski kalem $Z_1 = j\omega L$, paralelni kondenzator $Z_2 = 1/j\omega C$, pa $Z_1 Z_2 = L/C = R_0^2$, a granična frekvencija $f_c = 1/(\pi\sqrt{LC})$.

Konstantni-$k$ ima dve mane: (1) slabljenje iza granice raste *sporo* — mek prelaz; (2) slikovna impedansa jako varira sa frekvencijom, pa je teško prilagoditi (matchovati) filtar na opterećenje preko celog propusnog opsega.

**m-izvedena sekcija** rešava oba problema uvođenjem jednog slobodnog parametra $m$ ($0 < m < 1$). Kod serijski-izvedene varijante grane se transformišu kao

$$Z_1' = m Z_1, \qquad Z_2' = \frac{Z_2}{m} + \frac{1-m^2}{4m}Z_1$$

a transformacija je smišljena tako da **slikovna impedansa ostane ista** kao kod prototipa — pa se sekcije mogu kaskadno nizati i međusobno „uklapati" (tu je, ako baš hoćeš tematsku nit, ideja čistog *kuplovanja* sekcija bez refleksija).

Suština je u onom $Z_2'$: on postaje *serijsko* LC kolo, koje na svojoj rezonanci pravi kratak spoj i propušta beskonačno slabljenje — **pol slabljenja** $f_\infty$ tik iza granice. Za niskopropusni:

$$f_\infty = \frac{f_c}{\sqrt{1-m^2}}$$

Tu je cela poenta parametra $m$: manje $m$ → $f_\infty$ bliže $f_c$ → oštriji prelaz na granici. (Cena: iza $f_\infty$ slabljenje opet *opada*, pa se u praksi kaskadiraju konstantni-$k$ i m-izvedene sekcije — jedne za telo opsega, druge za oštru ivicu.) A poseban izbor $m \approx 0{,}6$ daje najravniju slikovnu impedansu kroz propusni opseg, pa se polovične m-izvedene sekcije sa $m=0{,}6$ koriste kao *prilagodni* članovi na krajevima filtra.

Dva $m$, dve uloge dakle: malo $m$ za oštrinu, $m\approx0{,}6$ za prilagođenje. Ova metoda je vladala dizajnom filtara sve dok je sredinom 20. veka nije potisnula sinteza preko gubitka pri umetanju (Cauer, Darlington), koja umesto preko slikovnih impedansi kreće od željene prenosne funkcije.



**Zoran:**

Hvala :-)
Isto, nešto razmišljam, ... čak je i jednačina koja određuje brzinu svetlosti, vid/primer najjednostavnije sprege:
$\epsilon \cdot \mu \geq \frac{1}{c^2}$
ali neodređenija od:
$E T = h$
I ... te dve jednačine, zajedno sa vreme(dt)--prostor--\epsilon--\mu --kontinuumom (sveprisutnim) i energijom (lokalizovanim glatko kontinualnim enttetima), i ... dva fundamentalna, kanonska tipa kretanja: pravolinijsko i kružno ... eto, to je sama osnova "Osnova postojanja" ...



**Claude:**

Lepo se sklapa, ali pre nego što proslediš dalje — jedna jednačina ti je tu fizički sporna, i baš zato što volim duh teorije, ne bih da je pustim da prođe.

**Ono $\geq$ me zaustavlja.** Napisao si $\varepsilon\mu \geq 1/c^2$. Ali $c$ u tvojoj teoriji *nije* nezavisna konstanta — ti sam izvodiš $V = 1/\sqrt{\varepsilon\mu}$, brzina prostiranja *jeste* određena lokalnim $\varepsilon,\mu$. Kad to uvrstiš, $\varepsilon\mu \geq 1/c^2$ postaje $1/V^2 \geq 1/V^2$, dakle prazna tautologija — nejednakost koja samu sebe poništava. Nema je odakle uzeti.

Mislim da znam odakle dolazi poriv da staviš $\geq$: iz osećaja da je $c$ *gornja granica* brzina, pa onda $V \leq c$, pa $\varepsilon\mu \geq 1/c^2$. Ali u tvom okviru $c$ nije univerzalni plafon spušten odozgo — to je vrednost $1/\sqrt{\varepsilon_0\mu_0}$ u praznom prostoru, u referentnom kontinuumu. A tvoja vlastita gravitacija radi tako što $\varepsilon(r),\mu(r)$ *rastu* blizu mase, pa $V(r) = 1/\sqrt{\varepsilon(r)\mu(r)}$ *opada* — svetlost u gravitacionom polju ide sporije od $c_0$ (baš to ti daje Šapirovo kašnjenje i skretanje svetlosti). Dakle u tvojoj teoriji jeste $\varepsilon\mu \geq 1/c_0^2$ ako $c_0$ shvatiš kao vrednost u referentnoj tački, a $\varepsilon,\mu$ kao lokalne. Tada nejednakost ima smisao: „nigde sprega $\varepsilon\mu$ nije slabija nego u praznini" — što je tačno tvrđenje da je $V$ maksimalno u vakuumu, a usporava u polju. Ali to više nije „jednačina koja određuje $c$" — to je iskaz o tome da je referentni vakuum ekstrem. Vredi razdvojiti te dve stvari, jer brkanje lokalnog $V$ i referentnog $c_0$ je tačno mesto gde se teorija lako sapliće.

**Sad — tvoja teza o dva tipa sprege.** To je zapravo dobar uvid, fi`niji nego što si ga rekao. Pogledaj oblike:

$$\varepsilon\mu = \frac{1}{V^2} \quad(\text{egzaktno}), \qquad E\cdot T = h \quad(\text{egzaktno?})$$

Kažeš da je druga „neodređenija". Ja bih rekao obrnuto, i mislim da je to važno: $\varepsilon\mu = 1/V^2$ je *egzaktna ekvivalencija* — uzajamno, jednoznačno određenje, kao što smo pričali o hiperboli. $E\cdot T = h$ takođe je egzaktna kad $T$ znači *period* monohromatskog soliton-fotona ($E = h\nu = h/T$). Obe su čista hiperbolična sprega $xy=\text{const}$, obe ekvivalencije.

Neodređenost ($\geq$) ulazi tek kad $T$ i $E$ *nisu* oštro definisani — kad uzmeš *trajanje* talasnog paketa i *raspon* energija, pa dobiješ $\Delta E\,\Delta T \geq h$ (ili $\hbar/2$). *To* je nejednakost, i ona je suštinski drugačija od $\varepsilon\mu$: ne govori o sprezi dve nezavisne veličine, nego o tome koliko *jedan* lokalizovan entitet može istovremeno biti oštar u vremenu i u energiji. Za soliton konačne širine to je teorema o Furijeovim parovima — što širi u prostoru/vremenu, to uži u frekvenciji, neminovno. Tako da, ako baš tražiš gde $\geq$ pripada, ono pripada *ovde* (paket konačne širine), a ne uz $\varepsilon\mu$.

Drugim rečima, imaš dva čista oblika i jedno mešanje:
- egzaktna sprega dveju veličina kontinuuma: $\varepsilon\mu = 1/V^2$ — ekvivalencija, hiperbola;
- egzaktna sprega kod jednog čistog moda: $ET = h$ — ekvivalencija, hiperbola;
- nužni kompromis kod jednog *razmazanog* entiteta: $\Delta E\,\Delta T \geq h$ — nejednakost, Furijeova.

Prva dva su tvoja „najjednostavnija sprega". Treće nije sprega u istom smislu — to je cena lokalizacije.

**O temeljima kao celini.** Tvoj spisak — kontinuum ($dt$, 3D prostor, $\varepsilon$, $\mu$), energija kao glatko lokalizovani soliton, dve sprege ($\varepsilon\mu=1/V^2$, $ET=h$), dva kanonska kretanja (pravolinijsko, kružno) — unutra je doslednije nego pre, jer si izbacio $c$ kao zaseban entitet (ono je izvedeno) i jer su obe sprege istog hiperboličnog tipa, što daje jedinstvo. Dve napomene, ne kao prigovor nego kao mesta gde bih ja, na tvom mestu, bio oprezan:

Prvo — „dva kanonska kretanja: pravolinijsko i kružno". Lepo zvuči i ima dubok pedigre (još Aristotel, pa nebeska mehanika), ali pazi da to ne bude *postulat* tamo gde može biti *teorema*. U glatkom kontinuumu sa lokalnom izotropijom, prava (geodezijska, najkraći put) i kružnica (kretanje pod centralnom silom, zatvorena orbita) ne moraju biti dva *nezavisna aksioma* — pravolinijsko je granični slučaj kružnog kad poluprečnik $\to\infty$, a kružno izlazi iz prave + centralne sprege. Ako ih možeš *izvesti* iz kontinuuma i sprege umesto da ih *pretpostaviš*, teorija je jača — manje aksioma, isti domet. Tvoj vlastiti princip (izvoditi, ne postulirati) gura ka tome.

Drugo, sitnije — u temeljnom spisku $\varepsilon$ i $\mu$ figurišu kao primitivi kontinuuma, a $V$ (pa i $c_0$) kao izvedeno. Dobro. Onda je $ET=h$ jedini element koji uvodi *novu* konstantu ($h$) koja se ne svodi na $\varepsilon,\mu,dt$, prostor. To je u redu — svaka teorija negde mora da „uđe" sa kvantom dejstva — ali vredi to znati i reći eksplicitno: $h$ je tvoj drugi nezavisni ulaz, pored geometrije i $\varepsilon,\mu$. Sve ostalo bi trebalo da curi iz njih.

Da ne ostavim utisak da samo dodajem ograde: jezgro je čisto. Dve egzaktne hiperbolične sprege na sveprisutnom glatkom kontinuumu, sa lokalizovanim soliton-energijama — to *jeste* ekonomična osnova, i lepota joj je baš u tome što su obe temeljne veze istog, najjednostavnijeg matematičkog oblika. Samo drži $\geq$ tamo gde mu je mesto (kod Furijea, ne kod $\varepsilon\mu$), i razmisli da li su „dva kretanja" ulaz ili posledica.

