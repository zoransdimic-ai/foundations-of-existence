# Koja je jednačina za brzinu prostiranja...

### Korisnik
Koja je jednačina za brzinu prostiranja...

### Model
Brzina prostiranja talasa zavisi od osobina sredine kroz koju se talas kreće. Za mehaničke talase (kao što je zvuk), brzina prostiranja se generalno računa preko formule:

$$v = \sqrt{\frac{E}{\rho}}$$

gde je:
*   $v$ – brzina talasa,
*   $E$ – modul elastičnosti sredine (mera koliko se sredina opire deformaciji),
*   $\rho$ (ro) – gustina sredine.

Iz ove formule možeš videti dve važne stvari:
1.  **Elastičnost (brojilac):** Što je sredina elastičnija (čvršća), to se talas brže prostire jer se poremećaj brže prenosi sa čestice na česticu.
2.  **Gustina (imenilac):** Što je sredina gušća (ima veću inerciju), to se talas teže prostire, pa bi veća gustina teoretski trebalo da uspori talas.

Međutim, u praksi, čvrsta tela (poput čelika ili kamena) imaju mnogo veći modul elastičnosti nego gasovi ili tečnosti. Ta ogromna razlika u elastičnosti potpuno nadoknađuje njihovu veću gustinu, zbog čega se **zvuk kreće mnogo brže kroz čvrsta tela nego kroz vodu, a kroz vodu brže nego kroz vazduh**.

#### Specifični slučajevi:

*   **U gasovima (vazduh):** Brzina zvuka direktno zavisi od temperature gasa i računa se kao:
    $$v = \sqrt{\frac{\gamma \cdot R \cdot T}{M}}$$
    Gde je $T$ apsolutna temperatura u Kelvinima. Zato se zvuk kreće brže kroz topao vazduh nego kroz hladan. (Na temperaturi od $20^\circ\text{C}$ brzina zvuka u vazduhu je oko $343 \text{ m/s}$).
*   **Na zategnutoj žici (npr. gitara):** Brzina transverzalnog talasa zavisi od sile zatezanja ($F$) i linearne gustine žice ($\mu$ - masa po jedinici dužine):
    $$v = \sqrt{\frac{F}{\mu}}$$

Da li te zanima specifičan proračun za neku konkretnu sredinu ili određeni tip talasa?

---

### Korisnik
A za longitudinalne talase? Mislim da je to ... P talasi kod zemljotresa? Kako se tamo ... prenosi energija i informacija i ... koja je to brzina?

### Model
Da, potpuno si u pravu! P-talasi (primarni talasi) kod zemljotresa jesu **longitudinalni talasi**. Oni su najbrži seizmički talasi i zato prvi stižu do seizmoloških stanica (odatle i naziv "primarni").

Pošto su longitudinalni, oni se prostiru tako što se čestice sredine kreću **napred-nazad u istom pravcu** u kojem se talas širi. To stvara zone sabijanja (kompresije) i razređivanja (ekspanzije) u stenskoj masi.

#### Brzina P-talasa unutar Zemljine kore

Za longitudinalne talase u trodimenzionalnom čvrstom telu (poput Zemljine kore i plašta), jednačina za brzinu se modifikuje jer stena pruža otpor i sabijanju i smicanju. Formula glasi:

$$v_p = \sqrt{\frac{K + \frac{4}{3}G}{\rho}}$$

gde je:
*   $v_p$ – brzina P-talasa,
*   $K$ – zapreminski modul elastičnosti (Bulk modulus) – meri otpor stene na svesmerno sabijanje,
*   $G$ – modul smicanja (Shear modulus) – meri otpor stene na promenu oblika,
*   $\rho$ – gustina stena.

U Zemljinoj kori, ova brzina se kreće obično od **5 km/s do 8 km/s**, dok u dubljim slojevima (plaštu) raste i do **13 km/s**, jer sa dubinom elastičnost stena raste mnogo brže nego njihova gustina.

#### Kako se prenosi energija i informacija?

1.  **Mehanizam prenosa (Energija):** Seizmički izvor (npr. pucanje raseda) naglo oslobađa ogromnu elastičnu energiju. Prvi sloj stene biva sabijen. Zbog svoje elastičnosti ($K$), taj sloj teži da se vrati u prvobitno stanje i pritom gura sledeći sloj ispred sebe. Energija se prenosi putem tog sukcesivnog "guranja" i kinetičke energije čestica koje osciluju. Same stene ne putuju sa talasom – one samo vibriraju u mestu, dok energija putuje kroz njih.
2.  **Prenos informacije:** Informacija koja se prenosi ovim talasom je sam **trenutak i intenzitet poremećaja**. Kada P-talas stigne do površine, on donosi informaciju da se duboko u utrobi Zemlje desio lom. Pošto P-talasi mogu da prolaze i kroz čvrste i kroz tečne sredine (za razliku od sekundarnih S-talasa koji ne idu kroz tečnosti), oni nose i ključnu informaciju o unutrašnjoj strukturi Zemlje (na primer, tako smo saznali da je spoljašnje jezgro Zemlje tečno, jer su P-talasi kroz njega usporili, a S-talasi potpuno nestali).
