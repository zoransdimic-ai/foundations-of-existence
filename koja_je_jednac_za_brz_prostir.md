# Koja je jednačina za brzinu prostiranja...

Ovaj fajl sadrži autentičan prepis razgovora o fizici talasa i zvuka, prilagođen za pregledno čitanje na GitHub-u.

---

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
