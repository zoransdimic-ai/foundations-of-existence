# Poglavlje 6: Zračenje crnog tela — kombinatorni put do Plankovog zakona

*Sastavljeno iz razgovora: "Zaglavljena chat sesija zbog velikog PDF-a" (20.04.2026) i "Izvođenje zakona zračenja crnog tela" (06.07.2026), koji sadrži finalnu, zaokruženu verziju izvođenja.*

---

## 6.1 Kombinatorno pitanje umesto bozonske statistike

Standardni put do Plankove raspodele prolazi kroz Boze-Ajnštajnovu statistiku i brojanje modova u šupljini. FOUNDATIONS pristup polazi od jednostavnijeg, direktno prebrojivog pitanja: **na koliko načina $n$ emitera (pretvarača) može emitovati $k$ solitona (fotona)?**

To je pitanje kombinacija sa ponavljanjem:

$$\bar{C}_n^k = \binom{n+k-1}{k}$$

Umesto da se odmah pretpostavi kvantna statistika, broje se **eksplicitno** sve konfiguracije — na primer, svih 21 konfiguracija za $n=3$ emitera i $k=5$ fotona, ili 120 konfiguracija za $n=4$, $k=7$, grupisanih po "signaturi" particije (koliko emitera dobija 0, 1, 2... fotona). Zaključak iz ovog direktnog prebrojavanja: uniformne raspodele (svaki emiter dobija približno isti broj fotona) imaju **najmanje** mogućih aranžmana, dok neujednačene raspodele (nekoliko emitera nosi većinu energije) dominiraju brojem. To je statistička osnova iz koje se, bez ijedne pretpostavke o bozonima, prirodno pojavljuje oblik Plankove raspodele.

## 6.2 Od kombinatorike do $u=(e^{h\nu/k_BT}-1)^{-1}$

Formalni put:

1. Stirlingova aproksimacija za veliko $n,k$ daje funkciju složenosti $\Theta(n,k)$.
2. Linearizacija $\theta=\ln\Theta^{1/n}$, tretirana kontinualno preko $u=E/E_{ss}$ (odnos energije prema energiji pojedinačnog solitona).
3. Diferencijalni korak $du/d\theta$, upoređen sa termodinamičkom definicijom entropije $S=k_B\ln\Omega$ i $dQ=T\,dS$, vodi — elegantno i bez ijednog pominjanja bozonske statistike ili kvantovanja modova šupljine — do:

$$u = \frac{1}{e^{h\nu/k_BT}-1}$$

što je, u suštini, Boze-Ajnštajnov broj popunjenosti fotonskih stanja — dobijen čisto kombinatornim brojanjem konfiguracija emisije, a ne postuliranjem kvantne statistike.

## 6.3 Geometrijski deo: foton kao sferni soliton

Da bi se od broja popunjenosti $u$ došlo do stvarnog spektralnog fluksa snage, potreban je geometrijski korak koji standardni Rejli-Džinsov pristup rešava brojanjem modova u šupljini. Ovde se umesto toga foton tretira direktno kao sferni soliton (Poglavlje 2–3), i računa se njegov **prosečan poprečni presek**:

$$\bar{A}_{c.s.} = \frac{\pi}{6}\lambda_{ss}^2$$

Iz ovoga se, bez ikakvog pozivanja na gustinu modova u šupljini, direktno izvodi zavisnost fluksa snage od $\nu^3$. Konačan rezultat:

$$PFpf(\nu,T) = \frac{6}{\pi}\frac{h}{c^2}\cdot\frac{\nu^3}{e^{h\nu/k_BT}-1}$$

## 6.4 Poređenje sa standardnim rezultatom — pošteno otvoreno pitanje

Standardna Plankova spektralna radijansa glasi $B(\nu,T)=\dfrac{2h}{c^2}\dfrac{\nu^3}{e^{h\nu/k_BT}-1}$ — koeficijent $2h/c^2$. Dobijeni koeficijent, $\dfrac{6}{\pi}\dfrac{h}{c^2}\approx1.9099\,\dfrac{h}{c^2}$, odstupa od standardnog za svega **~4.5%** (odnos $\tfrac{6/\pi}{2}=\tfrac{3}{\pi}\approx0.955$).

To je dovoljno blizu da ukazuje da geometrijski argument (sferni presek solitona) hvata suštinu $\nu^3$ zavisnosti — ali se ne poklapa tačno sa standardnim rezultatom, koji dolazi iz brojanja modova u šupljini (dve polarizacije × gustina stanja). Otvoreno pitanje, pošteno postavljeno: odakle tačno dolazi ta razlika — da li iz razlike između radijanse po steradijanu i hemisfernog fluksa, ili iz faktora 2 za polarizacije koji u ovoj geometrijskoj konstrukciji nigde eksplicitno ne ulazi. Naknadna analiza pokazala je da su i druge moguće vrednosti prefaktora — $\dfrac{12\pi}{\pi^2-6}$, $2.28$ — sve reda jedinice i sve zavise od tačnog oblika profila ($\cos^2$ naspram sfere oštrih ivica) i od načina brojanja polarizacija. **Struktura izvođenja je čvrsta; kalibriše se samo taj jedan broj.**

Važna nezavisna provera koja ide u prilog izvođenju: integracija $PFpf$ po $\nu$ daje $\int \nu^3/(e^{h\nu/kT}-1)\,d\nu \propto T^4$ — dakle reprodukuje se Štefan-Bolcmanov zakon, što ne bi bio slučaj da je nešto strukturno pogrešno, samo prefaktor nije konačno kalibrisan.

## 6.5 Provera koja ne zavisi od prefaktora: Vinov zakon pomeraja

Vinov zakon pomeraja, $\lambda_{max}T=b$, zavisi **samo od oblika krive** — od $\nu^3/(e^{h\nu/kT}-1)$ — a ne od konstante ispred nje. To znači da odnos $h/k_B$ koji se dobija iz ovog izvođenja **ne zavisi** od toga da li je prefaktor $2$ ili $6/\pi$: taj deo rezultata stoji nezavisno od otvorenog pitanja iz §6.4, i predstavlja čvrst, proverljiv deo modela — uključujući i eksperimentalni plan (bolometar, prizma, galvanometar; fitovanje krive da se istovremeno dobiju $h$ i $k_B$, pa dalje povezivanje sa Milikanovim $h/e$ i Tomsonovim $e/m$ eksperimentom — videti Poglavlje 9).

---

*Sledeće poglavlje: **Lagranžijan** — demistifikacija Lagranžijanske mehanike, izvedena direktno iz kolica, sile i energije, bez pozivanja na princip najmanje akcije kao polazište.*
