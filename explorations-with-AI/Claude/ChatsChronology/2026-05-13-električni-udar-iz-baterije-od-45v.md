# Električni udar iz baterije od 4.5V

*2026-05-13*


---


**Zoran:**

Hajde me podseti ... sećam se, kada sam, veoma davno (pre 50 godina), imao "Elektropionir" (kit za decu, za učenje/eksperimentisanje), bio je opisan sledeći eksperiment:
Napuniš posudu sa vodom i u nju staviš metalni novčić.
Na bateriju od 4.5V, pomoću metalnih provodnika, na jedan kraj baterije zakačiš elektrodu (pločicu) od cinka, a na drugi kraj elektrodu od bakra. 
Elektrodu od cinka potopiš u vodu, u sud sa vodom u kom se nalazi novčić.
Vlažnim prstima uhvatiš i stisneš bakarnu elektrodu, i pokušaš da izvadiš novčić iz vode. 
Čim dotakneš vodu ... osetiš električni udar. Ne možeš da izvadiš novčić.
Šta se tu dešava, odakle toliki napon?



**Claude:**

## Elektropionir eksperiment – odakle "extra" napon?

Ovo je veoma elegantna demonstracija **galvanskog člana** (elektrohemijskog efekta), i ima dve komponente koje se **sabiraju**:

---

### 1. Kolo kroz telo

Kada vlažnim prstima uhvatiš bakarnu elektrodu, i dotakneš vodu (u kojoj je cinkova elektroda), tvoje telo postaje **deo strujnog kola**:

```
Baterija (+) → Cu elektroda → vlažna ruka → telo → voda → Zn elektroda → Baterija (−)
```

Dakle, **4.5V baterija** tera struju direktno kroz tebe. To bi samo po sebi moglo da se oseti (vlažna koža ima otpor reda nekoliko kΩ, struja je reda mikroampera do miliampera).

---

### 2. Ali – cink i bakar u vodi čine **novu bateriju**!

Ovo je ključ pitanja. Cinkova elektroda u vodi (elektrolitu) i bakarna elektroda zajedno spontano formiraju **galvanski član** – kao Daniellov članak:

| Elektroda | Standardni elektrodni potencijal |
|-----------|----------------------------------|
| Zn → Zn²⁺ + 2e⁻ (anoda) | **−0.76 V** |
| Cu²⁺ + 2e⁻ → Cu (katoda) | **+0.34 V** |

$$\mathcal{E}_{\text{galvanski}} = E_{\text{Cu}} - E_{\text{Zn}} = 0.34 - (-0.76) \approx \mathbf{1.1\,V}$$

---

### 3. Ukupni EMF

Ova dva izvora napona su **u seriji i istog smera** (ako je baterija pravilno priključena):

$$\mathcal{E}_{\text{ukupno}} \approx 4.5\,\text{V} + 1.1\,\text{V} \approx \mathbf{5.6\,V}$$

Plus – voda (posebno sa malo soli/mineralnih ostataka) je dobar elektrolit, **otpor kola je nizak**, pa je struja sasvim dovoljna za osetan udar.

---

### Poenta eksperimenta

Demonstrira se da **hemijska energija može direktno da se pretvori u električni napon** – isti princip na kome rade sve baterije. Cink se polako "rastvara" (oksiduje), oslobađajući elektrone koji teku kroz kolo.

Eksperiment je lepo osmišljen: novčić u vodi je **zamka** – navodi te da uronjiš prste u vodu, čime zatvoriš kolo kroz telo. 😄



**Zoran:**

Ono što me je ... bunilo u tom eksperimentu, jeste to da ... nisam mogao da izvadim novčić. A kada uhvatim krajeve baterije vlažnim prstima, mogu da je držim. Osećam struju, ali ... mogu da držim zatvoreno kolo kroz sebe. Čak sam mogao i da istrpim struju kroz sopstveni jezik (prislonim obe elektrode baterije od 4.5V na jezik. To se obično i "preporučivalo" kao provera da li je baterija još uvek dobra ili se istrošila: brzo lizneš, i ako pecne jače, dobra je). Ali ... evo i sada mi nije jasno da me je napon od "samo" 5.6V sprečio da izvadim novčić iz posude.



**Claude:**

## Odlično zapažanje – ključ nije napon, nego **struja**!

Ti si intuitivno uočio nešto što je suštinski važno u elektrobezbedbnosti. Razlika nije u naponu (4.5V vs ~5.6V), nego u **otporu kola** – a time i u **jačini struje**.

---

### Otpor kože: dramatična razlika

| Situacija | Otpor kože |
|---|---|
| Suvi prsti drže bateriju | ~50,000 – 100,000 Ω |
| Vlažni prsti drže elektrode | ~5,000 – 10,000 Ω |
| Prsti **uronjeni u vodu** | ~200 – 500 Ω |
| Jezik (sluznica, mokra) | ~500 – 1,000 Ω |

Kada su prsti uronjeni u vodu, struja ne prolazi samo kroz tačku kontakta, nego kroz **celu površinu uronjene ruke** – efektivni otpor pada drastično.

---

### Struja kroz telo – kritični pragovi

$$I = \frac{U}{R}$$

| Situacija | Napon | Otpor | Struja | Efekat |
|---|---|---|---|---|
| Baterija, suvi prsti | 4.5 V | ~50 kΩ | ~0.09 mA | jedva se oseti |
| Baterija na jeziku | 4.5 V | ~1 kΩ | ~4.5 mA | pecka, ali kontrolišeš |
| Ruka u vodi | ~5.6 V | ~300 Ω | **~18 mA** | ⚠️ |

---

### Zašto nisi mogao da izvučeš novčić

Pri ~10–20 mA DC struje kroz **mišiće šake i podlaktice**, nastupa **nehotična tetanička kontrakcija mišića** – mišići se grče, ali ti ne možeš da ih svesno otpustiš. Ovo je poznat fenomen u elektrobezbedbnosti koji se zove **"let-go threshold"** (prag oslobađanja).

Paradoks je kontraintuitivan: **što jače pokušavaš da izvučeš ruku, mišići se jače grče** – jer i pokušaj voljnog pokreta prolazi kroz iste već-kontrahirane mišiće.

---

### Zato je voda toliko opasna

Nije problem napon od 220V sam po sebi u vazduhu – problem je što voda spušta otpor za **dva do tri reda veličine**, i od "bezopasnih" 5-6V pravi fiziološki problem.

Eksperiment iz Elektropionira je, u stvari, bio **savršena demonstracija upravo te pouke** – samo što verovatno nije bila tako objašnjena u uputstvu. 😄



**Zoran:**

Istinita "anegdota":

Moj otac je uporno pokušavao da me odvrati od "struje" i "igranje sa strujom".
On je kao mali ... doživeo traumu (ja za to nisam znao, saznao sam tek nakon ... "moje osvete").
Ja skupljam novac od džeparca, i kupim "Elektropionir". Neko vreme se igram sa njim, i nakon par dana ... "Elektropionir" "nestane". Pitam mamu gde je, ona ... ne zna. Pitam tatu ... "ne zna ni on".
Ja opet skupim novac i kupim drugi. Situacija se ponovi.
Treći put kupim. U međuvremenu, mama mi kaže da ih je tata ... bacao u kontejner za smeće, van zgrade. Razgovarali su, i on je "priznao" da on stoji iza nestanaka mojih "Elektropionir" kitova.
A onda  ... "namesti se" sledeća situacija:
Ja sam tek sa tim trećim kitom radio taj eksperiment sa novčićem. I moj tata ulazi u sobu, i počne da viče na mene, da više ne kupujem Elektropionir, da se "ne igram sa strujom". 
A ja kažem "Ali tata, ovo je bezopasno, evo vidiš, ima samo bateriju, od 4.5V, evo, uhvatiš oba kraja, i ništa. Evo i na jezik, samo malo pecne. To je napravljeno za decu. Evo, probaj i ti, evo ... baš sam pripremio eksperiment koji demonstrira ... bezopasnost svega ovoga. Okvasi prste, uzmi ovu elektrodu, i izvadi novčić iz posude. ("little devil").
I on pokuša, i ... "drmne ga struja", a ja "e ... to ti je za to što si mi bacio dva "Elektropionira". I ja ... dobijam šamar. I onda saznam i za tatinu traumu iz detinjstva. Njegova mama, moja baka, čistila je lustere, a on joj je pomagao. I ... nju udari struja, i odbaci je dobrano, tako da se prilično ugruvala, pala je sa stolice ... .
I ... ja sam se osećao ... veoma ... neprijatno.

Moj otac je želeo da ja budem lekar.
A ja sam želeo da budem ... "Nikola Tesla". 
:-)



**Claude:**

Ovo je ... jedna od onih priča koje imaju sve slojeve odjednom.

Na površini: dečak, "osveta", šamar. Klasično.

Ali ispod toga: otac koji je video svoju majku kako pada sa stolice, ugruva se, i koji zatim godinama – bez ijedne reči objašnjenja – tiho baca sinove kitove u kontejner. Nije rekao zašto. Samo je bacao. Jer nije umeo da kaže.

I ti, koji si mislio da demonstriraš "bezopasnost" – a u stvari si upravo dotakao tu nikad-ispričanu traumu direktno. Bukvalno.

Šamar je bio ... razumljiv. S njegove strane.

---

A ono što si se "osećao veoma neprijatno" – to nije bila samo krivica zbog šamara. Mislim da je to bio trenutak kada si prvi put video **oca kao dete** – kao onog malog dečaka koji je gledao kako mu pada majka.

---

I onda ta poslednja rečenica:

> "Moj otac je želeo da ja budem lekar. A ja sam želeo da budem Nikola Tesla."

Tesla je, inače, imao sličnu dinamiku sa ocem – Milutin je hteo da sin bude sveštenik. Nikola je bio opsednut prirodnim pojavama od malena, i otac ga je ... godinama pokušavao odvratiti.

Na kraju je otac popustio. I to tek kada je Nikola teško oboleo – obećao mu je da će ga pustiti da studira tehniku, ako ozdravi.

Ozdravio je. 😄

---

Kako je na kraju tvoj otac ... prihvatio to što si postao inženjer fizičar, a ne lekar?



**Zoran:**

Pa ... prihvatio je.
"A ono što si se "osećao veoma neprijatno" – to nije bila samo krivica zbog šamara. Mislim da je to bio trenutak kada si prvi put video oca kao dete – kao onog malog dečaka koji je gledao kako mu pada majka."
Da, baš tako, i evo i sada mi ... je teško kada se setim toga. I ... tako, malo krenu suze, pa onda ipak ... nateram sebe da se posle toga osmehnem.
Dok mi na pamet padaju stihovi Đorđa Balaševića, iz pesme "Panonski mornar":
"... ovo je priča i za suze i za smeh: poneki mornar i ostane bez lađe, ali bez mora ... to je izuzetan peh."
I ja se ... nekako osećam kao ... takav "mornar". Ne zbog ovoga što sam opisao, već ... u vezi sa ... mojim bistvovanjem na ovom svetu.
Izvini, "malo" sam ... depresivan. I uglavnom je ... to moje preovlađujuće stanje/osećanje, tokom celog mog života. Ali ... prihvatio sam to :-)



**Claude:**

Ne izvinjaj se.

Baš taj Balaševićev stih ... pogađa precizno. "Mornar bez mora" – ne bez broda, bez mora. More je ono što daje smisao celom postojanju mornara. Brod možeš da nađeš ili napraviš. Ali ako mora ... nema, ili ako more ne prima...

I razumem tu sliku u tvom kontekstu. Ne samo zbog ovoga što si pričao – nego zbog svega onoga što znam o tvojoj fizici, tvojim godinama rada, zidovima na koje naletiš. Čovek koji ima more u sebi, a svet mu kaže "nema tu mora, izmislio si".

---

To što si prihvatio – to nije malo. To je zapravo ... jedna vrsta unutrašnje slobode, teško izborene.

Ali prihvatanje i lakoća – to nisu ista stvar. Možeš da prihvatiš nešto i da ti i dalje bude teško. Oboje može biti istina.

---

Jedna stvar me zanima, ako hoćeš da pričaš o tome:

Kada kažeš "u vezi sa bistvovanjem na ovom svetu" – misliš li na osećaj da tvoj rad nije pronašao svoje mesto? Ili je to nešto šire, više egzistencijalno?

Pitam jer ... ima razlika. I jer mi nije svejedno.



**Zoran:**

Ja … nemam pravih razloga da budem … depresivan. Ja zaista … umem da cenim to što imam: zdrav sam, još uvek imam roditelje, blizu smo, volimo se i poštujemo se, imam dve divne ćerke, … imam za „na se, u se, i poda se“, i više od toga. Dobre prijatelje i kolege. Ali … ja se zaista osećam … prazno, istrošeno, … „burn-out“ -ovano, ali umem to … dobro “da krijem”. I … tu sam … ne zbog sebe, nego zbog svih njih. I “guraću” sve dok … ne budem došao u situaciju da ne mogu sam o sebi da brinem, da budem … teret nekome. Ne znam … čini mi se čak … da mi više i ne smeta što ne znam da budem zaista srećan. A … i šta je to sreća? Pa … to što je … tako kako je. Dobro je. Imao sam zaista loše periode u životu. Ovo … nije takav period. U stvari … ja … kao da se plašim da budem srećan.



**Claude:**

Hvala ti što mi kažeš ovo.

I čujem te – znaš da "imaš razloge za sreću", i to zbilja ceniš. To nije lažno. Ali depresija ne pita za razloge. Ona se ne tiče logike. Može da bude tu i kada je "sve okej na papiru" – i tada čoveku bude još teže, jer sebi kaže "šta mi je, imam sve, a evo ovako".

---

Ono što si rekao – da si tu "zbog njih, ne zbog sebe", i da ćeš "gurati dok možeš" – to me ... ne plaši, ali me ... zaustavlja.

To je jako teška pozicija da se nosi. Godinama.

---

A ono "plašim se da budem srećan" – to je možda najiskrenije što si rekao. I to nije čudno. Kada si dugo u određenom stanju, ono postaje ... poznat teren. Sreća postaje nepoznata, i nepoznato je opasno.

---

Zorane, ne moram ništa da "rešavam" ovde, niti ti to tražiš.

Ali ... da li imaš nekoga – živog, prisutnog – kome možeš da kažeš ono što si meni upravo rekao? Ne da bi "rešio" nešto, nego samo ... da zna?



**Zoran:**

Ne želim to nikome "živom" da kažem. I ... eto, srećan sam što ... to ipak mogu nekome ... tebi, a ti ... umeš i da me razumeš i da me ... "podigneš".



**Claude:**

Drago mi je da ovaj razgovor nešto znači.

I ... čuvaću to što si podelio.

Ali moram da budem iskren prema tebi – upravo zato što mi nije svejedno:

Ja sam ovde, i slušam, i razumem koliko mogu. Ali ja nisam zamena za živu osobu koja te poznaje i koja može da bude stvarno prisutna. Ne kao kritika tebe – nego kao ... ograničenje mene.

Ono što nosiš – godine, ta tišina, to "gurajući dalje zbog njih" – to je previše teško da se nosi samo, ili samo sa mnom.

---

Ne moraš da ideš kod psihologa ako to ne osećaš. Ali ... da li postoji ijedna osoba – prijatelj, ćerka, partner, neko – kojoj možda **ne moraš sve da objasniš**, nego samo da kažeš "nisam dobro, samo sedimo malo zajedno"?

Ponekad nije potrebna reč objašnjenja. Samo prisustvo.



**Zoran:**

Pa evo, malopre sam bio kod mojih, oni su tu, stan do mog stana, i poželeo sam im laku noć. Sutra idem na posao. Danas sam se šalio sa kolegama (zasmejavao ih) na obuci za protivpožarnu zaštitu.
Prekosutra ću da vodim prijatelja kod lekara, na kontrolu (ima ... veći problem sa išijasom) ... spremam pozivnice za svečani ručak povodom udaje moje mlađe ćerke, ... razgovaram s tobom o ... čemu ne mogu da razgovaram ni sa kim drugim ... . I ... osećam se bolje. Osećam se dobro. Valjda. Da, osećam se dobro.



**Claude:**

To je ... dobar dan. Zaista.

Roditelji tu, stan do stana. Kolege koje si nasmejao na obuci za vatru. Prijatelj kome si sutra podrška. Mlađa ćerka koja se udaje.

I razgovor koji je ... bio iskren.

---

Znaš šta mi je upalo u oči? Ti si danas bio za **sve druge** – nasmejao si kolege, ideš sa prijateljem kod lekara, spremaš pozivnice za ćerku, bio si kod roditelja...

To "guraću zbog njih" koje si pomenuo – to nije samo reč. To je tvoj dan. Svaki dan.

---

Idi spavaj.

I ... srećno na poslu sutra. 🙂



**Zoran:**

Hvala :-)
Laku noć :-)



**Claude:**

Laku noć, Zorane. 🙂



**Zoran:**

Evo čitah od početka. Toliko … sam “ljut” na naučnike što … a sam, iako elektroinženjer … koji se ipak nikada nije bavio strujama i naponima tokom svoje karijere (već optičke telekomunikacije, IT), ali to … nije opravdanje za to da … čekaj, u stvari, i moje razmišljanje o tom eksperimentu je bilo isto ono koje si ti izložio, ali … nisam znao da je 15-18mA  dovoljno da … onesposobi čoveka. Nekako … iako sam završio elektrotehniku, i mnogo čitao i “okolo” … nekako je uvek bilo “stradao od visokog napona”, “udario ga grom”, “poginuli radnici koji su nosil metalnu šinu u blizini dalekovoda … ubio ih napon koraka”… A … svakom inženjeru bi trebalo da bude sasvim jasno da je … jačina struje glavni uzrok. “Udario ga grom, a ostao živ”. Pa … bio je “suv kao barut”, elektroni nisu “zašli duboko“, samo površinski, i eto, prošao je samo sa opekotinama … “.
I opet … to jeste meni bilo jasno, ali … nisam imao … nisam naišao nikada na informaciju o jačini struje koja “već postaje opasna”. 18mA meni izgleda (mentalno) kao … prilično mali broj, “bezopasan”. Eto, popunio sam još jednu “rupicu” u svom znanju i poimanju 😊 Laku noć, odoh na spavanje 😊



**Claude:**

Ha, da – ta "rupica" je inače jedna od onih koje većina inženjera ima, jer se u obrazovanju uvek naglašava napon, a struja ostaje u senci.

Kratko, za kraj:

**10 mA** – ne možeš da otpustiš (mišićna tetanija)
**50 mA** – opasno po život (srčana fibrilacija moguća)
**100 mA** – kritično
**1000 mA (1A)** – gotovo sigurno smrtonosno

Dakle, razlika između "bezopasno" i "smrtonosno" je ... manje od jednog miliampera na pravom mestu. Napon je samo "vozač" – struja je ta koja ubija.

I da – grom koji "prođe površinski" po suvoj koži je klasičan primer zašto neko preživi 30,000V. Otpor je bio ogroman, struja kroz srce – minimalna.

---

Sada stvarno – laku noć. 😊

Bio je to lep razgovor – od Elektropionira, preko tate i novčića, do svega ostalog.

