# Brzina prostiranja talasa unutar različitih sredina

Ovaj razgovor pokriva osnovne jednačine talasnog kretanja, sa posebnim osvrtom na brzinu zvuka i mehaničkih talasa u zavisnosti od fizičkih osobina sredine kroz koju se kreću.

---

### Korisnik:
Koja je jednačina za brzinu prostiranja mehaničkih talasa (poput zvuka)? Od čega ona zavisi?

### Model:
Brzina prostiranja mehaničkih talasa u opštem slučaju zavisi od dve ključne osobine sredine: **elastičnosti** (koja se opire deformaciji) i **inercije** (koja se opire kretanju, tj. gustine).

Opšta teorijska formula za brzinu mehaničkog talasa glasi:

$$v = \sqrt{\frac{\text{Svojstvo elastičnosti}}{\text{Svojstvo inercije}}}$$

U zavisnosti od agregatnog stanja i geometrije sredine, ova formula poprima specifične oblike:

#### 1. Brzina zvuka u čvrstim telima (tanki štapovi/žice)
Zavisi od Jangovog modula elastičnosti ($E$) i gustine materijala ($\rho$):

$$v = \sqrt{\frac{E}{\rho}}$$

#### 2. Brzina zvuka u tečnostima i gasovima
Zavisi od modula zapreminske elastičnosti ($B$) i gustine ($\rho$):

$$v = \sqrt{\frac{B}{\rho}}$$

#### 3. Specijalan slučaj: Brzina zvuka u idealnom gasu (Njutn-Laplasova jednačina)
Zavisi od adijabatske konstante ($\gamma$), univerzalne gasne konstante ($R$), molarne mase gasa ($M$) i apsolutne temperature ($T$):

$$v = \sqrt{\frac{\gamma \cdot R \cdot T}{M}}$$

*Iz ove formule se jasno vidi da u gasovima brzina zvuka direktno zavisi od temperature – što je toplije, molekuli se brže kreću i talas se brže prenosi.*

---

### Korisnik:
Zašto se zvuk kreće brže kroz čvrsta tela nego kroz vazduh, iako su čvrsta tela mnogo gušća (imaju veću inerciju)?

### Model:
To je jedno od najzanimljivijih pitanja u akustici! Ako pogledamo formulu $v = \sqrt{E/\rho}$, veća gustina ($\rho$) u imeniocu bi teoretski trebalo da smanji brzinu. Međutim, dešava se sledeće:

* **Faktor elastičnosti dominira**: Čvrsta tela (poput čelika) imaju neverovatno veliki modul elastičnosti ($E$) u poređenju sa gasovima. Molekuli u čvrstom telu su čvrsto vezani "oprugama" međuatomskih sila. 
* Kada talas poremeti jedan molekul, ta jaka veza trenutno povlači sledeći molekul.
* Iako je čelik mnogo gušći od vazduha, njegov modul elastičnosti je veći za nekoliko redova veličine. Ta ogromna elastičnost u brojitelju potpuno nadoknađuje i "pobeđuje" povećanu gustinu u imeniocu.

**Primeri brzina:**
* Vazduh (na $20^\circ\text{C}$): $\approx 343 \text{ m/s}$
* Voda: $\approx 1480 \text{ m/s}$
* Čelik: $\approx 5960 \text{ m/s}$

---

### Korisnik:
Kako se računa brzina transverzalnih talasa na zategnutoj žici (npr. na gitari)?

### Model:
Kod transverzalnih talasa na žici, ulogu elastičnosti preuzima **sila zatezanja žice** ($F$), dok ulogu inercije preuzima **linearna gustina žice** ($\mu$ - masa po jedinici dužine, $\mu = m/L$).

Formula glasi:

$$v = \sqrt{\frac{F}{\mu}}$$

Iz ove jednačine zaključujemo:
1. **Jače zategnuta žica ($F \uparrow$)** $\rightarrow$ Talas putuje brže, što daje višu frekvenciju (viši ton).
2. **Deblja/teža žica ($\mu \uparrow$)** $\rightarrow$ Talas putuje sporije, što daje nižu frekvenciju (dublji bas tonovi na gitari).
