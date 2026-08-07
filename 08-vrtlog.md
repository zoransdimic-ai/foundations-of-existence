# Poglavlje 8: Vrtlog (vortex) — poreklo "materijalnih" čestica

*Sastavljeno iz razgovora "Resuming Interrupted Conversation" (14.06.2025) i "Hajde da razmotrimo kretanje s..." (22.07.2025).*

---

## 8.1 Sudar dve kapljice

Ako je Energieelement (foton) sferna kapljica energije koja se kreće kroz prostor određen poljima $\epsilon$ i $\mu$ (Poglavlje 2–3), postavlja se prirodno pitanje: šta se dešava kada se dve takve kapljice direktno sudare?

Promena pravca kretanja svake od njih mora biti posledica lokalnih varijacija skalarnih polja $\epsilon$ i $\mu$ u oblasti sudara — jer u kontekstu onoga što model uopšte sadrži (prostor, polja $\epsilon$, $\mu$, i fluid kapljica), nema drugog entiteta koji bi mogao biti uzrok. Jedini razuman, najjednostavniji uzrok tih lokalnih varijacija jeste **uzajamni suprotstavljeni tok** ("confrontational flux") fluidâ koje čine kapljice — lokalna "kompresija" ili interferencija fluidnih gustina kada jedan fluid prolazi kroz prostor koji već zauzima drugi.

## 8.2 Da li sudar može formirati vrtlog

Pitanje koje sledi: mogu li se te lokalne varijacije organizovati tako da stvore **cirkulatorno polje brzina** — stabilan, samoodrživ vrtlog — umesto da se kapljice jednostavno raziđu?

Za to je potrebno da polje $1/\sqrt{\epsilon\mu}$ ima lokalnu topografiju koja favorizuje rotaciono kretanje: cikličnu putanju, centripetalnu organizaciju, energetsku konzistentnost (zakon $E\cdot T=h$ zadovoljen kroz ceo vrtlog), i stabilnost jednom kad je formiran.

## 8.3 Konstruisanje modela — korak po korak

Polazi se od najjednostavnijeg matematičkog modela kružnog kretanja, $v(r)=\omega r$, normalizovanog na konačnom radijusu $R$: $v(r)/v(R)=r/R$. Poređenjem sa normalizovanom brzinom $v(r)/v_{max}=1/\sqrt{(\epsilon(r)/\epsilon_0)(\mu(r)/\mu_0)}$, sledi da bi radijalna raspodela oba polja trebalo da bude $\epsilon(r)/\epsilon_0=\mu(r)/\mu_0=R/r$.

To, međutim, ne može biti tačno — postoji singularitet za $r=0$, a FOUNDATIONS pristup (Poglavlje 1) ne dozvoljava singularitete. Najjednostavniji način da se singularitet ukloni: uvesti malu konstantu, $\dfrac{R}{R_0+r}$, čime izraz dobija konačnu maksimalnu vrednost.

Ta maksimalna vrednost treba da bude proporcionalna ukupnoj energiji sudarenih kapljica, $E=E_1+E_2$ — pa se $R$ zamenjuje sa $E/K_F$, gde je jedinica $E/K_F$ ista kao jedinica dužine. Pošto polja ne smeju imati vrednost 0 (to bi značilo beskonačnu brzinu, a brzina u univerzumu ima granicu), i pošto je sudar kapljica veoma brz proces, model se dalje profinjuje pretpostavkom eksponencijalne zavisnosti:

$$\frac{\epsilon(r)}{\epsilon_0} = \frac{\mu(r)}{\mu_0} = \exp\!\left(\frac{1}{K_F}\cdot\frac{E}{R_0+r}\right), \qquad \frac{v(r)}{v_{max}} = \exp\!\left(-\frac{1}{K_F}\cdot\frac{E}{R_0+r}\right)$$

Ovaj oblik ima nekoliko poželjnih svojstava: savršeno je glatko-kontinualan; jača perturbacija (veće $E$) daje veću varijaciju polja; parametri $K_F$ i $R_0$ dozvoljavaju fino podešavanje; a za $r\to\infty$, polja teže ka $\epsilon_0$ i $\mu_0$, kako i treba.

## 8.4 Šta je $K_F$ — i šta je $R_0$

Pošto je $E$ energija, dimenzija konstante $K_F$ je **sila**. Radi se, pokazuje se dalje (videti Poglavlje 5), o maksimalnoj mogućoj sili u univerzumu — $F_{max}$. Sve gravitacione jednačine izvode se odatle na potpuno logičan način, srednjoškolskom matematikom, bez ijedne dodirne tačke sa teorijom relativnosti ili kvantnom mehanikom — a njihova ispravnost proverava se poređenjem sa Pound-Rebka rezultatom, skretanjem svetlosti, Šapirovim kašnjenjem i precesijom Merkurove orbite.

Konstanta $R_0$ za ove proračune (gravitacija na makroskopskoj skali) može se zanemariti — veoma je mala, proporcionalna $hc/E$, i postaje značajna tek pri modelovanju samog elektrona ili protona (Poglavlje 3).

## 8.5 Objedinjenje: gravitacija i elektromagnetizam iz istog izvora

Iz ovog modela proizilazi jedna od najvažnijih konceptualnih tvrdnji čitavog FOUNDATIONS pristupa:

> **Gradijent $\epsilon$ i $\mu$ polja *jeste* gravitacija.**
> **Električno i magnetno polje su neminovna posledica postojanja $du(r)/d\epsilon(r)$ i $du(r)/d\mu(r)$** — gde je $u(r)$ radijalna gustina energije vrtloga.

Drugim rečima: električno i magnetno polje nisu fundamentalni entiteti sami po sebi, već **derivativni fenomeni** — posledica toga što se gustina energije vrtloga $u(r)$ menja u zavisnosti od lokalnih vrednosti $\epsilon(r)$ i $\mu(r)$. Fizika je, u ovom smislu, već objedinjena na nivou aksioma iz Poglavlja 1: jedan kontinuum ($\epsilon,\mu$), jedna vrsta lokalizovane pobude (energetski vrtlog), a gravitacija i elektromagnetizam su dva različita načina na koja se ta ista struktura ispoljava — gradijent polja u jednom slučaju, izvod gustine energije po polju u drugom.

---

*Sledeće poglavlje: **Eksperimentalne postavke** — kako izmeriti $\epsilon_0$ Kelvinovim zaštitnim prstenom, kako izvesti Cavendishov eksperiment, i šta Thompson-Lampardov kondenzator ima zajedničko sa svim tim.*
