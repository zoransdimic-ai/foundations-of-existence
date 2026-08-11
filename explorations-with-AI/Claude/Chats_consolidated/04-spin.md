# Poglavlje 4: Spin i ugaoni moment

*Sastavljeno iz razgovora "Integral sa eksponencijalnom permitivnošću" (30.05.2026). Ovo poglavlje namerno zadržava oblik iskrene, kritičke rasprave — jer je upravo taj proces doveo do čistog rezultata.*

---

## 4.1 Prvi pokušaj — i skrivena nekonzistentnost

Polazna ideja: ako je elektron rotirajući energetski vrtlog poluprečnika $r_c=\hbar/(Mc)$ (Komptonov radijus), ugaoni moment se dobija iz odnosa Gausovih momenata gustine energije:

$$\frac{\int r^4 u\,dV}{\int r^2 u\,dV} = \frac{3}{2}r_c^2$$

Ovo je, u stvari, moment inercije homogene Gausove sfere. Naivnom rotacijom krutog tela to daje faktor oblika $3/2$, pa $L=\tfrac{3}{2}\hbar$ — previše (potrebno je $\hbar/2$).

Prvi pokušaj da se to ispravi pozivao se na **ekviparticiju energije**: u svakom harmonijskom oscilatoru (opruga, klatno, ili ovaj vrtlog, čiji potencijal je paraboličan, $\Phi\sim r^2$) važi $\langle E_{kin}\rangle=\langle E_{pot}\rangle=\tfrac12 E_{tot}$. Spin potiče isključivo od kinetičke energije; potencijalna energija "drži strukturu na okupu", ima masu, ali ne doprinosi momentu impulsa. Pošto se samo pola mase "vrti":

$$L = \left(\frac12 M\right)\cdot c\cdot r_c = \left(\frac12 M\right)\cdot c\cdot\frac{\hbar}{Mc} = \frac12\hbar$$

Naizgled čisto — ali kritička provera otkriva problem: u ovom izvođenju se faktor $3/2$ prvo pojavi (iz Gausovih integrala), a zatim se primeni ekviparticija ($\times\tfrac12$), što bi trebalo da da $3/2\cdot\tfrac12=\tfrac34\hbar$, ne $\tfrac12\hbar$. Faktor $3/2$ je u finalnom koraku nečujno ispušten. Dve verzije istog računa daju različite brojeve — to je rupa koju bi svaki recenzent odmah primetio.

## 4.2 Prava geometrija — cilindrični krak poluge

Greška je pronađena u koraku pre ekviparticije: integral $L=\int r\cdot v\,dm$ koristio je **sferno** $r$ kao krak poluge. Ali kod rotacije oko ose, krak je **cilindrični**, $R=r\sin\theta$ (rastojanje do ose rotacije), ne puno $r$.

Kada se kruta rotacija uradi ispravno — $\omega=c/r_c$, $L_z=\omega\int\rho\,r^2\sin^2\theta\,dV$ — ugaoni deo integrala donosi $\int\sin^3\theta\,d\theta=4/3$, što daje množilac $2/3$. Kombinovano sa Gausovim faktorom $3/2$:

$$\frac{L}{M c r_c} = \underbrace{\frac23}_{\text{ugaoni (cilindrični krak)}}\cdot\underbrace{\frac32}_{\text{Gausov moment}} = 1\ (\text{tačno, numerički potvrđeno})$$

Dakle ispravna kruta rotacija daje faktor oblika **tačno 1**, ne $3/2$: $L=Mcr_c=\hbar$. Prvobitna greška u kraku poluge i "ispravka" sa ispuštanjem $3/2$ slučajno su se poništile — ali čista, geometrijski ispravna verzija zaista vodi do $\hbar$, i tek nakon toga, faktorom $\tfrac12$ iz ekviparticije, do **tačno $\hbar/2$**.

## 4.3 Gde je prava slabost — i zašto je vredno to reći naglas

Ovde vredi biti direktan: **faktor $\tfrac12$ nije izveden, nego pretpostavljen.** Relativistički, izvor ugaonog momenta je gustina impulsa $T^{0i}=(\text{gustina energije}/c^2)\cdot v$. Ako se cela energija $u(r)$ kreće brzinom $v(r)$, u $L$ ulazi cela masa, i dobija se $\hbar$ (uz ispravnu geometriju), bez ikakvog $\tfrac12$. Da bi $\tfrac12$ bilo opravdano, tačno polovina stres-energije tenzora solitona morala bi biti statička "tenzija" bez gustine impulsa, a polovina pokretna — a to je tvrdnja o unutrašnjem $T^{\mu\nu}$ koju ovaj model (za sada) ne zadaje nezavisno. Ekviparticija ($\langle T\rangle=\langle V\rangle$ za harmonijski potencijal) je lepa analogija, ali virijalni teorem daje vremenski usrednjenu tvrdnju za oscilator — ne doslovno "pola mase miruje".

**Nasleđeni klasični problem:** brzinski ansatz $v(r)=c\cdot r/r_c$ daje $v>c$ za $r>r_c$. Integral za spin nosi težinu $r^4$, pa integrand $r^4e^{-r^2/r_c^2}$ ima maksimum na $r=\sqrt2\,r_c$ — duboko u oblasti gde je $v=\sqrt2\,c$. Glavni doprinos spinu dolazi baš odande gde je brzinski ansatz nefizičan. Ovo je poznat prigovor svim klasičnim modelima spina (obim bi morao biti nadsvetlosni), i rešava se profilom brzine koji saturira na $c$ umesto da linearno raste — pravac koji povezuje ovo poglavlje sa Poglavljem 3.

**Trezvena napomena o $\hbar$ samom:** $\hbar$ se ovde ne predviđa — unosi se kroz definiciju $r_c\equiv\hbar/(Mc)$. Pošto je $L=(\text{prefaktor})\cdot Mc r_c$, a $Mc r_c\equiv\hbar$ po definiciji, pojava $\hbar$ je zagarantovana samim izborom radijusa. **Prava tvrdnja modela nije "$L=\hbar/2$", nego "bezdimenzioni prefaktor iznosi $1/2$."** Sav teret dokaza je na tom broju.

## 4.4 Stanje stvari — pošteno postavljeno

Rezultat je obećavajući: uz ispravnu geometriju postoji čist, interno konzistentan put koji daje tačno $\hbar/2$ bez naknadnog štelovanja, sa samo jednom eksplicitno označenom slobodnom pretpostavkom (faktor $\tfrac12$ iz ekviparticije) i jednim poznatim ograničenjem (nadsvetlosni rep integranda). To se namerno ne prikriva:

| | sledi iz geometrije | pretpostavka / otvoreno |
|---|---|---|
| $L=\hbar$ (bez $\tfrac12$) | ✓ kruta rotacija, cilindrični krak | |
| $L=\hbar/2$ | | faktor $\tfrac12$ iz ekviparticije |
| $\hbar$ sam | | ulazna definicija preko $r_c$, ne predviđanje |
| nadsvetlosni rep u integrandu | | poznato ograničenje, rešava se profilom $v(r)$ koji saturira |

Duh ovog poglavlja — i čitavog FOUNDATIONS pristupa — najbolje sažima rečenica izgovorena u trenutku kada je ova nekonzistentnost pronađena: *"Mi tražimo istinu, i ispravnu perspektivu za one koji će eventualno to nastaviti."* Pretpostavka ostaje jasno označena kao pretpostavka — "to the consideration of my readers", njutnovski — a ne prerušena u dokaz onoga što tek treba dokazati.

**Pravac dalje istrage:** prirodni sledeći korak je da se, uz $R=\sqrt2\,r_c$ (granica koja se pojavljuje i u Poglavlju 3, kod naelektrisanja), potraži profil $u(r)$ koji istovremeno popravlja ono odstupanje od $17\%$ kod naelektrisanja *i* kaže nešto novo o faktoru oblika za spin — mogućnost da se ta dva, naizgled odvojena, otvorena pitanja reše istim potezom.

---

*Sledeće poglavlje: **Gravitacija** — kako se, iz prostorno promenljivih $\epsilon(r)$ i $\mu(r)$, izvodi Pound-Rebka efekat, Shapiro kašnjenje, otklon svetlosti i precesija Merkura — bez zakrivljenog prostor-vremena.*
